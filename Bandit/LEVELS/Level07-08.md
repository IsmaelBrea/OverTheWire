# Bandit Level 7 → Level 8

## 🎯 Objetivo

En este nivel, debes encontrar la contraseña que se encuentra e dentro del archivo data.txt y que va seguido de la palabra millionth.

Este archivo contiene la contraseña para el siguiente nivel.

---
## Información de conexión

* **Usuario:** `bandit6`
* **Host:** `bandit.labs.overthewire.org`
* **Puerto:** `2220`
* **Contraseña:** *(usa la que obtuviste del nivel anterior)*

## Pasos para resolverlo

1️. Lista los archivos de tu directorio
```bash
ls
```

Podemos ver que solo tenemos el archivo data.txt en está máquina.Vamos a ver el contenido del archivo para ver como está organizado:
```bash
cat data.txt
```
Vemos que es un archivo enorme con la siguiente estructura:
particles       KAYXCo1eFgPFI1pZ5onMz1UehMbIKfgb
necessary       RSqyZKAQN8QGRlNHRYV6kPOpUvXe58y4
revealing       GPnzz469Ec2fmsPAT2WbFrDQrVJP33XT
complying       H34Pvu5GS596OxyPokMIbiURYQNtIHD2
sparkles        7xGCE2O5LdFMazSPOkzxZESfWCQMwHW0


palabra -> contraseña

Buscar la palabra manualmente sería muy costoso e ineficiente.

Por tanto tendremos que filtrar una búsqueda de millionth en el archivo data.txt


2️. Filtrar con grep
Usamos gre para filtrar una palabra en un archivo:
```bash
grep "millionth" data.txt
```

Obtenemos lo siguiente:
millionth       dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc


Esta es la contraseña para el siguiente nivel: dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc

 Esta es la **contraseña del Level 8**.

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

`strings <archivo>` — extrae cadenas de texto legibles de archivos binarios o ejecutables.

`base64 <archivo>` — codifica o decodifica datos en formato Base64.

`tr <a-z> <A-Z>` — traduce o reemplaza caracteres (por ejemplo, pasar de minúsculas a mayúsculas).

`tar -xf <archivo.tar>` — empaqueta o desempaqueta archivos (muy usado junto con compresión).

`gzip <archivo>` — comprime archivos en formato .gz (con gunzip los descomprime).

`bzip2 <archivo>` — comprime archivos en formato .bz2 (con bunzip2 los descomprime).

`xxd <archivo>` — muestra un volcado hexadecimal (hex dump) del archivo, o lo convierte de hex a binario.
 


### CONSEJOS
    No abras el archivo entero con cat

    Usa grep para localizar rápido

    Aunque en el nivel aparezcan otros comandos, lo más sencillo es usar grep. Los comandos que aparecen en el nivel son útiles para próximos niveles.