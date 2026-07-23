# Windows Enumeration

# Metodología

1. Identificar el sistema operativo.
**Saber versión, arquitectura y edición.**

2. Identificar el usuario actual.
**Permisos y privilegios del usuario.**

3. Enumerar usuarios y grupos.
**Descubrir cuentas y roles.**

4. Enumerar procesos.
**Detectar software vulnerable o extraño.**

5. Enumerar servicios.
**Servicios mal configurados o con permisos débiles.**

6. Enumerar tareas programadas.
**Ejecuciones automáticas explotables.**

7. Enumerar recursos compartidos.
**Shares accesibles con información sensible.**

8. Buscar credenciales.
**Archivos, configuraciones y texto plano.**

9. Enumerar permisos.
**ACLs débiles en carpetas y archivos.**

10. Documentar hallazgos.
**Registrar todo para reproducibilidad.**

---

# Información del sistema

## Versión de Windows

systeminfo  
**Información completa del sistema.**

ver  
**Versión básica de Windows.**

wmic os get Caption,Version,OSArchitecture  
**Nombre, versión y arquitectura.**

---

## Hostname

hostname  
**Nombre del equipo.**

---

## Usuario actual

whoami  
**Usuario actual.**

whoami /all  
**Información completa del usuario.**

whoami /priv  
**Privilegios del usuario.**

whoami /groups  
**Grupos del usuario.**

---

# Usuarios

## Usuarios locales

net user  
**Lista de usuarios locales.**

---

## Información de un usuario

net user USERNAME  
**Detalles del usuario.**

---

## Grupos locales

net localgroup  
**Lista de grupos locales.**

---

## Miembros de un grupo

net localgroup Administrators  
**Miembros del grupo Administrators.**

---

# Red

## Configuración IP

ipconfig /all  
**Interfaces, DNS, DHCP, MAC.**

---

## Rutas

route print  
**Tabla de rutas.**

---

## Conexiones

netstat -ano  
**Conexiones activas con PID.**

---

## Puertos

netstat -an  
**Puertos abiertos.**

---

# Procesos

tasklist  
**Procesos en ejecución.**

---

# Servicios

sc query  
**Servicios instalados.**

tasklist /svc  
**Procesos asociados a servicios.**

---

# Tareas Programadas

schtasks  
**Tareas programadas del sistema.**

---

# Recursos Compartidos

net share  
**Shares disponibles.**

---

# Variables de Entorno

set  
**Variables del sistema.**

---

# Unidades

wmic logicaldisk get caption,description  
**Unidades y tipo.**

---

# Permisos

## Carpetas

icacls C:\Path  
**Permisos de la carpeta.**

---

# Búsqueda de Archivos

## Configuración

dir /s /b *.config  
**Buscar archivos .config.**

---

## Archivos de texto

dir /s /b *.txt  
**Buscar archivos .txt.**

---

## Archivos XML

dir /s /b *.xml  
**Buscar archivos .xml.**

---

## Archivos INI

dir /s /b *.ini  
**Buscar archivos .ini.**

---

# Información de Red

## ARP

arp -a  
**Tabla ARP.**

---

## DNS

ipconfig /displaydns  
**Cache DNS.**

---

# PowerShell

## Versión

$PSVersionTable  
**Versión de PowerShell.**

---

## Procesos

Get-Process  
**Procesos activos.**

---

## Servicios

Get-Service  
**Servicios activos.**

---

## Usuarios

Get-LocalUser  
**Usuarios locales.**

---

## Grupos

Get-LocalGroup  
**Grupos locales.**

---

# Herramientas

winPEAS  
**Enumeración automática.**

Seatbelt  
**Auditoría de seguridad.**

PowerUp  
**PrivEsc en PowerShell.**

Sysinternals Suite  
**Herramientas avanzadas de análisis.**

---

# Archivos interesantes

unattended.xml  
**Credenciales en texto plano.**

sysprep.xml  
**Configuraciones sensibles.**

web.config  
**Credenciales de aplicaciones web.**

applicationHost.config  
**Configuración de IIS.**

hosts  
**Resoluciones locales.**

SAM  
**Hashes de usuarios.**

SYSTEM  
**Claves del sistema.**

SOFTWARE  
**Configuraciones y claves.**

---

# Recursos

LOLBAS  
**Binarios nativos explotables.**

Microsoft Learn  
**Documentación oficial.**

Hack The Box Academy  
**Laboratorios prácticos.**

TryHackMe  
**Máquinas de entrenamiento.**

winPEAS  
**Enumeración automática.**

---



