# Powershell

El objetivo de este readme es agregar funcionalidades de diferentes comandos que pertenecen al roadmap de ciberseguridad de roadmap.sh y al mismo tiempo agregar algunos que crea útiles de explicar y escapen a los básicos.

### ipconfig

Provee información de la red configurada en una computadora.

```bash
ipconfig
```

con ipconfig /all, provee mas informacion.

### ver

Determina la version del sistema operativo.

```bash
ver

output:
"Microsoft Windows [Version 10.0.17763.1821]"
```

### systeminfo

Provee detalles del sistema.

```bash
systeminfo

output:
"Host Name:                 WIN-SRV-2019
OS Name:                   Microsoft Windows Server 2019 Datacenter
OS Version:                10.0.17763 N/A Build 17763
OS Manufacturer:           Microsoft Corporation
OS Configuration:          Standalone Server
OS Build Type:             Multiprocessor Free"
```

### netstat

provee las conexiones establecidas. Ejemplo:

```bash
systeminfo

output:
" Proto  Local Address          Foreign Address        State
  TCP    10.10.230.237:22       ip-10-11-81-126:53486  ESTABLISHED"
```

con netstat -abon, podemos traer todas las conexiones con sus puertos, observar el programa asociado.

### type

mismo funcionamiento que CAT en linux. Visualiza el contenido del archivo desde consola.

```bash
type file.txt

output:
" file content"
```

### tasklist

abrir administrador de tareas en consola.

### taskkill

suprimir una tarea desde consola (se debe añadir el Proccess Id (PID)).

```bash
taskkill /PID 4567
```

### shutdown

reinicia el sistema.

```bash
shutdown /r
```

### shutdown con timer

reinicia el sistema en un tiempo determinado.

```bash
shutdown /r /t 0
```

### shutdown abort

aborta la peticion de reinicio.

```bash
shutdown /a
```

### Write-Output

misma funcionalidad que el echo.

### Get-Command

listar comandos. Ejemplo:

```bash
Get-Command -Name Remove*
```

Esto traera comandos que empiecen con el verbo remove.
