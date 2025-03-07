# Security Misconfiguration

Security Misconfiguration ocurre cuando un sistema, aplicación o infraestructura tiene configuraciones inseguras que exponen información sensible o permiten ataques. Los atacantes utilizaran bots para explotar estas vulnerabilidades.

Estas configuraciones pueden incluir:

- Falta de TLS
- Headers faltantes (CORS policy, rate limit, HSTS)
- Uso de credenciales por defecto (ej., admin/admin).
- Errores en permisos (ej., archivos accesibles públicamente).
- Exposición de mensajes de error detallados (ej., stack traces con información sensible).
- Configuraciones inseguras en servidores y bases de datos (ej., acceso sin autenticación).
- Deshabilitar o no configurar medidas de seguridad (ej., CORS mal configurado, headers de seguridad faltantes).

## Ejemplo de Security Misconfiguration

❌ Caso 1: Consola de administración sin protección
Un sistema expone su panel de administración sin autenticación en:

```bash
http://example.com/admin
```

📌 Problema: Si un atacante descubre esta URL, puede acceder y modificar configuraciones.

✅ Solución:

- Restringir acceso con autenticación fuerte.
- Usar listas blancas de IPs o VPN.

❌ Caso 2: Mensajes de error detallados
Si una aplicación muestra errores completos, puede filtrar información sensible:

```bash
@app.route('/login', methods=['POST'])
def login():
try:
user = authenticate(request.form['username'], request.form['password'])
return "Login exitoso"
except Exception as e:
return str(e) # ❌ Muestra el error completo (archivo donde esta el error, como se produce el mismo y su status code)
```

📌 Problema: Un atacante podría ver información interna como rutas, consultas SQL o estructura del código.

✅ Solución:

```bash
@app.route('/login', methods=['POST'])
def login():
try:
user = authenticate(request.form['username'], request.form['password'])
return "Login exitoso"
except Exception:
return "Error en la autenticación", 400 # ✅ Mensaje genérico
```

❌ Caso 3: Permisos de archivos y directorios
Si un servidor tiene permisos incorrectos, los archivos pueden ser accesibles públicamente:

```bash
http://example.com/.env → Muestra claves API y credenciales
http://example.com/database.db → Descarga la base de datos
```

✅ Solución:

- Configurar permisos correctos (chmod 600 .env).
- Bloquear el acceso a archivos sensibles desde el servidor (.htaccess, nginx.conf).

Cómo prevenir Security Misconfiguration
✅ 1. Eliminar credenciales por defecto

- Cambiar contraseñas de administrador en sistemas y bases de datos.
- Usar autenticación fuerte (2FA).
  ✅ 2. Restringir acceso a archivos sensibles

- Bloquear acceso a .env, config.php, database.db, etc.
- Usar permisos correctos (chmod 600).
  ✅ 3. Configurar correctamente servidores y frameworks

-Deshabilitar directorios de listado (Options -Indexes en Apache).

- Configurar CORS correctamente (evitar Access-Control-Allow-Origin: \*).
  ✅ 4. No exponer errores detallados en producción
- En producción, mostrar mensajes genéricos y loguear detalles internamente.
  ✅ 5. Mantener software actualizado

Aplicar parches de seguridad en servidores, frameworks y dependencias.
