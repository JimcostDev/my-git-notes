## Git: Comandos Básicos

### 🛠️ **Inicializar un repositorio (`git init`)**
El comando `git init` crea un nuevo repositorio de Git en un directorio existente. Al ejecutarlo, Git genera una carpeta oculta llamada `.git`, que contiene toda la información necesaria para el control de versiones, como el historial de cambios, las ramas y la configuración del repositorio.

```shell
git init
```

---

### 📌 **Agregar cambios al área de preparación (`git add`)**
El comando `git add` mueve archivos modificados o nuevos al área de preparación (staging area), indicándole a Git que deben incluirse en el próximo commit.

- Agregar un archivo específico:
```shell
git add archivo.txt
```

- Agregar todos los archivos modificados: Ideal para preparar todos los cambios antes de un commit.
```shell
git add -A
```
- Añade archivos solo dentro del directorio actual y subdirectorios (no sube cambios fuera de la carpeta en la que estás).
```shell
git add .
```
---

### ✅ **Confirmar cambios en el repositorio (`git commit`)**
El comando `git commit` guarda los cambios agregados al área de preparación en el historial del repositorio. Cada commit representa una versión específica del proyecto y debe incluir un mensaje descriptivo.

```shell
git commit -m "Mensaje descriptivo del cambio"
```

💡 **Flujo de trabajo típico en Git:**
1. Inicializar un repositorio con `git init` (solo una vez por proyecto).
2. Modificar o agregar archivos.
3. Usar `git add` para preparar los archivos para el commit.
4. Confirmar los cambios con `git commit -m "Descripción de los cambios"`.

Con estos comandos básicos, puedes comenzar a gestionar versiones de tu proyecto de manera eficiente. 🚀
