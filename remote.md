# Trabajo Remoto

* `git push origin <rama>`: Envia los commits locales al repositorio remoto.

* `git pull`: Descarga y fusiona los cambios desde el repositorio remoto al local.
> ⚠️ **Nota conceptual:** Este comando es en realidad la combinación de dos acciones consecutivas: `git fetch` y `git merge`. Al resolver un `git pull`, es muy común que surjan **conflictos de fusión** si otra persona modificó las mismas líneas en el servidor remoto. 
>
> Para entender cómo manejar estos escenarios o cómo resolver los conflictos que puedan aparecer, consultá nuestra guía de [fusión](fusion.md).

## 💻 Ejemplos de uso

### 1. Envío de commits al repositorio remoto
Cuando terminás de registrar tus cambios locales en tu rama independiente y querés subirlos a GitHub por primera vez o enviar nuevos avances, usás `git push`:

```bash
# Enviar los commits locales a la rama correspondiente en GitHub
git push origin <rama>
```

### 2. Sincronizar el repositorio local con los cambios del equipo
Para bajarte las explicaciones o correcciones que tus compañeros ya subieron al repositorio remoto y fusionarlas directamente en tu rama de trabajo actual, usás `git pull`:

```bash
# Descargar y fusionar los cambios desde el repositorio remoto al local
git pull
```