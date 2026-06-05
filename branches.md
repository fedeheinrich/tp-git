# Gestión de Ramas (Branches)
Las ramas nos permiten desarrollar nuevas funcionalidades, corregir errores o experimentar sin afectar el código principal y estable del proyecto.
 * **`git branch`**: Lista las ramas e indica en cuál estás posicionado.
 * **`git branch <nombre>`**: Crea una nueva rama.
 * **`git branch -d <nombre>`**: Borra una rama especificada de forma segura.
 * **`git branch -D <nombre>`**: Borra una rama especificada de forma forzada. El cambio esta en la D mayuscula, que git la interpreta como una medida de fuerza para saltearse la proteccion del mismo.
 * **`git checkout <rama>`**: Cambia a otra rama.
 * **`git checkout -b <rama>`**: Crea una nueva rama y se mueve a ella en el mismo paso.
 * **`git checkout -`**: Comando rápido para volver a la última rama en la que estabas posicionado.
 * **`git checkout -`**: Comando rápido para volver a la última rama en la que estabas posicionado.
 * **`git switch <rama> / git switch -c <rama>`**: Comandos más modernos, dedicados exclusivamente al cambio y creación de ramas.

## Ejemplos de uso

Se requiere implementar una nueva funcion al proyecto, esta se va a llamar {Funcion_1}.

### Primer paso: Chequeamos donde estamos parados
```bash
 git branch
```
### Segundo paso: Si estamos en 'Main' o cualquier otra rama que no sea 'Dev' hacemos el switch a la 'Branch Dev' para poder realizar una ramificacion segura y acorde a los parametros sugeridos para el uso de buenas practicas.
```bash
  git checkout Dev
```
### Tercer paso: Traemos los ultimos cambios que hayan sucedido en la 'Branch Dev' para no tener conflictos u errores cuando se haga la ramificacion correspondiente.
```bash
  git pull origin dev
```
  Nota: git pull origin dev es el comando utilizado para traer los ultimos cambios de una rama en especifico.
  
### Cuarto paso y ultimo: Ya en este este punto estamos en la 'Branch Dev' con sus ultimas actualizaciones, por lo que resta solamente hacer el branch de la nueva funcion. Aqui podemos hacer dos pasos:
  Crear la branch y movernos a ella
  ```bash
    git checkout -b feature/Funcion_1
  ```
  O solamente crear la branch sin movernos de rama
  ```bash
    git branch feature/Funcion_1
  ```
### Quinto paso(Opcional): Ahora si se quiere borrar una branch especifica {Funcion_1} y segura, el comando a tener en cuenta es el siguiente:
```bash
    git branch -d [feature/Funcion_1]
```
