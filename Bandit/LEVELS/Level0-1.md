# Bandit Level 0 → Level 1

En este nivel, debes conectarte al servidor remoto usando SSH y encontrar la contraseña del siguiente nivel.  
La contraseña está guardada en un archivo llamado `readme` ubicado en el directorio home del usuario.

## Información de conexión

- Usuario: `bandit0`  
- Host: `bandit.labs.overthewire.org`  
- Puerto: `2220`  
- Contraseña: `bandit0`

## Pasos para resolverlo

1. En la terminal del usuario anterior bandit0 hacer lo siguiente:
```bash
ls
```
Verás un archivo llamado readme.

Usa el comando cat para leer el contenido del archivo:
```bash
cat readme
```
El contenido es la contraseña para el siguiente nivel: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If


Anota esa contraseña para poder entrar al siguiente nivel:
Antes de escrbir este comando sal de la sesión de bandit 0 para acceder a bandit1: 
```bash
exit
ssh -p 2220 bandit1@bandit.labs.overthewire.org
```

Comandos útiles para este nivel

    ls — Listar archivos en el directorio actual

    cat — Mostrar contenido de un archivo

    ssh — Conectarse a un servidor remoto usando Secure Shell
    
    exit — Salir de la sesión ssh actual

### CONSEJOS

    Guarda siempre las contraseñas y los comandos que usas en un archivo de notas local.

    Las contraseñas pueden cambiar, así que mantener notas te ayuda a no perder progreso.


    Cada nivel se resuelve usando la contraseña del anterior y conectándote con SSH en el puerto 2220.
