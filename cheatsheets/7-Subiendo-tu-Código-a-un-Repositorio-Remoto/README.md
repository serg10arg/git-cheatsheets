## Cheatsheet: Creando y Subiendo a un Repositorio Remoto - Compartiendo tu Código con el Mundo

Este cheatsheet te guiará a través del proceso de crear un repositorio remoto y subir tus cambios desde tu repositorio local. Aprenderás cómo conectar tus repositorios y compartir tu trabajo con otros.

### 1. ¿Qué es un Repositorio Remoto?

Un repositorio remoto es una copia de tu proyecto Git **alojada en un servidor externo**, como GitHub, GitLab o Bitbucket.  Te permite respaldar tu código, colaborar con otros y acceder a tu proyecto desde diferentes ubicaciones.

### 2. ¿Por qué Usar Repositorios Remotos?

* **Respaldo:** Protege tu trabajo en caso de fallas en tu computadora.
* **Acceso desde Múltiples Equipos:** Trabaja en tu proyecto desde cualquier lugar.
* **Colaboración:** Comparte tu código y trabaja en conjunto con otros.

### 3. Flujo de Trabajo con Repositorios Locales y Remotos

* **Repositorio Local:**  Tu copia de trabajo en tu computadora.
* **Repositorio Remoto:**  La copia alojada en un servicio de hosting.
* **Comandos para Interactuar:**  `git push`, `git clone`, `git fetch`, `git pull`.

### 4. Creando un Repositorio Remoto

1. **Elige un Servicio de Hosting:**  GitHub, GitLab, Bitbucket.
2. **Crea una Cuenta:** Regístrate en el servicio de hosting elegido.
3. **Crea un Repositorio Vacío:** En la interfaz del servicio de hosting, crea un nuevo repositorio sin archivos iniciales.
4. **Obtén la URL del Repositorio:** Copia la URL del repositorio, que usarás para conectarlo con tu repositorio local.

### 5. Conectando tu Repositorio Local con el Remoto

1. **Inicializa un Repositorio Git Local (si no lo has hecho):**
    ```bash
    $ git init 
    ```
2. **Añade el Repositorio Remoto:** Usa el comando `git remote add` para asociar una URL remota con un nombre corto.  "origin" es el nombre corto por convención.
    ```bash
    $ git remote add origin <URL_del_repositorio_remoto>
    ```

### 6. Subiendo Cambios al Repositorio Remoto

1. **Prepara tus Cambios:**  Realiza commits en tu repositorio local para guardar tus cambios.
2. **Sube los Cambios:** Usa el comando `git push` para enviar los commits al repositorio remoto.
    ```bash
    $ git push origin <nombre_rama> 
    ```
    * **origin:** El nombre corto del repositorio remoto.
    * **nombre_rama:** El nombre de la rama que deseas subir.

### 7. Ramas Remotas y Ramas de Seguimiento

* **Rama Remota:**  Una rama que existe solo en el repositorio remoto.
* **Rama de Seguimiento:**  Una rama local que refleja el estado de una rama remota.
* **Ejemplo:** Cuando subes una rama llamada "feature" a "origin", se crea una rama remota llamada "origin/feature" que puedes seguir localmente.

### 8. Ejemplo Práctico: Creando y Subiendo un Proyecto

1. **Crea un Repositorio Local:**
    ```bash
    $ mkdir mi_proyecto
    $ cd mi_proyecto
    $ git init
    ```
2. **Crea un Archivo y Realiza un Commit:**
    ```bash
    $ echo "¡Hola Mundo!" > README.md
    $ git add README.md
    $ git commit -m "Commit inicial"
    ```
3. **Crea un Repositorio Remoto en GitHub (por ejemplo) y Copia la URL.**
4. **Conecta el Repositorio Local al Remoto:**
    ```bash
    $ git remote add origin <URL_de_GitHub>
    ```
5. **Sube los Cambios al Repositorio Remoto:**
    ```bash
    $ git push origin main
    ```

¡Ahora tu código está respaldado en la nube y listo para la colaboración!
