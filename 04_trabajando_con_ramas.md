## Trabajar con ramas, cambiar entre ellas, fusionar cambios y deshacer cambios

## Gestionar ramas y el historial en Git

### 🌿 **Espacio de trabajo / Inicio de ramas**  
> Crear, cambiar y listar ramas

- **`git branch`** → Lista las ramas locales.  
- **`git branch <nombre>`** → Crea una nueva rama sin cambiar a ella.  
- **`git branch -d <nombre>`** → Elimina una rama (solo si fue fusionada).  
- **`git branch -D <nombre>`** → Fuerza la eliminación de una rama sin importar si fue fusionada.  
- **`git checkout -b <nombre>`** → Crea y cambia a una nueva rama en un solo paso.  
- **`git switch <nombre>`** → Alternativa moderna a `git checkout` para cambiar de rama.
- **`git switch -c <nombre>`** → Crear una rama y directamente moverte a ella en lugar de usar `git checkout -b`. 

### 🔀 **Área de trabajo / Fusionar cambios**  
> Combina ramas ya existentes

- **`git merge <rama>`** → Fusiona los cambios de una rama en la actual.  

### 📜 **Repositorio / Historial de commits**  
> Ver el historial de cambios confirmados

- **`git log --oneline`** → Muestra un historial de commits en formato resumido.  

---

## Deshacer cambios en Git

### 🛠️ **Espacio de trabajo (Working Directory)**  
> Cambios hechos localmente antes de usar `git add`

- **`git checkout -- <archivo>`** → Restaura un archivo a su última versión confirmada.  
- **`git restore .`** → Revierte todos los archivos modificados al último commit.  
- **`git clean -fd`** → Elimina archivos y carpetas no rastreados permanentemente.  

### 🚧 **Área de preparación (Staging Area)**  
> Cambios añadidos con `git add`, pero aún no confirmados

- **`git reset HEAD <archivo>`** → Saca un archivo del staging sin perder los cambios.  
- **`git reset .`** → Saca todos los archivos del staging sin perder cambios.  
- **`git rm --cached <archivo>`** → Saca el archivo del área de staging y pero no borra el archivo de tu carpeta local. 

### 🗃️ **Repositorio / Historial de commits**  
> Cambios ya confirmados con `git commit`

- **`git reset --hard HEAD`** → Elimina el último commit y borra todos los cambios locales.  
- **`git reset --soft <ID del commit>`** → Vuelve a un commit anterior pero mantiene todos los cambios en staging (listos para hacer commit de nuevo).
- **`git reset --mixed <ID del commit>`** → (por defecto) → Vuelve a un commit anterior, mantiene los cambios en el directorio de trabajo, pero los saca del staging.
- **`git reset --hard <ID del commit>`** → Vuelve a un commit anterior y borra todos los cambios posteriores, tanto en staging como en el directorio de trabajo.    
- **`git checkout <ID del commit>`** → Navega a un commit anterior sin alterar el historial (modo `detached HEAD`).  
- **`git switch -`** → Cambia de nuevo a la última rama visitada.
  
### 🧭 **Volver atrás en tus movimientos (`reflog`)**

- **`git reflog`** → Muestra el historial de todos los movimientos recientes de `HEAD`, incluyendo cambios de ramas, commits y checkouts.  
  Útil para volver al **último commit o rama visitada**, incluso después de usar `git checkout <ID>`.

### 📦 **Guardado temporal (Stash)**  
> Guarda cambios en progreso sin hacer commit, dejando el directorio limpio para cambiar de rama o hacer otras tareas

- **`git stash`** (o `git stash push`) → Guarda los cambios rastreados (modificados y en `staging`) y vuelve al estado del último commit.
- **`git stash pop`** → Aplica el último stash en la rama actual y lo elimina de la pila.
- **`git stash apply`** → Aplica el último stash pero lo mantiene guardado (útil si necesitas aplicarlo en varias ramas).
- **`git stash list`** → Muestra todos los stashes guardados con su identificador (ej. `stash@{0}`).
- **`git stash drop`** → Elimina un stash específico (ej. `git stash drop stash@{1}`).
- **`git stash -u`** (o `--include-untracked`) → Incluye también archivos nuevos (untracked) al guardar.
- **`git stash -a`** (o `--all`) → Incluye archivos nuevos e ignorados (untracked + ignored).
- **`git stash push -m "mensaje"`** → Guarda el stash con un nombre descriptivo para identificarlo fácilmente en el `list`.
- **`git stash --keep-index`** → Guarda los cambios pero mantiene el área de `staging` intacta (útil para probar solo lo que irá en el commit).
- **`git stash branch <nombre>`** → Crea una nueva rama desde el commit donde se hizo el stash y aplica los cambios allí; ideal para evitar conflictos cuando llevas mucho tiempo sin aplicar un stash.

> [!WARNING]
> Si al hacer `pop` o `apply` se producen **conflictos**, Git **no eliminará** el stash de la pila. Resuelve los conflictos manualmente, haz `git add` y, una vez resuelto, ejecuta `git stash drop` para limpiar el stash usado.

> [!TIP]
> Puedes combinarlo con:
> - **`git switch -`** → Vuelve a la última rama en la que estabas (muy útil tras ver un commit antiguo).
> - **`git switch <nombre-de-la-rama>`** → Vuelve manualmente a la rama deseada si sabes su nombre.