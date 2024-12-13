Una vez la línea base ha sido determinada, el siguiente paso importante es monitorear la red para identificar desviaciones de la línea base.
- Examinar los *componentes de la red* para detectar actividad inusual.
- **Actividad inusual:** Transferencias de datos grandes e inusuales, por ejemplo.

# Componentes de red a ser monitorizados

## Análisis de flujo
El flujo se refiere al movimiento de las comunicaciones en la red, este incluye información relacionada con paquetes, protocolos y puertos.

Los atacantes pueden utilizar puertos y protocolos que no están comúnmente asociados, esto lo hace para mantener comunicación entre su maquina y el sistema comprometido. A lo anterior se le denomina **comando y control**.

**Por ejemplo**, los actores maliciosos pueden utilizar el protocolo HTTPS a través del puerto 8088 en lugar de su puerto comúnmente asociado 443 para comunicarse con los sistemas comprometidos.

## Información sobre la carga útil de paquetes
Las organizaciones pueden monitorizar la información de la carga útil de los paquetes para descubrir actividades inusuales, como datos sensibles que se transmiten fuera de la red, lo que podría indicar un posible ataque de exfiltración de datos.

## Patrones temporales
Los paquetes contienen información relacionada al tiempo. Es útil analizar esta información para encontrar patrones inusuales de tiempo, es decir, flujo de datos durante instantes en los que es poco usual tener tráfico de red presente.

**Por ejemplo**, una empresa que opera en Norteamérica experimenta grandes flujos de tráfico entre las 9 de la mañana y las 5 de la tarde, que es la línea de base de la actividad normal de la red. Si de repente aparecen grandes volúmenes de tráfico fuera de las horas normales de actividad de la red, se considera que está fuera de la línea de base y debe investigarse.

# NOC Network Operations Center
Es una unidad organizativa encargada de la supervisión de la red y la respuesta ante interrupciones. Un NOC es responsable de mantener el rendimiento, la disponibilidad y el tiempo de actividad de la red.

