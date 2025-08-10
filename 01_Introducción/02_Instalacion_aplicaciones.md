# Paso 0 – Poner a punto tu Debian para el curso
💡 Todo lo haremos en la terminal.

1. Abrir terminal

   - Atajo Ctrl + Alt + T o buscamos "Terminal".
  
2. Actualizar el sistema

```bash
sudo apt update && sudo apt upgrade -y
```

3. Instalar utilidades esenciales
   Paquetes que vamos a usar durante todo el curso.

   ```bash
   sudo apt install vim nano curl wget net-tools htop unzip tar git -y
   ```

   Explicación rápida:

   - **vim y nano**: editores de texto en terminal.
   - **curl y wget**: descargar desde internet.
   - **net-tools**: incluye ifconfig y otros comandos de red básico.
   - **htop**: monitor de procesos interactivo.
   - **unzip y tar**: descomprimir.
   - **git**: manejo de versiones en Github.
  
4. Comprobamos conectividad a la red:

   ```bash
   ip a
   ping -c 4 google.com
   ```

   - Si ping responde, estamos conectados a Internet.
  
5. Activar el usuario root.
   Si queremos acceder como root directamente:

   ```bash
   sudo passwd root
   ```

   Luego podrás iniciar sesión como root con:

   ```bash
   su -
   ```

6. Desactivar auto-bloqueo de pantalla.
   Esto evita que la VM se bloquee cada poco tiempo mientras trabajamos.
