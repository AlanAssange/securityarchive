# Hardening

El hardening en sistemas operativos incluye configurar y asegurar un sistema operativo para reducir sus vulnerabilidades y mejorar su defensa contra ataques. Este proceso incluye deshabilitar servicios y puertos innecesarios, aplicar parches de seguridad y actualizaciones, configurar mecanismos de autenticación fuertes, reforzar el principio de mínimo privilegio y habilitar firewalls, como también sistemas de detección de intrusión.

El hardening en sistemas operativos también incluye setear permisos correctos a diferentes archivos, asegurar los logs del sistema y auditarlo regularmente para asegurar las mejores prácticas. El objetivo es minimizar la superficie de ataque y proteger al sistema de potenciales amenazas, ergo, exploits.

## Hardening en redes

Una buena práctica para aplicar el principio de privilegio mínimo es limitar el acceso a la red, a fin de mejorar su seguridad. Es prioritario establecer un rango de IPs permitidas para acceder al servidor de una compañía, por ejemplo. Dejando por fuera las IPs que comprometerían al sistema como tal. Denegando el acceso de todo aquel que intente acceder al servidor por IPs que estén fuera de las permitidas.

Cada puerto abierto es un posible punto de entrada. Es recomendable cerrar todos los puertos que no estén siendo utilizados o requeridos. A veces, los puertos se abren sin que el usuario esté al tanto de esto. Puede ocurrir que se abran con la instalación del sistema operativo u otras aplicaciones.

## Encriptado de datos

Una buena práctica para aplicar seguridad a los datos de un sistema, es encriptarlos a través del sistema operativo, como por ejemplo, utilizando el sistema de encriptado del filesystem (conocido como EFS). Podemos seleccionar aquellos archivos que querramos encriptar y separarlos del completo del sistema operativo.

También, podremos utilizar una encripción del disco completa o (FDE), encripta todo lo que se encuentre dentro del disco y puede hacerse a través de Windows BitLocker o en el caso de macOS, FileVault.

En el caso de querer encriptar la comunicación en red, es aconsejable utilizar una VPN.

## Firewall software

En la actualidad, existen firewalls dedicados vía software, que correrán a través de cada uno de los endpoints a los que nosotros querramos llegar desde nuestra WorkStation. Este firewall corre por debajo y permite habilitar o deshabilitar el tráfico de una aplicación o web, controlando sus procesos. Desde el firewall, podremos observar todos los datos que se envían, así tambien como los que llegan. Tiene la capacidad de identificar y bloquear los procesos no reconocidos, por lo que es efectivo contra el malware.

## Remover el software innecesario

Todos los softwares contienen bugs. Estos, son vulnerabilidades que pueden afectar a nuestro sistema. Todas las aplicaciones tienen procesos de patching diferentes, por lo que puede que inclusive actualizándolas, estas no tengan medidas de seguridad óptimas para su funcionamiento. Es recomendable remover el software que no se utiliza para reducir los riesgos de seguridad en el sistema.
