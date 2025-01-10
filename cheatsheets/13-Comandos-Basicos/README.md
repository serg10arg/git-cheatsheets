## Cheatsheet: Referencia Rápida de Comandos Git - Los Comandos Esenciales para Dominar Git

Este cheatsheet te proporciona una guía concisa y práctica de los comandos Git más utilizados, organizados por capítulos del libro "Learning Git" de Anna Skoulikari. Con ejemplos, explicaciones claras y consejos útiles, este recurso te ayudará a navegar por las operaciones fundamentales de Git, desde la gestión de archivos hasta la colaboración en proyectos.

### Cheatsheet 1: Git y la Línea de Comandos

*   **`clear`**: Limpia la pantalla de la línea de comandos.

    ```bash
    $ clear 
    ```
*   **`pwd`**: Muestra la ruta del directorio de trabajo actual.

    ```bash
    $ pwd
    /Users/usuario/ruta/al/directorio
    ```

*   **`ls`**: Lista los archivos y directorios visibles.

    ```bash
    $ ls
    archivo1.txt  carpeta1  imagen.jpg
    ```

*   **`ls -a`**: Lista los archivos y directorios ocultos y visibles.

    ```bash
    $ ls -a
    .  ..  archivo1.txt  .archivo_oculto  carpeta1  imagen.jpg
    ```

*   **`cd <ruta_al_directorio>`**: Cambia al directorio especificado.

    ```bash
    $ cd /Users/usuario/Documentos/proyecto
    ```
*   **`mkdir <nombre_del_directorio>`**: Crea un nuevo directorio.

    ```bash
    $ mkdir nueva_carpeta
    ```
*   **`git config --global --list`**: Muestra las variables de configuración global de Git y sus valores.

    ```bash
    $ git config --global --list
    user.name=Tu Nombre
    user.email=tu_correo@ejemplo.com
    ```
*   **`git config --global user.name "<nombre>"`**: Establece tu nombre de usuario en la configuración global de Git.

    ```bash
    $ git config --global user.name "Tu Nombre"
    ```
*   **`git config --global user.email "<correo>"`**: Establece tu dirección de correo electrónico en la configuración global de Git.

    ```bash
    $ git config --global user.email "tu_correo@ejemplo.com"
    ```

### Cheatsheet 2: Repositorios Locales

*   **`git init`**: Inicializa un repositorio Git en el directorio actual.

    ```bash
    $ git init
    Initialized empty Git repository in /ruta/al/repositorio/.git/
    ```
*   **`git init -b <nombre_de_la_rama>`**: Inicializa un repositorio Git y establece el nombre de la rama inicial.

    ```bash
    $ git init -b desarrollo
    Initialized empty Git repository in /ruta/al/repositorio/.git/
    ```
    **Consejo:** Usar un nombre de rama inicial diferente a "master" (por ejemplo, "main" o "desarrollo") promueve la inclusión y la neutralidad.

### Cheatsheet 3: Haciendo un Commit

*   **`git status`**: Muestra el estado del directorio de trabajo y el área de preparación (staging area). Útil para ver qué archivos se han modificado o preparado para el commit.

    ```bash
    $ git status
    On branch main
    Changes to be committed:
      (use "git restore --staged <file>..." to unstage)
          modified:   archivo.txt
    ```

*   **`git add <nombre_de_archivo>`**: Agrega un archivo al área de preparación. Prepara un archivo modificado para ser incluido en el próximo commit.

    ```bash
    $ git add archivo.txt
    ```

*   **`git add <archivo1> <archivo2> ...`**: Agrega múltiples archivos al área de preparación.

    ```bash
    $ git add archivo1.txt archivo2.js
    ```
*   **`git add -A`**: Agrega todos los archivos modificados al área de preparación. Equivalente a usar `git add .`, pero también incluye archivos eliminados.

    ```bash
    $ git add -A
    ```
*   **`git commit -m "<mensaje>"`**: Crea un nuevo commit con el mensaje especificado. Guarda los cambios preparados en el historial del repositorio.

    ```bash
    $ git commit -m "Corrección de errores menores"
    ```
    **Consejo:** Escribe mensajes de commit claros y concisos que describan los cambios realizados.

### Cheatsheet 4: Ramas (Branches)

*   **`git branch`**: Lista las ramas locales, indicando la rama actual con un asterisco (*).

    ```bash
    $ git branch
    * main
      desarrollo
      caracteristica
    ```

*   **`git branch <nombre_de_la_rama>`**: Crea una nueva rama.

    ```bash
    $ git branch nueva_caracteristica
    ```
*   **`git checkout <nombre_de_la_rama>`**: Cambia a la rama especificada.

    ```bash
    $ git checkout desarrollo
    ```

*   **`git checkout -b <nombre_de_la_rama>`**: Crea una nueva rama y cambia a ella en un solo paso.

    ```bash
    $ git checkout -b correccion_error
    ```

### Cheatsheet 5: Fusionando (Merging)

*   **`git merge <nombre_de_la_rama>`**: Fusiona la rama especificada en la rama actual.

    ```bash
    $ git merge desarrollo
    ```
    **Consejo:** Asegúrate de estar en la rama de destino (donde quieres fusionar los cambios) antes de ejecutar este comando.

### Cheatsheet 7: Creando y Enviando (Pushing) a un Repositorio Remoto

*   **`git push <nombre_del_remoto> <nombre_de_la_rama>`**: Sube los cambios de una rama local a un repositorio remoto.

    ```bash
    $ git push origin main
    ```
    **Consejo:** En el primer push, es posible que necesites usar `git push -u origin main` para establecer la rama remota como rama de seguimiento predeterminada.

