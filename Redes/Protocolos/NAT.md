# NAT

Network Address Translation (NAT) actúa como un intermediario entre los dispositivos de una red LAN y el internet. NAT ayuda a conservar las direcciones ip y mejorar la privacidad y seguridad traduciendo las direcciones ip de una red privada a una ip pública para comunicarse en internet.

## Como funciona NAT?

NAT se encuentra implementado en el router, también se puede encontrar en otros dispositivos de networking como un firewall. Cuando un dispositivo en la red LAN se comunica con una red externa, NAT permite que estos dispositivos compartan una ip pública singular, que queda registrada en internet. Esto se logra a través de los diferentes tipos de traducción:

- Static NAT: Un mapeo uno a uno entre una IP privada y una ip pública. A cada ip privada se le asigna una ip pública única dentro de la misma red.
- Dynamic NAT: Un mapeo uno a uno entre una IP privada y una ip pública pero la ip pública se elige desde un pool en vez de ser pre-asignada.
- Port Address Translation (PAT): Conocida también como NAT Overload, mapea múltiples IPs privadas hacia una IP pública única, utilizando un puerto único para diferenciar las conexiones.

## Ventajas de NAT

- Conservación de direcciones IP: NAT ayuda a mitigar la escasez de direcciones IPv4 permitiendo que múltiples dispositivos de una red privada utilicen una misma dirección IP pública, reduciendo la necesidad de comprar direcciones IP adicionales.

- Seguridad y privacidad: Ocultando las IP internas, NAT añade una capa de oscuridad que logra dificultades a los atacantes a la hora de encontrar dispositivos específicos dentro de una red.

- Flexibilidad: NAT permite cambiar tu IP interna sin actualizar la IP pública, reduciendo tiempo y esfuerzo en reconfigurar la red.

## Desventajas de NAT

- Errores de compatibilidad: Ciertas aplicaciones y protocolos pueden encontrar problemas a la hora de operar en un entorno NAT, como autentificaciones basadas en IP o peer-to-peer networking.

- Impacto de performance: El proceso de traducción puede introducir latencia y reducir la performance en redes de alto tráfico.
