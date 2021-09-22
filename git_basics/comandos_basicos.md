# <span style="color:red">Comandos básicos Git    </span>
Git es la base tanto de GitHub Gitlab y otros gestores de repositorios que utilizan la herramienta git de base. Se presentan a continuación una serie de comandos basicos:

## <span style="color:green">1. Crear un repositorio    </span>

## 
Para trabajar en estos es importante entender el concepto **repository**. Podría entenderse como la carpeta que contiene un determinado proyecto de Git .  

Depende de la locación de este repositorio se tienen dos tipos:

- **Local repository** - Un repo aislado almacenado en nuestra PC, este será el sito que solo nosotros tenemos acceso y donde se desarrolarán nuestro cambios.
- **Remote repository** - Un repo general alojado en un servido remoto. Esta será el destino de nuestro repositorio local para trabajar en equipo o para versionar, compartir o respladar un determinado proyecto. A este repositorio tiene acceso cualquier persona que tenga internet si es abierto o a quienes decidamos compartirselo si es cerrado. 

Para crear un repositorio nos alojamos en la carpeta y ejecutamos 

```bash
git init
```
(Esto no lo vamos a utliizar haciendo uso de GitHub o GitLab)

## <span style="color:yellow">2. Comenzar a commitear un código    </span>

En git se puede considerar que existen determinados checkpoints asociados a tareas o etapas del desarrollo de código, a esto se le denominan **commits**. Estos también sirven para registrar en el pasado determinados cambios. Por ejemplo se pueden utilizar para registrar que se agregó una nueva funcionalidad, se solucionó un bug o para notificar un determinado avance.


### <span style="color:yellow">2.1 Checkear el estado del repositorio   </span>

Es importante antes de comitear conocer cual es el estado de situación del código respecto al commit anterior, o que modificaciones nuevas hubieron en referencia a este. Para eso se ejecuta 

```bash 
git status 
```
### <span style="color:yellow"> 2.2 Agregar un archivo  </span>


Supongamos que luego de creado el repositorio se desea agregar un cierto archivo. Para eso se lo agrega a la carpeta local y al ejecutar el step 2.1 este se listará en terminal. 

Para agregar ese archivo a un determinado commit que se hará a continuación se debe ejecutar 

```bash
git add file.m file2.html file3.js
```
Para agregar todos los cambios se ejecuta:

```bash
git add .
```

### <span style="color:yellow"> 2.3 Crear un commit con el archivo anterior  </span>

Como definimos anteriormente un commit es una especie de foto del repostorio en un determinado tiempo almacenado en el historial. Para crear ese commit con el archivo que agregamos anteriormente ejecutamos:

```bash
git commit -m "Descripción del commit"
```
Una vez que hagamos un push de estos cambios al repositorio remoto la descripicón del commit será publica por lo que debe ser ordenada y clara respecto a las modificaiones que realizó ese commit. Por ejemplo "Fixed bug plot function plotVtk.m"

### <span style="color:yellow"> 2.3 Historial de commits  </span>
Supongamos que cometí un error y quiero recuperar el trabajo anterior, para eso un commit viejo puede ser la salvación. Se puede ver el historial de commits de determinada rama del repostiorio ejeuctando:

```bash
git log
```
Esto despliega las descripciones de cada commit, el autor del mismo, la fecha y un hash asociado. Para volver atrás tenemos una maquina del tiempo entre commits ejecutando:

```bash
git checkout <commit-hash>
```
### <span style="color:yellow"> 2.4 Excluir determinados formatos o archivos  </span>

Existen casos donde es util agregar determinadas excepciones que no se desean registrar, por ejemplo archivos de salida .pdf, .vtk, .png etc. Para eso podemos agregar determinados archivos específicos o formatos a un .**.gitignore** 

Mas infomración se encuentra en este [gitignore link](https://help.github.com/en/articles/ignoring-files).


## <span style="color:orange"> 3.Manejo de branches  </span>

Un determinado **branch** puede interpertase como una rama del código indivudal para el desarrollo de determinada funcionalidad o solucionar un bug sin interrumpir o alterar la rama principal (origin / master).

Con git se puede crear diferentes (i.e. we can create different **branches**) entonces diversas versiones del código y desarrollo se pueden avanzar en paralelo para luego interactuar

Por defecto al crear un detrminado repositorio y agregar commits estos se realizan en la rama principal **master** o  **master**.

### <span style="color:orange"> 3.1 Crear un nuevo branch </span>

Al ejecutar el item 2.1 y ejecutar el comando a continuacón se creará un branch derivado de la rama en la que nos encontremos con un determinado nombre asignado:

```bash
git branch <nombre del branch>
```
### <span style="color:orange">  3.2 Navegar entre branches </span>


Para cambiar de branch basta utilizar el comando visto en el item 2.3 con un flag -b. Aplicado a branches es:


```bash
git checkout -b <branch a moverse>
```

### <span style="color:orange">  3.3 Fusionar dos branches </span>

Supongase que en el branch de desarrollo se realizaron determinados cambios y que se desean agreagar a la rama principal **master**. Para esto se realiza un merge que fusiona los cambios de una rama con la otra, y nos indica si existen conflictos. Estos merge también peuden deshacerse con el item visto en 2.3. Supongase que nos encontramos en **master** y queremos traer el branc **branch_cambios**. Luego de asegurarnos con `git status``que estamos parados en el lugar correcto ejecutamos:

```bash
git merge **branch_cambios**
```
Esto inegrará el  **branch_cambios** a **master**. En caso de que existen conflictos esto es notificado por git y deben solucionarse manualemente. 

### <span style="color:orange">  3.4 Borrar un branch </span>

Una vez que **branch_cambios** cumplió su función se puede borrar utilizando el siguiente comando:

```bash
git branch -d **branch_cambios**
```



