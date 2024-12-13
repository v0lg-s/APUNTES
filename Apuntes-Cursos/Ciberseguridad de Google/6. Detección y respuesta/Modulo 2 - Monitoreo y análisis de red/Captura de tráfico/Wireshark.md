Es un analizador de protocolos de código abierto, Tiene interfaz gráfica. 

# Filtros de visualización
Wireshark permite aplicar filtros de visualización sobre los archivos de captura de paquetes. Se pueden aplicar filtros como: Protocolos, direcciones IP, puertos y cualquier otra propiedad posible de un paquete.

# Operadores

## Operadores de comparación
Se pueden usar operadores en forma abreviada para localizar campos de cabecera y valores específicos. Por ejemplo:

```
ip.src == 8.8.8.8
&
ip.src eq 8.8.8.8
```

Son equivalentes.

| **Tipo de Operador** | **Símbolo** | **Abreviatura** |
| -------------------- | ----------- | --------------- |
| Igual                | ==          | eq              |
| No igual             | !=          | ne              |
| Mayor que            | >           | gt              |
| Menor que            | <           | lt              |
| Mayor o igual que    | >=          | ge              |
| Menor o igual que    | <=          | le              |

## Operador de contención
El operador `contains` se utiliza para filtrar los paquetes que contienen una coincidencia exacta de una cadena de texto. **Ejemplo:**

![[EjemploWiresharkContains.png]]Muestra todos los flujos HTTP que coinciden con la palabra clave "moved".

## Operador de coincidencias
El operador `matches` se utiliza para filtrar los paquetes basándose en la expresión regular (regex) especificada.

# Filtrado
## Filtrado por protocolos
Es tan simple como poner el nombre del protocolo en la barra de herramientas de filtrado.
- telnet
- arp
- dns
- http
- ftp
- ssh
- icmp

## Filtrado por dirección IP
Se pueden localizar paquetes con una dirección específica. 
- Para filtrar paquetes que contengan una dirección IP específica:
	- `ip.addr == 172.21.224.2`
- Para filtrar paquetes provenientes de una dirección IP de origen específica:
	- `ip.src == 10.10.10.10`
- Para filtrar paquetes enviado a una dirección IP de destino específica:
	- `ip.dst == 4.4.4.4`

## Filtrado por dirección MAC
```
eth.addr == 00:70:f4:23:18:c4
```

## Filtrado de puertos
El Filtrado de puertos se utiliza para filtrar paquetes basándose en los números de puerto. Esto resulta útil cuando se desea aislar tipos específicos de Tráfico. El Tráfico DNS utiliza el puerto 53 TCP o UDP por lo que esto listará el tráfico relacionado con las consultas y respuestas DNS solamente.

**Ejemplo:**
- Para filtrar por un puerto UDP:
	`udp.port == 53`

- Para filtrar por un puerto TCP:
	`tcp.port == 25`