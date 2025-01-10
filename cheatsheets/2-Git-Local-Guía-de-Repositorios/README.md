## Cheatsheet: Repositorios Locales en Git - Tu Espacio de Trabajo Personal

Este cheatsheet te sumerge en el mundo de los repositorios locales en Git, explorando los conceptos y comandos esenciales para un control de versiones efectivo en tu propio equipo.

### 1. ¿Qué es un Repositorio Local?

Imagina un repositorio local como tu propio "laboratorio" para tu proyecto. Es una copia completa del proyecto, incluyendo todo su historial de cambios, almacenada directamente en tu computadora.  Te permite trabajar de forma independiente, experimentar con nuevas ideas y realizar cambios sin afectar el proyecto principal hasta que estés listo para compartirlos.

### 2. Inicializando un Repositorio Local

Para crear un repositorio local Git en un directorio existente, usa el comando `git init`.

```bash
$ git init
Initialized empty Git repository in /ruta/a/tu/proyecto/.git/
```
Este comando crea un directorio oculto llamado `.git` dentro de la carpeta de tu proyecto. Este directorio `.git` es el "cerebro" de tu repositorio, donde Git guarda toda la información sobre el historial de cambios, ramas y configuraciones.

#### 2.1. Ramas Iniciales

Por defecto, `git init` crea una rama llamada "master". Sin embargo, es recomendable usar "main" como rama principal por razones de inclusión. Puedes especificar la rama inicial al crear el repositorio:

```bash
$ git init -b main
Initialized empty Git repository in /ruta/a/tu/proyecto/.git/
```

### 3. Áreas Clave de un Repositorio Local

Un repositorio local se compone de cuatro áreas principales:

* **Directorio de trabajo:** La carpeta visible en tu sistema de archivos donde modificas los archivos del proyecto.
* **Área de preparación (Staging Area):** Un espacio intermedio donde se "preparan" los cambios antes de guardarlos en un commit. Actúa como un "borrador" para organizar los cambios que se incluirán en el siguiente commit.
* **Historial de commits:** Un registro cronológico de todas las instantáneas (commits) del proyecto, representando cada cambio como un punto en el tiempo.
* **Repositorio local (`.git`):** El directorio oculto que guarda toda la información de Git sobre el proyecto, incluyendo el historial de commits, las ramas y la configuración.

### 4. Flujo de Trabajo Básico

1. **Modifica archivos en tu directorio de trabajo:** Edita, crea o elimina archivos como lo harías normalmente.
2. **Prepara los cambios:** Usa el comando `git add` para agregar los archivos modificados al área de preparación.
   ```bash
   $ git add archivo1.txt archivo2.js
   ```
3. **Crea un commit:** Usa el comando `git commit` para guardar los cambios preparados en una nueva instantánea (commit) en el historial de commits.
   ```bash
   $ git commit -m "Mensaje descriptivo del commit"
   ```
    * `-m "Mensaje..."`: Añade un mensaje que describe los cambios realizados en el commit.

### 5. Comandos Útiles

* **`git status`:** Muestra el estado actual del repositorio, incluyendo los archivos modificados, los archivos preparados y la rama actual.
* **`git log`:** Muestra el historial de commits del proyecto, incluyendo la fecha, el autor y el mensaje de cada commit.

### 6. Archivos Rastreados vs. No Rastreados

Git clasifica los archivos en dos categorías:

* **Rastreados:** Archivos que Git está monitoreando y para los cuales guarda el historial de cambios.
* **No Rastreados:** Archivos nuevos que Git aún no está rastreando. Debes usar `git add` para agregarlos al área de preparación y comenzar a  rastrearlos.

### 7. Resumen

Los repositorios locales son la base del control de versiones con Git. Te permiten trabajar de forma independiente, experimentar con cambios y guardar el historial de tu proyecto de manera organizada.

