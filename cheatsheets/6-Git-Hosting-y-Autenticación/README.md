## Cheatsheet: Servicios de Hosting y Autenticación en Git - Conectando con el Mundo

Este cheatsheet te guiará a través de los servicios de hosting y el proceso de autenticación en Git, permitiéndote colaborar en proyectos y compartir tu código con el mundo.

### 1. ¿Qué son los Servicios de Hosting de Git?

Los servicios de hosting de Git, como **GitHub, GitLab y Bitbucket**, son plataformas online que te permiten **almacenar tus repositorios Git en la nube**.  Estos servicios facilitan la colaboración en proyectos, el control de versiones y la distribución del código.

### 2. ¿Por qué usar Servicios de Hosting?

* **Colaboración:** Trabaja con otros desarrolladores en proyectos compartidos.
* **Control de versiones en la nube:** Respalda tu código y accede a él desde cualquier lugar.
* **Visibilidad:** Comparte tu código con el mundo o mantenlo privado para tu equipo.
* **Herramientas de gestión de proyectos:**  Utiliza funciones como seguimiento de incidencias, wikis y tableros de proyectos.

### 3. Autenticación: Asegurando tus Repositorios

Para acceder a tus repositorios en un servicio de hosting, necesitas autenticarte.  Esto verifica tu identidad y te otorga los permisos necesarios.

#### 3.1 Protocolos de Autenticación:

Los dos protocolos principales para autenticación son:

* **HTTPS (Hypertext Transfer Protocol Secure):**  Utiliza un nombre de usuario y una contraseña o un token de acceso personal para la autenticación.
* **SSH (Secure Shell):**  Utiliza un par de claves SSH (pública y privada) para la autenticación. La clave pública se registra en el servicio de hosting, mientras que la clave privada se guarda en tu computadora.

#### 3.2 Eligiendo un Protocolo:

* **HTTPS:** Más fácil de configurar, ideal para principiantes.
* **SSH:**  Más seguro, no requiere ingresar contraseñas cada vez.

### 4.  Configurando la Autenticación:

#### 4.1 HTTPS:

1. **Crea una cuenta en un servicio de hosting** como GitHub, GitLab o Bitbucket.
2. **Genera un token de acceso personal (GitHub, Bitbucket)** o **utiliza tu contraseña de cuenta (GitLab)**.
3. **Al clonar o interactuar con el repositorio remoto, se te solicitarán tus credenciales HTTPS**.  Ingresa tu nombre de usuario y token/contraseña.

#### 4.2 SSH:

1. **Genera un par de claves SSH en tu computadora**. Puedes usar `ssh-keygen` en la línea de comandos.
2. **Añade la clave pública a tu cuenta del servicio de hosting**.
3. **Añade la clave privada al agente SSH**. Esto permite que Git use la clave privada para autenticarse sin solicitarla cada vez.

### 5. Resumen:

Los servicios de hosting de Git son esenciales para la colaboración y la gestión de código.  La autenticación segura es crucial para proteger tus repositorios. Elige el protocolo que mejor se adapte a tus necesidades y configura la autenticación para comenzar a compartir tu código con el mundo.

**Recuerda:**

* No compartas tu clave privada SSH con nadie.
* Mantén tus credenciales de autenticación seguras.
* Explora la documentación del servicio de hosting que elijas para obtener instrucciones detalladas sobre la configuración de la autenticación.
