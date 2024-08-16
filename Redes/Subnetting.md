# Subnetting

El subnetting, o subdivisión de red, es el proceso de dividir una red IP grande en subredes más pequeñas y manejables. Esto permite una mejor organización de las direcciones IP, mejora la seguridad y el rendimiento de la red, y facilita la administración.

Ventajas del Subnetting:

Optimización del Uso de Direcciones: Permite utilizar las direcciones IP de manera más eficiente, reduciendo el desperdicio de direcciones en redes grandes.
Seguridad Mejorada: Permite segmentar la red en subredes independientes, lo que puede limitar el alcance de posibles problemas de seguridad y facilitar la implementación de políticas de acceso.
Mejora del Rendimiento: Reduce el tamaño de las tablas de enrutamiento y la cantidad de tráfico de broadcast en cada subred, lo que puede mejorar el rendimiento de la red.
Ejemplo:
Imaginá una red con la dirección IP 192.168.1.0/24. Esto significa que tenés una red con 256 direcciones IP (de 192.168.1.0 a 192.168.1.255). Si se divide esta red en 4 subredes, se usa una subnet mask de /26. Cada una de las subredes tendría 64 direcciones IP, proporcionando 62 direcciones utilizables para hosts (considerando que la primera es la dirección de red y la última es la dirección de broadcast)

A continuación, un ejemplo de nuestra ip, su subnet y default gateway.

<img src="img\subnetexample.png">

Cuando una subnet mask es 255.255.255.0 quiere decir que los primeros tres octetos se mantendrán siempre iguales en nuestra red.
Si nuestra ip es 192.168.1.0, **192.168.1** (es decir, los primeros tres octetos) nunca cambiarán sus números (los primeros tres octetos de la subnet mask en 255 marcan esto) y todos los dispositivos de nuestra red tendrán los primeros tres octetos de IP seguido del cuarto octeto con el host que esté disponible. 

El último octeto en nuestra subnet mask (.0) indica que puede ser cualquier número de 0 a 255. Dejando un total de 256. Pero hay tres que no se pueden tocar. En este caso, .0 y .255 HOST (Broadcast Address). El router también toma un IP address (default gateway) por lo que si el default gateway host termina en .1, no podrá tocarse el valor 1. Quedarán 253.


## En síntesis:

255 subnet mask: estos números nunca cambiarán.
0 subnet mask: este número cambiará dependiendo al dispositivo que esté asignado.

Primeros tres octetos: llamados **Network Portion**
Último octeto: llamado **HOST portion**.

Default gateway: Router IP - Cuando un dispositivo de mi red quiere interactuar con otro que está por fuera, debe hacerlo por el router consultando al default gateway para salir de lo conocido.

Cuando una máscara de subred es 255.255.255.0, esto significa que los primeros tres octetos (24 bits) de la dirección IP se usan para identificar la red y el último octeto se usa para identificar los dispositivos dentro de esa red.

Máscara de subred 255.255.255.0:

En notación binaria: 11111111.11111111.11111111.00000000.
Los bits en 1 indican la parte de la dirección que pertenece a la red.
Los bits en 0 indican la parte de la dirección que pertenece a los hosts dentro de la red.
Dirección IP 192.168.1.0 con una máscara de subred 255.255.255.0:

Red: 192.168.1 (los primeros tres octetos).
Hosts: el último octeto (los últimos 8 bits), que puede variar de 0 a 255, pero 0 generalmente se usa para la dirección de red y 255 para la dirección de broadcast.
Por lo tanto, en una red con la máscara 255.255.255.0, todos los dispositivos tendrán direcciones IP que comparten los primeros tres octetos (192.168.1 en este caso). La variación estará en el último octeto, que identifica cada dispositivo individual en la red.

Ejemplos de direcciones IP válidas en esta red serían 192.168.1.1, 192.168.1.2, 192.168.1.3, etc., hasta 192.168.1.254, mientras que 192.168.1.0 es la dirección de red y 192.168.1.255 es la dirección de broadcast para la red.


Cuando se rompen las reglas para armar un rango de IPS se habla de una classless network, porque estoy asignando pocas ip para la magnitud de mi red.
Ej:
10.7.1.0
255.255.255.0

<!-- Nuestras computadoras tienen 16 millones de ip para responderse con motivos de testing. Todas las IP que arrancan con 127.x.x.x -->