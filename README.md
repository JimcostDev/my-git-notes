# Configuración de Git y generación de una clave SSH en Windows

## 🔹 1. Crear una cuenta en GitHub
- Ve a [GitHub](https://github.com) y regístrate si aún no tienes una cuenta.

---

## 🔹 2. Instalar Git
- Descarga Git desde [git-scm.com](https://git-scm.com/download/win).
- Ejecuta el instalador y sigue las instrucciones para completar la instalación.

---

## 🔹 3. Configuración global de Git
- Abre **Git Bash** desde el menú de inicio o haciendo clic derecho en un directorio y seleccionando *Git Bash Here*.
- Configura tu nombre y correo electrónico globalmente:

```shell
git config --global user.name "Tu nombre"
git config --global user.email "tu@email.com"
```

---

## 🔹 4. Generación de una clave SSH
- En **Git Bash**, ejecuta:

```shell
ssh-keygen -t rsa -b 4096 -C "tu_email@example.com"
```

- Reemplaza *tu_email@example.com* con tu correo asociado a GitHub.
- Presiona *Enter* para aceptar la ubicación predeterminada (`C:\Users\TuUsuario\.ssh\id_rsa`).
- Puedes dejar la frase de contraseña en blanco o definir una por seguridad.

---

## 🔹 5. Copiar la clave SSH
- Abre el Explorador de Archivos y ve a `C:\Users\TuUsuario\.ssh`.
- Abre el archivo **id_rsa.pub** con un editor de texto.
- Copia su contenido al portapapeles (`Ctrl + C`).

---

## 🔹 6. Agregar la clave SSH en GitHub
1. Inicia sesión en GitHub.
2. Ve a **Settings** (*Configuración*).
3. Dirígete a **SSH and GPG keys**.
4. Haz clic en **New SSH key** (*Nueva clave SSH*).
5. Asigna un nombre en *Title* y pega la clave copiada en *Key*.
6. Haz clic en **Add SSH key**.

---

## 🔹 7. Configuración específica del repositorio
Si deseas establecer una configuración distinta en un repositorio específico:

```shell
git config user.name "Nombre de usuario"
git config user.email "correo@example.com"
```

Este proceso garantiza que Git esté correctamente configurado y autenticado con GitHub a través de SSH en Windows. 🚀
