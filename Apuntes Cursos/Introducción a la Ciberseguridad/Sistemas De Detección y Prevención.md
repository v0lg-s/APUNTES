# IDS (Sistema de Detección de Intrusiones)
Puede ser una de varias herramientas en un servidor, firewall o sistema operativo; también puede ser un dispositivo dedicado en la red.

## Funcionamiento
Escanea datos junto a una base de datos de reglas o firmas maliciosas, en busca de tráfico malicioso.
- El IDS ==no toma medidas contra una amenaza== sino que crea una alerta para un administrador de la red.
- Detecta, registra y genera informes.
- Sus análisis ralentizan la red por lo que se coloca fuera de línea o en paralelo a la comunicación por lo que solo "observa" lo que pasa más no interviene.

![[IDS.png]]

# IPS (Sistemas de Prevención de Intrusiones)

A diferencia del IDS el IPS si puede bloquear o denegar el tráfico según una regla positiva o coincidencia de firma.

## Funcionamiento
- Detecta sondeos, ataques y escaneos de puertos.
- Se integra con otras herramientas para generar informes, mejorar rendimiento o analizar registros.
- El IPS si intercepta y analiza en tiempo real el tráfico entrante a la red.
- *Snort* es uno de los más reconocidos.

![[IPS.png]]