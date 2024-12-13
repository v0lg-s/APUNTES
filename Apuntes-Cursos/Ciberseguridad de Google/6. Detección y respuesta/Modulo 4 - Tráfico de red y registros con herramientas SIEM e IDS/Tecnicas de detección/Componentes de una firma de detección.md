# Componentes de una regla de IDS basado en red NIDS

Los componentes son:
- Acción
- Encabezado 
- Opciones de reglas
## Acción
- Determina la acción a tomar si los criterios de la regla coinciden.
- Algunas acciones comunes son: `Alert`, `Pass`, `Drop` o `Reject`. Pueden variar según el IDS.

### Alert
Instruye al IDS de alertar acerca de tráfico de red especificado. El IDS revisará los paquetes y enviará una alerta en caso de que las reglas coincidan.
### Drop
Esta acción también genera una alerta, pero descarta el tráfico. Esto solo sucede en un IPS.
### Pass
Esta acción permite que el tráfico pase a través de la interfaz de red. Se puede usar para hacer caso omiso de otra regla en un caso especifico. **Ejemplo:** Una excepción a una regla con ``drop`` se puede hacer con ``pass``.
### Reject
Esta acción no permite el paso de tráfico. Con esta acción, se envía un paquete TCP con la flag *reset* esto indica a los computadores que dejen de enviar mensajes entre sí.
## Encabezado
- Dirección IP de origen y destino.
- Puertos de origen y destino.
- Protocolos.
- Dirección de tráfico.
**Ejemplo**
Si queremos verificar tráfico sospechoso en un puerto debemos definir primero la fuente del tráfico sospechoso en el encabezado. Se pueden especificar IP's externas y protocolos.
`tcp 10.120.170.17 any -> 133.113.202.181 80`

*IP*
Origen: 10.120.170.17
Destino: 133.113.202.181

*Puerto*
Origen: Cualquiera
Destino: 80

## Opciones de reglas
Usualmente están separadas por ";" y encerradas en paréntesis.

**Ejemplo:**

```
(msg:"Esto es un mensaje";sid:12345;rev:1;)
```

- El primer campo *"msg"* se refiere al mensaje que imprimirá la alerta.
- El campo "*sid*" es el identificador único de la firma. Significa SignatureID
- El campo "*rev*" significa revisión. Cada vez que una firma se cambia o actualiza el número de este campo cambia.

# Ejemplo de firma
```bash
alert http $HOME_NET any -> $EXTERNAL_NET any (msg:"GET on wire"; flow:established; content:"GET"; sid:12345; rev:1;)
```
