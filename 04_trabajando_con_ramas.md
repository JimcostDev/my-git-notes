## Trabajar con ramas, cambiar entre ellas, fusionar cambios y deshacer cambios

### 📌 **Gestionar ramas**  
- **`git branch`** → Lista, crea o elimina ramas.  
- **`git checkout <nombre de la rama>`** → Cambia entre ramas.  
- **`git checkout -b <nombre de la rama>`** → Crea y cambia a una nueva rama en un solo paso.  
- **`git switch <nombre de la rama>`** → Alternativa moderna a `git checkout` para cambiar de rama.  

### 🔀 **Fusionar cambios**  
- **`git merge <rama>`** → Fusiona los cambios de una rama en otra.  

### 📜 **Historial de cambios**  
- **`git log --oneline`** → Muestra un historial de commits en formato resumido.  

---

## Deshacer cambios en Git  

### 🔄 **Deshacer cambios en el directorio de trabajo (antes de `git add`)**  
- **`git checkout -- <archivo>`** → Restaura un archivo específico a su última versión confirmada.  
- **`git restore .`** → Restaura todos los archivos modificados al último commit (equivalente a `git checkout -- .`).  

### 🚫 **Quitar cambios del área de preparación (`git add` pero sin `git commit`)**  
- **`git reset HEAD <archivo>`** → Quita un archivo del área de staging sin perder los cambios.  
- **`git reset .`** → Quita todos los archivos del área de staging sin perder los cambios.  

### ❌ **Deshacer commits**  
- **`git reset --hard HEAD`** → Revierte completamente el último commit y borra los cambios locales.  
- **`git reset --hard <ID del commit>`** → Vuelve a un commit específico y elimina todos los cambios posteriores.  

### ⏪ **Explorar commits anteriores sin afectar la historia**  
- **`git checkout <ID del commit>`** → Permite ver un commit específico sin modificar la historia (modo `detached HEAD`).  
- **`git switch -`** → Vuelve rápidamente a la última rama en la que estabas.  

### 🧹 **Eliminar archivos no rastreados**  
- **`git clean -fd`** → Borra archivos y carpetas no rastreadas de forma permanente.  

---
