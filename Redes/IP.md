# IP

Cuando hablamos de IP(Internet protocol) debemos tener en cuenta que es un identificador único que permite el envío de información y la comunicación entre dispositivos en una red. Sin una IP, pierden la capacidad de comunicación y a su vez, de conexión a internet.

Usualmente, las IPs están representadas por cuatro octetos (secuencias de ocho bits que cada uno puede ser 0 o 1) de números que van del 0 al 255 separados por puntos.

Ejemplo: 192.168.123.210

## Diferencias entre IP pública e IP privada

Una IP **pública** es una dirección única asignada a los dispositivos de una red. Este tipo de ip es alcanzable (enrutable) vía internet y permite a los dispositivos comunicarse con otras redes, servidores o dispositivos que se encuentren en cualquier lugar del mundo. Son asignadas por el ISP (internet service provider) y tienen la particularidad de poder ser estáticas (permanentes) o dinámicas (es decir, que cambien periódicamente)

Una IP **privada** se utiliza dentro de un área local (LAN) y no es visible en internet. Estas direcciones están reservadas para uso interno dentro de una red local (una organización o una casa como ejemplos) y son asignadas por el router o el administrador de red para los dispositivos que estén dentro de una misma red. Ejemplo: computadora personal, impresora o smartphone. Para ser enrutadas hacia internet, requerirán ser traducidas por el protocolo NAT que permite transformar la ip privada en pública (por ende, será única) y comunicarse con otras ip públicas. También, tienen la particularidad dependiendo de la configuración de la red de ser estáticas o dinámicas.

Rangos de direcciones ip privadas:

10.0.0.0 to 10.255.255.255 (Class A)
172.16.0.0 to 172.31.255.255 (Class B)
192.168.0.0 to 192.168.255.255 (Class C)

## IP Default gateway (O puerta de enlace predeterminada)

Una ip de tipo default gateway es un nodo de una red que sirve como punto de acceso (AP) o intermediario entre una red local y redes externas, como internet. Cuando un dispositivo en una red local precisa comunicarse con un dispositivo fuera de su red (como acceder a una página web o enviar un email) envía los datos a su default gateway, quien se encarga de enrutarlo hacia el destino externo apropiado. El default gateway actúa como un director de tráfico, asegurando que los paquetes de datos se envíen correctamente entre la red interna y las redes externas.

## IPV4

IPV4: Dirección lógica de 32 bits que identifica nuestra computadora en la red. Por lógico, entendemos que nuestra computadora puede cambiar su IP y que no está arraigado a un dispositivo de hardware. Si se cambia de red, también se cambia de dirección IP. Si una pc está conectada a varias redes, puede tener múltiples IPs.

## Clases de IPv4

<img src="img\ipv4classes.png"/>

*créditos de la imagen:RichTechGuy youtube*

de la clase A a la C, hablamos de IPs de tipo Unicast(es decir, direcciones ip que van desde un punto singular de origen hacia un único destino). La clase D, está reservada para tráfico de tipo Multicast(Punto singular de origen hacia múltiples destinos). Y luego está la clase E está creada con propósitos de investigación y es experimental (no utilizada en networking). Las clases A, B y C tienen un tamaño estándar de subnet:

CLASE A: 16.8 millones de direcciones IP.
CLASE B: 65.5 mil direcciones IP
CLASE C: 256 direcciones IP

Nuestro router nos asigna IPs privadas a los dispositivos de nuestra red local y utiliza un protocolo llamado NAT para convertir nuestras ip privadas en una única ip pública en orden de conectar y transmitir datos vía internet. Esto soluciona la repetición de IPs privadas en diferentes dispositivos alrededor del mundo asignando una ip pública única compartida por todos los dispositivos de una red LAN.

Para continuar, recomiendo seguir con el apartado de <a href="Subnetting.md" target="_blank">Subnetting</a>.


 

