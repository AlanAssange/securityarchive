# Puertos comunes y sus usos

Los puertos comunes están estandarizados y son utilizados por varios protocolos de red y servicios. Es crucial su entendimiento para configurar firewalls, detectar potenciales amenazas y manejar el tráfico en la red. Algunos de los mas utilizados incluyen el puerto 80 y 443 para tráfico de HTTP y HTTPS, 22 para acceso remoto seguro al SSH, 25 para la transmisión de emails via SMT y 53 para resolución de DNS. FTP utiliza el puerto 21 para control y 20 para la transferencia de datos, mientras que los puertos 137-139 y 445 están asociados con los datos compartidos via SMB. Los servicios de base de datos suelen utilizar puertos especificos, como el 3306 para MySql y 1433 para Microsoft SQL Server.

Witin computer networking, ports serve a similar purpose. When a computer system seeks to connect to another computer, the port serves as a communication endpoint. It is also possible for different services running on the same computer to expose various ports and communicate with one another using these ports. In simple terms, if a software application or service needs to communicate with others, it will expose a port. Ports are identified with positive 16-bit unsigned integers, ranging from 0 to 65535. Other services use this port number to communicate with the service or app. Port numbers are divided into three ranges: well-known ports, registered ports, and dynamic or private ports.

Los puertos están divididos en tres rangos: Well-known ports, registered ports y dynamic or private ports.

Well-kown ports (también conocidos como puertos de sistema) están numerados del 0 al 1023. Por ejemplo: para conectar hacia el host example.com vía SSH, utilizaría este comando:
- El cliente y el servidor deben estar emparejados (Esto es importante por las reglas de firewall que puede haber entre medio de una comunicación)

ssh username@example.com -v
In this example, -v stands for verbose, and you should see output similar to this:

debug1: Connecting to example.com [<IP Addr>] port 22
As shown, SSH is trying to connect to example.com using port number 22. You may use the -p option to specify another port number; otherwise, SSH will default to 22.

```bash
ssh username@example.com -v
```

En este ejemplo, -v es verbose y deberias ver un output similar a este:

```bash
debug1: Connecting to example.com [<IP Addr>] port 22
```

SSH está intentando conectarse a example.com utilizando el puerto número 22. También se podría utilizar la opción -p para especificar otro puerto, pero por default SSH estará en el 22.

El IANA (Internet Assigned Numbers Authority) ha asignado números de puertos para servicios utilizados en la cotidianidad como SSH, FTP, HTTP, HTTPS y otros. Acá listo los mas comunes:

- 20: FTP (File Transfer Protocol) Transferencia de datos
- 21: FTP Control de comandos
- 22: SSH (Secure Shell)
- 23: Telnet - Servicio de login remoto, mensajes de texto no encriptados
- 25: SMTP (Simple Mail Transfer Protocol) - Enrutar emails
- 53: DNS (Domain Name System) - Servicio
- 80: HTTP - Utilizado en la World Wide Web
- 110: POP3 (Post Office Protocol) - Utilizado por los clientes para recuperar emails de un servidor.
- 119: NNTP (Network News Transfer Protocol)
- 123: NTP (Network Time Protocol)
- 143: IMAP (Internet Management Protocol) Gestión de mail digital
- 161: SNMP (Simple Network Management Protocol)
- 443: HTTPS (HTTP Secure) over TLS-SSL

En mi trabajo, usualmente utilizo los puertos 80,443, 20, 21, 22, 23, 25 y 53. 

 

