## Cheatsheet: Creando un Commit en Git - Guardando tus Cambios como Instantáneas

Este cheatsheet te guiará a través de los conceptos y pasos prácticos para crear commits en Git, permitiéndote guardar versiones específicas de tu proyecto y construir un historial de cambios claro y organizado.

### 1. ¿Qué es un Commit?

Un commit es como una fotografía de tu proyecto en un momento específico. Captura el estado actual de todos los archivos del proyecto y lo guarda como una "instantánea" en el historial de commits. Cada commit tiene un identificador único (hash) y un mensaje que describe los cambios realizados.

**¿Por qué hacer Commits?**

* **Guardar el progreso:** Registrar el desarrollo del proyecto a medida que avanzas.
* **Revertir cambios:**  Volver a versiones anteriores del proyecto si es necesario.
* **Colaboración:** Facilitar el trabajo en equipo al compartir los cambios de manera organizada.

### 2. Los dos pasos para crear un commit

Crear un commit en Git es un proceso de dos pasos:

1. **Preparar los cambios (Staging):**  Seleccionar los archivos modificados que deseas incluir en el commit y agregarlos al área de preparación (staging area).
2. **Crear el commit:**  Guardar los cambios preparados en una nueva instantánea en el historial de commits.

### 3. Preparando Cambios con `git add`

El comando `git add` se utiliza para agregar archivos modificados al área de preparación. Puedes usar diferentes opciones para agregar archivos:

* **`git add <nombre_de_archivo>`:** Agrega un solo archivo al área de preparación.
* **`git add <archivo1> <archivo2> ...`:** Agrega múltiples archivos al área de preparación.
* **`git add .`:** Agrega todos los archivos modificados en el directorio actual y sus subdirectorios al área de preparación.

**Ejemplo:**
```bash
# Agregar un solo archivo
$ git add index.html

# Agregar múltiples archivos
$ git add estilo.css script.js

# Agregar todos los archivos modificados
$ git add .
```

### 4. Creando un Commit con `git commit`

Después de preparar los cambios, usa el comando `git commit` para crear un nuevo commit.

```bash
$ git commit -m "Mensaje descriptivo del commit"
```

**El mensaje del commit (-m):**

* Es **obligatorio** y debe describir de manera **concisa y clara** los cambios realizados en el commit.
* Usa un lenguaje imperativo en tiempo presente (por ejemplo, "Corregir error en la función X" en lugar de "Se corrigió el error en la función X").
* Separa el asunto del cuerpo del mensaje con una línea en blanco, si es necesario, para una mejor legibilidad.

**Ejemplo de un buen mensaje de commit:**

```
Añadir función de búsqueda al sitio web

Esta nueva función permite a los usuarios buscar productos por nombre y categoría.
```

### 5. Comprobando el estado con `git status`

El comando `git status` es tu mejor amigo en Git.  Te muestra el estado actual del repositorio, incluyendo:

* **Archivos modificados:**  Archivos que han sido modificados pero no se han preparado para el commit.
* **Archivos preparados:** Archivos que se han agregado al área de preparación y están listos para ser incluidos en el próximo commit.
* **Rama actual:** La rama en la que estás trabajando actualmente.

**Ejemplo:**

```bash
$ git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   funcion_busqueda.js
	modified:   index.html

Changes not staged for commit:
  (use "git add <file>..." to index, use "git restore <file>..." to discard changes in working directory)
	modified:   script.js
```

### 6. Resumen

Crear commits es la base del control de versiones con Git. Te permite guardar el progreso, volver a versiones anteriores y colaborar de manera efectiva en tus proyectos.

Recuerda:

* **Prepara tus cambios con `git add`.**
* **Crea commits con mensajes descriptivos usando `git commit -m "..."`.**
* **Usa `git status` para comprobar el estado de tu repositorio.**

