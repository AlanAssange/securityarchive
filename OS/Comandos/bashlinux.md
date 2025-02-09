# Bash linux

El objetivo de este readme es agregar funcionalidades de diferentes comandos que pertenecen al roadmap de ciberseguridad de roadmap.sh y al mismo tiempo agregar algunos que crea útiles de explicar y escapen a los básicos.

### ifconfig

Provee información de la red configurada en una computadora.

```bash
ifconfig
```

### dig

Diminutivo para Domain Information Groper, es un comando utilizado para performar DNS queries y obtener información valiosa sobre los dominios, IPs y registros DNS.

```bash
dig
```

Para ver la dirección IP de un DNS podríamos utilizar:

```bash
dig www.example.com
```

## nmap

NMAP (Network Mapper) es una herramienta de escaneo de red utilizada para descubrir hosts y servicios en una red, identificando puertos abiertos y detectando vulnerabilidades. Provee información detallada sobre las redes, incluyendo sus direcciones IP, sistemas operativos y servicios corriendo por dentro. Nmap brinda soporte a varias técnicas de escaneo como TCP SYN, UDP, y detección de versionado de servicio. Es comúnmente utilizado para tareas de seguridad de red, escaneo de vulnerabilidades e inventario y organización de red, ayudando a los administradores y profesionales de la seguridad a asegurar sus entornos de red.

nmap cheatsheet: https://www.tutorialspoint.com/nmap-cheat-sheet

ejemplo para escanear un target particular:

```bash
nmap 192.168.0.1
```
