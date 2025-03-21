# LAN

Una red LAN (Local Area Network) es un grupo de computadoras u otros dispositivos interconectados dentro de un límite de espacio, como una oficina, escuela o inclusive una casa. Esta red facilita compartir recursos, datos y aplicaciones conectadas a los dispositivos. Pueden ser cableadas (ethernet) o inalámbricas (Wi-fi).

## Componentes de una LAN

- Workstations: Dispositivos como computadoras, laptops o smartphones conectados a una red.
- Servers: Computadoras que proveen recursos y servicios a las workstations
- Switches: Dispositivos de red que conectan workstations y servers, y distribuyen el tráfico de manera eficiente.
- Routers: Dispositivos que conectan la red LAN a internet u otras redes (ejemplo: red WAN)

## Seguridad de una red LAN

Como las redes LAN conectan múltiples dispositivos, también son un eje central de varias vulnerabilidades de seguridad. Implementar medidas de seguridad efectivas es vital para prevenir el acceso no autorizado, filtraciones de datos y malwares. Algunas de las mejores prácticas son las siguientes:

- Firewalls: Hardware y software-based firewalls para proteger tu red de amenazas internas y externas
- Antivirus software: Utilizar antivirus en workstations y servers para prevenir infecciones malware.
- Wireless Security: Implementar medidas de seguridad robustas como la encriptación WPA2 y contraseñas fuertes para prevenir acceso no autorizado.
- Segmentación de red: Dividir la red en zonas separadas basadas en distintos niveles de acceso y funciones para contener potenciales amenazas.

## Topologias

Dentro de las topologias LAN, encontramos las siguientes:

- Star Topology: Los dispositivos se conectan desde un dispositivo central como un switch. Esta es la topologia mas comun encontrada al dia de hoy debido a su escalabilidad (sin embargo, su costo es elevado)

Debido a que requiere mas cable y la compra de equipamiento dedicado, es mas caro que otras topologias. Sin embargo, provee ventajas significantes. Por ejemplo, es mas escalable ya que se pueden agregar la cantidad de dispositivos necesarios para la demanda de la red sin problemas.

Sin embargo, mientras mas escale la red, mas mantenimiento necesitará para continuar funcionalidad. Esta dependencia incrementada sobre el mantenimiento hace que los problemas se resuelvan de forma más lenta. Si el hardware centralizado (switch) que conecta los dispositivos falla, todos los dispositivos no podrán enviar o recibir datos.

- Bus topology: Esta conexion depende solo de un cable. Esta topología es similar a un árbol del que cuelgan muchas hojas.

Como los datos son destinados a que viajen a través de todos los dispositivos conectados al mismo cable, es propenso a ponerse lento y a sufrir cuellos de botella si los dispositivos dentro de la topología simultaneamente solicitan datos.

Sin embargo, esta topología es una de las mas fáciles y eficientes en costos para setear ya que solo se necesita cable y un equipamiento dedicado para conectar los dispositivos.
