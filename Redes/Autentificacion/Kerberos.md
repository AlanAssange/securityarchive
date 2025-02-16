# Kerberos

Kerberos es un protocolo de autenticación en red designado para proveer una fuerte autenticación en aplicaciones cliente-servidor. Fue desarrollador por MIT en 1980 y es nombrado como el perro de tres cabezas de la mitología griega que cuidaba las puertas de Hades, simbolizado el protocolo que provee autentificación en un entorno potencialmente hostible del ambiente en red.

## Como funciona?

Kerberos es un protocolo de autentificación SSO (Single sign on), una sesión que permite a un usuario autorizado a acceder a un servidor mediante un esquema de tickets.

Kerberos comprende tres componentes: Cliente, servidor y el centro de distribución de keys (servidor de autenticación que garantiza el ticket de acceso). Este esquema comienza con el cliente enviando una solicitud al servidor de autentificación usando usuario y contraseña. Esta solicitud se encripta como una secret key, verifica el nombre de usuario y contraseña y almacena la key en la base de datos del servidor de autentificación. Luego, descifra la contraseña y le concede el permiso de acceso al cliente.

### Mas información

https://youtu.be/1yWW7VQUX0A?si=c9dOaFVYfkeLI6Rv
