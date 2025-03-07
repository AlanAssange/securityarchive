# Broken Object Property Level Authorization

Can user A access user B data?

Broken Object Property Level Authorization o BOPLA, es una vulnerabilidad de seguridad en aplicaciones web en la que los controles de acceso a nivel de propiedad dentro de un objeto no están correctamente implementados. Esto permite que un usuario acceda, modifique o elimine propiedades de un objeto a las que no debería tener acceso, incluso si no puede acceder al objeto completo. Revela datos sensibles y excesivos y explota endpoints modificando sus valores.

Supongamos que una aplicación de banca en línea devuelve un objeto JSON con los datos del usuario:

```bash
{
  "user_id": 1234,
  "name": "Juan Pérez",
  "account_balance": 5000,
  "role": "admin"
}
```

Si el usuario autenticado no es un administrador, pero aún así recibe el campo "role": "admin", un atacante podría intentar modificar este valor en una solicitud y ganar privilegios elevados. Esto tambien puede llevar a un masivo robo de datos.

## Causas comunes de BOPLA

- Falta de control de acceso a nivel de propiedad

- La API devuelve más datos de los necesarios sin filtrar información sensible.
- Confianza en el frontend para ocultar datos (Aunque los campos no se muestren en la interfaz, siguen estando en la respuesta de la API.)
- Modificación de datos en el cliente sin validación en el servidor
- Si el usuario puede modificar propiedades como role o account_balance sin una validación en el backend, puede escalar privilegios o alterar datos críticos.

## Prevenir BOPLA

- Implementar controles de acceso a nivel de propiedad. Solo acceso legitimo.
- Asegurar que solo los datos necesarios sean expuestos al usuario según sus permisos.
- No confiar en la seguridad del frontend
- Validar siempre en el backend qué datos se pueden leer o modificar.
- Utilizar filtrado de respuestas en la API
- Enviar solo los datos requeridos para el usuario en cada solicitud.
- uditar y probar regularmente la seguridad
- Utilizar herramientas como OWASP ZAP o Burp Suite para detectar exposiciones de datos indebidas.

## Diferencia con Broken Object Level Authorization (BOLA)

BOLA (Broken Object Level Authorization): Se enfoca en la autorización a nivel de objeto, permitiendo acceso a objetos que no deberían ser accesibles por un usuario.
BOPLA (Broken Object Property Level Authorization): Afecta la autorización dentro del objeto, exponiendo o permitiendo cambios en propiedades que deberían estar restringidas.
