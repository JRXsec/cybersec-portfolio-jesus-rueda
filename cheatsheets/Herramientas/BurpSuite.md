**Para qué sirve**
Interceptar, modificar, repetir y manipular peticiones HTTP. También sirve para fuzzing, pruebas de extensiones, análisis de parámetros y descubrir vulnerabilidades en aplicaciones web.

**Cuándo la uso**
En la fase de enumeración web y explotación, cuando quiero ver cómo funciona una petición, modificar parámetros, probar extensiones, fuzzear valores o automatizar ataques.

**Comandos básicos**
Proxy → Interceptar y modificar peticiones.
HTTP History → Ver todas las peticiones que ha hecho el navegador.
Repeater → Repetir una petición cambiando parámetros.
Decoder → Codificar y decodificar datos.

Primero debemos abrir Burpsuite y seleccionar un Target. Una vez lo tengamos ya podremos trabajar sobre él.

INTRUDER  
Podemos crear una wordlist en un .txt para que Burpsuite cambie todas las extensiones, por ejemplo php por php3, php2, php4...

Ahora abrimos la request en el intruder para probar extensiones.

Una vez tenemos la respuesta del servidor (habiendo subido un archivo cualquiera) cambiamos el parámetro:
filename = a filename = .\$php$  
para que pruebe con las extensiones que hemos puesto en el .txt.

El . va fuera de los \$ y la lista no lleva .
