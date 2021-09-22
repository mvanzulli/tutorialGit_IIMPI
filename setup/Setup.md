# <span style="color:red">Setup    </span>

## <span style="color:orange"> 1. Crear un usuario   </span>

Inicialmente es imprescindible crear un usuario en la página de GitHub (Microsoft) o GitLab.

- GitHub: [Sign up Github](https://github.com/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home)
- Si no quiere venderse al mejor postor y proteger sus códigos (datos) FING dispone de GitLabFING con el nombre de usario y contraseña de EVA: [Sign up GitLabFing](https://gitlab.fing.edu.uy/users/sign_in)

## <span style="color:orange"> 1.1 Via linux terminal   </span>

Git es utilizado principalemente por linea de commando ya que de este modo se disponen una más amplia gama de funcionalidades. Para instalar git en linux:
```
sudo apt-get install git
```
### <span style="color:orange"> 1.2 Via windows terminal   </span>

Se puede utilizar instalando git Bash termional para windows instalando el programa del siguiente link:  [Download git app](https://git-scm.com/downloads)

### <span style="color:orange"> 1.1 Setear credenciales  </span>

Para asociar un nombre y que luego que el registro en el desarrollo del código indique nuestras credenciales es necesario indicarle a git las credenciales y mail del usuario. 

```
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

## <span style="color:orange"> 1.1 Via windows desktop   </span>

También es posible utilizarlo en windows a través de la aplicación con una interfaz intuitiva y de simple uso. En general esta interfaz suele ser útil para observar de una forma gráfica la interacción entre los repositorios locales y remotos. 

La aplicación está disponible para windows en el siguiente link: [Descargar desktop windows 64bit](https://desktop.github.com/)

## <span style="color:orange"> 3. Crear llave publica y llave privada   </span>
Suele ser útil crear un sistema de autentifcación mediante la técnica criptográfica de llave pública y llave privada. Esto evita verificar las credenciales en cada interacción con el repositorio remoto con el usuario y la clav. 

Las intstrucciones para GitHub se encuetran en el siguiente enlace: [Instrucciones llave públuca/privada ](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent?utm_source=Blog)

Las intstrucciones para GitLab se encuetran en el siguiente enlace: [Instrucciones llave públuca/privada ](https://docs.gitlab.com/ee/ssh/)
