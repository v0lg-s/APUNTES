# WEP (Wired Equivalent Privacy)
Es un protocolo de seguridad inalámbrica diseñado para que, cómo lo indica su nombre, proporcione el mismo nivel de privacidad en conexiones inalámbricas que el nivel disponible en conexiones por cable.

Desarrollado en 1999, actualmente en desuso y bastante inseguro. **Protocolo de seguridad de alto riesgo.**

# WPA (Wi-Fi Protected Access)
Se desarrolló en 2003 para mejorar y sustituir WEP. Se pretendía que fuera una medida transitoria. Los fallos de WEP estaban en cómo se utilizaba la encriptación. WPA utilizó un protocolo llamado Protocolo de Integridad de Clave Temporal (TKIP).
- El algoritmo de encriptación de WPA usa claves secretas más grandes que las WEP, esto hace más dificil adivinar la clave por prueba y error.
- Incluye comprobación de integridad con una etiqueta de autenticación del mensaje. Esta comprobación rechaza la transmisión si un atacante intenta alterar la transmisión y reenviarla.
- **Debilidades:** 
	- Los atacantes usan un ataque de reinstalación de claves (KRACK) para desencriptar las transmisiones con WPA.
	- Los atacantes pueden introducirse en el proceso de protocolo de enlace de autenticación WPA e insertar una nueva clave de encriptación en lugar de la dinámica asignada por WPA. Si establecen la nueva clave en todos ceros, es como si la transmisión no estuviera encriptada en absoluto.

# WPA2
Es la segunda versión de WPA. Se lanzó en 2004.
- Mejora la anterior versión utilizando el Estándar de Encriptación Avanzada (AES). 
- Mejora el uso de TKIP.
- Utiliza el protocolo de código de autenticación de mensajes mediante cadena de bloques de cifrado en modo contador (CCMP), que proporciona encapsulación y garantiza la autenticación e integridad de los mensajes.
- **Debilidad:**
	- Es vulnerable a ataques KRACK.

## Modo Personal
Adecuado para redes domésticas por:
- Fácil de configurar.
- Menos tiempo en la configuración inicial que en el modo empresarial.
- La frase de contraseña global o clave de encriptación (clave que protege la red inalámbrica encriptando la información) debe aplicarse a cada una de las computadores y accesos de una red. Ideal para redes domésticas.

## Modo Empresarial
- Proporciona la seguridad necesaria para entornos empresariales.
- Configuración inicial más complicada.
- Ofrece un control individualizado y centralizado de la accesibilidad Wi-Fi. (Admins de la red pueden retirar o conceder acceso a los usuarios en cualquier momento)
- Los usuarios de la red nunca tienen acceso a las claves de encriptación. (No pueden recuperar las claves de red)

# WPA3
WPA3 es un protocolo Wi-Fi seguro y su uso está creciendo a medida que salen al mercado más dispositivos compatibles con WPA3. Estas son las diferencias clave entre WPA2 y WPA3:

- WPA3 aborda la vulnerabilidad del protocolo de enlace de autenticación a los ataques KRACK, presente en WPA2.
    
- WPA3 utiliza la Autenticación Simultánea de Iguales (SAE), un acuerdo de autenticación de contraseñas y uso compartido de claves de cifrado. Esto impide que los atacantes descarguen datos de las conexiones de redes inalámbricas a sus sistemas para intentar descodificarlos.
    
- WPA3 ha aumentado la encriptación para que las contraseñas sean más seguras utilizando una encriptación de 128 bits, y el modo WPA3-Enterprise ofrece una encriptación opcional de 192 bits.

