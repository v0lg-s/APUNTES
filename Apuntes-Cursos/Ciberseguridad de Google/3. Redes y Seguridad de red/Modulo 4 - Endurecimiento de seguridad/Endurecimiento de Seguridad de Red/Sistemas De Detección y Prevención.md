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

|**Dispositivos / Herramientas**|**Ventajas**|**Desventajas**|
|---|---|---|
|Firewall|Un firewall permite o bloquea el tráfico basándose en un conjunto de reglas.|Un firewall sólo es capaz de filtrar paquetes basándose en la Información proporcionada en la cabecera de los paquetes.|
|Sistema de detección de intrusiones (IDS)|Un IDS detecta y alerta a los administradores sobre posibles intrusiones, ataques y otro tipo de tráfico malicioso.|Un IDS sólo puede escanear en busca de ataques conocidos o anomalías obvias; los ataques nuevos y sofisticados podrían no ser detectados. En realidad, no detiene el Tráfico entrante.|
|Sistema de prevención de intrusiones (IPS)|Un IPS monitorea la actividad del sistema en busca de intrusiones y anomalías y toma medidas para detenerlas.|Un IPS es un dispositivo en línea. Si falla, se interrumpe la conexión entre la red privada e Internet. Puede detectar falsos positivos y bloquear el tráfico legítimo.|
|Administración de información y eventos de seguridad (SIEM)|Una herramienta SIEM recopila y analiza los datos de registro de varios equipos de red. Agrega los eventos de Seguridad para su Monitoreo en un tablero central.|Una herramienta SIEM sólo informa sobre posibles Problemas de Seguridad. No lleva a cabo ninguna acción para detener o prevenir eventos sospechosos.|
