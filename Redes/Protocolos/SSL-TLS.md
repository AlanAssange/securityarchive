# SSL/TLS

SSL (Secure Sockets Layer) y TLS (Transport Layer Security) son protocolos criptográficos utilizados para proveer seguridad en las comunicaciones vía internet.
Estos protocolos encriptan los datos transmitidos sobre la web para que cualquiera que intente interceptar los packets no pueda interpretar los datos. Una diferencia importante a saber es que SSL está deprecado debido a fallas de seguridad, y la mayoría de los navegadores web modernos no lo sportan. Pero TLS continúa siendo seguro y es utilizado con regularidad a nivel mundial, por lo que es preferible utilizar TLS.

## SSL

SSL, or Secure Sockets Layer, is an encryption-based Internet security protocol. It was first developed by Netscape in 1995 for the purpose of ensuring privacy, authentication, and data integrity in Internet communications. SSL is the predecessor to the modern TLS encryption used today.

SSL es un protocolo de seguridad desarrollado por netscape en 1995 con el propósito de asegurar la privacidad y la integrida de los datos. SSL es el predecesor del TLS moderno.
Un sitio web que implementa SSL o TLS tiene HTTPS en su URL, en vez de HTTP.

A website that implements SSL/TLS has "HTTPS" in its URL instead of "HTTP."

## Como funciona SSL

En orden de proveer privacidad, SSL encripta los datos transmitidos en al web. Esto implica que aquel que intente interceptar los datos solo verá caracteres imposibles de desencriptar.
SSL inicia un proceso de autenticación llamado handshake entre dos dispositivos comunicándose, para asegurar que ambos servicios estén protegidos.
SSL verifica que los datos lleguen al recipiente indicado.
En 1999 SSL fue actualizado para convertirse en TLS.

Originalmente, los datos en la web eran transmitidos en texto plano para que cualquiera pueda leerlos si recibían o interceptaban el mensaje. Por ejemplo, si un consumidor visitaba un sitio web de un shopping y realizaba una orden ingresando su número de tarjeta de crédito al sitio web, ese número navegaría a través del internet al descubierto

SSL fue creado para corregir este problema y proteger la privacidad del usuario. Al encriptar sus datos entre el usuario y el servidor web, SSL aseguraba que cualquiera que interceptara estos datos tan solo fuera capaz de ver un lío de caracteres. El número de la tarjeta del consumidor estaba a salvo, solo visible para el sitio web al ingresar estos datos.

## TLS

SSL es el predecesor de otro protocolo llamado TLS. en 1999 la IETF (Internet ENngineering task force) propuso una actualización a SSL. Como netscape no estaba involucrado, el nombre fue modificado a TLS. Las diferencias no fueron drásticas, sin embargo el cambio de nombre implicaba un cambio de dueño.

SSL se encuentra deprecado debido a TLS.

TLS encripta los datos enviados a través de internet para asegurar que los eavesdroppers y hackers sean incapaces de ver que es lo que se está transmitiendo. Es un protocolo criptográfico que provee seguridad end-to-end de datos entre aplicaciones sobre internet. Es utilizado en los buscadores web, y puede ser usado por otras aplicaciones como e-mail, file transfers, videoconferencias, mensajería instantánea y de voz, como servicios de internet como DNS y NTP.

Sin TLS, la información sensible como un login, los detalles de una tarjeta de crédito u otros detalles personas pueden ser fácilmente robados por otras personas, y tanto la correspondencia como los chats online o las llamadas pueden ser monitoreadas.

## SSL certificate

SSL solo puede ser implementado por sitios web que tengan un certificado SSL (técnicamente, un certificado TLS). Un certificado SSL es como un ID card que prueba que alguien es quien realmente dice ser. Estos certificados son mostrados por los sitios web o servidores de aplicaciones.

Hay varios tipos de certificados SSL.

- Single-Domain: Un certificado ssl que aplica solo a un dominio, es decir el nombre del sitio web.
- Wildcard: Como el single domain, aplica a un solo dominio. Sin embargo, incluye sus subdominios. Por ejemplo:

```bash
www.cloudflare.com
www.developers.cloudflare.com
www.blog.cloudflare.com
```

- Multi-domain: Aplica a multiples dominios no relacionados.

Los certificados SSL tambien vienen con diferentes niveles de validacion. Un nivel de validación es un chequeo que aumenta dependiendo la profundidad del mismo.

What are the types of SSL certificates?
There are several different types of SSL certificates. One certificate can apply to a single website or several websites, depending on the type:

-Domain Validation: Este es el mas elemental, por ende, el más barato. Todo lo que debe hacer una empresa es probar que controlan el dominio.

- Organization Validation: Las autoridades del SSL contactan a la persona o empresa que requiere el certificado. Este certificado es el mas fiable para los usuarios.
- Extended validation: Esto requiere un análisis en profundidad de toda la organización antes de que el certificado SSL pueda ser asegurado.

## Diferencias entre SSL y TLS

- Secure Sockets Layer (SSL) es un protocolo de comunicación, o conjunto de reglas, que crea una conexión segura entre dos dispositivos o aplicaciones de una red. Es importante establecer confianza y autenticar a la otra parte antes de compartir credenciales o datos a través de Internet. SSL es una tecnología que sus aplicaciones o navegadores pueden haber utilizado para crear un canal de comunicación seguro y cifrado a través de cualquier red. Sin embargo, SSL es una tecnología antigua que contiene algunos fallos de seguridad. La seguridad de la capa de transporte (TLS) es la versión mejorada de SSL que corrige las vulnerabilidades SSL existentes. TLS se autentica de manera más eficiente y sigue siendo compatible con los canales de comunicación cifrados.

## Uso en HTTPS

HTTP es un protocolo o conjunto de reglas de comunicación para la comunicación cliente-servidor a través de cualquier red. HTTPS es la práctica de establecer un protocolo SSL/TLS seguro en una conexión HTTP insegura.

Antes de que se conecte con un sitio web, el navegador utiliza TLS para comprobar el certificado TLS o SSL del sitio web. Los certificados TLS y SSL muestran que un servidor cumple con los estándares de seguridad actuales. Puede encontrar pruebas sobre el certificado en la barra de direcciones del navegador. Una conexión auténtica y cifrada muestra https:// en lugar de http://. La s adicional significa seguro.
