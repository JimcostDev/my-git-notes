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
- **`git rm --cached <archivo>`** →  Saca el archivo del área de staging y pero no borra el archivo de tu carpeta local. 

### 🗃️ **Repositorio / Historial de commits**  
> Cambios ya confirmados con `git commit`

- **`git reset --hard HEAD`** → Elimina el último commit y borra todos los cambios locales.  
- **`git reset --soft <ID del commit>`** → Vuelve a un commit anterior pero mantiene todos los cambios en staging (listos para hacer commit de nuevo).
- **`git reset --mixed <ID del commit>`** →  (por defecto) → Vuelve a un commit anterior, mantiene los cambios en el directorio de trabajo, pero los saca del staging.
- **`git reset --hard <ID del commit>`** → Vuelve a un commit anterior y borra todos los cambios posteriores, tanto en staging como en el directorio de trabajo.    
- **`git checkout <ID del commit>`** → Navega a un commit anterior sin alterar el historial (modo `detached HEAD`).  
- **`git switch -`** → Cambia de nuevo a la última rama visitada.  

