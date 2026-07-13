````md
# 🪟 Windows Enumeration

# Metodología

1. Identificar el sistema operativo.
2. Identificar el usuario actual.
3. Enumerar usuarios y grupos.
4. Enumerar procesos.
5. Enumerar servicios.
6. Enumerar tareas programadas.
7. Enumerar recursos compartidos.
8. Buscar credenciales.
9. Enumerar permisos.
10. Documentar todos los hallazgos.

---

# Información del sistema

## Versión de Windows

```cmd
systeminfo
```

```cmd
ver
```

```cmd
wmic os get Caption,Version,OSArchitecture
```

---

## Hostname

```cmd
hostname
```

---

## Usuario actual

```cmd
whoami
```

```cmd
whoami /all
```

```cmd
whoami /priv
```

```cmd
whoami /groups
```

---

# Usuarios

## Usuarios locales

```cmd
net user
```

---

## Información de un usuario

```cmd
net user USERNAME
```

---

## Grupos locales

```cmd
net localgroup
```

---

## Miembros de un grupo

```cmd
net localgroup Administrators
```

---

# Red

## Configuración IP

```cmd
ipconfig /all
```

---

## Rutas

```cmd
route print
```

---

## Conexiones

```cmd
netstat -ano
```

---

## Puertos

```cmd
netstat -an
```

---

# Procesos

```cmd
tasklist
```

---

## Servicios

```cmd
sc query
```

```cmd
tasklist /svc
```

---

# Tareas Programadas

```cmd
schtasks
```

---

# Recursos Compartidos

```cmd
net share
```

---

# Variables de Entorno

```cmd
set
```

---

# Unidades

```cmd
wmic logicaldisk get caption,description
```

---

# Permisos

## Carpetas

```cmd
icacls C:\Path
```

---

# Búsqueda de Archivos

## Configuración

```cmd
dir /s /b *.config
```

---

## Archivos de texto

```cmd
dir /s /b *.txt
```

---

## Archivos XML

```cmd
dir /s /b *.xml
```

---

## Archivos INI

```cmd
dir /s /b *.ini
```

---

# Información de Red

## ARP

```cmd
arp -a
```

---

## DNS

```cmd
ipconfig /displaydns
```

---

# PowerShell

## Versión

```powershell
$PSVersionTable
```

---

## Procesos

```powershell
Get-Process
```

---

## Servicios

```powershell
Get-Service
```

---

## Usuarios

```powershell
Get-LocalUser
```

---

## Grupos

```powershell
Get-LocalGroup
```

---

# Herramientas

- winPEAS
- Seatbelt
- PowerUp
- Sysinternals Suite

---


# Archivos interesantes

- unattended.xml
- sysprep.xml
- web.config
- applicationHost.config
- hosts
- SAM
- SYSTEM
- SOFTWARE

---

# Recursos

- LOLBAS
- Microsoft Learn
- Hack The Box Academy
- TryHackMe
- winPEAS

---

# Notas

Añadir observaciones, comandos útiles y técnicas aprendidas durante laboratorios y máquinas.
````
