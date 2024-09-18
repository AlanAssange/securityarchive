# VLAN

una VLAN (Virtual Local Area Network) o red local virtual es una agrupación lógica de dispositivos o usuarios dentro de una red, basado en atributos compartidos como locación, departamento o requisitos de seguridad. Las VLAN mejoran la seguridad de red, estableciendo una locación de recursos mas eficaz y simplificando el manejo de las redes.

## Caracteristicas de las VLAN

- Isolación: Las VLANs aíslan el tráfico entre diferentes grupos, ayudando a minimizar el riesgo de acceso no autorizado a los datos sensibles.
- Escalabilidad: Las VLANs permiten a los administradores de red cambiar y mejorar las redes sin causar disrupciones
- Reducción de costo: Las VLANs reducen la necesidad de hardware adicional reutilizando los switches y las redes, añadiéndoles funcionalidad.
- Mejoras de performance: Las VLANs reducen el tráfico no necesario al limitar el dominio de broadcast.

## Tipos de VLAN

- Port-based VLAN: En este tipo, los servicios son separados en base a su conexión física al switch. Cada puerto es asignado a una VLAN específica.
- Protocol-Based VLANs: Los dispositivos se agrupan en base al protocolo de red que utilizan. Por ejemplo, todos los dispositivos IP pueden ser asignados a una VLAN, mientras que los dispositivos IPX pueden ser asignados a otra.
- MAC-based VLANs: Dispositivos asignados a una VLAN en base a su MAC address. Esto acerca la posibilidad de mayor seguridad y flexibilidad pero requiere mayor esfuerzo administrativo.

- Las VLAN son creadas y manipuladas a través de switches que soportan la configuración VLAN. Los switches utilizan una VLAN ID (que va de 1 a 4094) para identificar de forma única cada VLAN. VLAN trunking protocol (VTP) y IEEE 802.IQ estándar son típicamente utilizados para manejar las VLAN entre diferentes switches.

- Aunque las VLAN presentan un rol crucial en la seguridad de redes, no son impenetrables. El acceso no autorizado puede ocurrir si las VLAN no son privadas o no existe una lista de control de acceso (que deben implementarse a fin de asegurar la red).

