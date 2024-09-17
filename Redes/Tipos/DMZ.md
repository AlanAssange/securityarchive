# DMZ

<img src="https://www.fortinet.com/content/dam/fortinet/images/cyberglossary/dmz-benefits.jpeg" alt="DMZ model"/>

DMZ conocido también como _Demilitarized Zone_ es una red perimetral que funciona como una separación dentro de una organización interna. Su primer propósito es aislar datos críticos de potenciales amenazas, proveyendo una capa extra de seguridad dentro de una red de área local.

El objetivo de una DMZ es permitir a la organización acceder a redes no confiables como internet y asegurar que la red LAN continúe segura. Las organizaciones suelen guardar en la DMZ los servicios externos y sus recursos, los servidores para el DNS, FTP, mail, voIP y webservers. Estos servicios, servidores y sus recursos se aislan y se les da un acceso limitado a la red LAN, para asegurar que puedan ser accesibles vía internet pero estos a su vez no accedan a la red LAN. Esto logra como resultado que se le dificulte mas a agentes maliciosos ganar acceso directo a los datos de una organización y sus servidores internos vía internet. Una compañía puede minimizar sus vulnerabilidades creando un ambiente seguro de amenazas mientras que permite que sus empleados puedan comunicarse eficientemente y compartir la información vía una conexión segura.

## Pero como funciona una red DMZ?

Negocios con un dominio web público que los clientes utilicen deben hacer que su web sea accesible en internet. Para proteger la red LAN, el web server es instalado en una computadora separada de sus recursos interos. La red DMZ habilita la comunicación entre los recursos del negocio protegidos (como bases de datos internas) y el tráfico de internet.

Una red DMZ provee un buffer entre internet y la red LAN. La DMZ es aislada por un gateway de seguridad como un firewall que filtra el tráfico entre la red DMZ y la red LAN. El servidor DMZ por default es protegido por otro gateway de seguridad que filtra el tráfico que viene de redes externas.

## Beneficios de utilizar una DMZ

El principal beneficio de una DMZ es proveer una red interna con seguridad avanzada que restrinja acceso a datos sensibles y servidores. La DMZ habilita a quienes visitan la página web a obtener ciertos servicios mientras provee un buffer entre ellos y la red privada de la organización. Como resultado, la DMZ también ofrece beneficios de seguridad como:

- Control de acceso: El negocio puede proveer a los usuarios acceso a servicios fuera de sus perímetros de red vía internet. DMZ habilita el acceso a estos servicios mientras implementa una segmentación en la red para que los usuarios no autorizados tengan dificultades para ingresar a la red privada. Puede incluir también un proxy server, que centralizará el tráfico interno y simplificará el monitoreo y grabación de dicho tráfico.
- Previene el reconocimiento de red: Al proveer un buffer entre internet y la red privada, la DMZ previene que los atacantes performen trabajos de reconocimiento para buscar potenciales vulnerabilidades. Los servidores dentro de la DMZ se exponen públicamente pero con otra capa de seguridad (firewall) que impide al atacante observar por dentro de la red interna. Aunque un sistema DMZ quede comprometido, el firewall interno separará la red privada de la DMZ para mantenerlo seguro.

## Diseño de la DMZ

Una DMZ puede ser diseñada de varias formas, desde un solo firewall, duales o múltiples. La mayoría de las arquitecturas DMZ actuales utilizan firewalls duales que pueden ser expandidos para desarrollar sistemas más complejos.

Firewall singular: Una DMZ con un solo firewall requiere tres o mas interfaces de red. La primera es la red externa, que conecta con el internet público hacia el firewall. La segunda es la red interna, mientras que la tercera está conectada a la DMZ. Varias reglas monitorean y controlan el tráfico que está permitido a acceder a la DMZ y limitan la conectividad sobre la red interna.

Firewall dual: Opción mas segura. El primer firewall solo admite tráfico externo hacia la DMZ y el segundo firewall solo admite tráfico que vaya desde la DMZ hacia la red interna. Un atacante debería comprometer ambos firewalls para ganar acceso a la LAN de la organización.
Las organizaciones pueden editar los controles de seguridad también para varios segmentos en la red. Esto significa que con un sistema detección de intrusión (IDS) puede ser configurado para bloquear el tráfico que no pertenezca a una solicitud de tipo HTTPS hacia el protocolo de control de transmisión (TCP) port 443.

Las redes DMZ tienen su objetivo en proteger datos sensibles y recursos que utilicen las empresas como máquinas virtuales, para aislar las redes o aplicaciones particulares del resto de sus sistemas. El crecimiento de la nube implica que muchos negocios no necesitan web servers internos. Incluso se han migrado muchas infraestructuras externas a la nube utilizando SaaS (Software-as-a-Service).

Por ejemplo, un servicio cloud como Microsoft Azure permite a una organización que ejecute aplicaciones sobre VPNs (virtual private network) utilizar una aproximación híbrida hacia el DMZ situándose entre los dos.

## Debería usar DMZ en mi router?

Una DMZ puede ser utilizada en un router de una red de casa. El router DMZ será una LAN, con computadoras y otros dispositivos conectados allí. Algunos routers tienen un host DMZ que aloja a los dispositivos para operar fuera del firewall y actúa como DMZ. Todos los otros servicios se encuentran situados dentro del firewall. 

## Ejemplo gráfico de DMZ

<div id="dmz-examples" align="center">
  <img src="img\dmzexample.png" width="400"/>
  - En este ejemplo, podemos visualizar como la nueva red DMZ se implanta entre los dos firewalls. De esta manera, las solicitudes hacia el webserver no ingresarán en la red interna, protegiendo la información sensible.
  <img src="img\dmzexample2.png" width="400"/>
  - Como los requests deben ser en formato HTTPS, le diremos a nuestro firewall que solo admita solicitudes cuyo port sea 443 (https). De esta manera, garantizamos que solo accedan a nuestro firewall las solicitudes correspondientes, todas las demás serán bloqueadas. En el caso de nuestro segundo firewall, no se admitirá acceso de ningun tipo de solicitud, protegiendo la red LAN.
</div>


