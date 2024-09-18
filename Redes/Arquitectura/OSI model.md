# Modelo OSI

El modelo de interconexión de sistemas abiertos (ISO/IEC 7498-1), conocido como “modelo OSI”, (en inglés, Open Systems Interconnection) es un modelo de referencia para los protocolos de la red (no es una arquitectura de red), creado en el año 1980 por la Organización Internacional de Normalización. Se usa en la enseñanza como una manera de mostrar cómo puede estructurarse una «pila» de protocolos de comunicaciones

Debe recordarse siempre que es un modelo, una construcción teórica, por ende no tiene un correlato directo con el mundo real. Se trata de una normativa estandarizada útil debido a la existencia de muchas tecnologías, fabricantes y compañías dentro del mundo de las comunicaciones, y al estar en continua expansión, se tuvo que crear un método para que todos pudieran entenderse de algún modo, incluso cuando las tecnologías no coincidieran.

<img src="https://static.platzi.com/media/user_upload/Captura%20de%20Pantalla%202022-01-26%20a%20la%28s%29%207.18.25%20p.m.-c9668c1c-6cea-4114-a78f-a37d97f00bea.jpg" alt="OSI model"/>

El modelo OSI, está dividido en siete capas:
    - I -Física: Infraestructura física que transporta datos (hardware)
    - II - Link: Responsable de que los paquetes enviados por los dispositivos físicos se redirijan correctamente.
    - III -Red: Capa que envía los paquetes a través de una red
    - IV - Transporte: Los datos son redirigidos a un servicio capaz de manejar solicitudes.
    - V - Sesión: Capa capaz de mantener conexiones (software)
    - VI - Presentación: Capa que asegura que los datos estén en un formato utilizable
    - VII - Aplicación: Capa en la que los humanos procesan datos e información.

A continuación, recorreremos en profundidad cada una de las capas anteriormente nombradas.

<img src="img\osiwiki.png">

### Capa I: Fisica

La capa 1 representa la señal que permite a los bits y bytes transferir entre medios físicos.

Protocolos:
- Capa física de Ethernet
- Celular bluetooth

### Capa II: Link

La capa 2 es responsable de pasar datos físicos a lógicos.

Protocolos:
- Ethernet: Al conectar el cable físico, conectando redes.
- WiFi: Para acceder a redes via señales de radio. Utiliza protocolos llamados IEE 802.11

### Capa III: Red

La capa 3 es responsable de enrutar los paquetes entre redes vía routers.

Protocolos:
- IP: (Internet Protocol) utilizada todos los días para acceder a internet.
- ICMP: (Internet Control Message Protocol) utilizado por los dispositivos en red para diagnosticar las conexiones o para los dispositivos a fin de enviar y responder condiciones de error.
- IPSEC: (Internet Protocol Security) Permite comunicaciones encriptadas y seguras entre dos dispositivos en red.

### CAPA IV: Transporte

La capa 4 permite a las aplicaciones reproducirse en la red.

Protocolos:
- TCP: (Transmission control protocol): Asegura estabilidad y control de cuantos datos serán enviados en cualquier momento.
- UDP: (User Datagram Protocol): Permite el envío de datagramas de forma rápida en redes IP sin establecer previamente una conexión.

### CAPA V: Sesión

La capa 5 maneja las conexiones entre la aplicación y las capas por debajo. Incluye establecimiento, mantenimiento y terminación de conexiones, referidos como sesiones.

Protocolos:
- Socks: Protocolo para enviar paquetes por un servidor proxy.
- Netbios: Protocolo antiguo de windows para establecer sesiones y resolver nombres.

###  CAPA VI: Capa de presentación

La capa 6 es responsable de adaptar, transformar y traducir los datos. Permite que la capa de aplicación y las demás capas pueden entenderse entre ellas. Al mismo tiempo protege las capas de transporte.

Protocolos:
- ASCII, UTF

### CAPA VII: Aplicacion

La capa 7 se encarga de la lógica de negocio y la funcionalidad de la aplicación. Todo lo que el usuario interacciona por dentro de los servicios que recorren la aplicación. La mayoría de los desarrolladores crean aplicaciones en esta capa.

Protocolos:

- HTTP: (Hypertext transfer protocol) - Permite que accedamos a las aplicaciones web.
- FTP: (File transfer protocol) - Permite a los usuarios transferir archivos.
- SNMP(Simple network management protocol) - Protocolo para leer y actualizar configuraciones de los dispositivos en red.


## Fuentes
- <a href="https://www.w3schools.com/cybersecurity/cybersecurity_networking.php" target="_blank">W3SCHOOLS</a>
