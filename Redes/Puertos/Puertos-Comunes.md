# Puertos comunes y sus usos

Los puertos comunes están estandarizados y son utilizados por varios protocolos de red y servicios. Es crucial su entendimiento para configurar firewalls, detectar potenciales amenazas y manejar el tráfico en la red. Algunos de los mas utilizados incluyen el puerto 80 y 443 para tráfico de HTTP y HTTPS, 22 para acceso remoto seguro al SSH, 25 para la transmisión de emails via SMT y 53 para resolución de DNS. FTP utiliza el puerto 21 para control y 20 para la transferencia de datos, mientras que los puertos 137-139 y 445 están asociados con los datos compartidos via SMB. Los servicios de base de datos suelen utilizar puertos especificos, como el 3306 para MySql y 1433 para Microsoft SQL Server.

Todos los navegadores web envian sus datos sobre el puerto 80.

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

- 21: FTP (File Transfer Protocol)
- 22: SSH (Secure Shell) - Utilizado para loguearse en sistemas de forma segura via interfaces de texto.
- 23: Telnet - Servicio de login remoto, mensajes de texto no encriptados
- 25: SMTP (Simple Mail Transfer Protocol) - Enrutar emails
- 53: DNS (Domain Name System) - Servicio
- 80: HTTP - Utilizado en la World Wide Web. Tu navegador utiliza este puerto para descargar texto, imagenes o videos desde cualquier página web.
- 110: POP3 (Post Office Protocol) - Utilizado por los clientes para recuperar emails de un servidor.
- 119: NNTP (Network News Transfer Protocol)
- 123: NTP (Network Time Protocol)
- 143: IMAP (Internet Management Protocol) Gestión de mail digital
- 161: SNMP (Simple Network Management Protocol)
- 443: HTTPS (HTTP Secure) over TLS-SSL

En mi trabajo, usualmente utilizo los puertos 80,443, 20, 21, 22, 23, 25 y 53.
