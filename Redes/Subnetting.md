# Subnetting

El subnetting, o subdivisión de red, es el proceso de dividir una red IP grande en subredes más pequeñas y manejables. Esto permite una mejor organización de las direcciones IP, mejora la seguridad y el rendimiento de la red, y facilita la administración.

Ventajas del Subnetting:

Optimización del Uso de Direcciones: Permite utilizar las direcciones IP de manera más eficiente, reduciendo el desperdicio de direcciones en redes grandes.
Seguridad Mejorada: Permite segmentar la red en subredes independientes, lo que puede limitar el alcance de posibles problemas de seguridad y facilitar la implementación de políticas de acceso.
Mejora del Rendimiento: Reduce el tamaño de las tablas de enrutamiento y la cantidad de tráfico de broadcast en cada subred, lo que puede mejorar el rendimiento de la red.
Ejemplo:
Imaginá una red con la dirección IP 192.168.1.0/24. Esto significa que tenés una red con 256 direcciones IP (de 192.168.1.0 a 192.168.1.255). Si se divide esta red en 4 subredes, se usa una subnet mask de /26. Cada una de las subredes tendría 64 direcciones IP, proporcionando 62 direcciones utilizables para hosts (considerando que la primera es la dirección de red y la última es la dirección de broadcast)

## Subnet Mask

Una "subnet mask" o máscara de subred es un componente que define qué parte de una dirección IP pertenece a la red y qué parte pertenece a los hosts dentro de esa red. Mientras que la dirección IP puede tener 256 valores, la subnet mask solo puede tener nueve valores en octetos y divide a la dirección IP entre una **sección de red** y una **sección de hosts** 

<img src="img\subnetoct.png"/>

*créditos de la imagen:RichTechGuy youtube*

Solo un octeto puede tener un valor diferente a 0 o 255. Será una secuencia de unos seguidos de ceros.

Los bits en 1 indican la parte de la dirección que pertenece a la red.
Los bits en 0 indican la parte de la dirección que pertenece a los hosts dentro de la red.
---
Porción de red = 1
Porcion de hosts = 0
---

Veamos un ejemplo de cómo se divide una ip en porción de red y en porción de hosts en binario:

<img src="img\netportionexample.png"/>

*créditos de la imagen:RichTechGuy youtube*

En este ejemplo, observamos que las porciones de red (es decir, sus dos octetos) se conservan en 1 y las porciones de hosts se mantienen en 0.

Si una dirección IP cuya porción de red es 172.16 quiere enviar un packet hacia otra computadora, sus porciones de red deberán coincidir aunque sus hosts sean distintos. La computadora determina que su destino se encuentra dentro de la misma red y envía el paquete.

Cuando la dirección IP no se encuentra dentro de la misma red (es decir, sus porciones de red no coinciden), los paquetes serán enviados a una IP gateway para enrutarlos hacia donde corresponda. la IP gateway, también es conocida como default gateway.


A continuación, un ejemplo de nuestra ip, su subnet y default gateway.

<img src="img\subnetexample.png">

*créditos de la imagen:RichTechGuy youtube*

Cuando una subnet mask es 255.255.255.0 quiere decir que los primeros tres octetos se mantendrán siempre iguales en nuestra red.
Si nuestra ip es 192.168.1.0, **192.168.1** (es decir, los primeros tres octetos) nunca cambiarán sus números (los primeros tres octetos de la subnet mask en 255 marcan esto) y todos los dispositivos de nuestra red tendrán los primeros tres octetos de IP seguido del cuarto octeto con el host que esté disponible. 

El último octeto en nuestra subnet mask (.0) indica que puede ser cualquier número de 0 a 255. Dejando un total de 256. Pero hay tres que no se pueden tocar. En este caso, .0 y .255 HOST (Broadcast Address). El router también toma un IP address (default gateway) por lo que si el default gateway host termina en .1, no podrá tocarse el valor 1. Quedarán 253.


## En síntesis:

255 subnet mask: estos números nunca cambiarán.
0 subnet mask: este número cambiará dependiendo al dispositivo que esté asignado.

Primeros tres octetos: en el ejemplo mostrado con anterioridad, les llamaremos **Network Portion**
Último octeto: lo llamaremos **HOST portion**.

Cuando una máscara de subred es 255.255.255.0, esto significa que los primeros tres octetos (24 bits) de la dirección IP se usan para identificar la red y el último octeto se usa para identificar los dispositivos dentro de esa red.

Máscara de subred 255.255.255.0:

En notación binaria: 11111111.11111111.11111111.00000000.
(Para calcular la cantidad de Ips disponibles en este caso, deberíamos hacer dos sobre ocho. Nos dará como resultado 256, quitando las dos IPs reservadas para la **Network IP** (primera dirección ip de nuestra subred) o dirección de red y **Broadcast IP** (última dirección ip de nuestra subred) o dirección de broadcast)

Dirección IP 192.168.1.0 con una máscara de subred 255.255.255.0:

Red: 192.168.1 (los primeros tres octetos).
Hosts: el último octeto (los últimos 8 bits), que puede variar de 0 a 255, pero 0 generalmente se usa para la dirección de red y 255 para la dirección de broadcast.
Por lo tanto, en una red con la máscara 255.255.255.0, todos los dispositivos tendrán direcciones IP que comparten los primeros tres octetos (192.168.1 en este caso). La variación estará en el último octeto, que identifica cada dispositivo individual en la red.

Ejemplos de direcciones IP válidas en esta red serían 192.168.1.1, 192.168.1.2, 192.168.1.3, etc., hasta 192.168.1.254, mientras que 192.168.1.0 es la dirección de red y 192.168.1.255 es la dirección de broadcast para la red.

Default gateway: Router IP - Cuando un dispositivo de mi red quiere interactuar con otro que está por fuera, debe hacerlo por el router consultando al default gateway para salir de lo conocido.


## CIDR (Class Inter-Domain Routing)

Bits que representan la cantidad de unos en una subnet mask separados de la dirección ip por una barra a modo de anotación. Podemos utilizarlo para restarle a los 32 bits que conforman los cuatro octetos la cantidad de bits que marca el CIDR y que nos dé como resultado la cantidad de ceros que posee la subnet mask.

## IPs privadas

Este tipo de IPs no pueden ser accesibles a través de internet. 


## Recursos útiles para practicar subnetting:

<a href="https://richtechguy.com/subnetting-practice-tool/" target="_blank">Subnetting practice tool</a>

<!-- Nuestras computadoras tienen 16 millones de ip para responderse con motivos de testing. Todas las IP que arrancan con 127.x.x.x conocidas como localhost o loopback address -->
<!-- Cuando se rompen las reglas para armar un rango de IPs se habla de una classless network, porque estoy asignando pocas ip para la magnitud de mi red. -->
