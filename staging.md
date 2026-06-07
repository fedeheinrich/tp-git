# Área de preparación (staging)

El área de preparación funciona como una zona intermedia entre los archivos modificados y el commit.

- `git add <archivo>`: Agrega un archivo en específico al área de preparación.

- `git add .`: Agrega todos los archivos modificados y nuevos al área de preparación.

- `git add -p`: Permite seleccionar manualmente qué partes o líneas de un archivo se agregan al staging area.

- `git rm --cached <archivo>`: Quita un archivo del área de preparación sin eliminarlo del disco local.

- `git restore <archivo>`: Descarta los cambios realizados en un archivo y lo devuelve a su último estado guardado.

- `git clean -fd`: Elimina archivos y carpetas sin seguimiento del directorio de trabajo.

## Ejemplos de uso

### 1. Agregar un archivo en específico para el próximo commit:

Si modificamos únicamente README.md y queremos incluirlo en el próximo commit: 

```bash
git add README.md
```

### 2. Seleccionar cambios específicos de un archivo:

Si un archivo contiene varias modificaciones pero solo queremos incluir algunas en el próximo commit: 

```bash
git add -p archivo.js
```

### 3. Quitar un archivo del área de preparación:

Si agregamos un archivo por error pero queremos conservar sus cambios: 

```bash
git rm --cached archivo.json
```