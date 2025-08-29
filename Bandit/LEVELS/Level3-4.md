#  Bandit Level 3 → Level 4 (Inhere Folder)

## 🎯 Objetivo:
En este nivel, debes encontrar y leer un archivo oculto dentro del directorio `inhere`.  
El archivo tiene un nombre que comienza con puntos (`...`) y no aparece con un listado normal.

## Información de conexión
- **Usuario:** `bandit3`  
- **Host:** `bandit.labs.overthewire.org`  
- **Puerto:** `2220`  
- **Contraseña:** _(usa la que obtuviste del nivel anterior)_

## Pasos para resolverlo

1. Lista todos los archivos, incluidos los ocultos, con el comando:

   ```bash
   ls -a

 . (punto simple) representa el directorio actual donde estás ubicado.
.. (punto doble) representa el directorio padre o superior, es decir, el directorio que contiene al actual.

Verás archivos o carpetas especiales, como ...Hiding-From-You.

    Para leer el contenido de ese archivo, usa:

    cat ...Hiding-From-You

    El contenido del archivo contiene la contraseña para el siguiente nivel: 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

    Guárdala para usarla luego.

Comandos útiles

    ls -a — Lista todos los archivos, incluyendo los ocultos (los que empiezan con .).

    cat <archivo> — Muestra el contenido de un archivo.

    exit (Ctl+D o Ctl+C) — Salir de la sesión SSH

    **Flags basicas de ls (para conocer todo usar man -ls):
    Las letras vienen de palabras descriptivas en inglés:
    Letra	Significado
    a	all (todos)
    l	long (largo)
    h	human-readable (legible para humanos)
    r	reverse (invertir orden)
    t	time (ordenar por fecha)
    R	recursive (recursivo, en subdirectorios)

Consejos

    Los archivos que comienzan con . o más puntos son ocultos y no se ven con ls normal.

    Usa siempre ls -a para encontrar estos archivos secretos.

    Guarda las contraseñas que encuentres para no perder progreso.

    **Saber usar ls, cd y cat y entender como localizar ficheros ocultos en un directorio**