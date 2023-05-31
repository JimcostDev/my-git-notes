## Git: Comandos Básicos

### `git init`

El comando `git init` se utiliza para inicializar un nuevo repositorio de Git en un directorio existente. Al ejecutar `git init`, Git crea una nueva carpeta oculta llamada ".git" en el directorio actual. Esta carpeta contiene toda la información necesaria para el control de versiones de Git, como el historial de cambios, las ramas y las configuraciones.

### `git add`

El comando `git add` se utiliza para agregar archivos al área de preparación (staging area) en Git. Cuando realizas cambios en tus archivos en el directorio de trabajo, debes usar `git add` para seleccionar los archivos que deseas incluir en el próximo commit. Puedes agregar archivos de forma individual especificando su nombre (`git add archivo.txt`) o agregar todos los archivos modificados en el directorio actual utilizando el comodín `*` (`git add *`).

### `git commit`

El comando `git commit` se utiliza para confirmar los cambios que están en el área de preparación y guardarlos en el repositorio. Cada commit en Git representa una versión específica de tu proyecto. Para realizar un commit, debes proporcionar un mensaje descriptivo que explique los cambios realizados. Por ejemplo, puedes utilizar `git commit -m "Agrega nuevas funcionalidades"` para hacer un commit con un mensaje específico.

El flujo típico de trabajo con estos comandos es el siguiente:

1. Inicias un nuevo repositorio en un directorio existente con `git init`.
2. Realizas cambios en tus archivos en el directorio de trabajo.
3. Utilizas `git add` para agregar los archivos modificados o nuevos al área de preparación.
4. Utilizas `git commit` para confirmar los cambios en el repositorio, junto con un mensaje descriptivo.

Estos comandos básicos de Git te permiten comenzar a versionar y controlar los cambios en tu proyecto de manera efectiva.
