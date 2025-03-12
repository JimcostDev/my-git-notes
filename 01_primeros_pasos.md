# Git: Primeros pasos - Working Directory, Staging Area y Repository

En Git, existen tres conceptos clave que debes comprender al comenzar a utilizarlo:

---

## 📂 1. Directorio de trabajo (*Working Directory*)
El *directorio de trabajo* es el espacio en tu sistema de archivos donde realizas modificaciones en los archivos de tu proyecto. Contiene la versión actual de los archivos en tu máquina local, permitiéndote editar, agregar o eliminar contenido.

💡 **Punto clave:** Aquí es donde realizas cambios antes de prepararlos para su confirmación.

---

## 📌 2. Área de preparación (*Staging Area* o *Index*)
El *área de preparación* actúa como un espacio intermedio donde seleccionas qué cambios serán incluidos en el próximo commit. Cuando modificas archivos en el directorio de trabajo, debes agregarlos al área de preparación con:

```shell
git add <archivo>
```

O para agregar todos los archivos modificados:
```shell
git add .
```

💡 **Punto clave:** Solo los cambios agregados al área de preparación serán incluidos en el próximo commit.

---

## 📜 3. Repositorio (*Repository*)
El *repositorio* es donde se almacenan de forma permanente los cambios confirmados. Contiene el historial completo del proyecto, incluyendo versiones anteriores y detalles de cada modificación.

Para confirmar los cambios agregados al área de preparación, usa:
```shell
git commit -m "Mensaje descriptivo del cambio"
```

📌 **Tipos de repositorio:**
- **Local**: Almacenado en tu máquina, contiene el historial del proyecto.
- **Remoto**: Almacenado en plataformas como GitHub, GitLab o Bitbucket para colaboración y respaldo.

---

## 🔄 Flujo de trabajo en Git
1. Modificas archivos en el **Directorio de trabajo**.
2. Usas `git add` para mover los cambios al **Área de preparación**.
3. Confirmas los cambios con `git commit`, almacenándolos en el **Repositorio**.

Este proceso garantiza un control preciso sobre las versiones del proyecto y facilita la colaboración entre desarrolladores. 🚀
