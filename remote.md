# Trabajo Remoto

- `git push origin <rama>`: Envía los commits locales al repositorio remoto.

- `git pull`: Descarga y fusiona los cambios desde el repositorio remoto al local.

  > ⚠️ **Nota conceptual:** Este comando es en realidad la combinación de dos acciones consecutivas: `git fetch` y `git merge`. Al resolver un `git pull`, es muy común que surjan **conflictos de fusión** si otra persona modificó las mismas líneas en el servidor remoto.
  >
  > Para entender cómo manejar estos escenarios o cómo resolver los conflictos que puedan aparecer, consultá nuestra guía de [fusión](fusion.md).

- `git remote`: Muestra el nombre de tu servidor remoto configurado.

- `git remote -v`: Lista el nombre de tu repositorio remoto junto con las URL exactas a las que está apuntando.

## 💻 Ejemplos de uso

### 1. Envío de commits al repositorio remoto

Cuando terminas de registrar tus cambios locales en tu rama independiente y quieres subirlos a GitHub por primera vez o enviar nuevos avances, usas `git push`:

```bash
# Enviar los commits locales a la rama correspondiente en GitHub
git push origin <rama>
```

### 2. Sincronizar el repositorio local con los cambios del equipo

Para bajarte las explicaciones o correcciones que tus compañeros ya subieron al repositorio remoto y fusionarlas directamente en tu rama de trabajo actual, usas `git pull`:

```bash
# Descargar y fusionar los cambios desde el repositorio remoto al local
git pull
```

### 3. Mostrar repositorios remotos

Para ver los repositorios remotos configurados, usas `git remote`:

```bash
# Mostrar el nombre del repositorio remoto configurado (por ejemplo, "origin")
git remote
```

### 4. Mostrar repositorios remotos con URL

Para ver los repositorios remotos con sus URLs, usas `git remote -v`:

```bash
# Mostrar el nombre del repositorio remoto y su URL
git remote -v
```
