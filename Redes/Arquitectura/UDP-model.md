# UDP

User Datagram Protocol (UDP) es otro protocolo utilizado para comunicar datos entre dispositivos.

UDP es un protocolo stateless que no requiere una conexión constante entre dos dispositivos para que los datos sean enviados.

UDP es utilizado en situaciones donde las aplicaciones pueden tolerar la pérdida de datos (como streaming de video o chat de voz) o escenarios donde una conexión inestable no es el final de todo.

## Ventajas de UDP

- UDP es mucho mas rápido que TCP.
- UDP deja a la aplicación que decida si hay algún control sobre cuan rápido se envían los packets.
- UDP no reserva una conexión continua como el modelo TCP.

## Desventajas de UDP

- A UDP no le importa si recibe los datos o no.
- Esto implica que los usuarios con mala conexión tendran una pésima calidad de servicio.

## Headers

Los packets UDP son mucho mas simples que los TCP.

- TTL (Time To Live): Este campo setea un timer de expiración para el packet.
- Source Address: Dirección IP desde donde el packet es enviado.
- Destination Address: Hacia donde van los packets.
- Source Port: Este valor es el puerto abierto habilitado por el remitente para enviar el packet UDP. Este valor se escoge de manera al azar (Dentro de los puertos 0-65535 que no están en uso al momento).
- Destination Port: Este valor es el numero de puerto que una aplicación o servicio está utilizando en su host remoto (para recibir los datos). Ejemplo: un webserver corre en el puerto 80. A diferencia del source port, este no es elegido al azar.
- Data: Donde los datos (bytes o archivos) están siendo guardados.
