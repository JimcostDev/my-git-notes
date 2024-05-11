## Trabajar con ramas, cambiar entre ellas, fusionar cambios y deshacer cambios.

- `git log --oneline`: Muestra un registro de los commits en una sola línea, proporcionando un resumen conciso del historial del repositorio.

- `git branch`: Permite listar, crear o eliminar ramas.

- `git checkout`: Se utiliza para cambiar entre ramas o versiones de archivos.

- `git checkout -b`: Crea una nueva rama y cambia a ella en un solo paso.

- `git merge`: Fusiona los cambios de una rama en otra.


## Deshacer cambios en Git

1. **`git checkout -- <nombre del archivo>`**:
   - Úsalo para revertir los cambios locales en un archivo específico antes de hacer `git add`.

2. **`git reset HEAD <nombre del archivo>`**:
   - Úsalo para quitar un archivo específico del área de preparación después de hacer `git add`, pero antes de hacer `git commit`.

3. **`git reset`**:
   - Úsalo para quitar todos los archivos del área de preparación después de hacer `git add`, pero antes de hacer `git commit`.

4. **`git reset --hard HEAD`**:
   - Úsalo para deshacer completamente el último commit, borrando los cambios realizados desde ese commit y revertiendo los archivos en tu directorio de trabajo al estado en el que estaban en el último commit.
   - Útil si deseas deshacer completamente el último commit y perder los cambios locales no guardados.

5. **`git reset --hard <ID del commit>`**:
   - Úsalo si deseas volver a un commit específico y eliminar todos los cambios posteriores. Esto reescribirá la historia del repositorio y los cambios posteriores se perderán.

6. **`git checkout <ID del commit>`**:
   - Úsalo si solo deseas revisar el estado de un commit específico sin perder los cambios posteriores. Esto te permitirá "viajar en el tiempo", pero estarás en un estado de "detached HEAD".

