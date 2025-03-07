# Improper Inventory Management

Improper Inventory Management ocurre cuando un sistema de gestión de inventario tiene fallas en su control, falta de nocion de todas las APIs que estan productivas y no tienen un versionado correcto, lo que puede llevar a:

- Venta de productos fuera de stock.
- Manipulación de inventario por usuarios no autorizados.
- Errores en la actualización de stock después de compras o devoluciones.
- Falta de auditoría y control de cambios en el inventario.
- Esto puede causar pérdidas económicas, fraude y mala experiencia del cliente.
- Endpoints no parcheados e innecesarios que lleven a ningun lugar o a informacion vulnerable
- Documentacion desactualizada
- Robo de datos via APIs deprecadas.

## Prevenir Improper Inventory Management

✅ 1. Definir procesos estandarizados para el desarrollo de las APIs
✅ 2. Definir versionado de las APIs y retiro de las mismas cuando estan deprecadas.
✅ 3. Auditar constantemente los accesos de terceros partidos.
✅ 4. Registrar auditorías de cambios en inventario (quién, cuándo y cómo se modificó).
✅ 5. Implementar límites y validaciones en cambios de stock para evitar fraudes.
