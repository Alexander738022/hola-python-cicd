# Consulta de Comandos Git y Flujo de Pull Requests 

Este archivo contiene el resumen de la investigación sobre el control de versiones con Git y el funcionamiento de las solicitudes de extracción en GitHub.

---

## 1. Resumen de Comandos Git Esenciales

* **`git init`**: Inicializa un repositorio Git local en la carpeta del proyecto. Crea el sistema de rastreo oculto.
* **`git status`**: Muestra el estado actual de los archivos. Indica qué archivos han sido modificados, cuáles están listos para guardarse y cuáles no están siendo rastreados por Git.
* **`git add .`**: Agrega todas las modificaciones y archivos nuevos al "Área de Preparación" (*Staging Area*), listos para el commit.
* **`git commit -m "mensaje"`**: Registra los cambios guardados en el historial local con un mensaje corto que describe la actualización efectuada.
* **`git branch -M main`**: Configura o renombra la rama principal del proyecto como `main`.
* **`git push -u origin main`**: Sube los registros locales al servidor remoto de GitHub por primera vez. Después de esto, basta con usar solo `git push`.

---

## 2. Investigación: ¿Qué es y cómo funciona un Pull Request (PR)?

Un **Pull Request** (o Solicitud de Extracción) es una función exclusiva de la plataforma web de GitHub (no es un comando que se escriba en la consola). Permite a los desarrolladores avisar al equipo o al profesor que han terminado de trabajar en una característica nueva dentro de una rama secundaria y que está lista para integrarse a la rama principal.

### Flujo de trabajo paso a paso:
1. **Crear una rama secundaria:** Se crea un desvío de la rama principal para hacer los cambios sin romper lo que ya funciona (`git checkout -b nueva-tarea`).
2. **Guardar y enviar cambios:** Se hace el código, se guarda localmente y se sube la rama a GitHub (`git push origin nueva-tarea`).
3. **Abrir la solicitud en la web:** En GitHub se crea el Pull Request explicando los cambios realizados.
4. **Pruebas automáticas (CI/CD):** Nuestro archivo `ci-cd.yml` de GitHub Actions se activa solo y revisa que las pruebas pasen con el check verde 🟢.
5. **Fusión (Merge):** El administrador o profesor aprueba la solicitud y los cambios se unen de forma segura a la rama principal (`main`).