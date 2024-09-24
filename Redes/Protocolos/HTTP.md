# HTTP y HTTPS

HTTP (Hypertext Transfer Protocol) y HTTPS (HTTP Secure) son protocolos fundamentales para la comunicación web. HTTP es la raíz del intercambio de datos en la World Wide Web, permitiendo a los buscadores solicitar recursos desde los servidores web. HTTP transmite datos en texto plano y sus direcciones añaden capas de encriptado utilizando protocolos SSL-TLS (Secure Sockets Layer) (Transport Layer Security). Este encriptado protege la confidencialidad e integridad de los datos en tránsito, asegurando la ifnormación sensible como las credenciales de logueo y las transacciones financiales. HTTP también provee autenticación, asegurando que los usuarios se están comunicando con el sitio indicado. En los años recientes, hubo una significante adopción del protocolo HTTPS, con la mayoría de los buscadores marcando los sitios HTTP como "no seguros". 


## HTTP en profundidad
HTTP is a protocol for fetching resources such as HTML documents. It is the foundation of any data exchange on the Web and it is a client-server protocol, which means requests are initiated by the recipient, usually the Web browser. A complete document is typically constructed from resources such as text content, layout instructions, images, videos, scripts, and more.

HTTP es un protocolo para bvuscar recursos como documentos HTML. Es un protocolo de tipo cliente-servidor, lo que significa que sus solicitudes se inician desde el recipiente (que usualmente, es un buscador web). Un documento completo está construído por recursos como contenidos de texto, instrucciones en un layout, imagenes, videos, scripts y más. Ejemplo:

<img src="https://mdn.github.io/shared-assets/images/diagrams/http/overview/fetching-a-page.svg"/>

Los clientes y servidores se comunican intercambiando mensajes individuales. Los mensajes enviados por el cliente se llaman requests y los mensajes enviados por el server como respuestas se llaman responses.

<img src="https://mdn.github.io/shared-assets/images/diagrams/http/overview/http-layers.svg"/>

## Componentes de los sistemas basados en HTTP

Los request son enviados por una entidad (el usuario o un proxy). La mayoría de las veces es a través de un web browser, pero puede ser cualquier cosa como por ejemplo, un robot que popula contenido en la web y mantiene un search index. Cada request individual es enviado hacia un servidor, que maneja y provee la respuesta. Entre el cliente y el servidor hay numerosas entidades llamadas proxy, que performan diferentes operaciones y actúan como un gateway o caché, por ejemplo.

Hay mas computadoras entre un browser y el servidor manejando el request: routers, modems y más. Gracias al sistema diseñado en capas de la web, están ocultos en la capa de red y capa de transporte. HTTP está en la cima, en la capa de aplicación. 

## Client, the user-agent

El user-agent, es cualquier herramienta que esté al alcance del usuario. Este rol es realizado por el navegador web, pero puede ser realizado por programas utilizados por los ingenieros y desarrolladores web para debugear sus aplicaciones.

El navegador es siempre la entidad que inicia el request. Jamás será el servidor.

Para mostrar una página web, el servidor envía un request para buscar el documento HTML que representa la web. Luego, analiza el archivo, haciendo request adicionales correspondientes a la ejecución de scripts, a la capa de información como puede ser el CSS y sub-recursos dentro de la página (usualmente, imágenes y videos). El navegador combina estos recursos para presentar un documento completo, la página web. Los scripts ejecutados pueden ejecutar mas recursos y el navegador actualizará la página web.

Una página web es un documento de hipertexto, lo que significa que algunas partes mostradas son links, que pueden ser activados por el click del mouse para abrir una nueva página, permitiendo al usuario navegar por dicha web. El navegador traduce estas direcciones en HTTP requests, e interpreta sus HTTP responses para presentar al usuario una respuesta limpia.

## The web server

En el lado opuesto de la comunicación, está el servidor. Que sirve el documento solicitado por el cliente. Un servidor aparece como una computadora virtual singular, pero puede ser una colección de servidores compartiendo la carga (load balancing) u otro software (como cachés, database server o e-commerce server) generando el documento bajo demanda.

## Proxies

Entre el navegador web y el servidor, numerosas computadoras y máquinas transmiten los mensajes HTTP. Debido a la estructura en capas del stack web, muchos de estos operan entre el navegador web y el servidor, siendo transparentes para la capa HTTP y teniendo un impacto significante en la performance de la app. Estos pueden ser:

- Caché (público o privado, como el caché de navegador)
- Filtering (como un antivirus o controles parentales)
- Load balancing (para permitir múltiples servidores en diferentes requests)
- Authentication ( para controlar el acceso a diferentes recursos)
- Logging (Permite el guardado de la información histórica del usuario)

## Aspectos básicos de HTTP

Http es diseñado para ser simple y human-readable, inclusive con sus complejidades encapsulando mensajes HTTP en frames. Los mensajes HTTP pueden ser leídos por humanos, proveyendo testings fáciles a los desarrolladores y reduciendo complejidad a los newcomers.

HTTP es stateless pero no sessionless: No hay link entre dos request que sean llevados a cabo bajo la misma conexión. Por ejemplo: utilizando el carrito de compras de un e-commerce. Mientras que el core de HTTP es stateless, las cookies de HTTP permiten al usuario mantener la sesión de forma satisfactoria. Utilizando extensibilidades en los headers, la scookies de HTTP se añaden al flujo, permitiendo la creación de una sesión en cada request HTTP para compartir el mismo contexto o estado.

## Que puede ser controlado por HTTP?

Funciones controladas por HTTP:

- Caching: Cómo los documentos son cacheados, puede ser controlado por HTTP. El servidor puede instruir a los proxies y clients sobre que cachear y durante cuanto tiempo.
- Authentication: Algunas páginas pueden estar protegidas para que solo usuarios específicos puedan acceder a ellas. Autenticación básica puede ser proveída por HTTP, utilizando el WWW-Authenticate y headers similares o seteando una sesión específica via HTTP cookies.
- Sessions: Utilizar las cookies de HTTP te permite linkear requests con el estado del servidor. Esto crea sesiones, útiles para e-commerces y también para permitir al sitio guardar configuraciones del usuario.

## Mensajes HTTP

Hay dos tipos de mensajes HTTP, requests y responses.

### Requests

<img src="https://mdn.github.io/shared-assets/images/diagrams/http/overview/http-request.svg"/>

Los requests consisten de los siguientes elementos:

- Un método HTTP, un verbo como GET, POST, OPTIONS, HEAD que defina la operación que el cliente desea realizar. Traer un recurso, postear un valor en un formulario HTML (POST), y otras operaciones necesarias en ciertos casos.
- El path del recurso que se busca: El URL del recurso, dominio y puerto.
- La versión del protocolo HTTP
- Headers opcionales que den información adicional a los servidores.
- Un body que contenga los datos enviados.

### Responses

<img src="https://mdn.github.io/shared-assets/images/diagrams/http/overview/http-response.svg"/>

Las respuestas consisten de los siguientes elementos:

- Un status code, indicando si el request fue exitoso o no y el por qué.
- Un status message, indicando una breve descripción del status code.
- Headers HTTP, como los del request.
- Opcionalmente, un body conteniendo el recurso solicitado.


