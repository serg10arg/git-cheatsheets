## Cheatsheet: Rebase en Git - Reescribiendo la Historia para una Colaboración Limpia

Este cheatsheet te guiará a través del proceso de **rebase en Git**, una poderosa herramienta que te permite reescribir la historia de tu rama, creando un historial de proyecto más lineal y fácil de entender. Aprenderás cómo funciona el rebase, sus ventajas, las precauciones que debes tomar y cómo manejar los conflictos que puedan surgir durante el proceso.

### 1. ¿Qué es Rebase?

**Rebase** es una operación que **toma los commits de una rama y los "reaplica" sobre otra rama**, creando nuevos commits con diferentes hashes.  En esencia, reescribes la historia de la rama, moviendo sus commits a una nueva base.

**Ejemplo:**

Imagina que tienes una rama llamada "feature" que se ramificó de "main".  Al hacer rebase de "feature" sobre "main", los commits de "feature" se moverán para que parezcan haber sido creados después de los commits más recientes de "main", creando una línea de desarrollo única y sin ramificaciones.

### 2.  Ventajas de Usar Rebase

* **Historial de Proyecto Lineal:** Rebase ayuda a mantener un historial de proyecto limpio y lineal, facilitando la comprensión de los cambios y la búsqueda de errores.
* **Evita Merge Commits:** A diferencia de la fusión, el rebase evita la creación de "merge commits" innecesarios, lo que hace que el historial sea más conciso.
* **Colaboración Más Fluida:** Rebase puede facilitar la integración de cambios de diferentes colaboradores, especialmente cuando se trabaja en ramas de larga duración.

### 3.  Precauciones al Usar Rebase

**¡Atención! Rebase reescribe la historia de la rama.  Esto puede ser peligroso si no se utiliza con precaución.**

* **Regla de Oro del Rebase:** **Nunca hagas rebase de una rama que ya ha sido compartida con otros colaboradores**.  Reescribir una rama pública puede causar confusión y problemas de sincronización.
* **Usa Rebase con Ramas Locales:** Es más seguro usar rebase con ramas locales que aún no se han enviado al repositorio remoto.

### 4.  Pasos para Realizar un Rebase

1. **Cambiar a la rama que deseas rebasear:**

    ```bash
    $ git checkout <nombre_rama>
    ```
2. **Ejecutar el comando rebase:**

    ```bash
    $ git rebase <nombre_rama_destino> 
    ```
   Esto rebaseará la rama actual sobre la rama especificada.

### 5. Manejo de Conflictos durante el Rebase

Al igual que con las fusiones, durante un rebase **pueden surgir conflictos si se han realizado cambios en las mismas secciones de un archivo en ambas ramas.**

**Pasos para resolver conflictos durante un rebase:**

1. **Identificar los archivos en conflicto:** Git te indicará los archivos que tienen conflictos.
2. **Resolver los conflictos:** Abre los archivos en conflicto, analiza los cambios y elige qué versión del código quieres conservar.  Elimina los marcadores de conflicto.
3. **Agregar los archivos resueltos:** Usa `git add` para marcar los archivos con los conflictos resueltos.
4. **Continuar el rebase:** Ejecuta `git rebase --continue` para continuar con el proceso.

**Si deseas abortar el rebase en cualquier momento, usa `git rebase --abort`.**

### 6.  Ejemplo Práctico

1. **Tienes una rama llamada "feature" y quieres rebasearla sobre "main".**

2. **Cambiar a la rama "feature":**

    ```bash
    $ git checkout feature
    ```

3. **Rebasear "feature" sobre "main":**

    ```bash
    $ git rebase main
    ```

4. **Si hay conflictos, resuélvelos y usa `git add` para agregar los archivos.**

5. **Continuar el rebase:**

    ```bash
    $ git rebase --continue
    ```

6. **Empujar la rama rebaseada al repositorio remoto (opcional):**

    ```bash
    $ git push --force-with-lease origin feature 
    ```
   **Usa `--force-with-lease` para evitar sobrescribir accidentalmente los cambios de otros.**

### 7. Resumen

Rebase es una herramienta poderosa que te permite reorganizar los commits de una rama, creando un historial de proyecto más limpio y lineal.  Es importante usar rebase con precaución, especialmente al trabajar con ramas compartidas.  Comprender cómo funciona el rebase y cómo manejar los conflictos te permitirá aprovechar al máximo esta herramienta para una colaboración eficiente. 
