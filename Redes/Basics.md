# Redes

En términos de tecnologías de la información, una red refiere a una colección de dispositivos interconectados como computadoras, servidores, impresoras y otro tipo de hardware que al vincularse comparten recursos, intercambian información y se comunican entre ellos. Estos, pueden estar conectados a través de un **switch**, un dispositivo de red que permite conectar múltiples dispositivos en un área corta (como una casa u oficina) entre si y compartir información.

A continuación, veremos un ejemplo de como funciona el switch:

<div id="switchExample" align="center"><img src="img\switchexample.png"/></div>

Si el device 1 intenta enviar una imagen al device 3, puede hacerlo primero enviando la imagen hacia el switch y luego el switch reenviará la imagen al device 3. El switch interpretará que la intención del device 1 fue enviarsela al tercero via una dirección que llamaremos **Mac Address**, una identificación única asignada a un dispositivo por su fabricante en orden de permitirle al dispositivo poder conectarse a una red. El Mac Address puede encontrarse en el hardware o accediendo vía software a las especificaciones del producto (en el caso de un smartphone, navegando hacia la pestaña de propiedades por dentro de las opciones del sistema). 

Ejemplos de MAC Address:

<div id="badges" align="center">
  <img src="img\macaddress1.png" width="100"/>
  <img src="img\macaddress2.png" width="100"/>
</div>

En este escenario, acabamos de recrear una red de tipo **LAN** (Local Area Network), que está conformada por un grupo de dispositivos conectados de manera local en un area pequeña. ¿Pero que pasaría si dos redes de tipo LAN intentan consultarse entre ellas?. A continuación, adjunto un ejemplo:




