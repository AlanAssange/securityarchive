# Redes

En términos de tecnologías de la información, una red refiere a una colección de dispositivos interconectados como computadoras, servidores, impresoras y otro tipo de hardware que al vincularse comparten recursos, intercambian información y se comunican entre ellos. Estos, pueden estar conectados a través de un **switch**, un dispositivo de red que permite conectar múltiples dispositivos en un área corta (como una casa u oficina) entre si y compartir información.

A continuación, veremos un ejemplo de como funciona el switch:

<div id="switchExample" align="center"><img src="img\switchexample.png"/></div>

Si el device 1 intenta enviar una imagen al device 3, puede hacerlo primero enviando la imagen hacia el switch y luego el switch reenviará la imagen al device 3. El switch interpretará que la intención del device 1 fue enviarsela al tercero via una dirección que llamaremos **Mac Address**, una identificación única asignada a un dispositivo por su fabricante en orden de permitirle al dispositivo poder conectarse a una red. El Mac Address puede encontrarse en el hardware o accediendo vía software a las especificaciones del producto (en el caso de un smartphone, navegando hacia la pestaña de propiedades por dentro de las opciones del sistema). 

Ejemplos de MAC Address:

<div id="badges" align="center">
  <img src="img\macaddress1.png" width="400"/>
  <img src="img\macaddress2.png" width="400"/>
</div>

*Cada vez que un sistema quiera comunicarse a una dirección IP que esté en una red LAN, utilizará un protocolo llamado ARP(Address Resolution Protocol) que permitirá saber que dirección MAC le pertenece a la dirección IP del dispositivo.*

En este escenario, acabamos de recrear una red de tipo **LAN** (Local Area Network), que está conformada por un grupo de dispositivos conectados de manera local en un area pequeña. ¿Pero que pasaría si dos redes de tipo LAN intentan consultarse entre ellas?. A continuación, adjunto un ejemplo:

<div id="routerExample" align="center"><img src="img\routerexample.png"/></div>

Supongamos que el device 3 de la primer red LAN intenta enviar una imagen al dispositivo 4 de la segunda red LAN. Para esto, necesitaríamos una conexión entre ambas redes, y ahí es donde entra en juego el **Router**; dispositivo capaz de conectar dos redes LAN entre si asignando una **dirección IP** a cada uno de los dispositivos en la red, lo que también permite el acceso a INTERNET. Los invito a imaginar internet como un complejo infinito de switches que conectan dispositivos dentro de la red LAN y routers que asignan IPs y conectan redes LAN.


### Pero como me conecto a internet?

Para ver la conexión a internet: utilizaremos el siguiente ejemplo:

<div id="interExample" align="center"><img src="img\internetexample.png"/></div>

Como vemos en este ejemplo, el switch conecta todos los dispositivos de la red de nuestra casa vía sus mac adresses, el router a su vez conecta todos los dispositivos hacia internet. Si quisiéramos ingresar a youtube a través de nuestro navegador o abrir la aplicación de youtube en nuestro smartphone, nuestro router nos conectaría a un servidor web de youtube garantizando el acceso hacia la paltaforma(que para graficar, podríamos interpretar como una computadora hosteando los servicios de YT para que los usuarios accedan).

En el caso de estar conectados a Wi-Fi, el router que brinda la conexión también integra en sus funcionalidades al switch y performa ambas funcionalidades a la vez.

### Protocolo DHCP

Anteriormente vimos que el router se encarga de asignar una dirección IP a cada uno de los dispositivos en la red LAN. Esto lo hace a través de un protocolo llamado **DHCP(Dynamic Host Configuration Protocol)**. Este se encarga de asignar automáticamente una dirección IP a los dispositivos en una red para identificarlos. Estas IP no son accesibles por fuera de la red o en internet y son básicamente privadas. Para poder navegar por internet, los dispositivos comparten una IP pública que es transmitida a través del router, quien asigna la misma IP pública a todos los dispositivos. Es por esto mismo que cuando buscamos nuestra ip a través del comando ipconfig en windows o en las opciones de nuestro smartphone observamos una ip diferente a la que podemos encontrar consultando nuestra ip vía google. Lo que vemos en google es nuestra ip pública del router y quien la provee es nuestro **ISP(Internet Service Provider)**. Todas las IP públicas de los routers son únicas y sin embargo se repiten en todos los dispositivos conectados a la red.

### DNS

Cuando buscamos una página web en nuestro navegador, nuestro navegador contacta primero a un DNS(Domain Name System) que convierte el dominio de la página web en una dirección IP única asociada al servidor web de la página a la que queremos ingresar. Puede ser configurado manualmente o por un servidor DHCP. A continuación, veremos un ejemplo visual:

<div id="dnsExample" align="center"><img src="img\dnsexample.png"/></div>

### NAT

Al enviar una solicitud hacia una página web, es decir, un request, primero pasará por el router y este estará encargado de transformar la ip privada del dispositivo en la ip pública compartida del router. Para realizar esta acción, utiliza un protocolo llamado **NAT(Network Adress Translation)**. Cuando la dirección IP sea convertida, el router verificará el mejor camino para cumplir la solicitud hacia el servidor de la página web a la que queremos ingresar y buscará un puerto específico que maneje requests de tipo HTTP.

### Puertos

## Créditos
- Las imágenes forman parte del siguiente <a href="https://www.youtube.com/watch?v=9rABOh8oT24" target="_blank">video</a> del canal de YT an0nali

