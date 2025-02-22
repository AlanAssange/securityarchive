# Zero Trust

En ciberseguridad, el concepto de Zero Trust o confianza cero, recorre el principio de "nunca confies, siempre verifica" enfatizando en la necesidad de validar cada usuario, dispositivo y aplicación intentando acceder a los recursos, mas allá de su locación dentro o fuera del perímetro de la red. Zero trust asume que las amenazas ya existen dentro de la red y que no hay entidad que deba ser confiable por default. Los principios incluyen verificación estricta de la identidad, acceso least privilege, micro-segmentación y monitoreo continuo. Esta aproximación al límite de los accesos a los recursos basados en los roles de los usuarios, asegura que la seguridad de la red se mantenga en cada uno de los segmentos que están comprometidos. Zero trust está diseñado para proteger los entornos IT modernos de amenazas evolutivas, asegurando los datos y recursos y no solo un perímetro de la red.

En la arquitectura de confianza cero, la tecnología principal asociada a utilizar es ZTNA. Pero debemos entender que la confianza cero es un approach holístico a la seguridad en red que incorpora diferentes principios y tecnologías.

El TI tradicional confiaba en todos y todo dentro de una red. Una arquitectura de cero confianza no confía en nada y nadie.

## Pero cómo funcionaba antes?

Dentro del antiguo modelo Castle-And-Moat, todos los usuarios dentro de una VPN eran confiables. Esta vulnerabilidad es exacerbada por el hecho de que las compañías ya no tienen sus datos solo en un lugar. Hoy, la información se reparte sobre vendedores de cloud, lo que hace mas difícil tener un control de la red en su totalidad.

Zero Trust significa que nadie es confiable por defecto dentro o fuera de una red, y la verificación es requerida para todos los que intenten ganar acceso a los recursos de una red. Esta capa de seguridad se realiza para prevenir brechas en la seguridad de los datos. Los estudios muestran que el costo aproximado de un data breach está por encima de los tres millones de dólares. Considerándolo, no es una sorpresa que muchas organizaciones hayan adoptado este modelo.

## Principios de Zero Trust.

- Monitoreo continuo y validación: La filosofía detras de la red de confianza cero asume que hay atacantes dentro y fuera de la red, por lo que ni usuarios ni máquinas deben ser automáticamente confiables. Zero trust verifica la identidad del usuario y sus privilegios, como así tambien la identidad del dispositivo y su seguridad. Los logins y las conexiones periódicamente se desloguean, forzando a los usuarios y dispositivos continuamente a verificarse.

- Least privilege: Otro principio de Zero Trust es el acceso al privilegio mínimo. Esto implica que a los usuarios se les da solo el acceso que necesitan, como por ejemplo en la armada le dan a los soldados solo la información de lo que necesitan saber. Esto minimiza la exposición de los usuarios a las partes sensibles de las redes.

Implementar este principio implica un manejo precavido de los permisos de usuario. Las VPNS no suelen ser muy adecuadas para los principios de privilegio mínimo, ya que loguear una VPN da acceso al usuario a la red completa en su totalidad.

- Acceso al control de dispositivos: El sistema de ocnfianza cero precisa monitorear cuantos dispositivos están intentando acceder a la red, para asegurar que cada dipositivo es autorizado y lograr que todos los dispositivos de la red a su vez no se encuentren comprometidos.

- Microsegmentación: Práctica que rompe los perímetros de seguridad en zonas pequeñas para mantener acceso separado para las diferentes partes de la red. Por ejemplo, una red con archivos viviendo en un data center único que utiliza microsegmentación puede contener docenas de zonas seguras. Una persona con acceso a una de esas zonas no será capaz de acceder a otras de las zonas, debido a que estas están separadas por autorizaciones diferentes.

- Prevenir el movimiento lateral: En seguridad de redes, un movimiento lateral es cuando un atacante se mueve dentro de una red después de haber ganado acceso a la misma. El movimiento lateral puede ser difícil de detectar inclusive si el entry point es descubierto, porque el atacante puede haberse ido a comprometer otras partes de la red.

Zero trust está diseñado para contener a los atacantes a fin de que no puedan moverse lateralmente. Como el acceso de Zero Trust está segmentado y debe ser reestablecido periódicamente, un atacante no puede moverse sobre otros microsegmentos dentro de la red. Una vez que la presencia dle atacante es detectada, el dispositivo o cuenta de usuario puede entrar en cuarentena, cortando su acceso.

- MFA (Multi-factor Authentication): El factor de autentificación múltiple es un valor núcleo de la seguridad Zero Trust. Implica mas de una pieza de evidencia para autentificar a un usuario; Una contraseña no es suficiente para ganar acceso. Una aplicación muy común es la verificación en dos pasos, que además de requerir una contraseña, deben ingresar un código enviado desde otro dispositivo como un celular. Esto provee dos piezas de evidencia de que el usuario es quien dice ser.

## Beneficios de Zero Trust

Zero Trust es una filosofía ambientada a los entornos de TI modernos mas que a los tradicionales. Con una variedad de usuarios y dispositivos accediendo a los datos internos, y con datos guardados dentro y fuera de la red(como en cloud), es mas seguro asumir que ningún dispositivo es confiable.

- El beneficio primario de aplicar principios de confianza cero es ayudar a reducir la superficie de ataque en la organización. Adicionalmente, Zero Trust minimiza el daño cuando un ataque ocurre en un área diminuta de la microsegmentación, que también beneficia al costo de recuperación de la compañía. Zero Trust disminuye el impacto de robo de credenciales y ataques de tipo phishing requiriendo factores múltiples de autentificación.

También, verificando cada solicitud, reduce el riesgo de dispositivos vulnerables.

## Que es una ZTNA?

Una ZTNA (Zero Trust Network Access) es la tecnología principal que habilita a las organizaciones a implementar la seguridad Zero Trust. Concilia la infraestructura y los servicios, encriptando las conexiones entre los dispositivos y los recursos que precisan.

## Casos de uso de zero trust

- Cualquier organización basada en una red que guarde información digital debe considerar utilizar su arquitectura y considerar reemplazar o aumentar una VPN. La mayoría de las organizaciones confían en las VPNs par aproteger sus datos, pero no son ideales para defenderse de los riesgos de hoy.

- Trabajo remoto: Mientras que las VPN crean cuellos de botella y pueden reducir la productividad para trabajadores remotos, Zero Trust puede extender sus conexiones desde cualquier lugar.
