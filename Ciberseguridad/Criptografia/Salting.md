# Salting

Salting es un concepto crucial dentro de la criptografía. Es una técnica implementada para mejorar la seguridad de las contraseñas o el equivalente a los datos sensibles agregando una capa extra de protección contra los intentos de hackeo, como los ataques de fuerza bruta o de diccionario. onsiste en agregar un valor aleatorio (llamado salt) a la contraseña antes de aplicarle una función hash.

## Por qué se usa?

Las funciones hash son deterministas, lo que significa que la misma entrada siempre produce la misma salida. Sin salting, los atacantes pueden usar tablas de búsqueda precomputadas como las rainbow tables para descifrar contraseñas comunes.

## Cómo funciona?

- Se genera un salt aleatorio único. (combinacion de bits aleatoria, diferente para cada usuario)
- Se concatena el salt con la contraseña antes de aplicar el hash.
- Se almacena tanto el salt como el hash resultante en la base de datos.
- Para verificar una contraseña, se extrae el salt, se aplica el mismo proceso de hash y se compara con el hash almacenado.

### Mas información

https://www.youtube.com/watch?v=PsIO0gxJF3g
