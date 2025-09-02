# Bandit Level 1 → Level 2


## 🎯 Objetivo:
En este nivel, debes encontrar la contraseña del siguiente nivel dentro de un archivo especial llamado `-`, que se encuentra en el directorio personal (`home`) del usuario.

---
## Información de conexión

- **Usuario:** `bandit1`  
- **Host:** `bandit.labs.overthewire.org`  
- **Puerto:** `2220`  
- **Contraseña:** _(usa la que obtuviste del nivel anterior)_

## Pasos para resolverlo

1. Conéctate al servidor con el usuario `bandit1`:

```bash
ssh -p 2220 bandit1@bandit.labs.overthewire.org
 ```

 Una vez dentro, lista los archivos del directorio:
```bash
ls
```

Verás un archivo llamado -.

Este archivo no se puede leer con un simple cat - porque el guion - se interpreta como entrada estándar (stdin)

Para leerlo correctamente, usa:
```bash
cat ./-
```

Esto fuerza a cat a interpretar - como el nombre del archivo, no como un parámetro.

También se puede usar la ruta absoluta: cat /home/bandit1/-

El contenido del archivo es la contraseña del siguiente nivel: 263JGJPfgU6LtdEvgfWU1XP5yac29mFx

Sal de la sesión actual para conectar como bandit2:
```bash
exit
```

Luego conéctate al siguiente nivel:
```bash
ssh -p 2220 bandit2@bandit.labs.overthewire.org
```

## Comandos útiles

 `ls ` — Lista los archivos en el directorio actual

 `cat` — Muestra el contenido de un archivo

 `ssh ` — Conexión remota al servidor

 `exit ` — Salir de la sesión SSH actual

### CONSEJOS

    Guarda las contraseñas y comandos en un archivo de notas.

    El nombre - se interpreta como entrada estándar, por eso usamos ./- para evitar confusión.

    Siempre usa el puerto 2220 al conectarte con SSH.



    **Saber usar los comandos ls, cd, cat y saber que se usa ./ para evitar confusiones en los nombres cuando empiezan por - ya que se entienden que son flags al empezar por -**