# API1: Broken Object Level Authorization

Puede un usuario acceder a los datos de otro usuario dentro de un mismo sistema, o acceder a un objeto al que no está autorizado a ingresar?

BOLA lleva a falencias en la Autorizacion del usuario a acceder a un objeto que no esta autorizado a ingresar.

Ejemplo real: Pelotons API exposing user data.

BOLA (Broken Object Level Authorization) es una vulnerabilidad de seguridad en la que un atacante puede acceder o manipular objetos que no debería poder ver o modificar debido a una falta de control adecuado en la autorización a nivel de objeto.

Cuando una aplicación expone recursos (por ejemplo, usuarios, pedidos, archivos) a través de identificadores predecibles en una API (como IDs en URLs o parámetros de consulta), un atacante puede modificar estos identificadores para acceder a objetos de otros usuarios sin la autorización adecuada.

Ejemplo:

```bash
GET www.example.com/api?userid=1003
```

Si un atacante cambia el ID en la solicitud a otro usuario válido, como:

```bash
GET www.example.com/api?userid=1004
```

Y la API responde con los datos del usuario 5678 sin verificar si el solicitante tiene permiso, entonces hay una vulnerabilidad BOLA.

Consecuencias:

- Exposición de datos sensibles de otros usuarios.
- Modificación o eliminación de información de otros usuarios.
- Elevación de privilegios si se pueden modificar ciertos objetos.

Cómo prevenir BOLA

- Autorización estricta: Verificar siempre que el usuario autenticado tenga permiso para acceder o modificar el recurso solicitado.
- Reglas de acceso en el backend: No confiar en controles de seguridad solo en el frontend.
- Registros de auditoría: Para detectar intentos de acceso no autorizados.
- Discutir las reglas de autorización durante la fase de diseño del API.
- Revisar los requerimientos del negocio y definir las políticas de acceso a los datos.
- Implementar testeos pre-producción para encontrar falencias de tipo BOLA.
