# OWASP - Seguridad de APIs

Sabían que el 83% del tráfico de internet está manejado por APIS? Y solo el 4% del testing de las mismas es realizado en base a su seguridad.

Los atacantes, buscan apis que tengan mas permisos de los requeridos, retornen mucha informacion, accedan a funciones no autorizadas o expongan fallas logicas.
Para un ciberataque clásico, se conoce la Cyber Kill Chain, pero esta es muy sofisticada ya que está compuesta por el proceso de Reconocimiento, infiltración, armamento, movimiento lateral, escalado de privilegios y finalmente el data breach. Esto no es así con las APIS,
ya que en el momento que el atacante encuentra la vulnerabilidad, puede explotarla debido a que la vulnerabilidad está expuesta (Fallas lógicas del negocio inclusive).

Las Apis, a su vez, pueden ser descubiertas inclusive si no están documentadas. Es tan simple como ver en las herramientas de desarrolladores el tráfico del navegador web.

PCI DSS 4.0 introduced stronger requirements for API security, including identifying business logic abuse, authentication, and stricter access controls. It emphasizes securing APIs to prevent threats like unauthorized access and data breaches.

## Que es OWASP?

Open WorldWide Application Security Project u OWASP, Es una organización sin fines de lucro que produce las mejores guías para la seguridad de las aplicaciones. Dentro de ellas, se encuentra el OWASP TOP 10.

## OWASP TOP 10

Marca el estandar de riesgos de seguridad en las aplicaciones web. A continuacion, se adjunta el TOP 10:

<img src="/Ciberseguridad/img/topten.png"/>

Este tipo de ataques (que serán desarrollados a continuación) nos permite ver que:

- Los ataques son nuevos y diferentes
- Son difíciles de detectar
- Se necesita involucrar desarrolladores en seguridad
