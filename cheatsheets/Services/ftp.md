**Servicio**

FTP

**Puerto habitual**

21

**Qué es**

Protocolo para transferir archivos entre cliente y servidor. Permite subir, descargar y listar archivos. Suele aceptar el usuario Anonymous con permisos limitados (normalmente solo lectura).

**Riesgos habituales**

- Usuario Anonymous habilitado con acceso a archivos sensibles
- Credenciales enviadas en texto plano
- Permisos mal configurados en directorios
- Posibilidad de subir archivos ejecutables si el servidor está mal configurado
- Filtración de información por banners o listados

**Enumeración básica**

Conexión FTP normal por el puerto 21:
ftp IP

Conexión FTP usando hostname:
ftp hostname

Conexión por un puerto específico:
ftp IP PUERTO

Apunte: Anonymous suele ser un usuario común con solo permisos de lectura.
