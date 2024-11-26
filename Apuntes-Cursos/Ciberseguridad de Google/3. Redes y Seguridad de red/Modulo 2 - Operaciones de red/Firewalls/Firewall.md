Un firewall o cortafuegos es un dispositivo de red que monitorea el tráfico desde y hacía nuestra red. 
- Bloquea o permite el tráfico basado en un conjunto de reglas establecidas.

Tiene funciones como *Filtrado de Puertos* que bloquea o habilita cierto número de puertos para limitar comunicaciones no deseadas.

**Por ejemplo:** Un firewall se puede configurar de tal manera que solo acepte comunicaciones por el puerto 443 HTTPS y bloquear el resto de comunicaciones y puertos. Esto se define según las necesidades de la organización.

# Firewalls según la infraestructura
## Firewall de Hardware
Es un dispositivo físico que analiza cada paquete antes de dejarlo entrar a la red.
- Tiene un mayor costo que el firewall de software típicamente.
## Firewall de Software
Realiza la misma tarea que un Firewall de Hardware solo que no es un dispositivo físico sino que es un programa de computador. Si el firewall está instalado en un computador, analizará todo el tráfico que este computador recibe. Si está instalado en un servidor, protegerá a todos los dispositivos conectados al servidor.

- Usa capacidad de procesamiento del dispositivo en el que está instalado.
## Firewalls basados en la nube
Software de firewall alojado en la nube de un proveedor de servicios. FaaS (Firewall as a Service)

# Firewalls según el tipo de operación
## Firewall de estado
Es un tipo de Firewall que realiza un seguimiento de la información que pasa a través de él y filtrar las amenazas de manera proactiva.
- Analiza la red en busca de características y comportamiento que pueda parecer sospechoso y bloquearlos de la red.

## Firewall sin estado
Es un tipo de firewall que opera basado en reglas predefinidas y no mantiene un seguimiento a la información de los paquetes de datos.
- Las reglas predefinidas por el administrador le dicen al router qué debe aceptar y que debe rechazar de la red.

**Menos seguros que los Firewalls de estado**

## Firewalls de Próxima Generación (NGFWs)
Son aún más seguros que los firewalls de estado. Proveen de:
- Inspección profunda de paquetes.
- Protección contra intrusión
- Inteligencia de amenazas: puede conectarse a servicios de inteligencia sobre amenazas basados en la nube y actualizarse rápidamente contra las ciberamenazas emergentes