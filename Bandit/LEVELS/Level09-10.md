# Bandit Level 9 → Level 10

## 🎯 Objetivo

La contraseña para el siguiente nivel se almacena en el archivo data.txt en una de las pocas cadenas legibles por humanos, precedida por varios caracteres ‘=’.


Este archivo contiene la contraseña para el siguiente nivel.

---
## Información de conexión

* **Usuario:** `bandit9`
* **Host:** `bandit.labs.overthewire.org`
* **Puerto:** `2220`
* **Contraseña:** *(usa la que obtuviste del nivel anterior)*

## Pasos para resolverlo

1️. Lista los archivos de tu directorio
```bash
ls
```
Podemos ver que solo está el archivo data.txt al igual que los anteriores.


2️. Filtrar por caracteres legibles (strings) y filtrar el resultado con grep por  ==

```bash
strings data.txt | grep "==="
```

Esto lo que hace es lo siguiente:
    -strings data.txt: extrae solo los caracteres legibles por humanos de data.txt
    -| (tubería): la tubería conecta la salida de un comando con la entrada de otro
    -grep "===":Filtra las líneas que contienen tres o más signos = consecutivos.

Esta es la contraseña para el siguiente nivel: FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey


 Esta es la **contraseña del Level 10**.

## Comandos útiles

`ls` — lista archivos en un directorio

`cd <directorio>` — cambiar de carpeta

`cat <archivo>` — mostrar contenido de un archivo

`file <archivo>` — ver tipo de archivo

`find / -user <usuario> -group <grupo> -size <tamaño>` — buscar archivos según propietario, grupo y tamaño

 `grep` — filtrar salidas por patrones de texto

 **Comandos que recomienda la página para este nivel:**
 `man <comando>` — abre el manual de ayuda de un comando en Linux (explica qué hace y cómo usarlo).

`grep <patrón> <archivo>` — busca líneas que contengan el texto o expresión regular indicada.

`sort <archivo>` — ordena las líneas de un archivo (alfabéticamente, numéricamente, etc.).

`uniq <archivo>` — elimina líneas duplicadas consecutivas (suele usarse junto con sort).
        uniq -c → muestra cuántas veces aparece cada línea.

        uniq -u → muestra solo las líneas que aparecen una vez.

        uniq -d → muestra solo las líneas que aparecen más de una vez.

`strings <archivo>` — extrae cadenas de texto legibles de archivos binarios o ejecutables.

`base64 <archivo>` — codifica o decodifica datos en formato Base64.

`tr <a-z> <A-Z>` — traduce o reemplaza caracteres (por ejemplo, pasar de minúsculas a mayúsculas).

`tar -xf <archivo.tar>` — empaqueta o desempaqueta archivos (muy usado junto con compresión).

`gzip <archivo>` — comprime archivos en formato .gz (con gunzip los descomprime).

`bzip2 <archivo>` — comprime archivos en formato .bz2 (con bunzip2 los descomprime).

`xxd <archivo>` — muestra un volcado hexadecimal (hex dump) del archivo, o lo convierte de hex a binario.
 


### CONSEJOS
