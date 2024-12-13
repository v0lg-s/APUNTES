# SIEM
- [[Herramientas SIEM]] Cómo funcionan estas herramientas?

1. **Recolectan y agregan datos:** Usualmente en forma de logs, provenientes de IDS, IPS, EDR, firewalls, servidores, routers y más.
2. **Normaliza la información:** Esto significa que los datos en crudo tomados por la herramienta SIEM serán limpiados y procesados removiendo atributos no esenciales.
3. **Analiza la información:** Esta información es analizada de acuerdo a reglas pre establecidas, compara esta información contra un conjunto de reglas para detectar posibles incidentes de seguridad. Posteriormente categoriza o reporta estos incidentes.
## Ventajas de SIEM
- **Accesibilidad a los Datos de Eventos:** Las herramientas SIEM proporcionan acceso a los datos de eventos y actividades que se producen en una red, incluida la actividad en tiempo real. 
- **Monitorear, Detectar y Alertar:** Las herramientas SIEM supervisan continuamente los sistemas y las redes en tiempo real. A continuación, analizan los Datos recopilados utilizando reglas de Detección para detectar actividades maliciosas. Si una actividad coincide con la regla, se genera una alerta y se envía para que los equipos de Seguridad la evalúen.
- **Almacenamiento de registros:** Las herramientas SIEM pueden actuar como un sistema de retención de datos, que puede proporcionar accesibilidad a los datos históricos. Los Datos pueden conservarse o borrarse después de un periodo dependiendo de los Requisitos de una organización.
# SOAR
SOAR (Security Orchestration, Automation and Response), es una colección de aplicaciones, herramientas y flujos de trabajo que usan automatización para responder a eventos de seguridad.