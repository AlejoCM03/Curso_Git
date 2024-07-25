# Git y GitHub: Uso de Wikis

## Introducción
Las Wikis de GitHub son una herramienta poderosa para documentar proyectos de software, permitiendo a los desarrolladores y equipos crear y mantener documentación estructurada directamente dentro del repositorio. Este documento ofrece una guía extensa sobre cómo utilizar las Wikis de GitHub, incluyendo su configuración, edición, navegación, uso de Markdown y otras características avanzadas.

## ¿Qué es una Wiki en GitHub?
Una Wiki en GitHub es una colección de páginas interconectadas que pueden ser editadas y actualizadas fácilmente. Las Wikis son ideales para almacenar documentación del proyecto, guías de usuario, especificaciones técnicas, notas de desarrollo y más.

## Configuración Inicial de una Wiki

### Habilitar la Wiki
Por defecto, cada repositorio en GitHub viene con una Wiki habilitada. Para verificar o habilitar la Wiki:

1. Ve a tu repositorio en GitHub.
2. Haz clic en la pestaña "Settings".
3. En la sección "Features", asegúrate de que la opción "Wikis" esté habilitada.

### Acceder a la Wiki
Para acceder a la Wiki de un repositorio:

1. Ve a tu repositorio en GitHub.
2. Haz clic en la pestaña "Wiki".

## Crear y Editar Páginas en la Wiki

### Crear una Nueva Página
1. En la pestaña "Wiki", haz clic en "New Page".
2. Introduce un título para la página. Este título se convertirá en el nombre del archivo.
3. Añade el contenido de la página utilizando Markdown.
4. Haz clic en "Save Page" para guardar los cambios.

### Editar una Página Existente
1. Navega a la página que deseas editar en la Wiki.
2. Haz clic en "Edit" en la parte superior de la página.
3. Realiza los cambios necesarios utilizando Markdown.
4. Haz clic en "Save Page" para guardar los cambios.

### Uso de Markdown en Wikis
GitHub Wikis utilizan Markdown para formatear el contenido. Aquí hay una referencia rápida a algunos de los elementos de Markdown más utilizados:

- **Encabezados:**
    ```markdown
    # Encabezado 1
    ## Encabezado 2
    ### Encabezado 3
    ```

- **Negritas y Cursivas:**
    ```markdown
    **Texto en negritas**
    *Texto en cursivas*
    ```

- **Listas:**
    ```markdown
    - Elemento de lista
    - Otro elemento de lista
      - Sub-elemento
    ```

- **Enlaces:**
    ```markdown
    [Texto del enlace](URL)
    ```

- **Imágenes:**
    ```markdown
    ![Texto alternativo](URL de la imagen)
    ```

- **Bloques de Código:**
    ```markdown
    ```nombre_del_lenguaje
    código
    ```
    ```

## Navegación y Organización de la Wiki

### Tabla de Contenidos
Para facilitar la navegación, es útil crear una tabla de contenidos (TOC) en la página principal de la Wiki.

**Ejemplo de Tabla de Contenidos:**
```markdown
# Tabla de Contenidos
- [Introducción](#introducción)
- [Instalación](#instalación)
- [Uso](#uso)
- [Contribución](#contribución)
- [Licencia](#licencia)
```
### Enlaces Internos
Puedes crear enlaces internos para navegar entre páginas de la Wiki.

**Ejemplo:**

```markdown
[Volver a la Página Principal](Home)
```
### Categorización de Páginas

Para mantener la Wiki organizada, es útil categorizar las páginas en secciones o categorías. Esto se puede hacer mediante la creación de una estructura de carpetas en la Wiki.

**Ejemplo de Organización de Páginas:**
```csharp
Home
|_ Guías de Usuario
   |_ Introducción.md
   |_ Instalación.md
|_ Referencia Técnica
   |_ API.md
   |_ Arquitectura.md
```
## Control de Versiones en Wikis
### Histórico de Cambios

GitHub Wikis mantienen un historial de cambios para cada página, permitiendo a los usuarios ver quién hizo qué cambios y cuándo.

**Ver el Histórico de Cambios:**
1. Navega a la página de la Wiki.
2. Haz clic en "History" en la parte superior de la página.
3. Explora los cambios y, si es necesario, restaura versiones anteriores.
### Clonar la Wiki
Las Wikis en GitHub son repositorios Git por derecho propio. Puedes clonarlas, editarlas localmente y luego enviar (push) los cambios.

**Clonar la wiki:**
```bash
git clone https://github.com/usuario/repositorio.wiki.git
```
**Hacer Cambios Localmente y Enviar:**
1. Realiza cambios en los archivos Markdown.
2. Añade y confirma los cambios:
```bash
git add .
git commit -m "Actualización de la documentación"
```
## Colaboración en Wikis
### Permisos de Colaboradores
Los colaboradores del repositorio tienen permisos para editar la Wiki. Para añadir colaboradores:

1. Ve a la pestaña "Settings" del repositorio.
2. Haz clic en "Manage access".
3. Invita a colaboradores y asigna roles.

### Discusión y Comentarios
Utiliza issues y pull requests en el repositorio principal para discutir cambios y mejoras en la documentación de la Wiki.

**Crear un Issue para Documentación:**

1. Ve a la pestaña "Issues" del repositorio.
2. Haz clic en "New Issue".
3. Describe el cambio o mejora propuesta en la documentación.

## Características Avanzadas de las Wikis
### Uso de Plantillas
Puedes crear plantillas para estandarizar el formato de las páginas de la Wiki.

**Ejemplo de Plantilla:**

```markdown
# Título de la Página

## Introducción
Breve descripción de la página.

## Contenido
Detalles del contenido principal.

## Ejemplos
Ejemplos relevantes.

## Referencias
Enlaces y referencias adicionales.

```
## Integración con GitHub Pages
Puedes integrar la Wiki con GitHub Pages para publicar la documentación en un sitio web estático.

### Habilitar GitHub Pages:

1. Ve a la pestaña "Settings" del repositorio.
2. En la sección "GitHub Pages", selecciona la rama y la carpeta de origen.
3. Haz clic en "Save".

### Uso de Macros y Snippets
Para reutilizar contenido, puedes crear macros y snippets que se pueden incluir en múltiples páginas.

**Ejemplo de Snippet:**

```markdown
<!-- _includes/header.md -->
# Encabezado Común

Este es un encabezado común utilizado en múltiples páginas.
```
**Incluir el Snippet en una Página:**
```markdown
{% include header.md %}
```
## Buenas Prácticas para Wikis
### Mantenimiento Regular
- ***Revisar y actualizar:*** Asegúrate de que la documentación esté actualizada y relevante.
- **Organización:** Mantén la Wiki bien organizada con una estructura clara.
- **Colaboración:** Fomenta la colaboración y la contribución de todos los miembros del equipo.

### Uso de Estándares de Documentación
- **Consistencia:** Usa un estilo de escritura consistente y claro.
- **Claridad:** Asegúrate de que la documentación sea fácil de entender y seguir.
- **Ejemplos:** Proporciona ejemplos prácticos y relevantes para ilustrar conceptos.
