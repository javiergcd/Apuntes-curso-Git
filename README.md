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
- "$ git --version" 

Configurar nombre y correo
- $ git config --global user.name “Su nombre”
- $ git config --global user.email “Su email”

Configurar el editor de texto de su elección
- $ git config --global core.editor “code”

Comprobar la configuracion actual 
- $ git config –list

Crear un proyecto desde cero
- $ git init nuevo_proyecto
- $ cd nuevo_proyecto

Iniciar el repositorio de una carpeta ya existente
- $ cd <directorio del proyecto>
- $ git init 

---
# STATES Y COMMITS
## ESTADOS EN GIT
Los archivos de un proyecto pueden presentar los siguientes estados:
- Modified (modificado)
- Staged (preparado)
- Commited (confirmado)
A la representacion grafica de los 3 estados:

![referencia_imagen](/src/estados.png)
