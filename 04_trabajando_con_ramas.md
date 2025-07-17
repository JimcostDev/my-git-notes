## Trabajar con ramas, cambiar entre ellas, fusionar cambios y deshacer cambios

## Gestionar ramas y el historial en Git

### 🌿 **Espacio de trabajo / Inicio de ramas**  
> Crear, cambiar y listar ramas

- **`git branch`** → Lista, crea o elimina ramas.  
- **`git checkout <nombre de la rama>`** → Cambia entre ramas.  
- **`git checkout -b <nombre de la rama>`** → Crea y cambia a una nueva rama en un solo paso.  
- **`git switch <nombre de la rama>`** → Alternativa moderna a `git checkout` para cambiar de rama.  

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
- **`git reset --hard <ID del commit>`** → Vuelve a un commit específico y elimina todo lo posterior.  
- **`git checkout <ID del commit>`** → Navega a un commit anterior sin alterar el historial (modo `detached HEAD`).  
- **`git switch -`** → Cambia de nuevo a la última rama visitada.  

