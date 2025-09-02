# Bandit Level 2 → Level 3

## 🎯 Objetivo:
En este nivel, debes encontrar la contraseña del siguiente nivel dentro de un archivo llamado `spaces in this filename` que se encuentra en el directorio personal (`home`) del usuario.

---
## Información de conexión

- **Usuario:** `bandit2`  
- **Host:** `bandit.labs.overthewire.org`  
- **Puerto:** `2220`  
- **Contraseña:** _(usa la que obtuviste del nivel anterior)_

## Pasos para resolverlo

1. Conéctate al servidor con el usuario `bandit2`:

```bash
ssh -p 2220 bandit2@bandit.labs.overthewire.org
 ```

 Lista los archivos del directorio:
 ```bash
ls
 ```

Verás un archivo con espacios en su nombre: spaces in this filename.

Para leer archivos con espacios en el nombre, tienes dos opciones:

Opción A (escapando los espacios con \):
 ```bash
cat -- '--spaces in this filename--'      */El -- le dice a cat "a partir de aquí, todo es nombre de archivo, no opciones" */
 ```


Opción B (usando comillas):
 ```bash
cat "spaces in this filename"
 ```
El contenido del archivo es la contraseña del siguiente nivel: MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

Sal de la sesión actual para conectar como bandit3:

 ```bash
exit
 ```

Luego conéctate al siguiente nivel:
 ```bash
    ssh -p 2220 bandit3@bandit.labs.overthewire.org
 ```


## Comandos útiles

 `ls`— Lista archivos

  `cat ` — Muestra el contenido de un archivo

   `ssh ` — Conexión remota

   `exit` (Ctl+D o Ctl+C) — Salir de la sesión SSH

### CONSEJOS

    Los nombres de archivo con espacios deben ir entre comillas o escapando cada espacio.

    Sigue guardando las contraseñas y comandos en tu archivo de notas local.

    Recuerda siempre usar el puerto 2220 al usar SSH.

    **Usar comillas ("") para leer un archivo que empieza por --**

