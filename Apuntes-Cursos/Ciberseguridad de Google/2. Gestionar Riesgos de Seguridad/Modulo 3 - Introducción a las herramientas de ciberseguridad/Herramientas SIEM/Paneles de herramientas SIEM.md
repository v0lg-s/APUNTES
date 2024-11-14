![[Herramientas SIEM]]

# Paneles SIEM
Las aplicaciones de herramientas SIEM, como cualquier otra aplicación, buscan mostrar la información de manera simple y sencilla, de manera que los datos allí expuestos sean fáciles de analizar para los profesionales de seguridad, y que se tomen decisiones informadas a partir de esta información. 

Permiten a los profesionales de seguridad acceder de manera rápida y sencilla a la información de seguridad de una organización.

Presentan la información en cuadros, gráficas y tablas.  

*Ejemplo:*
![[panel SIEM.png]]
# Personalización y métricas
De acuerdo a los objetivos de seguridad de una organización, los paneles de las herramientas SIEM se pueden personalizar para que muestren distintas métricas. Las métricas son atributos técnicos clave entre los que se pueden encontrar:
- Tiempo de respuesta
- Disponibilidad
- Tasa de fallo
Estas métricas son usadas para evaluar el desempeño de una aplicación de software.


# Paneles de Splunk 
## Panel de postura de seguridad
Diseñado para los centro de operaciones de seguridad (SOC). 
Muestra: 
- Últimas 24 horas de eventos.
- Tendencias notables relacionadas con la seguridad de una organización.

Ayuda a gestionar la infraestructura interna de una organización mediante: 
- Recopilación
- Búsqueda
- Supervisión
- Análisis de datos de logs

Para obtener una visibilidad completa de las operaciones diarias de una organización.

## Panel de resumen ejecutivo
Analiza y supervisa la salud general de la organización a lo largo del tiempo. Ayuda a los equipos de seguridad a mejorar las medidas para minimizar el riesgo. Puede ser usado para:
- Proporcionar estadísticas de alto nivel a las partes interesadas.
- Generar un resumen de los incidentes de seguridad y tendencias durante un periodo de tiempo específico.

## Panel de revisión de incidentes
Permite a los analistas a identificar los patrones sospechosos que pueden producirse en caso de incidente.
- Resalta los elementos de mayor riesgo que necesitan revisión inmediata.
- Proporciona una cronología visual de los acontecimientos que conducen a un incidente.

## Panel de análisis de riesgos
Ayuda a los analistas a identificar el riesgo para cada objeto de riesgo (por ejemplo, un usuario, una computadora o una dirección IP específicos).
- Muestra cambios en el comportamiento relacionados con el riesgo. (Inicios de sesión fuera de las horas normales o tráfico de red inusualmente alto desde una computadora).
- Ayuda a los analistas a priorizar sus esfuerzos de mitigación de riesgos.

# Paneles de Chronicle
## Panel de estadísticas empresariales
- Destaca alertas recientes
- Identifica nombres de dominio sospechosos en los logs (IOC) Indicadores de compromiso.
- Cada resultado se etiqueta con una puntuación de confianza para indicar la probabilidad de una amenaza.
- Proporciona un nivel de gravedad que indica la importancia de cada amenaza para la organización.
- Se puede usar para monitorizar intentos de inicios de sesión desde ubicaciones o dispositivos poco habituales.

## Panel de ingestión de datos y salud
- Muestra el número de registros de eventos, fuentes de registro y las tasas de éxito de los datos que se están procesando en Chronicle.
- Se puede utilizar para asegurarse que las fuentes de registro están configuradas correctamente.

## Cuadro de mando de coincidencias COI
- Indica las principales amenazas, riesgos y vulnerabilidades para la organización.
- Se puede usar para observar los nombres de dominio, las direcciones IP y los COI de los dispositivos para identificar tendencias.
- Los analistas de Seguridad pueden utilizar este panel para buscar actividad adicional asociada a una alerta, como el inicio de sesión de un usuario sospechoso desde una ubicación geográfica inusual.

## Panel principal
- Muestra un resumen de alto nivel de la información relacionada con la actividad de ingestión de datos, alertas y eventos de la organización a lo largo del tiempo.
- Se puede acceder a una cronología de eventos de seguridad (como un pico de intentos fallidos de inicios de sesión)
- Se pueden identificarlas tendencias de las amenazas a través de las fuentes de registro, los dispositivos, las direcciones IP y las ubicaciones físicas.

## Panel de detección de reglas
- Proporciona estadísticas relacionadas con los incidentes de mayor incidencia, gravedad y detecciones a lo largo del tiempo.
- Se puede usar para acceder a una lista de todas las alertas activadas por una regla de detección específica, como una regla diseñada para alertar cada vez que un usuario abre un archivo adjunto malicioso conocido de un correo electrónico.
- Los analistas usan estas estadísticas para ayudar a gestionar los incidentes recurrentes y establecer tácticas de mitigación para reducir el nivel de riesgo.

## Panel general de inicio de sesión de usuario
- Proporciona información sobre el comportamiento de acceso de los usuarios en toda la organización.
- Se puede usar para acceder a una lista de todos los eventos de inicio de sesión de los usuarios para identificar actividades inusuales de los usuarios.

Esta información se utiliza para ayudar a mitigar las amenazas, los riesgos y las vulnerabilidades de las cuentas de usuario y las aplicaciones de la organización.
