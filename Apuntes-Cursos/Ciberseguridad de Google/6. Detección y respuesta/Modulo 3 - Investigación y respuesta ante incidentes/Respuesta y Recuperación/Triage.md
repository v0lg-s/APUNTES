El proceso de triage como en un hospital, consiste en evaluar la urgencia médica de un paciente para establecer el orden en que será atendido y gestionar los recursos limitados. Así mismo, en seguridad informática, debemos evaluar la importancia de un evento de seguridad y su impacto para la organización, para asignar un nivel de prioridad.

El proceso consta de 3 pasos:
1. **Recibir y evaluar:** Se evalúa si se trata de un falso positivo y si está relacionado con un incidente existente.
	- **¿Es la alerta un Falso positivo?** Se debe determinar si la alerta es un auténtico problema de Seguridad o un falso **positivo**, o una alerta que detecta incorrectamente la presencia de una amenaza.
	- **¿Se activó esta alerta en el pasado?** En caso afirmativo, ¿cómo se resolvió? La historia de una alerta puede ayudar a determinar si se trata de un Problema nuevo o recurrente.
	- **¿Está la alerta activada por una vulnerabilidad conocida?** Si una alerta se dispara por una vulnerabilidad conocida, los analistas de Seguridad pueden aprovechar los conocimientos existentes para determinar una respuesta adecuada y minimizar el impacto de la vulnerabilidad.
	- **¿Cuál es la gravedad de la alerta?** La gravedad de una alerta puede ayudar a determinar la prioridad de la respuesta para que los problemas críticos se escalen rápidamente.
	
2. **Asignar prioridad:** Cuando se confirma que es un positivo verdadero, se establece su prioridad basándose en las políticas y lineamientos de la organización.
- Se valoran elementos como el **impacto funcional** (Prestación del servicio/disponibilidad), **impacto en la información** (Triada CID, robo de datos) y la  **fiabilidad de la recuperación** (¿Es posible la recuperación? si no, para que gastar tiempo y recursos.) 
4. **Recolectar y analizar:** Se recolecta y analiza la evidencia asociada con la alerta, como registros del sistema.