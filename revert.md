# Revertir commits

- `git revert <hash-del-commit>`: Se crea un nuevo commit para registrar los cambios realizados para revertir un commit específico.
- `git revert <hash-del-commit> -m <nombre-del-commit>`: Hace lo mismo que git revert pero permtie añadir el nombre del commit que registrará los cambios del revert.
- `git revert <rango-de-commits>`: Se crea un nuevo commit para registrar los cambios realizados para revertir los commits en el rango especificado.
- `git revert --abort`: Si se intenta revertir un commit que modificó archivos que fueron modificados más adelante se genera un conflicto, en caso de no querer seguir se puede abortar con este comando.

## Ejemplos de uso

```bash
# Se realizan y guardan 2 commits
nvim archivo.txt
git commit -am 'Cambio 1' # Hash: abc123
nvim archivo.txt
git commit -am 'Cambio 2' # Hash: def456

# Se intenta revertir el primer cambio
git revert abc123

# Ha ocurrido un conflicto

# Se aborta el revert
git revert --abort
```