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

REPEATER

Repeater sirve para repetir una petición HTTP y modificarla manualmente todas las veces que quieras. Cambias parámetros, headers, cookies o el body y ves cómo responde el servidor. Es perfecto para probar payloads, validar vulnerabilidades, hacer bypasses y entender el comportamiento exacto de una request.

Lo uso cuando quiero manipular una petición sin depender del navegador: envío la request al Repeater, edito lo que me interesa (parámetros, tokens, valores), la reenvío y comparo respuestas para ver si hay cambios, errores o comportamientos vulnerables.


Una vez tenemos la respuesta del servidor (habiendo subido un archivo cualquiera) cambiamos el parámetro:
filename = a filename = .\$php$  
para que pruebe con las extensiones que hemos puesto en el .txt.

El . va fuera de los \$ y la lista no lleva .
