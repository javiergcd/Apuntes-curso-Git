# Apuntes-curso-Git
Apuntes basicos y esenciales para el manejo de Git &amp; Github

## QUE ES GIT?
Git es un sistema distribuido de control de versiones, gratuito y de código abierto
bajo licencia GPLv2. Fue diseñado originalmente por Linus Torvalds, el creador de
Linux.
## QUE ES UN REPOSITORIO
Un repositorio es una carpeta en la que se
almacenan las diferentes versiones de los ficheros de un proyecto y el histórico de
los cambios que se han realizado en ellos. Los repositorios pueden ser:
- Repositorio local (en nuestro ordenador)
- Repositorio remoto (en un servidor externo)

## INSTALACION DE GIT


## COMANDOS ESENCIALES
Para conocer la versión de git que esta instalado en la maquina
> - "$ git --version" 

Configurar nombre y correo
> - $ git config --global user.name “Su nombre”
> - $ git config --global user.email “Su email”

Configurar el editor de texto de su elección
> - $ git config --global core.editor “code”

Comprobar la configuracion actual 
> - $ git config –list

Crear un proyecto desde cero
> - $ git init nuevo_proyecto
> - $ cd nuevo_proyecto

Iniciar el repositorio de una carpeta ya existente
> - $ cd <directorio del proyecto>
> - $ git init 

---
# STATES Y COMMITS
## ESTADOS EN GIT
Los archivos de un proyecto pueden presentar los siguientes estados:
- Modified (modificado)
- Staged (preparado)
- Commited (confirmado)
A la representacion grafica de los 3 estados:

![referencia_imagen](/src/estados.png)

## RESTAURAR A UNA VERSION ANTERIOR
Restaurar una versión previa que ha sido grabado en el repositorio previamente 
- $ git restore archivo.txt

En cao de que se quiera restaurar todo el directorio de trabajo
> - $ git restore .

En caso de que se quiera restaurar archivos que tengan una cierta extensión 
> - $ git restore ‘*.html’

## QUE ES UN COMMIT?
Un "commit" en Git es una acción que realiza el usuario para guardar un conjunto de cambios en el repositorio. Esencialmente, un commit registra una instantánea del estado actual de los archivos en tu proyecto en un momento dado. Cada commit tiene asociado un mensaje descriptivo que explica los cambios realizados en ese commit.

Los commits son fundamentales en Git y sirven varios propósitos:

1. **Historial de cambios**
2. **Revertir cambios**
3. **Trabajo colaborativo**
4. **Revisión y auditoría**

## COMANDO PARA UN COMMIT
Para agregar archivos al área de preparación (staging)
> - Para un archivo especifico:               **$ git add nombre_del_archivo** 

> - Para todos los archivos modificados:       **$ git add .**                       

Para guardar los cambios que tienen en el área de staging
> - **$ git commit**

Para añadir directamente un mensaje sin abrir el editor
> - **$ git commit -m “descripción del cambio”**

Enviar los cambios al repositorio remoto
> - **$ git push -u origin nombre_de_la_rama**

# BRANCH, MERGE Y CONFLICTOS


## QUE ES UN BRANCH?
Un "branch" en Git es una línea de desarrollo independiente que permite a los usuarios trabajar en características, correcciones de errores u otros cambios en paralelo sin afectar directamente la rama principal del proyecto, generalmente llamada "master" o "main".

![referencia_imagen](/src/branch.png)

La función de las ramas en un entorno de colaboración, donde diferentes personas están trabajando en un mismo código, se genera una evolución del código en paralelo. De esta forma, partiendo de un mismo código se generan diferentes ramas, esto sirve para aislar el trabajo de cada persona y una vez concluido se puede integrar el tronco del usuario hacia la rama principal.

# GITHUB
## DIFERENCIA ENTRE GIT Y GITHUB
La diferencia es que Git es un sistema de control de versiones distribuido que permite a los desarrolladores gestionar el historial de cambios de sus proyectos de software localmente. Por otro lado, GitHub es una plataforma en línea que aloja repositorios de Git de forma remota, facilitando la colaboración entre desarrolladores mediante herramientas como seguimiento de problemas, solicitudes de extracción y revisión de código.

![referencia_imagen](/src/Git%20&%20Github.png)

## CREAR UNA RAMA REMOTA
Creacion de una rama en el repositorio local
- >$ git switch -c website

Para clonar un repositorio remoto con la direccion SSH
- >$ git clone git@github.com:javiergcd/Apuntes-curso-Git.git

Para clonar un repositorio remoto con la direccion HTTPS
- >$ git clone https://github.com/javiergcd/Apuntes-curso-Git.git

Para subir cambios del repositorio local hacia el repositorio remoto
- >$ git push -u origin website

### Ejercicio 4.2
Creacion de un nuevo repositorio en Github con el nombre de "MiPrimerRepositorio", luego se debe vincular este repositorio con el repositorio local, a continuacion se muestra los comando utilizados para importar el proyecto a nuestra maquina.

![Imagen del ejercicio 4.2](/src/Ejercicio4.2.png)

### Ejercicio 4.3
Se debe realizar un cambio en el repositorio local que se importo anteriormente, entonces se realizara un commit y luego un push para sincronizar los cambios realizados hacia el repositorio que esta alojado en GitHub. A continuacion, se muestra los comandos utilizados:
![Imagen del ejercicio 4.3](/src/Ejercicio4.3.png)

# PUSH: PULL Y PULL REQUEST
## Que es una Pull Request?
Un "Pull Request" (PR) es una solicitud que un colaborador envía al propietario de un repositorio remoto para proponer cambios en el código fuente. Se utiliza para revisar, discutir y potencialmente fusionar esos cambios en el proyecto principal. Los PRs facilitan la colaboración y la revisión de código en proyectos de desarrollo de software.

## Hacer una buena Pull Request(PR)
Para hacer una buena Pull Request (PR) y aumentar las posibilidades de que tus cambios sean aceptados en un proyecto de código abierto, se debe tener en cuenta lo siguiente:
- Lee las Contribuciones del Proyecto
- Haz Cambios Significativos
- Cuida la Calidad del Código
- Mantén tus PRs Pequeñas y Enfocadas
- Describe tus Cambios Detalladamente
- Incluye Pruebas (si corresponde)
- Sé Receptivo a los Comentarios
- Mantén tus PRs Actualizadas
- Sé Paciente y Respetuoso

### Ejercicio 5.1
Se realizo la creacion de un "fork" de un repositorio publico.
![Imagen del ejercicio 5.1](/src/Ejercicio5.1.png)

Luego se realizo la clonacion en la maquina local

![Imagen del ejercicio 5.1b](/src/Ejercicio5.1b.png)


se hizo cambios ne el codigo, para luego hacer un push de estos cambio hacia el repositorio remoto.
![Imagen del ejercicio 5.1c](/src/Ejercicio5.1c.png)