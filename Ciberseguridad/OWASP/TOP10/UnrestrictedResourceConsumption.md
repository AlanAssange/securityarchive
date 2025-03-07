# Unrestricted Resource Consumption

Unrestricted Resource Consumption es un tipo de vulnerabilidad que se da cuando una aplicación o sistema no impone límites adecuados en el uso de recursos como CPU, memoria, ancho de banda, almacenamiento o conexiones de red. Esto puede permitir que un atacante consuma recursos en exceso, afectando el rendimiento y provocando una Denegación de Servicio (DoS) o incluso causando costos financieros elevados en la nube.

Ejemplo:

1. Peticiones ilimitadas a una API.

- Si una API no tiene límite de tasa, un atacante puede enviar miles de solicitudes por segundo, saturando el servidor y afectando a la disponibilidad.

La forma de mitigarlo, es implementar un rate limiting con herramientas que establezcan un Máximo de 10 solicitudes por minuto vía IP.

## Estrategias de Mitigación General

- Implementar Rate Limiting
- Restringir el número de solicitudes por usuario/IP en un periodo de tiempo.
- Limitar el Uso de Recursos
- Establecer restricciones en el tamaño de archivos subidos memoria y CPU utilizada.
- No permitir valores arbitrarios en peticiones del usuario.
- Implementar herramientas como Prometheus, Grafana o CloudWatch para detectar consumo anómalo de recursos.
- Implementar Expiración de Sesiones y Caché
- Evitar que recursos sean utilizados indefinidamente sin control.
