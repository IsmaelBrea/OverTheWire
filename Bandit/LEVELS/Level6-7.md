# Bandit Level 6 → Level 7

## 🎯 Objetivo

En este nivel, debes encontrar un archivo en el servidor que cumpla las siguientes condiciones:

* Propietario: usuario **bandit7**
* Grupo: **bandit6**
* Tamaño exacto: **33 bytes**

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
ls -la
```

Salida típica:
```bash
total 20
drwxr-xr-x   2 root root 4096 Aug 15 13:15 .
drwxr-xr-x 150 root root 4096 Aug 15 13:18 ..
-rw-r--r--   1 root root  220 Mar 31  2024 .bash_logout
-rw-r--r--   1 root root 3851 Aug 15 13:09 .bashrc
-rw-r--r--   1 root root  807 Mar 31  2024 .profile
```

No verás la contraseña aquí, ya que está en otra parte del sistema.

2️. Buscar archivos por propietario y grupo
```bash
find / -user bandit7 -group bandit6 2>/dev/null
```
find / → busca desde la raíz del sistema (todas las carpetas).

  -user bandit7 → solo archivos propiedad del usuario bandit7.
  
  -group bandit6 → solo archivos cuyo grupo es bandit6.
  
  2>/dev/null → oculta los errores de “permiso denegado”.

Salida esperada:
```bash
/var/lib/dpkg/info/bandit7.password
```

3️. Mostrar el contenido del archivo para obtener la contraseña
```bash
cat /var/lib/dpkg/info/bandit7.password
```

 Obtendrás la contraseña para el siguiente nivel: morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

 Esta es la **contraseña del Level 7**.

## Comandos útiles

`ls` — lista archivos en un directorio
`cd <directorio>` — cambiar de carpeta
`cat <archivo>` — mostrar contenido de un archivo
`file <archivo>` — ver tipo de archivo
`find / -user <usuario> -group <grupo> -size <tamaño>` — buscar archivos según propietario, grupo y tamaño
 `grep` — filtrar salidas por patrones de texto


### CONSEJOS
     Siempre filtra los errores de permisos con `2>/dev/null`.
     
     Combina `find` con `-size` si necesitas archivos de un tamaño específico.
     
     La contraseña suele estar en un archivo pequeño y legible.

