# Bandit Level 10 → Level 11

## 🎯 Objetivo

La contraseña para el siguiente nivel se almacena en el archivo data.txt, donde todas las letras minúsculas (a-z) y mayúsculas (A-Z) se han rotado 13 posiciones.

**Esto se llama cifrado ROT13**

Ejemplo:
a → n
b → o
c → p
…
n → a
o → b

Lo mismo con mayúsculas



Este archivo contiene la contraseña para el siguiente nivel.

---
## Información de conexión

* **Usuario:** `bandit10`
* **Host:** `bandit.labs.overthewire.org`
* **Puerto:** `2220`
* **Contraseña:** *(usa la que obtuviste del nivel anterior)*

## Pasos para resolverlo

1️. Lista los archivos de tu directorio y acceder a ellos
```bash
ls
```
Podemos ver que solo está el archivo data.txt al igual que los anteriores.

Vamos a ver que hay en data.txt
```bash
cat data.txt
```

Podemos ver lo siguiente:
VGhlIHBhc3N3b3JkIGlzIGR0UjE3M2ZaS2IwUlJzREZTR3NnMlJXbnBOVmozcVJyCg==


Las letras, números y los == al final no se parecen a un texto normal.

Eso es una señal de que está codificado en Base64. Base64 convierte cualquier dato (texto o binario) en un formato de letras y números seguro para texto.

Por qué no ROT13:

ROT13 solo cambia letras (a → n, b → o, etc.).

Si aplicáramos ROT13 a esto, seguirá siendo ilegible, porque Base64 no está cifrado con ROT13.



2️. Decodificar en base 64
```bash
base64 -d data.txt
```

Esta es la salida:

The password is dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

Base64 es una forma de convertir datos en letras y números, para que puedan pasarse fácilmente por Internet o guardarse en un archivo de texto.

Por ejemplo, si tienes algo raro como imágenes, contraseñas, o texto cifrado, Base64 lo convierte en algo que solo contiene A-Z, a-z, 0-9, +, / y a veces = al final.


Obtenemos lo siguiente: dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr


Esta es la **contraseña del Level 11**.

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
    -d → decodifica (convierte de Base64 a texto normal).

    -i → ignora caracteres que no son válidos (opcional).

    -w NUM → establece el ancho de línea al codificar (opcional).

`tr <a-z> <A-Z>` — traduce o reemplaza caracteres (por ejemplo, pasar de minúsculas a mayúsculas).

`tar -xf <archivo.tar>` — empaqueta o desempaqueta archivos (muy usado junto con compresión).

`gzip <archivo>` — comprime archivos en formato .gz (con gunzip los descomprime).

`bzip2 <archivo>` — comprime archivos en formato .bz2 (con bunzip2 los descomprime).

`xxd <archivo>` — muestra un volcado hexadecimal (hex dump) del archivo, o lo convierte de hex a binario.
 


### CONSEJOS
   - Identifica el tipo de codificación/cifrado

   - Usa los comandos adecuados

   - Visualiza el contenido antes de actuar

   - No ignores las pistas del enunciado

   - Practica la lógica paso a paso

        1.Mira el archivo.

        2.Intenta reconocer el formato.

        3.Aplica el comando correcto.

        4.Obtén la contraseña y prueba.