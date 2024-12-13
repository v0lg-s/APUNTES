Los IDS usan distintas técnicas para identificar patrones en comportamientos que puedan significar una amenaza o ataque.

Existen dos tipos de IDS
- **IDS basado en host:** Monitoriza la actividad interna de un host para identificar comportamiento no autorizado o anómalo. Como instalar una app no autorizada el IDS basado en hosts empieza a registrar y envía alertas.
- **IDS basado en red:** Monitoriza toda la actividad de la red para identificar comportamientos anómalos dentro de la red.

# Análisis basado en firmas
Es un método de detección usado para encontrar eventos de interés. 
- Una **firma** es un patrón que se asocia con actividad maliciosa, pueden contener patrones específicos como una secuencia de números binarios, bytes, o incluso datos específicos como una dirección IP.
	- **Firma antimalware** contiene patrones asociados al software malicioso. Esto puede incluir secuencias de comandos maliciosas que utiliza el software malicioso.
	- Si un evento coincide con la firma, el evento se registra y se genera una alerta.
- Los IoC y otros Indicadores de ataque pueden ser útiles para crear **firmas** específicas para detectar y bloquear ataques.

### **Ventajas**
- Baja tasa de falsos positivos.
### **Desventajas**
- Las firmas pueden ser evadidas, los atacantes pueden cambiar el comportamiento de su software malicioso para eludirlas. A esto se le denomina alterar la firma de un software malicioso.

- Las firmas requieren actualizaciones.

- Incapacidad de detectar amenazas desconocidas.

# Análisis basado en anomalías
El **Análisis basado en anomalías** es un Método de Detección que identifica comportamientos anómalos. Consta de dos fases: 
- **Fase de Entrenamiento** aquí debe establecerse una línea de base del comportamiento normal o esperado. Las líneas de base se desarrollan recopilando datos que corresponden al comportamiento normal del sistema. 
- **Fase de Detección**, la actividad actual del sistema se compara con esta línea de base. La actividad que se produce fuera de la línea de base se registra y se genera una alerta.

### **Ventajas**

- **Capacidad para detectar amenazas nuevas y en evolución:** A diferencia del análisis basado en firmas, que utiliza patrones conocidos para detectar amenazas, el análisis basado en anomalías _puede_ detectar amenazas desconocidas.

### **Desventajas**
- **Alto índice de falsos positivos:** Cualquier comportamiento que se desvíe de la línea de base puede ser marcado como anómalo, incluidos los comportamientos no maliciosos. Esto conduce a una alta tasa de falsos positivos.
    
- **Compromiso pre existente**: La existencia de un atacante durante la fase de Entrenamiento incluirá comportamientos maliciosos en la línea de base. Esto puede llevar a pasar por alto a un atacante preexistente.