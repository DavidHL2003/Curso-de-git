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

## *States y commits*

### *Los 3 estados de Git* 🎯
*Cuando usamos Git, los archivos de nuestro proyecto se pueden encontrar en uno de los siguientes estados:*

1. ***Modified:** El archivo contiene cambios pero todavía no han sido marcados para ser confirmados. Se encuentra en el directorio de trabajo.*

2. ***Staged:** Son los archivos que han sido modificados en el directorio de trabajo y se han marcado como preparados para ser confirmados en el repositorio local. Se encuentran en un área temporal transitoria. Esta acción recibe el nombre de add.*

3. ***Committed:*** *El archivo se encuentra grabado en el repositorio local. Esta acción recibe el nombre de commit.*

![git](img/git-estados.png)

### *¿Qué es un commit?* 🤔
* 📝 *Los commits sirven para registrar los cambios que se han producido en el repositorio, es una de las piezas más importantes para entender cómo funciona Git.*

* 📷 *Piensa en los commits como si fuesen fotografías. Cada fotografía muestra el estado de todos los archivos de tu repositorio en el momento en que se hizo y cada una va firmada con el autor, la fecha, localización y otra información útil.*

* 🎮 *En pocas palabras un commit es como un punto de guardado de la partida de tu juego.*

***¿Cómo puedo hacer un commit?***

1. *Si quieres guardar los cambios que tienes en el área de staging, puedes hacer un commit con el siguiente comando:*

    ```
    git commit
    ```

2. *Si quieres añadir directamente un mensaje sin abrir el editor, puedes usar el parámetro -m o --message:*

    ```
    git commit -m "Add new search feature"
    ```

### *¿Qué es el HEAD?*

*HEAD es el puntero que referencia el punto actual del historial de cambios del repositorio en el que estás trabajando. Normalmente será el último commit de la rama en la que te encuentres pero como también puedes moverte entre commits es posible que HEAD no sea el último commit.*

![git](img/branch-and-history.png)

### *Otros comandos basicos de Git 💯*

***Usando git add 👨‍💻*** 

*El comando git add en Git se usa para agregar archivos al área de preparación. Esto significa que estás indicando qué cambios quieres incluir en el próximo commit.*

* ⭐***Primera opción:*** *Puedes agregar archivos espesicos al area de preparación, esto es una buena practica.*
    ```
    git add archivo.txt
    ```

* 🙀***Segunda opción:*** *Puedes agregar todos los archivos al area de preparación al mismo tiempo, pero no es muy recomendado por que pueden a ver algunos archivos con errores que aún no fueron resueltos.*

    ```
    git add .
    ```

***Usando git log 👨‍💻***

* ⭐***Primera opción:*** *Con git log podemos ver el lista de todos los commits realizados cronologicamente.*

    ```
    git log
    ```
* 🙀***Segunda opción:*** *Para mostrar los commit en una forma mas compacta o de una sola linea utilizamos el siguiente comando.*

    ```
    git log --oneline
    ```
* ✨*Al ejecutar el comando git log --oneline nos muestra esto.*

    ```
    23a97fc (HEAD -> main, origin/main) Add: Sección States y commits
    b6483db Add:Inicializar un repositorio y subirlo a Github
    e98ddd5 Add:Configuración de Git
    0cc4583 Add:Instalación de git en Linux/MacOS/Windows
    88eb6d0 Add:Introdicción a Git
    8f20b19 Add:Creación del repositorio
    ```
***Usando git status 👨‍💻***
* 🔥 *Este comando lo utilizamos para ver el estado actual del repositorio, es decir, qué archivos han cambiado, cuáles están listos para hacer commit y cuáles no.*

    ```
    git status
    ```
* ✨*Al ejecutar el comando nos muestra esto:*

    ```
    On branch main
    Your branch is up to date with 'origin/main'.

    Changes not staged for commit:
    (use "git add <file>..." to update what will be committed)
    (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

    no changes added to commit (use "git add" and/or "git commit -a")
    ```
