# Bandit Level 8 → Level 9

## 🎯 Objetivo

En este nivel, debes encontrar la contraseña para el siguiente nivel se almacena en el archivo data.txt y es la única línea de texto que aparece solo una vez.


Este archivo contiene la contraseña para el siguiente nivel.

---
## Información de conexión

* **Usuario:** `bandit8`
* **Host:** `bandit.labs.overthewire.org`
* **Puerto:** `2220`
* **Contraseña:** *(usa la que obtuviste del nivel anterior)*

## Pasos para resolverlo

1️. Lista los archivos de tu directorio
```bash
ls
```

Podemos ver que solo tenemos el archivo data.txt en está máquina igual que antes 
.Vamos a ver el contenido del archivo para ver como está organizado:
```bash
cat data.txt
```
Vemos que es un archivo enorme con la siguiente estructura:
6h97TdcdpF2BJ2UKR8i9qsBrgGLmpTWO
gaFB2nTNG3cAodJSjsX7eKKE47CMramZ
joK9jsQZ5WecQwqLCYowTNOCHvBOKb0s
ARtGzJPICthTWu7pM4YWs4U4lDwruYBd
8N7a4ktvymA5lA7zynTwLQHelyy0I9BY
N6gK0tSzJg9HnkYfzJeR4hJFTPfs3w0X
flwlLshw1mbZtTzqFrv2VYfLySltkMxY
bpy71E9arX47Em0S85w7DpcKqS1BMdZT
YoxyBMpsIWJ45bCQkxvwNRlZK1Q6Zrjv
q2ptuUrdRrv6xRzTZ0ir3SefGwx52lYw
YoxyBMpsIWJ45bCQkxvwNRlZK1Q6Zrjv
0ZdojRHKYMZ2HH75mmFbUIBR8K8DRJTx

Eset archivo contiene muchas líneas, casi todas repetidas. La contraseña es la única línea que aparece solo una vez.



2️. Ordenar el archivo y mostrar las líneas no repetidas (sort y uniq)


```bash
sort data.txt | uniq -u
```

Esto lo que hace es lo siguiente:
    -sort: ordena las líneas
    -| (tubería): la tubería conecta la salida de un comando con la entrada de otro
    -uniq -u: recibe las líneas ordenadas y filtra solo las únicas.

Obtenemos lo siguiente:
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM


Esta es la contraseña para el siguiente nivel: dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc

 Esta es la **contraseña del Level 9**.

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
    No abras el archivo entero con cat

    Primero ordena

    Después filtra

    Si dudas, cuenta repeticiones (sort data.txt | uniq -c)

    Pipes (|) son la clave
    Recuerda que | conecta un comando con otro (salida → entrada). Aquí lo usas para no tener que guardar resultados intermedios.
