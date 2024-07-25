
# Git y GitHub: Herramientas Avanzadas

## Introducción
Git es una herramienta muy poderosa y flexible que ofrece numerosas funcionalidades avanzadas para gestionar y optimizar el flujo de trabajo de desarrollo. Este documento explora cómo guardar cambios temporales con `stash`, aplicar cambios selectivos con `cherry-pick`, usar hooks y alias para automatizar tareas, y trabajar con submódulos y subtrees.

## ¿Cómo Guardar Cambios Temporales con `stash`?
El comando `git stash` permite guardar cambios temporales en el directorio de trabajo y el área de preparación sin hacer un commit. Esto es útil cuando necesitas cambiar de contexto rápidamente y volver a esos cambios más tarde.

### Uso Básico de `git stash`
1. **Guardar cambios:**

    ```bash
    git stash
    ```
2. **Listar stashes:**
    ```bash
    git stash list
    ```
3. **Aplicar el último stash:**
    ```bash
    git stash apply
    ```
4. **Aplicar un stash específico:**
    ```bash
    git stash apply stash@{n}
    ```
5. **Eliminar el último stash:**
    ```bash
    git stash drop
    ```

### Guardar Cambios con un Mensaje
Puedes añadir un mensaje descriptivo al stash para facilitar la identificación.
```bash
git stash save "Mensaje descriptivo"
```

## Aplicación de Cambios Selectivos con `cherry-pick`
El comando `git cherry-pick` permite aplicar commits específicos de una rama a otra. Es útil para transferir cambios específicos sin hacer merge completo.

### Uso Básico de `git cherry-pick`
1. **Seleccionar y copiar un commit:**
    ```bash
    git cherry-pick <commit-hash>
    ```
2. **Aplicar múltiples commits:**
    ```bash
    git cherry-pick <commit-hash1> <commit-hash2>
    ```

### Resolución de Conflictos
Si hay conflictos, Git pausará el cherry-pick para que los resuelvas. Después de resolver los conflictos, continúa el proceso:
```bash
git cherry-pick --continue
```

## Uso de Hooks y Alias para Automatizar Tareas

### Hooks
Los hooks son scripts que Git ejecuta automáticamente en ciertos eventos. Pueden ayudar a automatizar tareas como pruebas, validaciones y despliegues.

### Ejemplos de Hooks Comunes
- **Pre-commit:** Se ejecuta antes de hacer un commit.
    ```bash
    # .git/hooks/pre-commit
    #!/bin/sh
    npm test
    ```
- **Post-merge:** Se ejecuta después de un merge.
    ```bash
    # .git/hooks/post-merge
    #!/bin/sh
    npm install
    ```

### Alias
Los alias en Git son comandos personalizados que pueden simplificar tareas repetitivas.

### Crear Alias
1. **Añadir alias en la configuración de Git:**
    ```bash
    git config --global alias.st status
    git config --global alias.ci commit
    git config --global alias.co checkout
    ```

### Uso de Alias
Una vez configurados, puedes usar los alias en lugar de los comandos completos:
```bash
git st  # Equivalente a git status
git ci  # Equivalente a git commit
git co  # Equivalente a git checkout
```

## ¿Cómo Trabajar con Submódulos y Subtrees?

### Submódulos
Los submódulos permiten incluir repositorios Git como subdirectorios en otro repositorio. Esto es útil para mantener dependencias en proyectos separados pero relacionados.

### Añadir un Submódulo
1. **Añadir un submódulo:**
    ```bash
    git submodule add https://github.com/usuario/submodulo.git
    ```
2. **Inicializar y actualizar submódulos:**
    ```bash
    git submodule update --init
    ```

### Trabajar con Submódulos
1. **Actualizar submódulos:**
    ```bash
    git submodule update --remote
    ```
2. **Eliminar un submódulo:**
    ```bash
    git submodule deinit -f submodulo
    git rm -f submodulo
    ```

### Subtrees
Los subtrees permiten combinar proyectos Git en un solo repositorio, ofreciendo una alternativa más sencilla que los submódulos.

### Añadir un Subtree
1. **Añadir un subtree:**
    ```bash
    git subtree add --prefix=subcarpeta https://github.com/usuario/proyecto.git rama --squash
    ```

### Actualizar un Subtree
1. **Actualizar desde el repositorio remoto:**
    ```bash
    git subtree pull --prefix=subcarpeta https://github.com/usuario/proyecto.git rama --squash
    ```

### Beneficios de los Subtrees
- **Simplicidad:** No requiere comandos adicionales para clonar o actualizar.
- **Integración:** Los cambios se integran directamente en el historial del repositorio principal.