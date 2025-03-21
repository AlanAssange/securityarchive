# DNS

DNS (Domain Name System) es un protocolo fundamental de internet que traduce nombres de dominio legibles por los seres humanos (como www.ejemplo.com) a direcciones IP, como 192.0.2.1, que utilizan las computadoras para localizar y comunicarse entre ellas. Esencialmente, los DNS actúan como una guía telefónica de internet, permitiendo a los usuarios acceder a sitios web y servicios sin la necesidad de memorizar sus IP numéricas. Cuando un usuario tipea un nombre de dominio en el buscador, una query de DNS es enviada hacia un servidor DNS, que resuelve el dominio en su IP correspondiente permitiendo asi que el navegador se conecte al servidor apropiado.

Podemos dividir un hostname o nombre de dominio en tres partes:

- www: sub-dominio
- ejemplo: dominio
- com: top-level-domain (TLD)

cuya dirección ip será 192.0.2.1 .

resultado: www.ejemplo.com

# Authoritative DNS Server

Un servidor DNS autoritativo, es responsable de guardar todos los records de solicitudes DNS de un dominio en particular. Dependiendo del tipo de record, es enviado de vuelta hacia el servidor DNS recursivo (propiciado por la ISP), en el que una copia local sera cacheada para futuros request. Todos los records DNS vienen con un valor TTL que especifica cuanto tiempo un record debe ser cacheado.
