**Para qué sirve**
Sirve para escanear puertos, servicios, versiones y vulnerabilidades de un host. Es la herramienta principal de enumeración en cualquier auditoría o CTF.

**Cuándo la uso**
En la fase de enumeración inicial, para descubrir qué servicios están expuestos y qué vectores de ataque pueden existir.

**Comandos básicos**
Nmap S4vitar:
nmap -p- --open -T5 -v -oG allPorts ipHost -n

Nmap completo:
nmap -sV 10.130.143.112

Escaneo rápido de los 100 puertos más comunes:
sudo nmap -F -T5 <OBJETIVO>

Escaneo completo de todos los puertos:
sudo nmap -p- -T4 10.129.89.226

Ver la versión de un servicio en un puerto:
nmap -p 8009 -sV --version-intensity 9 <target-ip>

Comando simplificado para ver el servicio de un puerto:
nmap -sV -p3333 IP

Ver requisitos de autenticación de un servicio:
nmap -p 8009 --script ajp-auth <target-ip>
