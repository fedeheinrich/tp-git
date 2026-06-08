# Reset

Los comandos de reset permiten volver a un estado anterior del repositorio. Dependiendo qué se use, los cambios pueden mantenerse o eliminarse.

- `git reset --soft <hash>`: Vuelve a un commit anterior y elimina los commits posteriores, pero mantiene los cambios realizados para que puedan volver a confirmarse en un nuevo commit.

- `git reset --hard <hash>`: Vuelve a un commit anterior y elimina los commits posteriores junto con todos los cambios realizados. Los cambios descartados no se pueden recuperar fácilmente.

## Ejemplos de uso

### 1. Volver atrás sin perder trabajo:

Si hicimos varios commits y queremos corregirlos, podemos volver a un commit anterior manteniendo sus cambios con: 

```bash
git reset --soft <hash>
```

### 2. Eliminar cambios y regresar a una versión anterior:

Si queremos descartar por completo los últimos cambios, lo hacemos con:

```bash
git reset --hard <hash>
```