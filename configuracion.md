# Configuración e Inicialización

### Antes de comenzar a registrar cambios en un proyecto, es fundamental configurar nuestra identidad en Git y preparar el espacio de trabajo local.

## Comandos Principales

* **`git config`**: Permite establecer variables de configuración globales o locales, como el nombre de usuario y el correo electrónico de quien va a realizar los commits.
* **`git clone {url}`**: Descarga una copia exacta de un repositorio remoto junto con todo su historial de versiones a la máquina local.
  
## Ejemplos de uso

* **`A continuación se detalla el flujo de trabajo inicial para configurar tu entorno por primera vez y arrancar un proyecto desde cero o desde la nube.`**

### Paso 1: Configurar la identidad global
Establecemos el nombre y correo electrónico que daran autor a los futuros commits que se realicen en el proyecto. Esto es un requisito obligatorio antes de empezar a trabajar.
```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu-email@ejemplo.com"
```

### Paso 2: Verificar la configuración establecida
Para confirmar que los datos se guardaron correctamente en el sistema, podemos listar todas las variables activas.
```bash
git config --list
```

## Estos paso  siguientes son optarorios segun lo que se quiera realizar. Crear un nuevo repositorio a partir de una carpeta vacia en tu ordenador(Local), o traer un repositorio ya existente desde git.

### Opcion A (Iniciar un proyecto Local)
Si estás empezando un proyecto propio desde cero en tu computadora, te posicionás en la carpeta del proyecto mediante la terminal. A continuacion detallo como seria llegar hasta la carpeta con la consola:
> [!NOTE]
> ```text
> C:\ (Raíz del disco)
> └── Users/
>     └── TuUsuario/
>         └── Desktop/ (Escritorio)
>             └── Repositorio/ (Tu carpeta de Git)
>                 ├── branches.md
>                 └── configuracion.md
> ```
> ```text
> # 1. Aseguramos que estamos parados en la raíz del disco C:
>cd C:\
>
># 2. Nos movemos a la carpeta de tu usuario (reemplazá "TuUsuario" por el nombre real de tu equipo)
>cd Users\TuUsuario
>
># 3. Entramos al Escritorio
>cd Desktop
>
># 4. Entramos finalmente a la carpeta del proyecto
>cd Repositorio
> ```

Luego de haber hecho estos pasos ejecutamos:
```bash
git init
```

### Opcion B (clonar un repositorio en git existente)
Si el proyecto ya existe en una plataforma remota (como GitHub) y querés importarlo a tu equipo en una carpeta vacia para empezar a trabajar en él, copiás su URL y realizas el mismo procedimiento
anteriormente detallado y antes de ejecutar el comando (**`git init`**), lo cambias por el siguiente comando:
```bash
git clone [https://github.com/usuario/nombre-del-proyecto.git](https://github.com/usuario/nombre-del-proyecto.git)
```
