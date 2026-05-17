# Consulta de Comandos Git y Flujo de Pull Requests 🚀

Este archivo contiene el resumen de la investigación sobre el control de versiones con Git y cómo se manejan las solicitudes de extracción con ejemplos prácticos.

---

## 1. Resumen de Comandos Git Esenciales y Ejemplos

* **`git init`**
  * **Para qué sirve:** Inicializa un repositorio Git local en la carpeta del proyecto. Crea el sistema de rastreo oculto.
  * **Ejemplo práctico:** Cuando empiezas un proyecto desde cero en tu computadora, abres la terminal en esa carpeta y ejecutas:
    ```bash
    git init
    ```

* **`git status`**
  * **Para qué sirve:** Muestra el estado actual de los archivos. Indica qué archivos han sido modificados o cuáles son nuevos.
  * **Ejemplo práctico:** Si acabas de editar tu código y quieres ver si Git detectó los cambios antes de guardarlos, escribes:
    ```bash
    git status
    ```

* **`git add .`**
  * **Para qué sirve:** Agrega todas las modificaciones y archivos nuevos al "Área de Preparación" (*Staging Area*), listos para el commit.
  * **Ejemplo práctico:** Si creaste los archivos `app.py` y `README.md`, usas este comando para decirle a Git: *"Agrégalos a la foto que voy a tomar"*:
    ```bash
    git add .
    ```

* **`git commit -m "mensaje"`**
  * **Para qué sirve:** Registra los cambios guardados en el historial local con un mensaje corto que describe la actualización efectuada.
  * **Ejemplo práctico:** Para guardar de forma definitiva el archivo de pruebas en tu historial local, escribes:
    ```bash
    git commit -m "Agregado el archivo test_app.py con la prueba de Hola Mundo"
    ```

* **`git branch -M main`**
  * **Para qué sirve:** Configura o renombra la rama principal del proyecto como `main`.
  * **Ejemplo práctico:** Al crear un repositorio nuevo, para asegurarte de que tu rama principal no se llame "master" sino "main", ejecutas:
    ```bash
    git branch -M main
    ```

* **`git push -u origin main`**
  * **Para qué sirve:** Sube los registros locales al servidor remoto de GitHub por primera vez. Después de esto, basta con usar solo `git push`.
  * **Ejemplo práctico:** Para enviar todo el proyecto que tienes en tu computadora hacia tu cuenta de GitHub en internet por primera vez:
    ```bash
    git push -u origin main
    ```

---

## 2. Investigación: ¿Qué es y cómo funciona un Pull Request (PR)?

Un **Pull Request** (o Solicitud de Extracción) es una función exclusiva de la plataforma web de GitHub (no es un comando de consola). Permite a los desarrolladores avisar al equipo o al profesor que han terminado de trabajar en una característica nueva dentro de una rama secundaria y que está lista para integrarse a la rama principal (`main`).

### Ejemplo de flujo de trabajo paso a paso:

Imagina que vas a agregar una nueva función a tu aplicación sin dañar la versión que ya funciona en `main`:

1. **Crear y cambiarte a una rama secundaria:** Crea un desvío llamado `feature-nueva-funcion`:
   ```bash
   git checkout -b feature-nueva-funcion