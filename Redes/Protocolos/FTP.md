# FTP

El protocolo FTP (File Transfer Protocol) es un protocolo cliente servidor utilizado para transferir archivos en una red. FTP utiliza dos canales, el canal de datos (Data channel) y el canal de control (Control channel):

- Data channel: Utilizado para transferir archivos
- Control channel: Utilizado por el cliente para enviar comandos al servidor como solicitar un archivo o un directorio.

Cuando un cliente solicita un archivo, el servidor abre un data channel para transferir el archivo hacia el cliente. 

Los clientes pueden performar varias acciones utilizando FTP, tales como:

- Descargar archivos
- Subir archivos
- Eliminar archivos
- Renombrar archivos y copiarlos

Fue utilizado en el pasado y perdió popularidad debido a HTTP para transferir archivos y publicarlos en la web, pero continúa siendo un protocolo común para asegurar datos privados como por ejemplo, en un sistema bancario.