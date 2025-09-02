
# Bandit Level 5 → Level 6 (Inhere Folder)

## 🎯 Objetivo

En este nivel, debes encontrar y leer un archivo dentro del directorio `inhere` que cumpla las siguientes condiciones:

* Legible por humanos (**human-readable**)
* Tamaño exacto de **1033 bytes**
* No ejecutable

Este archivo contiene la contraseña para el siguiente nivel.

---
## Información de conexión

* **Usuario:** `bandit5`
* **Host:** `bandit.labs.overthewire.org`
* **Puerto:** `2220`
* **Contraseña:** *(usa la que obtuviste del nivel anterior)*

## Pasos para resolverlo

1. Accede al directorio `inhere`
```bash
cd inhere
```

2. Busca archivos por tamaño exacto
```bash
find . -type f -size 1033c
```

-`.` → buscar desde el directorio actual
-`-type f` → solo archivos normales
-`-size 1033c` → exactamente 1033 bytes

Esto debería devolver algo como:

./maybehere07/.file2


3. Comprueba si el archivo es legible por humanos
```bash
file ./maybehere07/.file2
```

Salida esperada:
```bash
./maybehere07/.file2: ASCII text, with very long lines (1000)
```

 `ASCII text` indica que es **human-readable**, por lo que este es el archivo correcto.

4. Muestra el contenido del archivo para obtener la contraseña
```bash
cat ./maybehere07/.file2
```

 Obtendrás la contraseña para el siguiente nivel: HWasnPhtq9AVKe0dmk45nxy20cvUa6EG



## Comandos útiles

`ls` — Lista archivos en el directorio actual

`cd <directorio>` — Cambia de carpeta

`cat <archivo>` — Muestra el contenido de un archivo

`file <archivo>` — Muestra el tipo de archivo (texto, binario, etc.)

`find . -type f -size <tamaño>` — Busca archivos por tamaño


### CONSEJOS

Verifica siempre el tipo de archivo con `file` antes de leerlo, para asegurarte de que es legible.

Usa `find` para localizar archivos con características específicas, como tamaño o tipo.
 
Guarda todas las contraseñas que encuentres, son necesarias para el siguiente nivel.




------------------------------------------------------------------------
EXPLICACIÓN DEL COMANDO FIND
find sirve para buscar archivos o carpetas dentro de un directorio y sus subdirectorios.
man find

Ejemplos simples

1. Buscar todos los archivos en el directorio actual:
```bash
find .     #Empieza la búsqueda de archivos en el directorio actual
```

2. Buscar archivos por nombre (-name):
```bash
find . -name "archivo.txt"   # Busca exactamente este archivo
find . -name "*.txt"         # Busca todos los .txt
```

3. Buscar solo archivos o solo carpetas (-type):
```bash
find . -type f   # solo archivos
find . -type d   # solo directorios
```

4. Buscar por tamaño (-size):
```bash
find . -size 33c
```

5. Combinar file con distintas flags:
```bash
find . -type f -exec file {} \; | grep "ASCII"
-type f: limita la búsqueda solo a archivos (no carpetas).
-exec file {} \;:
```
 exec para ejecutar un comando sobre cada archivo encontrado.

    file {} -> ejecuta file sobre cada archivo ({} representa el archivo actual).

    \; → marca el final del comando para -exec.

    -| grep "ASCII"

    | → tubería, pasa la salida del comando anterior al siguiente.


    grep "ASCII" → filtra solo las líneas que contengan la palabra "ASCII" (es decir, archivos legibles por humanos).
