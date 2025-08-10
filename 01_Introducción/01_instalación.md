## Instalación de un Linux Minimalista en VirtualBox

Utilizamos Debian netinst, aunque Ubuntu Server minimal es también una gran opción porque:

- Son estables.

- Son muy usadas en entornos reales.

- Te dejan instalar solo lo necesario.

- Aprenderás administración pura.

## 1️⃣ Preparar el entorno

1. Descarga la ISO minimalista:

    - Debian: https://www.debian.org/distrib/netinst (elige la "netinst" para instalación mínima).

    - Ubuntu Server: https://ubuntu.com/download/server (elige la LTS más reciente).

2. Abre VirtualBox y crea una nueva máquina:

    - Nombre: Debian-Minimal o Ubuntu-Server.

    - Tipo: Linux.

    - Versión: según la distro (Debian 64-bit o Ubuntu 64-bit).

3. Asignar recursos:

   - RAM: 2 GB mínimo (4 GB si tu PC lo permite).

   - CPU: 2 núcleos mínimo.

   - Disco: 20 GB (dinámico, formato VDI).

4. Adjuntar la ISO:

   - Configuración → Almacenamiento → Controlador IDE → Agregar disco → Selecciona la ISO.

## 2️⃣ Instalación paso a paso (Debian/Ubuntu minimal)

Cuando inicies la VM:

1. Selecciona instalación normal (no gráfica si quieres la experiencia más pura).

2. Idioma, zona horaria y teclado → español/es.

3. Nombre de máquina: linux-lab.

4. Dominio: deja en blanco.

5. Usuario root:

   - Crea contraseña segura.

6. Usuario normal:

   - Nombre: tu nombre o admin.

   - Contraseña: segura, diferente de root.

7. Particionado:

   - Usa Guiado – utilizar todo el disco.

   - No LVM si quieres simplicidad al principio.

8. Selección de software:

   - ❌ Quita entorno de escritorio.

   - ✅ Deja marcado Utilidades estándar del sistema y Servidor SSH.

   - Esto te deja un Linux puro en terminal.

9. Instala GRUB cuando lo pida.

10. Reinicia y quita la ISO.

## 3️⃣ Primer arranque

Te encontrarás con algo así:

```yami
Debian GNU/Linux 12 linux-lab tty1

linux-lab login:
```

- Inicia con tu usuario y contraseña.

- Ya estás en la terminal minimalista.

## 4️⃣ Primeras tareas de configuración

Nada más instalar:

```bash
# Actualizar el sistema
sudo apt update && sudo apt upgrade -y

# Instalar utilidades esenciales
sudo apt install vim nano curl wget net-tools htop unzip tar -y

# Comprobar red
ip a
ping google.com
```

## 5️⃣ Objetivo de esta máquina

- Aprenderás desde lo más básico: directorios, permisos, procesos, redes…

- Instalarás y configurarás servicios manualmente (web, FTP, bases de datos, firewall, etc.).

- Documentarás cada cambio en tu portfolio.
