# Fusionar el contenido de 2 ramas

- `git merge <branch>`: Inserta el contenido de la rama especificada en la rama actual combinándolas.
- `git merge <branch> -m <mensaje>`: Inserta el contenido de la rama especificada en la rama actual combinándolas y agregando un título manualmente.
- `git merge --abort`: Aborta el merge en caso de que algo saliera mal, como por ejemplo un conflicto.

## Conflictos

- Cuando las 2 ramas tienen cambios en el mismo lugar git no sabe cuál cambio guardar y cuál descartar, produciéndose un conflicto.
- Al usar un editor de texto en el archivo con conflictos, se pueden ver los conflictos para solucionarlos.
- Los editores de texto con interfaz gráfica permiten elegir automáticamente con cuáles cambios quedarse.
- Se puede abortar el merge con `git merge --abort`

## Notas:

- El merge es un commit, no darle un título va a causar que el merge se detenga y se le deberá asignar un título a no ser que git se lo asigne automáticamente.
- Los títulos de los merge no suelen requerir dar mucha información ya que los commits que contienen se encargan de eso.
- Los merge suelen hacerse haciendo uso del pull request para que otros colaboradores puedan analizarlo y aprobar o solicitar cambios basándose en su análisis.

## Ejemplos de uso:

```bash
# Asumiendo que estamos en la brach main y tenemos una branch conflicto donde ambos modificaron la misma línea de REAMDE.md, realizamos un merge
git merge conflicto

# Se generará un conflicto en caso de que ambas ramas hayan modificado una misma línea
# El mensaje de error y git status nos darán información importante para proceder

# En caso de querer revertir el merge
# Abortamos el merge
git merge --abort

# En caso de querer solucionar el conflicto y seguir con el merge
# Entrar al archivo para arreglar el conflicto
nvim README.md

# Añadir el archivo y hacer un commit del conflicto solucionado para terminar el merge
git add README.md
git commit -m "fix(README): Se soluciona el conflicto"
```