# Git y GitHub: Trabajo con el Historial de Cambios

## Introducción
Git es un sistema de control de versiones distribuido que permite a los desarrolladores rastrear y gestionar cambios en el código fuente a lo largo del tiempo. GitHub es una plataforma basada en Git que facilita la colaboración y el manejo de proyectos. Este documento se enfoca en cómo trabajar con el historial de cambios en Git y GitHub, incluyendo la reescritura del historial, la reversión y restauración de cambios, y la búsqueda de errores.

## Reescribiendo el Historial con `amend` y `rebase` Interactivo

### `git commit --amend`
El comando `git commit --amend` permite modificar el último commit realizado. Es útil para corregir mensajes de commit, agregar archivos olvidados o ajustar cambios.

**Ejemplo:**
```bash
# Realizas un commit inicial
git commit -m "Initial commit"

# Te das cuenta que olvidaste añadir un archivo o cometiste un error en el mensaje del commit
git add archivo_olvidado.txt
git commit --amend
```
Este comando abrirá el editor de texto configurado para que modifiques el mensaje del commit si es necesario.

### `git rebase -i`
El rebase interactivo (`git rebase -i`) es una poderosa herramienta para reescribir el historial de commits. Permite combinar, reordenar, editar, y eliminar commits.

**Ejemplo:**
```bash
# Inicia un rebase interactivo sobre los últimos 3 commits
git rebase -i HEAD~3
```
Esto abrirá un editor de texto con una lista de los últimos 3 commits. Puedes realizar acciones como `pick` (mantener), `squash` (combinar), `edit` (editar) y `reword` (modificar el mensaje del commit).

## Revertir y Restaurar Cambios con `revert` y `reset`

### `git revert`
El comando `git revert` crea un nuevo commit que deshace los cambios de un commit anterior, sin modificar el historial.

**Ejemplo:**
```bash
# Revertir el commit con hash abc123
git revert abc123
```

### `git reset`
El comando `git reset` puede deshacer commits y cambios en el área de preparación. Hay tres modos principales:

- `--soft`: Mantiene los cambios en el área de preparación.
- `--mixed` (predeterminado): Mantiene los cambios en el directorio de trabajo.
- `--hard`: Deshace todos los cambios, incluyendo los del directorio de trabajo.

**Ejemplo:**
```bash
# Restablecer al commit anterior, manteniendo los cambios en el directorio de trabajo
git reset --mixed HEAD~1
```

## Búsqueda de Errores con `bisect` y `blame`

### `git bisect`
El comando `git bisect` ayuda a encontrar el commit específico que introdujo un error. Se realiza una búsqueda binaria en el historial de commits para identificar el commit problemático.

**Ejemplo:**
```bash
# Iniciar bisect
git bisect start
# Marcar el commit actual como malo
git bisect bad
# Marcar un commit anterior conocido como bueno
git bisect good abc123

# Git ahora seleccionará un commit intermedio para probar.
# Después de probar, marca si es bueno o malo con:
git bisect good # o git bisect bad
```

### `git blame`
El comando `git blame` muestra quién hizo cada cambio en un archivo, línea por línea. Es útil para rastrear cuándo y por quién se introdujo un cambio específico.

**Ejemplo:**
```bash
# Mostrar el historial de cambios para archivo.txt
git blame archivo.txt
```

