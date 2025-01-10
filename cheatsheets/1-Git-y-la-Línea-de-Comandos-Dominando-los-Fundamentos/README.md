## Cheatsheet: Git y la Línea de Comandos - Dominando los Fundamentos

Este cheatsheet te guiará a través de los conceptos y comandos esenciales presentados en el capítulo "Git y la Línea de Comandos" del libro *Learning Git*. Te proporcionará ejemplos prácticos y explicaciones claras para que puedas comenzar a trabajar con Git desde la línea de comandos con confianza.

### 1. ¿Qué es Git?

Git es un **sistema de control de versiones (VCS)** que se utiliza para rastrear los cambios realizados en los archivos de un proyecto a lo largo del tiempo. Permite a los desarrolladores:

* **Registrar el historial de cambios:** Cada cambio se guarda como una "instantánea" (commit), lo que te permite volver a versiones anteriores del proyecto si es necesario.
* **Colaborar con otros:** Facilita el trabajo en equipo al permitir que múltiples personas trabajen en el mismo proyecto sin sobrescribir los cambios de los demás.

### 2. La Línea de Comandos (CLI)

La línea de comandos es una **interfaz de texto** que se utiliza para interactuar con el sistema operativo de tu computadora. Es una herramienta poderosa para trabajar con Git, ya que te brinda acceso a **todas las funcionalidades de Git**.

### 3. Comandos Esenciales de la Línea de Comandos

Estos son algunos comandos básicos de la línea de comandos que necesitarás para trabajar con Git:

* **`pwd` (Print Working Directory):** Muestra la ubicación actual del directorio en el que te encuentras.
   ```bash
   $ pwd
   /Users/usuario/Documentos/proyecto
   ```

* **`ls` (List):** Muestra los archivos y directorios dentro del directorio actual.
   ```bash
   $ ls
   archivo1.txt  archivo2.pdf  carpeta1
   ```

* **`cd` (Change Directory):** Cambia al directorio especificado.
   ```bash
   $ cd carpeta1
   ```

* **`mkdir` (Make Directory):** Crea un nuevo directorio.
   ```bash
   $ mkdir nueva_carpeta
   ```

* **`clear`:** Limpia la pantalla de la terminal.


### 4. Instalando Git

Antes de comenzar a usar Git, debes tenerlo instalado en tu computadora.  Puedes descargar Git desde el sitio web oficial: [https://git-scm.com/](https://git-scm.com/).

Para verificar si Git está instalado, ejecuta el siguiente comando:

```bash
$ git version
git version 2.39.0
```

### 5. Configurando Git

Después de instalar Git, debes configurarlo con tu nombre de usuario y correo electrónico.  Esta información se utilizará para identificar tus commits.

```bash
$ git config --global user.name "Tu Nombre"
$ git config --global user.email "tu_correo@ejemplo.com"
```

### 6. Preparando un Editor de Texto

Necesitarás un **editor de texto** para crear y editar archivos dentro de tu proyecto Git.  Algunos editores populares incluyen:

* **Visual Studio Code:** Un editor de código fuente potente y personalizable.
* **Sublime Text:** Un editor ligero y rápido.
* **Atom:** Un editor de código fuente de código abierto desarrollado por GitHub.

### 7. Resumen

Este cheatsheet te ha presentado los fundamentos de Git y la línea de comandos, incluyendo la instalación de Git, la configuración básica y algunos comandos esenciales.

