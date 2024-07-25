

# Trabajo Colaborativo en Git y GitHub

## Introducción
Git y GitHub no solo son herramientas para gestionar el código, sino también plataformas poderosas para la colaboración en proyectos de software. Este documento explora cómo aprovechar al máximo Git y GitHub para trabajar de manera efectiva en equipo, incluyendo el uso de projects, flujos de trabajo adecuados, asignación de roles y permisos, uso de etiquetas e hilos, gestión de issues, y revisión de código y comentarios.

## ¿Qué son los Projects?
Los projects en GitHub son herramientas de gestión de proyectos que ayudan a organizar y planificar el trabajo. Permiten crear tableros Kanban para visualizar tareas, asignar tareas a miembros del equipo, y rastrear el progreso de manera eficiente.

**Características principales:**
- **Columnas personalizables:** Agrupa tareas en columnas como "To do", "In Progress", y "Done".
- **Tarjetas:** Cada issue, pull request o nota puede ser una tarjeta en el tablero.
- **Integración:** Se integra con issues y pull requests para mantener todo sincronizado.

**Ejemplo de uso:**
```bash
# Crear un nuevo project en GitHub:
1. Ve al repositorio en GitHub.
2. Haz clic en la pestaña "Projects".
3. Haz clic en "New project" y sigue las instrucciones.
```

## Colaboración con otros desarrolladores usando un flujo de trabajo adecuado
Un flujo de trabajo (workflow) adecuado es crucial para la colaboración efectiva. Algunos de los flujos de trabajo más comunes son:

### Git Flow
Un flujo de trabajo robusto que incluye ramas para desarrollo (`develop`), producción (`master`), y características (`feature`).

**Pasos básicos:**
1. **Crear una rama de feature:**
    ```bash
    git checkout -b feature/nueva-funcionalidad
    ```
2. **Desarrollar la funcionalidad y hacer commits.**
3. **Mergear la rama de feature a develop:**
    ```bash
    git checkout develop
    git merge feature/nueva-funcionalidad
    ```

### Forking Workflow
Ideal para proyectos de código abierto, donde los contribuidores crean forks del repositorio y envían pull requests para revisión.

**Pasos básicos:**
1. **Hacer un fork del repositorio en GitHub.**
2. **Clonar el fork:**
    ```bash
    git clone https://github.com/usuario/fork-del-repo.git
    ```
3. **Crear una rama de feature, desarrollar y hacer commits.**
4. **Enviar un pull request al repositorio original.**

## Asignación de Roles y Permisos
GitHub permite asignar roles y permisos para gestionar quién puede hacer qué en un repositorio.

### Roles comunes:
- **Owner:** Control total sobre el repositorio.
- **Admin:** Puede gestionar la configuración y los miembros.
- **Write:** Puede hacer push y mergear pull requests.
- **Read:** Acceso de solo lectura.

**Asignar roles:**
1. Ve al repositorio en GitHub.
2. Haz clic en la pestaña "Settings".
3. Selecciona "Manage access".
4. Agrega colaboradores y asigna roles adecuados.

## Uso de Etiquetas e Hilos
Las etiquetas y los hilos ayudan a organizar y priorizar tareas.

### Etiquetas (Labels)
Permiten categorizar issues y pull requests para facilitar su gestión.

**Crear una etiqueta:**
1. Ve al repositorio en GitHub.
2. Haz clic en la pestaña "Issues".
3. Haz clic en "Labels" y luego en "New label".

### Hilos (Threads)
Facilitan la discusión sobre temas específicos dentro de issues y pull requests.

**Iniciar un hilo:**
1. En un issue o pull request, selecciona un comentario.
2. Haz clic en "Start a new thread".

## Issues
Los issues son la herramienta principal para rastrear tareas, mejoras y reportes de errores.

### Crear un issue:
1. Ve al repositorio en GitHub.
2. Haz clic en la pestaña "Issues".
3. Haz clic en "New issue" y llena los detalles.

### Gestionar issues:
- **Asignar:** Puedes asignar issues a colaboradores.
- **Etiquetar:** Usa etiquetas para categorizar issues.
- **Comentar:** Facilita la discusión y aclaración de tareas.

## Revisión de Códigos y Comentarios
La revisión de código es esencial para mantener la calidad y consistencia del código.

### Pull Requests
Permiten proponer cambios y facilitar la revisión antes de mergear a la rama principal.

**Crear un pull request:**
1. Realiza cambios en una rama.
2. Ve a la pestaña "Pull requests" en GitHub.
3. Haz clic en "New pull request" y sigue las instrucciones.

### Revisión de código:
- **Comentarios en línea:** Añade comentarios específicos en líneas de código.
- **Aprobaciones:** Los revisores pueden aprobar cambios o solicitar cambios adicionales.
- **Merge:** Una vez aprobado, el pull request se puede mergear a la rama principal.

