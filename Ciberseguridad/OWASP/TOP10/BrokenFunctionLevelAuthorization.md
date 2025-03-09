# Broken Function Level Authorization

Esta vulnerabilidad ocurre cuando una aplicación no implementa correctamente los controles de acceso a nivel de función, permitiendo que un usuario sin permisos adecuados acceda o ejecute acciones restringidas. Esto puede llevar a escalación de privilegios, acceso a datos sensibles o modificaciones no autorizadas.

Ejemplo de BFLA REAL: Bumble permitiendo modificar cuentas de free a premium desde un API.
Ejemplo de BFLA:

- Escenario: Sistema de gestión de usuarios con roles
  Un sistema tiene dos roles:

Usuario estándar: Puede ver su propio perfil.
Administrador: Puede gestionar a todos los usuarios.
Un usuario estándar intenta acceder a la función de administración de usuarios:

```bash
GET /admin/users
```

Si la aplicación no valida correctamente los permisos, el usuario puede acceder a datos que deberían estar restringidos.

## Causas Comunes de BFLA

- Falta de validación en el backend: Solo se verifica si el usuario está autenticado, pero no si tiene los permisos correctos.
- Confianza en la seguridad del frontend :Ocultar botones o enlaces en la interfaz no impide que un usuario acceda directamente a una función mediante una solicitud manual.
- Endpoints sin restricciones de acceso: Algunas rutas administrativas están accesibles sin verificación de permisos.

## Ejemplo en Código

Código vulnerable:

```bash
@app.route('/admin/users', methods=['GET'])
def get_all_users():
return jsonify(users) # Devuelve la lista de todos los usuarios
```

📌 Problema: Cualquier usuario autenticado puede acceder a este endpoint.

```bash
✅ Código corregido (con validación de permisos)

from flask import Flask, request, jsonify

app = Flask(**name**)

# Simulación de base de datos de usuarios

users = [
{"id": 1, "name": "Admin", "role": "admin"},
{"id": 2, "name": "Usuario1", "role": "user"}
]

# Función para verificar si el usuario tiene permisos de admin

def is_admin(user):
return user.get("role") == "admin"

@app.route('/admin/users', methods=['GET'])
def get_all_users():
user_role = request.headers.get("User-Role") # Suponiendo que el rol se envía en el header
if user_role != "admin":
return jsonify({"error": "Acceso denegado"}), 403 # Bloquear acceso
return jsonify(users)
🔹 Solución: Se valida el rol antes de permitir acceso a la función.
```

## Cómo prevenir BFLA

- Aplicar control de acceso en el backend: No confiar en el frontend para ocultar funciones sensibles.
- Usar middleware de autorización: Implementar verificaciones automáticas en cada solicitud.
- Principio de mínimo privilegio :Un usuario solo debe tener acceso a las funciones estrictamente necesarias.
- Revisar y probar endpoints de forma regular
- Usar herramientas como Burp Suite o OWASP ZAP para detectar rutas sin protección.

## Diferencia con otras vulnerabilidades de autorización

- BOLA (Broken Object Level Authorization) Acceso indebido a objetos individuales (ej., editar la cuenta de otro usuario).
- BOPLA (Broken Object Property Level Authorization) Modificación de propiedades dentro de un objeto sin permiso.
- BFLA (Broken Function Level Authorization) Ejecución de funciones restringidas sin los permisos adecuados.
