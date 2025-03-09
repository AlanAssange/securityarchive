# Pilares de la seguridad en APIs

Los tres pilares de la seguridad en las APIs son:

- Gobernancia: Desarrollar Apis Seguras
- Monitoreo: Detectar amenazas en producción
- Testing: Asegurarse que las APIs estén libres de defectos.

## Gobernancia

Que se espera del team de desarrollo cuando se crea y publica un API?
Cuales son los requerimientos de las documentaciones?
Cuales son las polìticas de autenticación?
Cómo se versionan las APIs? Se retiran las viejas?

Es fundamental conocer los servicios, los datos ingresados en los mismos y sus riesgos, como también que todo debe quedar documentado a fin de que los servicios puedan ser utilizados por otros usuarios o desarrolladores. Así, al lograr un proceso estándar de desarrollo, reforzaremos la seguridad de los servicios y su consistencia.

Conocer la infraestructura y hacer inventario de los servicios.
Saber donde corren.
Que bases de datos utilizan?
Que cada uno de ellos tenga su documentación correspondiente.

Nada queda fuera de los procesos. Nada sube a producción sin validaciones previas.

### Gobernancia - Documentar las APIs (Swagger)

Por documentacion de APIs, entendemos que se deben documentar bajo un estandar como Swagger.

Ejemplo:

- Estandar para Rest APIS
- Machine-readable (YAML, JSON)
- Third party integration
- Manualmente generada o automatica
- Controlar que es publico y que es privado
- Retirar documentacion antigua

Definir en contrato:

- Titulo, descripcion y version
- URL-BASE
- ENDPOINTS, PATHS
- Requests y responses
- Requerimientos de Autenticacion
- Parametros, tipos de datos
- Metodos

Anotaciones extra:

- Authentication: tipo (basica, token, certificado) y como se implementa
- Authorization: quien tiene acceso a que y como.
- Naming Conventions: URIs, Metodos, pluralizacion, lenguaje y sin abreviaciones.
- Error Codes: Status code, IDs, mensajes human-readable (Que no muestren informacion UTIL para un posible atacante)
  Pueden decir: Rechazado, denegado, input inapropiado
- Versioning: Cuando incrementarlo y cuando no, tipos de version.
- Units, formats, standards: Zona horaria, timezones.

Documentar cuando un api debe necesitar una nueva version y los parametros correctos par aun API rest para tener una authentication basica.

## Monitoreo

Como nuestras APIs operan y performan en producción?

### Runtime Protection

Requerir autentificaciòn de usuarios para acceder a ciertos endpoints.

Tráfico geográfico de usuarios o por rangos de IP que pueden intemplementarse.

### Threat Detection

Cómo analizamos el tráfico para observar tráfico fraudulento, ataques volumétricos y nuestras respuestas a tales incidentes (capturar mètricas en logs y ponerlos en un repositorio)?

### Control Validation

Verificar los controles de las Apis y descubrir anomalias. Gateway, firewall o las Apis mismas, que funcionen como estan diseñadas

Bloqueo Proactivo:
Api Gateway: Ciertos endpoints solo serán accesibles con el accesocorrespondiente.
Firewall: Rate limiting o una Whitelist de IPs.

Alerta reactiva: Logging para capturar el tráfico. Request y responses de las APIs. Recibir alertas y ser notificado por los logs para no bloquear el trafico legitimo.

### Ventajas del monitoreo

- Ayuda a verificar las APIs que estan en uso.
- Descubrir apis no conocidas o no documentadas.
- Tener el suficiente contexto para saber cuando una transaccion es legitima y cuando no.

## Testing

### Seguridad

- Endpoints no seguros
- IDs incrementales
- Inyecciones de SQL
- Validaciones de inputs
- Error handlings

### Datos

- Excesiva exposicion de datos
- Sensitive data exposure
- Informacion personal (salud o datos bancarios) expuesta
- Exposicion del directorio de los archivos

### Logica

- Gaps en authorization
- Control de acceso basado en roles
- Abuso de las funcionalidades del API

IMPORTANTE:

- Orientar el testing hacia fallas de seguridad y no solo lógicas.

## Approachs hacia el testeo de APIs orientado hacia seguridad.

- Opcion 1: utilizada por las empresas: no hacer nada.
- Opcion 2: Hacerlo nosotros. (Postman)
- Opcion 3: Pagar a alguien que sepa sobre seguridad. (Pentesting)
- Opcion 4: Automatizarzlo. Automatized Security Testing.
