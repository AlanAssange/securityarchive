# ARP

Arp es un protocolo utilizado por las IPs para asignar una dirección ip a una dirección física de un dispositivo, conocida como MAC (Media Access Control) address. ARP es esencial para enrutar datos entre dispositivos de una red LAN, ya que permite la traducción de las direcciones IP de un hardware específico de la red y esto es fundamental para la comunicación entre dispositivos de una red LAN.

Cuando un dispositivo quiere comunicarse con otro dentro de la misma red LAN, precisa determinar el MAC address correspondiente de la dirección IP objetivo. ARP ayuda en el proceso 
enviando una ARP request qeu contiene la dirección IP objetivo. Todos los dispositivos dentro del dominio broadcast reciben este request y lo comparan con su propia dirección IP. Si se encuentra el objetivo, el dispositivo con la dirección ip coincidente envía una respuesta ARP conteniendo su MAC address.

El dispositivo que inició el ARP request puede actualizar su caché con la nueva información, y luego proceder a enviar los datos hacia el MAC address del objetivo.