*   **`git remote add <nombre_corto> <URL>`**: Agrega una conexión a un repositorio remoto con el nombre corto y la URL especificados.

    ```bash
    $ git remote add origin https://github.com/usuario/repositorio.git
    ```

*   **`git remote`**: Lista las conexiones a repositorios remotos almacenados en el repositorio local por su nombre corto.

    ```bash
    $ git remote
    origin
    ```

*   **`git remote -v`**: Lista las conexiones a repositorios remotos con sus nombres cortos y URLs.

    ```bash
    $ git remote -v
    origin  https://github.com/usuario/repositorio.git (fetch)
    origin  https://github.com/usuario/repositorio.git (push)
    ```

### Cheatsheet 8: Clonando (Cloning) y Obteniendo (Fetching)

*   **`git clone <URL>`**: Crea una copia local de un repositorio remoto.

    ```bash
    $ git clone https://github.com/usuario/repositorio.git
    ```
*   **`git fetch <nombre_del_remoto>`**: Obtiene los cambios de un repositorio remoto sin fusionarlos en tu rama local.

    ```bash
    $ git fetch origin
    ```
    **Consejo:** Usa `git fetch` para actualizar tus ramas remotas con los cambios del repositorio remoto.

### Cheatsheet 9: Fusiones de Tres Vías (Three-Way Merges)

*   **`git branch --set-upstream-to=<nombre_del_remoto>/<nombre_de_la_rama>`**: Define una rama remota como rama de seguimiento (upstream) para la rama local actual. Esto simplifica los comandos `git pull` y `git push`.

    ```bash
    $ git branch --set-upstream-to=origin/desarrollo
    ```
    **Consejo:** Configurar la rama de seguimiento facilita la sincronización con el repositorio remoto.

### Cheatsheet 10: Conflictos de Fusión (Merge Conflicts)

*   **`git status`**: Muestra los archivos con conflictos de fusión.

    ```bash
    $ git status
    On branch main
    You have unmerged paths.
      (fix conflicts and run "git commit")
      (use "git merge --abort" to abort the merge)

        Unmerged paths:
          (use "git add <file>..." to mark resolution)
                both modified:   archivo.txt
    ```

*   **`git add <nombre_de_archivo>`**: Agrega un archivo con conflictos resueltos al área de preparación.

    ```bash
    $ git add archivo.txt
    ```
*   **`git merge --abort`**: Cancela una fusión en curso. Revierte los cambios a su estado antes de iniciar la fusión.

    ```bash
    $ git merge --abort
    ```
    **Consejo:** Usa `git merge --abort` para deshacer una fusión con conflictos que no puedes resolver.


### Cheatsheet 11: Rebase

*   **`git rebase <nombre_de_la_rama>`**: Reorganiza los commits de la rama actual, colocándolos como si se hubieran creado a partir de la rama especificada.

    ```bash
    $ git rebase desarrollo
    ```

*   **`git rebase --continue`**: Continúa el proceso de rebase después de resolver conflictos.

    ```bash
    $ git rebase --continue
    ```

*   **`git rebase --abort`**: Cancela un rebase en curso. Revierte los cambios a su estado antes de iniciar el rebase.

    ```bash
    $ git rebase --abort
    ```

*   **`git push --force-with-lease <nombre_del_remoto> <nombre_de_la_rama>`**: Fuerza la subida de una rama rebaseada al repositorio remoto. **Usa con precaución, ya que puede sobrescribir cambios en el repositorio remoto.**

    ```bash
    $ git push --force-with-lease origin main
    ```
    **Advertencia:**  `--force-with-lease` es más seguro que `--force`, pero aún así, debes tener mucho cuidado al usar este comando.

### Cheatsheet 12: Pull Requests (Merge Requests)

*   **`git push <nombre_del_remoto> <nombre_de_la_rama>`**: Sube una rama local al repositorio remoto para crear una Pull Request.

    ```bash
    $ git push origin nueva_funcionalidad
    ```

*   **`git push --set-upstream <nombre_del_remoto> <nombre_de_la_rama>`**: Sube una rama local y la establece como rama de seguimiento para la rama remota especificada.

    ```bash
    $ git push --set-upstream origin nueva_funcionalidad
    ```
    **Consejo:** Este comando es útil para crear una nueva rama remota y establecer la rama de seguimiento en un solo paso.

*   **`git remote prune <nombre_del_remoto>`**: Elimina las ramas remotas que ya no existen en el repositorio remoto.

    ```bash
    $ git remote prune origin
    ```
    **Consejo:** Usa `git remote prune` para mantener tus ramas remotas actualizadas y eliminar las que ya no son necesarias.


### Consejos Adicionales

*   **Ayuda de Git:** Usa `git help <comando>` para obtener información detallada sobre un comando específico.
*   **Practica:** La mejor manera de aprender Git es practicando. Crea repositorios de prueba, experimenta con los comandos y familiarízate con el flujo de trabajo.
*   **Mensajes de Commit Claros:** Escribe mensajes de commit que describan los cambios realizados de forma concisa y clara.
*   **Ramas para Nuevas Funcionalidades:** Crea ramas para desarrollar nuevas funcionalidades o correcciones de errores. Esto te permite trabajar de forma aislada y mantener un historial limpio.
*   **Revisa tu Código:** Revisa tu código antes de hacer commit para evitar errores y asegurar la calidad.
*   **Colaboración Eficaz:** Usa Pull Requests para facilitar la revisión de código y la colaboración en equipo.
