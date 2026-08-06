# Gestión de Ramas (Branches)

Las ramas nos permiten desarrollar nuevas funcionalidades, corregir errores o experimentar sin afectar el código principal y estable del proyecto.

### `git branch`: Lista las ramas e indica en cuál estás posicionado.

### `git branch <nombre>`: Crea una nueva rama.

### `git branch -d <nombre>`: Borra una rama especificada de forma segura.

### `git branch -D <nombre>`: Borra una rama especificada de forma forzada. El cambio está en la D mayúscula, que git la interpreta como una medida de fuerza para saltarse la protección del mismo.

### `git checkout <rama>`: Cambia a otra rama.

### `git checkout -b <rama>`: Crea una nueva rama y se mueve a ella en el mismo paso.

### `git checkout -`: Comando rápido para volver a la última rama en la que estabas posicionado.

### `git switch <rama>` / `git switch -c <rama>`: Comandos más modernos, dedicados exclusivamente al cambio y creación de ramas.

## Ejemplos de uso

Se requiere implementar una nueva función al proyecto, esta se va a llamar Funcion_1.

### Primer paso: Verificamos dónde estamos parados

```bash
git branch
```

### Segundo paso: Si estamos en <main> o cualquier otra rama que no sea <dev> hacemos el switch a la rama <dev> para poder realizar una ramificación segura y acorde a los parámetros sugeridos para el uso de buenas prácticas.

```bash
git checkout dev
```

### Tercer paso: Traemos los últimos cambios que hayan sucedido en la rama <dev> para no tener conflictos u errores cuando se haga la ramificación correspondiente.

```bash
git pull origin dev
```

Nota: `git pull origin <dev>` es el comando utilizado para traer los últimos cambios de una rama en específico. (En este caso <dev>)

### Cuarto paso y último: Ya en este punto estamos en la rama <dev> con sus últimas actualizaciones, por lo que resta solamente hacer la ramificación de la nueva función. Aquí podemos hacer dos pasos:

Crear la rama y movernos a ella:

```bash
git checkout -b feature/Funcion_1
```

O solamente crear la rama sin movernos de rama:

```bash
git branch feature/Funcion_1
```

### Quinto paso (Opcional): Ahora si se quiere borrar una rama específica, por ejemplo: Funcion_1, el comando a utilizar es el siguiente:

```bash
git branch -d feature/Funcion_1
```

Nota: Para eliminar también la rama en el remoto, ver la subsección Eliminar una rama remota en [remote.md](remote.md#eliminar-una-rama-remota).
