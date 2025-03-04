# Broken Authentication

Broken Authentication es un tipo de data breach que consiste en la vulnerabilidad de un API ante una autenticación pobre. Ejemplo:

- No utilizar autenticación en dos factores, no tener un captcha, OAuth o credenciales.

# Prevencion

- Realizar testing continuo para encontrar debilidades en las APIS
- No asumir que las apis estan ocultas o no seran encontradas.

# Riesgos

- Robo de datos
- Transacciones no autorizadas - Acceso no autorizado a sistemas y datos sensibles.
- Gran volumen de abuso en las APIS
- Ransomwares o PII Harvesting(Recolección de información de identificación de una persona).
- Toma de control de cuentas (Account Takeover - ATO).

1. Ataque de fuerza bruta
   Si una API permite intentos ilimitados de inicio de sesión, un atacante puede probar combinaciones de usuario y contraseña hasta encontrar una válida:

```bash
POST www.example.com/api/login?

{
"username": "victima",
"password": "123456"
}

Si la aplicación no bloquea los intentos después de varios fallos, es vulnerable.

```

2. Secuestro de sesión
   Si una aplicación usa cookies de sesión predecibles o no las invalida tras cerrar sesión, un atacante podría reutilizar una sesión activa:

```bash
GET www.example.com/api/dashboard?
Cookie: sessionid=abcd1234 # Si no cambia, un atacante puede robarla

```
