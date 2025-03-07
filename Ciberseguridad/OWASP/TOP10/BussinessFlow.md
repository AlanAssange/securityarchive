# Unrestricted Access to Sensitive Business Flows

Esta vulnerabilidad ocurre cuando una aplicación permite a los usuarios acceder sin restricciones a lógica de negocio crítica debido a una falencia en la misma como la compra de productos, la activación de cuentas o la modificación de pedidos. Un atacante podría abusar de estos flujos para obtener beneficios indebidos, realizar fraudes o afectar el negocio.

## Ejemplo de vulnerabilidad

Escenario: Cupón de Descuento Ilimitado
Una tienda en línea permite aplicar un cupón de descuento mediante la siguiente solicitud:

```bash
POST /apply_coupon
Body: {"coupon_code": "DESCUENTO50"}
```

Si no hay un control adecuado, un usuario podría aplicar el mismo cupón múltiples veces y obtener productos gratis.

## Causas comunes

- Falta de validación en el backend: No se verifica si un usuario ya ha utilizado una promoción o acción restringida.

- Ausencia de controles de estado: La aplicación no gestiona adecuadamente si un flujo de negocio ya ha sido completado.
- Confianza en la seguridad del frontend: No se debe confiar en que el frontend evitará acciones indebidas.

## Ejemplo en Código

❌ Código vulnerable (sin restricciones)

```bash
@app.route('/apply_coupon', methods=['POST'])
def apply_coupon():
    data = request.json
    if data['coupon_code'] == "DESCUENTO50":
        return jsonify({"discount": 50, "message": "Cupón aplicado"}), 200
    return jsonify({"error": "Cupón inválido"}), 400
```

📌 Problema: No verifica si el usuario ya ha usado el cupón.

✅ Código corregido (con restricciones)

```bash
used_coupons = {}

@app.route('/apply_coupon', methods=['POST'])
def apply_coupon():
user_id = request.headers.get("User-ID")
data = request.json
coupon_code = data.get('coupon_code')

    if user_id in used_coupons and used_coupons[user_id] == coupon_code:
        return jsonify({"error": "Cupón ya utilizado"}), 400

    if coupon_code == "DESCUENTO50":
        used_coupons[user_id] = coupon_code
        return jsonify({"discount": 50, "message": "Cupón aplicado"}), 200

    return jsonify({"error": "Cupón inválido"}), 400
```

🔹 Solución: Se verifica si el usuario ya ha usado el cupón antes de aplicarlo.

## Prevenir esta vulnerabilidad

- Implementar controles en el backend: No confiar en que el frontend evitará abusos.
- Límites y reglas en procesos críticos: Restringir el número de veces que se puede realizar una acción.
- Monitoreo de patrones de uso: Detectar comportamientos sospechosos como múltiples intentos de aplicar un cupón.
- Logs y auditoría: Registrar acciones importantes para identificar posibles abusos.
