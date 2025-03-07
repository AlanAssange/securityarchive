# Server Side Request Forgery

Server-Side Request Forgery (SSRF) es una vulnerabilidad en la que un atacante manipula un servidor para que realice solicitudes HTTP a recursos internos o externos. Esto puede llevar a:

- Acceder a servidores internos y APIs internas.
- Leer archivos internos o metadatos del servidor.
- Explotar servicios en la nube (AWS, GCP, Azure).
- Utilizar el servidor como proxy para atacar otras redes.

## Ejemplo de SSRF

Un sistema permite a los usuarios ingresar una URL para obtener una imagen de perfil:

```bash
GET /fetch_image?url=http://example.com/profile.jpg
```

El servidor descarga la imagen y la devuelve al usuario.

❌ Código vulnerable (sin restricciones)

```bash
from flask import Flask, request

app = Flask(**name**)

@app.route('/fetch_image')
def fetch_image():
url = request.args.get("url")
response = requests.get(url) # ❌ No hay validación de la URL
return response.content
```

📌 Problema: Un atacante puede usar esto para acceder a recursos internos:

```bash
GET /fetch_image?url=http://localhost:8000/admin
```

🔹 Posibles ataques:

- Acceder a bases de datos internas (http://localhost:5432).
- Leer metadatos de servicios en la nube (http://169.254.169.254/latest/meta-data/).
- Hacer que el servidor ataque otras redes (usándolo como proxy).

## Cómo prevenir SSRF

✅ 1. Lista Blanca de URLs
Permitir solo dominios confiables:

```bash
ALLOWED_DOMAINS = ["example.com", "cdn.example.com"]

def is_allowed(url):
from urllib.parse import urlparse
hostname = urlparse(url).hostname
return hostname in ALLOWED_DOMAINS

@app.route('/fetch_image')
def fetch_image():
url = request.args.get("url")
if not is_allowed(url):
return "URL no permitida", 403
response = requests.get(url)
return response.content
```

✅ 2. Bloquear IPs Internas
Rechazar solicitudes a direcciones privadas (127.0.0.1, 169.254.169.254, 192.168.x.x, etc.).

✅ 3. Restringir Protocolos y Puertos
Asegurar que solo se permiten solicitudes HTTP/HTTPS y bloquear puertos no deseados.

✅ 4. Usar un Proxy Seguro
En lugar de permitir solicitudes directas, utilizar un servicio proxy que valide las peticiones antes de ejecutarlas.

SSRF es una vulnerabilidad crítica que puede permitir acceso a recursos internos. Para prevenirlo, es clave:
✅ Implementar listas blancas de dominios
✅ Bloquear direcciones IP internas
✅ Limitar los protocolos y puertos accesibles
✅ Usar proxies seguros para peticiones externas
✅ Principio de minimo privilegio
✅ Entrenar a los QA para identificar vulnerabilidades de tipo SSRF
