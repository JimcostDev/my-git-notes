## Uso de `git remote` y `git push` en Git: Conexiones remotas y envío de cambios

### 📡 **Configurar una conexión remota (`git remote add origin`)**
Si tienes un repositorio en GitHub y deseas conectarlo con tu repositorio local, sigue estos pasos:

1. Copia la URL del repositorio remoto desde GitHub.
2. Abre la terminal y navega hasta el directorio de tu repositorio local.
3. Agrega la conexión remota con el siguiente comando:

```shell
git remote add origin https://github.com/tu-usuario/tu-repositorio.git
```

💡 **Nota:** Para verificar que la conexión remota se agregó correctamente, usa:
```shell
git remote -v
```
Esto mostrará la URL configurada para `origin`.

---

### 🚀 **Enviar cambios al repositorio remoto (`git push`)**
Si ya realizaste commits en tu rama local (por ejemplo, `master` o `main`) y deseas enviarlos al repositorio remoto:

1. Asegúrate de estar en la rama correcta:
```shell
git branch
```

2. Realiza el push de los cambios:
```shell
git push -u origin master
```

📌 **Explicación del comando:**
- `git push` → Envía los cambios al repositorio remoto.
- `-u` (o `--set-upstream`) → Establece la rama `master` como rama de seguimiento para futuros `git push` y `git pull`.
- `origin master` → Especifica que estás enviando los cambios a la rama `master` del remoto `origin`.

🔄 **En futuros push, solo necesitarás ejecutar:**
```shell
git push
```
Esto enviará los cambios a la rama previamente configurada.

---
