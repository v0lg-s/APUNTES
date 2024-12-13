No todos los indicadores de compromiso aportan el mismo valor a los equipos de seguridad. La pirámide del dolor contribuye a la identificación de su peso o valor en cuanto a información para los equipos de seguridad.

![[piramideDolor.png]]

La Pirámide del Dolor capta la relación entre los indicadores de compromiso y el nivel de dificultad que experimentan los actores maliciosos cuando los indicadores de compromiso son bloqueados por los Equipos de Seguridad.

Cada uno de los tipos de indicadores de compromiso (en azul) se comparan con el nivel de "dolor" (en verde) que experimenta el atacante cuando los equipos de seguridad bloquean la actividad asociada al indicador de compromiso.

**Por ejemplo**, el bloqueo de una dirección IP asociada a un actor malicioso se etiqueta como fácil porque los actores maliciosos pueden utilizar fácilmente diferentes direcciones IP para sortear esto y continuar con sus esfuerzos maliciosos.

1. **Valores hash:** Hashes que corresponden a archivos maliciosos conocidos. Suelen utilizarse para proporcionar referencias únicas a muestras específicas de software malicioso o a archivos implicados en una intrusión.
2. **Direcciones IP**: Una Dirección de Protocolo de Internet como 192.168.1.1
3. **Nombres de dominio**: Una dirección web como www.google.com
4. **Artefactos de red**: Pruebas observables creadas por actores maliciosos en una red. Por ejemplo, información encontrada en protocolos de redes como las cadenas User-Agent.
5. **Artefactos de host:** Pruebas observables creadas por actores maliciosos en un host. Un host es cualquier dispositivo que esté conectado en una red. Por ejemplo, el nombre de un archivo creado por software malicioso.
6. **Herramientas**: Software que utiliza un actor malicioso para lograr su objetivo. Por ejemplo, los atacantes pueden utilizar herramientas de descifrado de contraseñas como John the Ripper para realizar ataques de contraseña con el fin de obtener acceso a una cuenta.
7. **Tácticas, Técnicas y Procedimientos (TTP)**: Se trata del comportamiento de un actor malicioso. Las Tácticas se refieren a la descripción general de alto nivel del comportamiento. Las técnicas proporcionan descripciones detalladas del comportamiento relacionado con la táctica. Los Procedimientos son descripciones muy detalladas de la técnica. Las TTP son las más difíciles de detectar.