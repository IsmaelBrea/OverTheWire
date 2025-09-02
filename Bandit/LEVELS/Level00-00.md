# Bandit Nivel 0 

## 🎯 Objetivo:
Conectarse al servidor remoto por SSH y encontrar la contraseña para el siguiente nivel leyendo un archivo llamado `readme`.

---

## Información de conexión

- **Usuario:** `bandit0`
- **Host:** `bandit.labs.overthewire.org`
- **Puerto:** `2220`
- **Contraseña siguiente nivel:** `bandit0`
---

## Pasos para resolverlo

```bash
ssh -p 2220 bandit0@bandit.labs.overthewire.org
```

Nos conectamos al host de bandit0 en el puerto 2220

### CONSEJOS
Para ver todas las flags de un comando usar:
```bass```
man -comando

**Saber usa el comando SSH y man para saber que hace cada comando y que flags tiene**
