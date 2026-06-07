# Crear nuevos commits

- `git commit`: Abre el editor de texto para poder escribir mensajes más extensos para crear un commit con los datos en el [staging area](staging.md).
- `git commit -m <nombre-del-commit>`: Crea el commit escribiendo el mensaje en el mismo comando con los datos en el staging area.
- `git commit -a`: Revisa el working tree para encontrar los archivos que hayan sido modificados, agregados o eliminados, realiza el git add y git rm por sí mismo para guardarlos en el staging area y realiza un commit con esos cambios.

## Notas

- Los commits no guardan archivos, guardan cambios.
- Los commits permiten ver, guardar y revertir cambios en el repositorio.
- Los commits siempre deben tener algún mensaje.
- El comando `git commit` contiene varios parámetros de los cuales algunos son compatibles en el mismo comando y otros son mutuamente excluyentes.

## Ejemplos de uso:

```bash
# Se crea un archivo
touch README.md

# Se guarda el archivo nuevo
git add README.md

# Se guarda todo en un commit y se abre el editor de texto para elegir un título
git commit

## Versión acortada con parámetros:

# Se crea un archivo
touch README.md

# Se añade al staging area y se lo guarda en un commit al cual se le añade un mensaje desde el mismo comando
git commit -am "Se agrega el archivo README.md"

```
