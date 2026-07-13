
BURP SUIT

- **Proxy** → Interceptar y modificar peticiones.
- **HTTP History** → Ver todas las peticiones que ha hecho el navegador.
- **Repeater** → Repetir una petición cambiando parámetros.
- **Decoder** → Codificar y decodificar datos.



Primero debemos de abrir burpsuit y seleccionar un "Target" una vez lo tengamos ya podremos trabajar sobre el.


INTRUDER
Podemos crear una wordlist en un .txt para que burpsuit cambie todas las extensiones por ejemplo php por php3, php2, php4...

Ahora abrimos la request en el intruder para probar extensiones

una vez tenemos la respuesta del servidor (habiendo subido un archivo cualquiera) cambiamos el parámetro ==filename = a filename = .\$php$==  para que pruebe con las extensiones que hemos puesto en el .txt .

EL . VA FUERA DE LOS \$ Y LA LISTA NO LLEVA .  
