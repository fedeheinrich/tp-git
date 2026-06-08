# Visualización

Los comandos de visualización nos permiten consultar información del repositorio, revisar cambios y el estado de distintas versiones del proyecto sin modificarlo.

- `git log`: Muestra el historial completo de commits realizados en el repositorio.

- `git log --oneline`: Muestra el historial de commits de forma resumida, mostrando cada uno en una sola línea.

- `git log --graph`: Muestra en la terminal el árbol y las ramificaciones de los commits.

- `git log -n`: Limita la cantidad de commits que se muestran.

- `git log --author="nombre"`: Filtra los commits realizados por un autor en específico.

- `git log --grep="palabra"`: Busca commits donde el mensaje tenga cierta palabra.

- `git log --since, --after y --before`: Permite filtrar commits según un rango de fechas.

- `git log --pretty`: Permite personalizar el formato de salida de los commits.

- `git log --stat`: Muestra los archivos modificados en cada commit y un recuento de líneas.

- `git reflog`: Muestra un registro de los movimientos realizados por HEAD, permitiendo ver cambios recientes en las referencias locales.

- `git show <hash>`: Muestra la información detallada de un commit en específico, incluyendo sus cambios.

- `git diff`: Compara los cambios locales con la última versión guardada en el repositorio.

- `git diff <hash1> <hash2>`: Compara las diferencias entre los commits determinados.

- `git diff HEAD~<n>`: Compara el estado actual con el de varios commits anteriores.

- `git diff <rama> <otra_rama>`: Permite comparar las diferencias entre dos ramas distintas.

- `git diff --stat`: Muestra un resumen de los archivos modificados y sus cambios realizados.

- `git diff --word-diff`: Muestra la diferencia a nivel de palabras dentro de la misma línea.

- git bisect: Automatiza una búsqueda binaria para navegar rápido entre commits antiguos y encontrar el momento exacto en el que se introdujo un error.

- git checkout <hash>: Te permite "viajar en el tiempo" a un commit pasado (dejando la cabeza desconectada o *detached HEAD) únicamente para observar el código.

## Ejemplos de uso

### 1. Revisar quién hizo los últimos cambios:

Durante un TP, si queremos saber qué integrante realizó commit recientemente, y sus cambios, podemos ejecutar: 

```bash
git log
```

### 2. Revisar cambios antes de crear un commit:

Después de editar un archivo se puede ver qué líneas fueron modificadas con:

```bash
git diff
```

### 3. Buscar cuándo hubo un error:

Si un archivo empezó a fallar y queremos ver cuándo se introdujo el cambio, podemos revisar el historial con:

```bash
git log
```

y comparar versiones con:

```bash
git diff <hash1> <hash2>
```
