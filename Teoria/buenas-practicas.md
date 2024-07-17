# Buenas prácticas en Git y GitHub

## 1. Elige un flujo de trabajo
Es importante que conozcas o elijas un flujo de trabajo (workflow) según tus necesidades. Algunos ejemplos son:

- **Git Feature Branch Workflow**: Crea ramas dedicadas para cada nueva funcionalidad en lugar de trabajar directamente en la rama principal (master).

### Crear una nueva rama de característica
1. Asegúrate de estar en la rama principal (por ejemplo, `main` o `master`).
2. Ejecuta: `git checkout -b nombre-de-la-rama`.
3. Realiza tus cambios y confirma los commits.
4. Empuja la rama a tu repositorio remoto: `git push origin nombre-de-la-rama`.


- **Gitflow Workflow**: Similar al anterior, pero con una estructura de ramas diseñada alrededor de las entregas del proyecto.

### Crear una nueva rama de característica en Gitflow
1. Asegúrate de estar en la rama `develop`.
2. Ejecuta: `git checkout -b feature/nombre-de-la-caracteristica`.
3. Realiza tus cambios y confirma los commits.
4. Empuja la rama de característica a tu repositorio remoto: `git push origin feature/nombre-de-la-caracteristica`.


- **Forking Workflow**: Permite a cada colaborador tener su propio repositorio en lugar de usar uno centralizado.

### Contribuir en el Forking Workflow
1. Haz un "fork" del repositorio oficial en GitHub (esto crea tu propio repositorio remoto).
2. Clona tu fork en tu máquina local: `git clone URL-del-fork`.
3. Agrega el repositorio oficial como un control remoto adicional: `git remote add upstream URL-del-repositorio-oficial`.
4. Crea una nueva rama de característica: `git checkout -b nombre-de-la-caracteristica`.
5. Realiza tus cambios y confirma los commits.
6. Empuja la rama de característica a tu fork: `git push origin nombre-de-la-caracteristica`.
7. Abre una solicitud de extracción desde tu fork al repositorio oficial.


## 2. Estructura tus mensajes de commits
Tus mensajes de commits deben ser descriptivos. Puedes usar sufijos como:

- `feat`: Para nuevos features.
- `fix`: Para corrección de errores.
- `docs`: Cambios en la documentación.
- `test`: Adición de pruebas.
- `refactor`: Refactorización del código.

### Buenas prácticas para mensajes de commit

Escribir buenos mensajes de commit es fundamental para mantener un historial de cambios legible y comprensible. Aquí tienes algunas recomendaciones:

1. **Usa el verbo imperativo**: Elige verbos como "Add", "Change", "Fix" o "Remove" para expresar la acción realizada en el commit. Por ejemplo:
   - `git commit -m "Add new search feature"`
   - `git commit -m "Fix a problem with the topbar"`
   - `git commit -m "Change the default system color"`
   - `git commit -m "Remove a random notification"`

2. **No uses punto final ni puntos suspensivos**: Los mensajes de commit no necesitan puntuación adicional. Mantén el título conciso y sin puntos innecesarios:
   - ❌ `git commit -m "Add new search feature."`
   - ❌ `git commit -m "Fix a problem with the topbar..."`
   - ✅ `git commit -m "Change the default system color"`

3. **Limita el título a 50 caracteres**: Sé breve y directo. Si necesitas más contexto, agrégalo en el cuerpo del mensaje:
   - ❌ `git commit -m "Add new search feature and change typography to improve performance"`
   - ✅ `git commit -m "Change typography to improve performance"`

4. **Añade contexto en el cuerpo del mensaje**: Si es necesario, proporciona más detalles en el cuerpo del commit. Evita saturar el título:
   - Ejemplo:
     ```
     feat(auth): Agregar funcionalidad de autenticación de usuario
     fix(api): Resolver problema en la ruta de la API de productos
     docs(readme): Actualizar instrucciones de instalación
     style(css): Aplicar formato CSS consistente
     test(user): Agregar pruebas unitarias para el módulo de usuario
     ```


## 3. Utiliza pull requests
Antes de integrar cambios, envía un pull request. Esto permite revisar el código y mantener la calidad del proyecto. No importa si trabajas solo o en equipo, una revisión previa es saludable.

## 4. Añade solo los archivos relevantes
En lugar de usar `git add .`, añade solo los archivos en los que trabajaste. Esto evita incluir archivos innecesarios en el repositorio.

## 5. Documentación y README.md
El README.md es crucial. Describe el proyecto, cómo instalarlo, ejecutarlo y contribuir. Incluye ejemplos, capturas de pantalla y enlaces relevantes.

## 6. Licencias en proyectos de código abierto

Las licencias de código abierto se ajustan a la definición de código abierto y permiten que el software se utilice, modifique y distribuya libremente. Algunos aspectos clave son:

1. **Libertades Fundamentales**:
   - **Uso**: Los usuarios tienen el derecho de utilizar el software con cualquier propósito.
   - **Acceso al Código Fuente**: Los usuarios pueden acceder al código fuente del software.
   - **Modificación**: Los usuarios pueden modificar el código fuente según sus necesidades.
   - **Distribución**: Los usuarios pueden distribuir copias del software modificado o no modificado.

2. **Ejemplos de Licencias de Código Abierto**:
   - **GNU General Public License (GPL)**: Garantiza las libertades fundamentales y requiere que los programas derivados también sean de código abierto.
   - **MIT License**: Permite un uso amplio, incluso en proyectos comerciales, con poca restricción.
   - **Apache License**: Proporciona una licencia permisiva con algunas condiciones.
   - **BSD Licenses**: Varias variantes (por ejemplo, BSD 2-Clause y BSD 3-Clause) que son flexibles y ampliamente utilizadas.

3. **Compatibilidad con Licencias Propietarias**:
   - Algunas licencias de código abierto permiten crear productos propietarios a partir del código fuente abierto.

4. **Dominio Público**:
   - El software de dominio público (sin derechos de autor registrados) también cumple con los criterios de código abierto si se puede acceder a todo el código fuente.

#### Recursos Adicionales
- Sitio web de la Open Source Initiative
- Versión en línea del libro "Open Source Licensing: Software Freedom and Intellectual Property Law"

## 7. Uso de Markdown
Markdown es un lenguaje ligero para formatear texto. Puedes usarlo para crear títulos, listas, enlaces, imágenes y más. Aquí tienes un ejemplo:

```markdown
# Encabezado 1

## Encabezado 2

### Encabezado 3


# Lista de elementos
- Elemento 1
- Elemento 2
- Elemento 3

1. Elemento 1
2. Elemento 2
3. Elemento 3

* Elemento 1
* Elemento 2
* Elemento 3

# Énfasis

**Negrita**
*Cursiva*

# Enlaces

Enlace a [Google](https://google.co.jp)

# Imágenes

!Logo de Markdown

# Código

`print("Hola, mundo")`

```

Además también se puede incluir HTML.

```markdown
<p align="left">
    <img src="origen_imagen" width="100%">
</p>
```
