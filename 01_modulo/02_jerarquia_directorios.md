## Jerarquía de Directorios en Linux

En Linux ***todo es un archivo*** (incluso nuestro teclado o la tarjeta de red se representan como archivos).
El sistema de ficheros se organiza en una ***estructura jerárquica*** que empieza en / (raíz).

## 📂 Principales directorios del sistema

| 📁 Directorio | 📦 Contiene                                                                 |
|--------------|------------------------------------------------------------------------------|
| `/`          | Raíz del sistema. Todo cuelga de aquí.                                      |
| `/bin`       | Binarios esenciales para todos los usuarios (`ls`, `cp`, `mv`…)             |
| `/boot`      | Archivos para arrancar el sistema (kernel, GRUB…)                           |
| `/dev`       | Dispositivos representados como archivos (discos, USB…)                     |
| `/etc`       | Archivos de configuración del sistema                                       |
| `/home`      | Carpetas personales de los usuarios                                         |
| `/lib`       | Bibliotecas esenciales para los programas del sistema                       |
| `/media`     | Puntos de montaje de dispositivos externos (USB, CD…)                       |
| `/mnt`       | Montajes temporales                                                         |
| `/opt`       | Programas opcionales (no esenciales)                                        |
| `/proc`      | Información en tiempo real del sistema y procesos                           |
| `/root`      | Carpeta personal del usuario `root`                                         |
| `/run`       | Información temporal sobre procesos y servicios en ejecución                |
| `/sbin`      | Binarios esenciales para administración del sistema                         |
| `/srv`       | Datos servidos por servicios (web, FTP…)                                    |
| `/sys`       | Información sobre hardware y kernel                                         |
| `/tmp`       | Archivos temporales (se borran al reiniciar)                                |
| `/usr`       | Programas y utilidades de usuario                                           |
| `/var`       | Archivos variables (logs, colas de correo, cachés…)                         |

## 💡 Concepto clave

En Linux no hay letras de unidad como en Windows (C:, D:…).
Todo está bajo un único árbol de directorios que parte de /.
Si conectas un pendrive, no será "E:" sino que se montará en alguna carpeta (/media/usuario/pendrive por ejemplo).


## 🔍 Ejercicio práctico

1. Muestra el contenido de /:

   ```bash
   ls -l /
   ```

2. Entra en /etc y lista su contenido:

  ```bash
  cd /etc
  ls -l
  ```

3. Ve a /home y lista usuarios:

  ```bash
  cd /home
  ls -l
  ```

4. Mira que hay en /dev:

  ```bash
  cd /dev
  ```

5. Consulta el contenido de /proc/cpuinfo:

  ```bash
  cat /proc/cpuinfo
  ```
