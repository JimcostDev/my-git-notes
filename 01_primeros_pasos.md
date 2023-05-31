# Git: Primeros pasos - Working Directory, Staging Area y Repository

En el contexto de Git, existen tres conceptos clave que debes comprender al comenzar a utilizarlo:

## 1. Directorio de trabajo (Working Directory)

El *directorio de trabajo* es el lugar en tu sistema de archivos donde estás llevando a cabo tu trabajo actual. Contiene los archivos que estás modificando, agregando o eliminando en tu proyecto. Es simplemente una copia de los archivos en tu máquina local.

## 2. Área de preparación (Staging Area o Index)

El *área de preparación* es un espacio intermedio en Git donde se preparan los cambios antes de ser confirmados en el repositorio. Cuando realizas modificaciones en los archivos dentro del directorio de trabajo, necesitas agregar esos cambios al área de preparación antes de que puedan ser incluidos en el repositorio. Puedes seleccionar los archivos o partes específicas de archivos que deseas incluir en el área de preparación mediante el comando `git add`. Una vez que los cambios están en el área de preparación, están listos para ser confirmados.

## 3. Repositorio (Repository)

El *repositorio* es el lugar donde se almacenan de forma permanente los cambios confirmados en Git. Contiene todo el historial de cambios de tu proyecto. Es como una base de datos que guarda todas las versiones de los archivos y la información relacionada, como quién realizó los cambios y cuándo se realizaron. El repositorio puede estar en tu máquina local o en un servidor remoto (como GitHub, GitLab o Bitbucket).

El flujo típico de trabajo con Git consiste en realizar modificaciones en el directorio de trabajo, agregar los cambios al área de preparación y luego confirmarlos en el repositorio. Este proceso de agregar cambios al área de preparación y confirmarlos en el repositorio te permite tener un control preciso sobre las versiones de tu proyecto y facilita el trabajo colaborativo con otros desarrolladores.
