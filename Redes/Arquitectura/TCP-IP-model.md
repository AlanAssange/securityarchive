# TCP

TCP o Transmission Control Protocol es una de las reglas utilizadas en networking.

Este protocolo es bastante similar al modelo OSI, consiste en cuatro capas y es una version resumida del modelo OSI.

Las siguientes capas son:

- Aplicación
- Transporte
- Internet
- Interfaz de red

Es bastante similar a como funciona el modelo OSI, la información es añadida a cada capa del modelo TCP como una pieza de data (o packet). Este proceso es conocido como encapsulación, y el proceso reverso es decapsulación.

Una de las features del modelo TCP es que está basado en la conexión, lo que implica que el modelo TCP debe establecer una conexión entre cliente y dispositivo actuando como un servidor antes de que los datos sean enviados. Es por esto que el modelo garantiza que todos los datos serán recibidos del otro lado. Este proceso es llamado Three-way handshake.

## Ventajas del modelo TCP

- Garantiza la integridad de los datos
- Capaz de sincronizar dos dispositivos y prevenirlos de recibir los datos en orden incorrecto.
- Performa muchos procesos para garantizar confiabilidad.

## Desventajas del modelo TCP

- Una conexion lenta puede generar un cuello de botella en la información.
- Requiere una conexión confiable entre dos dispositivos. Si un simple chunk de datos no llega, entonces el dato por completo no será enviado y tocará reenviar.
- Es mucho mas lento que el UDP debido a que se realizan mas procesos entre los dispositivos.

## TCP Packets

los packets dentro del modelo TCP contienen varias secciones de información conocidos como Headers que se añaden en la encapsulación. Estos son los cruciales:

- Source Port: Este valor es el puerto abierto habilitado por el remitente para enviar el packet TCP. Este valor se escoge de manera al azar (Dentro de los puertos 0-65535 que no están en uso al momento).
- Destination Port: Este valor es el numero de puerto que una aplicación o servicio está utilizando en su host remoto (para recibir los datos). Ejemplo: un webserver corre en el puerto 80. A diferencia del source port, este no es elegido al azar.
- Source IP: Dirección IP del dispositivo que está enviando el packet.
- Destination IP: Dirección IP del dispositivo que está destinado a recibir el packet.
- Sequence number: Cuando una conexión ocurre, la primer pieza de datos transmitida lleva un número al azar.
- Data: Donde los datos están guardados.
- Flag: Este header determina como será tratado el packet durante el proceso de handshake.
- Checksum: valida la integridad de los datos.

Luego, discutiremos el proceso de Three way handshake. El término dado al proceso utilizado para establecer conexión entre dos servicios. Se comunican utilizando mensajes especiales:

- 1: SYN. Un mensajes SYN es el packet inicial enviado por un cliente durante el handshake. Este packet es utilizado para iniciar la conexión y sincronizar los dos dispositivos juntos.
- 2: SYN/ACK. Este packet es enviado por el servidor (dispositivo que recibe) para reconocer el intento de sincronización del cliente.
- 3: ACK. El paquete reconocido puede ser utilizado por el cliente o el servidor para reconocer que una serie de mensajes o packets se recibieron correctamente.
- 4: DATA. Cuando una conexión es establecida, los datos (archivo) se envian via el mensaje DATA.
- 5: FIN. Este paquete es utilizado para limpiar correctamente y cerrar la conexión luego de que esté completa.
- 6: RST. Este paquete cierra abruptamente la comunicación. Indica que hubo un problema durante el proceso. Por ejemplo, si el servicio o aplicación no está funcionando correctamente.
