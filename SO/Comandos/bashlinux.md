# Bash linux

El objetivo de este readme es agregar funcionalidades de comandos varios utilizados en una shell de linux.

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

### nmap

NMAP (Network Mapper) es una herramienta de escaneo de red utilizada para descubrir hosts y servicios en una red, identificando puertos abiertos y detectando vulnerabilidades. Provee información detallada sobre las redes, incluyendo sus direcciones IP, sistemas operativos y servicios corriendo por dentro. Nmap brinda soporte a varias técnicas de escaneo como TCP SYN, UDP, y detección de versionado de servicio. Es comúnmente utilizado para tareas de seguridad de red, escaneo de vulnerabilidades e inventario y organización de red, ayudando a los administradores y profesionales de la seguridad a asegurar sus entornos de red.

nmap cheatsheet: https://www.tutorialspoint.com/nmap-cheat-sheet

ejemplo para escanear un target particular:

```bash
nmap 192.168.0.1
```

### echo

Da como respuesta cualquier texto que le pongamos.

```bash
echo "Hola"

output = Hola
```

### whoami

Usuario con el que nos encontramos logueados actualmente.

```bash
whoami

output = usuariologueado
```

### find

Si sabemos el nombre de un archivo pero no recordamos donde esta:

```bash
find -name file.txt
```

Si recordamos la extension del archivo pero no su nombre:

```bash
find -name *.txt

##Como resultado, traera todos los archivos txt.
```

### grep

Permite buscar contenidos dentro de un archivo para valores especificos que estemos buscando.

```bash
grep "81.143.211.90" access.log

##Como resultado, traera donde se visualiza lo buscado en el archivo al cual le utilizamos GREP
```

### file

Permite saber que tipo de archivo es el seleccionado.

```bash
file myfile

output = myfile: ASCII TEXT

##Como resultado, traera el tipo de archivo.
```

### touch

Con touch, podemos crear un archivo y añadirle la extensión que deseemos.

```bash
touch example.json

##Como resultado,creará el archivo deseado.
```

### mkdir

Con mkdir podemos crear una carpeta en donde estemos parados.

### rm

Con rm, podemos borrar el archivo deseado.

### su

Con su, podemos cambiar al usuario seleccionado.

```bash
su user2

## Requerira la contrase;a del usuario.
```
