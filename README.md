# *Curso de Git & Github*
![git](img/git_github.jpg)
## *Descripción del curso* 🚀 
📝 *Este documento contiene mis notas personales sobre el curso de git y github para las configuraciones iniciales de git como los comandos que se utilizan para trabajar con proyectos de software, del mismo modo revisaremos las mejores practicas que se utilizan en git.*

## 🎁 *Regalo de bienvenida* 🎁
*¡Gracias por entrar a mi curso de Git! Como regalo de bienvenida, te dejo un conjunto de comandos Git esenciales para que empieces con el pie derecho.*


* 🎁 *Abrir regalo* 👉[https://academia-x.netlify.app/cheatsheets/git.html](https://academia-x.netlify.app/cheatsheets/git.html)


 ## 📋 Índice
> 1. [🚀 **Introducción a Git** ](#introducción-a-git)
> 2. [✏️ **States y commits**](#states-y-commits)
> 3. [🌳 **Ramas, merge y conflictos**](#ramas-merge-y-conflictos)
> 4. [🐙 **Github, push pull y pull-request**](#github-push-pull-y-pull-request)
> 5. [🧩 **Flujos de trabajo y estrategias de ramas en Git**](#flujos-de-trabajo-y-estrategias-de-ramas-en-git)
> 6. [⭐ **Buenas prácticas en git**](#buenas-prácticas-en-git)
> 7. [↩️ **Deshacer cambios**](#deshacer-cambios)
> 8. [🎯 **Hooks, Alias y Trucos Git**](#hooks-alias-y-trucos-git)

## *Introducción a Git*


### *¿Qué es Git?* 🤔
*Git es un sistema distribuido de control de versiones, gratuito y de código abierto bajo licencia GPLv2. Fue diseñado originalmente por Linus Torvalds12, el creador de Linux.*
*Git, al ser un sistema distribuido, aloja una copia completa del repositorio en cada máquina local que está trabajando en el código.*

![git](img/git.png)

### *Instalación Git*

1. ***Linux(Ubuntu\Debian)* 🐧**

* *Lo instalamos desde el repositorio de software de nuestra distrubución ejecutamos los siguientes comandos en nuestra terminal:*

    ```
    sudo apt update
    sudo apt install git
    ```
* *Verificamos la version de git que se instalo:*
    ```
    git --version
    ```
*Con eso ya tenemos git funcionando en nuestro Debian* 💯

2. ***MacOS* 🍏**

 *En macOS la forma de instalar git es con **Homebrew** a continuación te dejo los pasos para la instalación correctamente:*
* *Instalar **Homebrew** si aún no lo tienes instalado* 🔧
* *Instalar git con brew* 🔥
* *Verificamos la versión de git que se instalo* 💯

    ```
    xcode-select --install/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

    brew install git

    git --version
    ```

3. ***Windows* 💻**

*En Windows es más sencillo descargar el instalador oficial y seguir los pasos del asistente:*

* *Descargarga el instalador de* 👉[https://git-scm.com/download/win](https://git-scm.com/download/win)

* *Ejecuta el instalador* 🔥

* *Finaliza la instalación* 💯

### *Configuración de Git* 🛠️

*Para hacer que tus commits se asocien a tu nombre y aparezca correctamente tu avatar en la plataforma de GitHub, necesitamos realizar la siguiente configuración.*


1. *Configura tu nombre* 😀

    ```
    git config --global user.name "<tu nombre>"
    ```
2. *Configura tu correo electronico* ✉️

    ```
    git config --global user.email "<tu email>"
    ```
📌***NOTA***: *El correo electronico tiene que ser el mismo con el que estas registrado en Github.*

***Otras configuraciones adicionales* ⚙️** 

* *Para comprobar nuestra configuración de git ejecutamos el siguiente comando:*

    ```
    git config --list
    ```
* *Si necesitamos ayuda y mas opciones de configuración* 

    ```
    git config --help
    ```

### *Inicializar un repositorio Git desde cero y subirlo a GitHub* 🐱

1. ***Creamos nuestro archivo README.md***

* *Este archivo contendra toda la información sobre nuestro proyecto.*

    ```
    echo "# Curso-Git-Github-SCESI2025" >> README.md
    ```
2. ***Inicializar un repositorio***

 * *Inicializamos un repositorio Git vacío en tu nuestra carpeta actual.*

    ```
    git init
    ```
*Con eso ya tenemos inicializado nuestro repositorio pero solamente de forma local.*

3. ***Agregar el archivo***

* *Agregamos nuestro archivo README.md al área de preparación para que se pueda subir a Github.*

    ```
    git add README.md
    ```

4. ***Commit inicial***

* *Creamos nuestro primer commit para que se guarden los cambios del README.md*

    ```
    git commit -m "first commit"
    ```

5. ***Cambio de nombre de la rama***

* *Cambiamos el nombre de nuestra rama a main ya que inicialmente esta con Master*

    ```
    git branch -M main
    ```

6. ***Conexión del repositorio local con el remoto***

* *Conectamos nuestro repositorio local con el remoto con la url que nos proporciona Github*

    ```
    git remote add origin https://github.com/TuNombreDeGithub/Curso-Git-Github-SCESI2025.git
    ```

7. ***Envio del commit a Github***

* *Enviamos el commit inicial que realizamos a la rama main, el -u vincula nuestra rama local con la rama remota.*

    ```
    git push -u origin main
    ```

*Listo y con esos 7 pasos ya tenemos nuestro repositorio Git Inicializado y subido a Github 😎*
