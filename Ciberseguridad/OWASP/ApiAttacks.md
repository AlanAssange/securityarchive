# Api Attacks

A continuación se deja una constancia de los datos del TOP 10 por mas cantidad de usos de estas vulnerabilidades por todo internet:

<img src="/Ciberseguridad/img/breachanalysis.png"/>

Una de las cosas que debemos mejorar, es el rate limiting. Lo utilizamos para defendernos de los ataques de alto volumen y prevenirnos de los bots que generan mass harvesting. El sistema no es perfecto, y está expuesto a vulnerabilidades. Los atacantes pueden penetrar el rate limiting estableciendo un número entre 5 a 10, y luego distribuir sus ataques sobre miles de direcciones IP utilizando proxies para evadir la detección.

Mientras que nuestros request pueden tardar milisegundos en detectar si son válidos o no, los atacantes pueden tardar meses en desarrollar un ataque. Si las APIs no devuelven información valiosa, los hackers no se molestarían en enviar 500 millones de solicitudes al API. He aquí la raíz del problema.
