# 📚 – Cómo obtener ayuda en Linux

## 1️⃣ Manual de usuario (man)

El comando **man** (de manual) muestra la documentación oficial de caso todos los comandos.

```bash
man ls
```

Navegación:

- Flechas o PgUp/PgDn -> moverte.
- /palabra -> buscar dentro del manual.
- q -> salir.

Los manuales están divididos en secciones:

1. Comandos ejecutables.
2. Llamadas al sistema.
3. Llamadas a librerías.
4. Archivos especiales y drivers.
5. Formatos de archivos.
6. Juegos.
7. Miscelánea.
8. Comandos de administración.

Ejemplo:

```bash
man 5 passwd # Explica el formato del archivo /etc/passwd
```

## 2️⃣ Ayuda rápida (--help)

La mayoría de comandos aceptan:

```bash
ls --help
```

Esto muestra las opciones disponibles sin abrir el manual.

## 3️⃣ Info (info)

Algunos programas tienen documentación más extensa.

```bash
info coreutils 'ls invocation'
```

(Es menos usado que **man**, pero útil en ciertos casos).

## 4️⃣ Comando whatis

Muestra una descripción muy breve:

```bash
whatis ls
```

## 5️⃣ Comando apropos

Busca comandos relacionados con una palabra clave:

```bash
apropos network
```

## ⚙️ Opciones y argumentos

Cuando usas un comando, su sintaxis general es:

```css
comando [opciones] [argumentos]
```

- **Opciones**: modifican el comportamiento (-l, --all...).
- **Argumentos**: indican sobre qué actúa el comando (archivo, directorio...).

Ejemplo:

```bash
ls -la /etc
```

- **ls** -> comando.
- **-la** -> opciones (lista larga + mostrar ocultos).
- **/etc** -> argumento (directorio a listar).

## 📝 Ejercicio práctico

1. Muestra el manual de **cp** y localiza la opción para preservar atributos al copiar.
2. Usa **whatis** para saber qué hace **tar**.
3. Busca todos los comandos relacionados con usuarios usando **apropos**.
4. Ejecuta:

```bash
ls --help | less
```
y desplázate para ver todas las opciones.


