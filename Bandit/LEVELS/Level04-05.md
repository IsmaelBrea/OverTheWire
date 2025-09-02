# Bandit Level 4 → Level 5 (Inhere Folder y Único Archivo Legible)

## 🎯 Objetivo:
Encontrar el único archivo **legible por humanos** dentro del directorio `inhere` y obtener la contraseña.

---
## Información de conexión
- **Usuario:** `bandit4`  
- **Host:** `bandit.labs.overthewire.org`  
- **Puerto:** `2220`  
- **Contraseña:** _(usa la que obtuviste del nivel anterior)_

## Pasos para resolverlo
1. Entra en el directorio:
```bash
cd inhere
```
   
Lista los archivos:
```bash
ls
```

Usa file para identificar cuál es legible:
```bash
file ./*
```
   
Los archivos binarios aparecerán como data u otros tipos.

El único que diga ASCII text es el correcto.
```bash
./-file00: Non-ISO extended-ASCII text, with no line terminators, with overstriking
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
```

Lee el archivo con:
```bash
    cat ./-file07
```
   
Obtendrás la contraseña para el siguiente nivel: 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw


## Comandos útiles:

 `ls ` — lista archivos.

 `cd <dir>` — cambia de directorio.

   `file <archivo>` — muestra el tipo de archivo.

   `cat <archivo>` — muestra el contenido de un archivo.

   `reset` — reinicia la terminal si se rompe la vista.

### CONSEJOS

    ./* se usa porque los archivos empiezan con -, y así evitas que se interpreten como opciones.

    Solo uno de los archivos es texto legible, el resto son datos binarios.

    Guarda la contraseña para el siguiente nivel.


**Saber usar ls, cd, cat y file (que sirve para identificar los tipos legibles de los archivos en un directorio)**