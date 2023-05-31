## Uso de `git remote` y `git push` en Git: Conexiones remotas y envío de cambios

### 1. Ejemplo de `git remote add origin <url>`:

Supongamos que tienes un repositorio remoto en GitHub y deseas agregarlo como conexión remota en tu repositorio local.

* Primero, copia la URL del repositorio remoto desde GitHub.
* Abre tu terminal y navega hasta el directorio de tu repositorio local.
* Ejecuta el siguiente comando para agregar la conexión remota:

```shell
git remote add origin https://github.com/tu-usuario/tu-repositorio.git
```
### 2. Ejemplo de `git push -u origin master`:

Supongamos que has realizado algunos commits en tu rama local llamada "master" y deseas enviarlos al repositorio remoto que configuraste anteriormente.

* Asegúrate de estar en la rama "master" de tu repositorio local.
* Ejecuta el siguiente comando para realizar el push de tus commits al repositorio remoto:

```shell
git push -u origin master
```

El flag `-u` establece la rama "master" como la rama de seguimiento (upstream branch) para la conexión remota "origin". Esto significa que en futuros usos de git push sin especificar la rama y el nombre remoto, Git sabrá que deseas hacer push a la rama "master" del repositorio remoto "origin".
