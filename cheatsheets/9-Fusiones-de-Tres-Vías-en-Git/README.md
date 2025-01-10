## Cheatsheet: Fusiones de Tres Vías en Git - Integrando Historias Divergentes

Este cheatsheet te guiará a través del proceso de realizar una fusión de tres vías en Git. Aprenderás cómo integrar cambios de ramas con historias divergentes, comprender la importancia de este tipo de fusión y manejar situaciones donde las ediciones se realizan en los mismos archivos.

### 1. ¿Qué es una Fusión de Tres Vías?

Una fusión de tres vías ocurre cuando se intenta **integrar dos ramas cuyas historias de desarrollo han divergido**, es decir, cuando no se puede llegar a una rama simplemente avanzando la punta de la otra.

* **Rama de origen:** La rama que contiene los cambios que se desean integrar.
* **Rama de destino:** La rama que recibirá los cambios.
* **Antepasado común:** El último commit que ambas ramas comparten.

Git utiliza estos tres puntos (la rama de origen, la rama de destino y el antepasado común) para determinar cómo combinar los cambios, creando un nuevo **commit de fusión** que une las historias.


### 2. ¿Por qué son Importantes las Fusiones de Tres Vías?

Las fusiones de tres vías son **cruciales para la colaboración efectiva en proyectos Git**.  Permiten que múltiples desarrolladores trabajen en paralelo en diferentes ramas y luego integren sus cambios de manera ordenada.

**Escenarios comunes donde se utilizan fusiones de tres vías:**

* Varios desarrolladores trabajan en diferentes funcionalidades al mismo tiempo.
* Se integra una rama de desarrollo a la rama principal (main) después de que otros cambios se han realizado en main.
* Se fusionan cambios de un colaborador después de obtener los cambios más recientes del repositorio remoto.


### 3. Pasos para Realizar una Fusión de Tres Vías

1. **Cambiar a la rama de destino:** Asegúrate de estar en la rama que recibirá los cambios.

    ```bash
    $ git checkout <nombre_rama_destino>
    ```
2. **Fusionar la rama de origen:**

    ```bash
    $ git merge <nombre_rama_origen>
    ```
3. **Resolver conflictos (si existen):** Git intentará fusionar los cambios automáticamente.  Si hay conflictos (cambios en las mismas líneas de código), deberás resolverlos manualmente.

4. **Revisar y hacer commit:**  Después de resolver los conflictos, revisa los cambios fusionados y crea un nuevo commit para finalizar la fusión.

    ```bash
    $ git add .
    $ git commit -m "Fusión de <nombre_rama_origen> a <nombre_rama_destino>"
    ```


### 4. Ejemplo Práctico

Imagina que tú y un colaborador están trabajando en un proyecto. Tu colaborador trabaja en una rama llamada "feature" y tú en la rama "main". Ambos realizan cambios en el mismo archivo `README.md`.

1. **Tu colaborador fusiona "feature" a "main" y sube los cambios.**

2. **Tú obtienes los cambios más recientes del repositorio remoto:**

    ```bash
    $ git fetch origin
    ```
3. **Fusionas la rama "origin/main" (la rama remota actualizada) a tu rama "main" local:**

    ```bash
    $ git merge origin/main
    ```

   Si hay conflictos en `README.md`, Git te mostrará los marcadores de conflicto (<<<<<<<, =======, >>>>>>>).

4. **Resuelve los conflictos en `README.md` manualmente.**

5. **Haz commit de los cambios fusionados:**

    ```bash
    $ git add README.md
    $ git commit -m "Fusiona los cambios de la rama feature"
    ```

### 5. Resumen

Las fusiones de tres vías son una parte fundamental del flujo de trabajo en Git.  Permiten integrar cambios de ramas con historias divergentes de manera efectiva. Comprender cómo funcionan y cómo resolver conflictos te ayudará a colaborar de forma fluida y mantener un historial de proyecto organizado.
