# HTTPS

HTTPS (Hypertext Transfer Protocol Secure) es la versión segura de HTTP, que es el primer protocolo para enviar datos entre un navegador web y un sitio web. HTTPS está encriptado en orden de incrementar la seguridad en la transferencia de datos. Esto es importante cuando el usuario transmite data sensible, como el logging en una cuenta bancaria, servicio mail o proveedor de obra social.

Cualquier sitio web, especialmente aquellos que requieren credenciales de login, deben usar HTTPS. En los navegadores modernos como Chrome, los sitios web que no utilicen HTTPS están marcados diferente que aquellos que sí. Ejemplo:

<img src="https://www.cloudflare.com/img/learning/security/glossary/what-is-https/not-secure.png"/>


## Como funciona HTTPS?

HTTPS utiliza un protocolo de encriptado para encriptar comunicaciones. El protocolo es llamado Transport Layer Security (TLS), pero formalmente es conocido como Secure Sockets Layer (SSL). Este protocolo asegura comunicaciones utilizando lo que es conocido como infraestructura de llave pública asimétrica. Este tipo de sistema de seguridad utiliza dos tipos de llaves para encriptar comunicaciones entre dos partidos:

Llave privada - esta llave está controlada por el dueño del sitio web y está guardada en privado. Esta llave vive en el servidor web y es utilizada para desencriptar información encriptada por la llave pública. 

Llave pública - Esta llave está disponible para cualquiera que intente interactuar con el servidor en una forma que sea segura. Información que es encriptada por la llave pública solo puede ser desencriptada por la llave privada.

## Por qué HTTPS es importante?

Con HTTPS, el tráfico es encriptado de una forma que si los packets son interceptados, vendrán en un formato de caracteres sin sentido. Ejemplo:

- Antes de encriptar:

```bash
"Esto es un texto legible"
```
This is a string of text that is completely readable
- Luego de encriptar:

```bash
ITM0IRyiEhVpa6VnKyExMiEgNveroyWBPlgGyfkflYjDaaFf/Kn3bo3OfghBPDWo6AfSHlNtL8N7ITEwIXc1gU5X73xMsJormzzXlwOyrCs+9XCPk63Y+z0=
```

Con sitios web sin HTTPS, es posible por el ISP (Internet Service Provider) u otros intermediarios inyectar contenido en páginas web sin aprobación del dueño del website. Esto puede tomar forma de anuncios, cuando un ISP busca formas de incrementar la renovación de su servicio inyecta anuncios en las páginas web de sus clientes. Cuando esto ocurre, los profits de los anuncios no son compartidos con el dueño del sitio. HTTPS elimina la habilidad de terceros a inyectar anuncios dentro del contenido web.

Ejemplo:

<img src="https://www.cloudflare.com/img/learning/security/glossary/what-is-https/third-party-content.png"/>

## Que puertos utiliza HTTPS?

HTTPS utiliza el puerto 443. Esto diferencia HTTPS de HTTP, que utiliza el puerto 80.

(En terminos de networking, un puerto es un punto virtual donde la conexión a la red arranca y termina). Todas las computadoras conectadas a la red exponen un número de puertos para habilitarlas a recibir tráfico. Cada puerto es asociado con un proceso o servicio específico, y diferentes protocolos utilizan diferentes puertos)

HTTPS no es un protocolo separado de HTTP. Simplemente utiliza una encriptación TLS-SSL sobre el protocolo HTTP.

Cuando un usuario se conecta a una página web, la página web enviará sobre el certificado SSL la llave pública necesaria para empezar una sesión segura. Las dos computadoras, es decir cliente y servidor, irán sobre un proceso llamado SSL-TLS handshake, que es una serie de comunicaciones utilizadas para establecer una conexión segura.

Muchos proveedores de hosting de sitios web ofrecerán certificados TLS-SSL por una comisión. Estos certificados serán compartidos sobre muchos clientes. También existen certificados individuales, que por ende, serán mas caros.

