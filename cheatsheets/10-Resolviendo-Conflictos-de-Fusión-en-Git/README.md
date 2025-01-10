## Cheatsheet: Conflictos de Fusión en Git - Navegando las Colisiones de Código

Este cheatsheet te guiará a través del proceso de comprender y resolver **conflictos de fusión** en Git. Aprenderás cómo identificarlos, las causas comunes y los pasos para resolverlos de manera efectiva, asegurando una colaboración fluida y un historial de proyecto limpio.

### 1. ¿Qué son los Conflictos de Fusión?

Los conflictos de fusión ocurren cuando Git **no puede combinar automáticamente los cambios de diferentes ramas** durante una fusión o un rebase. Esto sucede cuando se realizan modificaciones en **las mismas secciones de un mismo archivo** en ambas ramas.

Imagina que tú y tu compañero están editando el mismo párrafo de un documento. Al intentar combinar sus versiones, surgen **conflictos** porque no está claro qué cambios se deben mantener.

### 2.  Causas Comunes de Conflictos de Fusión

* **Ediciones concurrentes:**  Dos o más personas modifican las mismas líneas de código en un archivo simultáneamente.
* **Eliminación de archivos:** Un archivo es eliminado en una rama mientras se edita en otra.
* **Modificaciones superpuestas:** Cambios realizados en diferentes partes de un archivo se superponen y crean inconsistencias.

### 3. Identificando Conflictos de Fusión

Git te alertará sobre los conflictos de fusión con mensajes específicos en la terminal.  Además, **marcará las áreas conflictivas dentro de los archivos afectados**.

**Ejemplo de Marcadores de Conflicto:**

```
<<<<<<< HEAD
Esta es la versión del archivo en la rama actual.
=======
Esta es la versión del archivo en la rama que se está fusionando.
>>>>>>> rama_fusionada
```

* **`<<<<<<< HEAD`:** Indica el inicio del bloque de código de tu rama actual.
* **`=======`:** Separa los bloques de código de las dos ramas.
* **`>>>>>>> rama_fusionada`:**  Indica el final del bloque de código de la rama que se está fusionando.

### 4. Resolviendo Conflictos de Fusión

1. **Abrir el archivo en conflicto:**  Abre el archivo marcado con conflicto en un editor de texto.

2. **Analizar los cambios:**  Revisa cuidadosamente los marcadores de conflicto y los cambios realizados en cada rama.

3. **Decidir qué cambios conservar:**  Elige qué cambios de cada rama deseas incluir en la versión final del archivo.  Puedes:

    * **Conservar una versión:** Eliminar el código de una rama y mantener el de la otra.
    * **Combinar los cambios:** Integrar manualmente las modificaciones de ambas ramas.
    * **Descartar ambos cambios:** Eliminar completamente la sección en conflicto y escribir nuevo código.

4. **Eliminar los marcadores de conflicto:**  Asegúrate de eliminar los marcadores  `<<<<<<<`, `=======`, y `>>>>>>>`.

5. **Guardar el archivo:** Guarda los cambios después de resolver los conflictos.

### 5. Finalizando la Fusión

1. **Agregar los archivos resueltos:**  Utiliza `git add` para marcar los archivos con los conflictos resueltos.

    ```bash
    $ git add <archivo_con_conflicto_resuelto>
    ```

2. **Hacer commit:** Crea un nuevo commit para registrar la resolución del conflicto.

    ```bash
    $ git commit -m "Resolución de conflicto en <nombre_del_archivo>"
    ```

### 6. Ejemplo Práctico

Supongamos que tienes un conflicto en el archivo `index.html`:

```html
<<<<<<< HEAD
<h1>Título original</h1>
=======
<h1>Nuevo título</h1>
>>>>>>> feature
```

Puedes decidir conservar el "Nuevo título" de la rama "feature":

```html
<h1>Nuevo título</h1>
```

Luego, guarda el archivo, agrega los cambios y haz commit:

```bash
$ git add index.html
$ git commit -m "Resolución de conflicto en index.html"
```

### 7. Resumen

Los conflictos de fusión son inevitables en la colaboración con Git.  Comprender cómo identificarlos, las causas comunes y los pasos para resolverlos te permitirá manejarlos con confianza, manteniendo la integridad de tu proyecto y un flujo de trabajo eficiente. 
