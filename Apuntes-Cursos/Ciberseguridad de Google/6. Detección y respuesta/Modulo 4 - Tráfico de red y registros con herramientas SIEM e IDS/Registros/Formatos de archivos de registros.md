Existen diferentes formatos de archivos para guardar registros, entre ellos están:
- JSON
- Syslog
- XML
- CSV
- CEF

# Notación de objetos JavaScript (JSON)
Es un formato de archivo usado para almacenar y transmitir datos. JSON es fácil de leer y escribir; además es ligero. Es comúnmente usado para transmitir datos en tecnologías web y usado en tecnologías de la nube.

## Componentes JSON
- Parejas clave-valor
- Comas
- Comillas dobles
- Paréntesis rizados "{}"
- Corchetes "[]"

### Pareja clave-valor
Conjunto de datos que representan dos elementos vinculados. Clave con su respectivo valor.

```JSON
"Alert": "Malware"
```

### Comas
Se utilizan para separar datos.
```JSON
"Alert": "Malware", "Alert code": 1090, "severidad": 10 
```

### Comillas dobles
Usados para encerrar cadenas de texto.

### Paréntesis rizados o llaves
Son usados para encerrar un objeto, es decir, un tipo de datos que almacena una lista separada por comas de pares clave-valor.

```JSON
"User":
{
	"id": "1234",
	"name": "user",
	"role": "engineer"
}
```

### Corchetes 
Los corchetes encierran arrays de datos, que es un tipo de dato que almacena datos en una lista ordenada separada por comas.
```JSON
["Administradores", "Users", "Engineering"]
```

# Syslog
Es un estándar para el registro y transmisión de datos.
## Capacidades
- **Protocolo**: El protocolo syslog se utiliza para transportar registros a un servidor de registros centralizado para su gestión.  Usa el puerto 514 para registros en texto plano, y el puerto 6514 para registros encriptados.
- **Servicio:** El servicio syslog actúa como un servicio de reenvío de registros que consolida los registros de múltiples fuentes en una única ubicación. Funciona mediante recepción y reenvío de cualquier entrada de registro syslog a un servidor remoto.
- **Formato de registro:** El formato Syslog es uno de los más utilizados. Es el formato de registros nativo de sistemas Unix. tiene tres componentes:
	- *Encabezado*
	- *Datos estructurados*
	- *Un mensaje*

## Elementos
**EJEMPLO:**
```Syslog
<236>1 2022-03-21T01:11:11.003Z virtual.machine.com evntslog - ID01 [user@32473 iut="1" eventSource="Application" eventID="9999"] This is a log entry!
```
### Encabezado

El encabezado contiene detalles como la marca de tiempo; el nombre de host, que es el nombre de la máquina que envía el registro; el nombre de la aplicación; y el ID del mensaje.

- **Marca** de tiempo: La marca de tiempo en este ejemplo es `2022-03-21T01:11:11.003Z`, donde `2022-03-21` es la fecha en formato AAAA-MM-DD.`T` se utiliza para separar la fecha y la hora. `01:11:11.003` es el formato de 24 horas de la hora e incluye el número de milisegundos 003. `Z` indica la zona horaria, que es el Tiempo Universal Coordinado (UTC).
- **Nombre de host**: virtual.machine.com
- **Aplicación**: evntslog
- **ID** del**mensaje**: ID01
### Datos estructurados

La parte de datos estructurados de la entrada del registro contiene información adicional sobre el registro. Esta información va entre corchetes y está estructurada en pares clave-valor. Aquí hay tres claves con sus valores correspondientes: `[user@32473 iut="1" eventSource="Application" eventID="9999"]`
### Mensaje

El mensaje contiene un mensaje de registro detallado sobre el evento. Aquí, el mensaje es `This is a log entry!.`

### Prioridad (PRI)

El Campo de prioridad (PRI) indica la urgencia del evento registrado y está contenido entre corchetes angulares. En este ejemplo, el valor de prioridad es `<236>`. Generalmente, cuanto más bajo es el nivel de prioridad, más urgente es el evento.

**Nota**: Los encabezados Syslog pueden combinarse con formatos JSON y XML. También existen formatos de registro personalizados.

# XML 
Utiliza etiquetas para almacenar e identificar datos.
## Elementos
- Elementos raíz
- Elementos hijo 

```XML
<Event>
	<EventID>4688</EventID>
	<Version>5</Version>
</Event>
```

El elemento `<Event>` es el elemento raíz y contiene dos elementos hijo `<EventID>, <Version>`. Cada hijo contiene datos.

## Atributos
Los elementos pueden contener atributos. Los atributos proporcionan información adicional sobre los elementos. Siempre deben ponerse entre comillas simples o dobles.

**Ejemplo:**
```XML
<EventData> 
	<Data Name='SubjectUserSid'>S-2-3-11-160321</Data> 
	<Data Name='SubjectUserName'>JSMITH</Data> 
	<Data Name='SubjectDomainName'>ADCOMP</Data> 
	<Data Name='SubjectLogonId'>0x1cf1c12</Data> 
	<Data Name='NewProcessId'>0x1404</Data> 
</EventData>
```

# CSV (Valores separados por coma)
Utiliza comas para separar los valores de los datos. La posición de los datos corresponde a su nombre de campo, el nombre del campo puede no estar incluido en el registro. Hay que tener claro qué campos son los que incluye un registro y su orden.

```CSV
2009-11-24T21:27:09.534255,ALERT,192.168.2.7,1041,x.x.250.250,80,TCP,ALLOWED,1:2001999:9,"ET MALWARE BTGrab.com Spyware Downloading Ads",1
```

# CEF (Formato de evento común)
Utiliza pares clave-valor para estructurar los datos e identificar los campos y sus valores correspondientes. Tiene los siguientes campos en su sintaxis.

```CEF
CEF:Version|Device Vendor|Device Product|Device Version|Signature ID|Name|Severity|Extension
```

**Nota:** Todo lo que aparezca en la parte Extension de la entrada del registro CEF debe escribirse en un formato clave-valor.

Combina syslog con CEF. 
**Ejemplo:**

```CEF
Sep 29 08:26:10 host CEF:1|Security|threatmanager|1.0|100|worm successfully stopped|10|src=10.0.0.2 dst=2.1.2.2 spt=1232
```

Esta entrada de registro contiene detalles sobre una aplicación Security llamada threatmanager que successfully stopped a worm de propagando desde la red interna en 10.0.0.2 a la red externa 2.1.2.2 a través del puerto 1232. Se informa de un nivel de gravedad alto de 10.

- **Syslog Timestamp:** Sep 29 08:26:10
- **Syslog hostname:** host
- **Extensión**: Este Campo contiene Datos escritos como pares clave-valor. Hay dos direcciones IP, `src=10.0.0.2` y `dst=2.1.2.2`, y un número de puerto de origen `spt=1232`. Las extensiones no son obligatorias y su adición es opcional.