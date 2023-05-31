# Configuración de Git y generación de una clave SSH en Windows

1. Crea una cuenta en GitHub:
   - Ve al sitio web de GitHub (https://github.com) y crea una cuenta si aún no tienes una.

2. Instala Git:
   - Descarga Git desde https://git-scm.com/download/win.
   - Ejecuta el instalador y sigue los pasos para completar la instalación.

3. Configuración global de Git:
   - Abre el "Git Bash" desde el menú de inicio o mediante clic derecho en el Explorador de Archivos y seleccionando "Git Bash Here".
   - Ejecuta los siguientes comandos, reemplazando "Tu nombre" y "tu@email.com" con tu información:

     ```
     git config --global user.name "Tu nombre"
     git config --global user.email "tu@email.com"
     ```

4. Generación de una clave SSH:
   - Abre el "Git Bash".
   - Ejecuta el siguiente comando para generar una nueva clave SSH:

     ```
     ssh-keygen -t rsa -b 4096 -C "tu_email@example.com"
     ```

     - Reemplaza "tu_email@example.com" con tu dirección de correo electrónico asociada a tu cuenta de GitHub.
     - Presiona Enter para aceptar la ubicación predeterminada y deja la frase de contraseña en blanco o crea una si deseas mayor seguridad.

5. Copiar la clave SSH:
   - Abre el Explorador de Archivos.
   - Navega hasta la carpeta `.ssh`, ubicada en tu directorio de usuario (por ejemplo, `C:\Users\TuUsuario\.ssh`).
   - Haz clic derecho en el archivo de clave pública (con extensión `.pub`) y selecciona "Abrir con" y luego elige un editor de texto.
   - Selecciona todo el contenido del archivo y cópialo al portapapeles (`Ctrl + C`).

6. Agregar la clave SSH a tu cuenta de GitHub:
   - Inicia sesión en tu cuenta de GitHub.
   - Haz clic en tu avatar en la esquina superior derecha y selecciona "Settings" (Configuración) en el menú desplegable.
   - Navega a "SSH and GPG keys" (Claves SSH y GPG).
   - Haz clic en "New SSH key" (Nueva clave SSH).
   - Dale un título descriptivo a la clave en el campo "Title" (Título).
   - Pega la clave SSH copiada anteriormente en el campo "Key" (Clave).
   - Haz clic en "Add SSH key" (Agregar clave SSH) para guardarla.

7. Configuración específica del repositorio:
   - En el directorio del repositorio donde deseas asociar la cuenta de GitHub, abre el "Git Bash".
   - Ejecuta los siguientes comandos, reemplazando "Nombre de usuario" y "correo@example.com" con los datos de la cuenta de GitHub:

     ```
     git config user.name "Nombre de usuario"
     git config user.email "correo@example.com"
     ```

Estos pasos te ayudarán a configurar Git y generar una clave SSH en Windows para asociarla a tu cuenta de GitHub. Recuerda que puedes utilizar la misma configuración de Git para trabajar con varios repositorios, pero cada repositorio puede tener una configuración específica.

