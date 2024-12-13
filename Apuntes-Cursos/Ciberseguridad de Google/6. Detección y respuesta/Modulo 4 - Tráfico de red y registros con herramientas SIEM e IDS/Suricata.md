Es un sistema de detección de intrusiones, un sistema de prevención de intrusiones y una herramienta de análisis de red.

## Características
- Es de código abierto
- Cuando funciona como **IDS** monitoriza el tráfico de red y alertar sobre actividades sospechosas e intrusiones.
- Puede configurarse como un **IDS** basado en host.
- Cuando funciona como **IPS** detecta y bloquea actividades y tráfico maliciosos. Requiere una configuración adicional.
- Cuando funciona en el modo de **Monitoreo de seguridad de red NSM**produce y guarda registros de red relevantes. Puede analizar el tráfico de red en directo, los archivos de captura de paquetes existentes y crear y guardar capturas de paquetes completas o condicionales. Esto puede ser útil para análisis forenses, respuesta ante incidentes y para probar firmas.

## Reglas o firmas

**Nota** El orden de las reglas se refiere al orden en que éstas son evaluadas por Suricata. Las reglas se procesan en el orden en que están definidas en el archivo de configuración. Sin embargo, Suricata procesa las reglas en un orden diferente por defecto: ``pass``, ``drop``, ``reject`` y ``alert``. El orden de las reglas afecta al veredicto final de un paquete, especialmente cuando se producen acciones contradictorias, como cuando una regla de abandono y una de alerta coinciden en el mismo paquete.

## Archivo de configuración
El archivo de configuración de Suricata es suricata.yaml, que utiliza el formato de archivo YAML para la sintaxis y la estructura. Los archivos de configuración le permiten personalizar exactamente cómo desea que su IDS interactúe con el resto de su entorno.

## Archivos de registro
Suricata genera dos archivos cuando se activan las alertas:
- **eve.json:** Es el archivo estándar de registro en Suricata. Los eventos de este archivo contienen un identificador único llamado flow_id que se utiliza para correlacionar los registros o alertas relacionados con un único flujo de red, lo que facilita el análisis del tráfico de red. (contiene información detallada y metadatos sobre los eventos y alertas generados)
- **fast.log:** Se utiliza para registrar información mínima sobre alertas, incluyendo detalles básicos sobre la dirección IP y el puerto del tráfico de red. El archivo fast.log se utiliza para el registro y las alertas básicas y se considera un formato de archivo heredado y no es adecuado para tareas de respuesta ante incidentes o de caza de amenazas.