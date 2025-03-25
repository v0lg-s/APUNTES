---

---
---
Un protocolo se refiere a un conjunto de reglas y convenciones que definen cómo deben comunicarse los dispositivos y sistemas en una red. Los protocolos son esenciales para garantizar que los datos puedan ser transmitidos, recibidos y comprendidos de manera coherente entre diferentes dispositivos y plataformas.

Cada capa de red del [[Modelo OSI|modelo OSI]] tiene distintos protocolos, que se activan en función del tipo de comunicación que se quiera establecer.
# Importancia
Las computadoras, al igual que los seres humanos, utilizan reglas o protocolos para comunicarse. Los protocolos son necesarios para que las computadoras se comuniquen correctamente a través de la red. Tanto en un entorno cableado como en uno inalámbrico, una red local se define como un área en la que todos los hosts deben "hablar el mismo idioma" lo que, en términos informáticos, significa que deben "compartir un protocolo común".

Si todas las personas de una misma sala hablaran idiomas diferentes, no podrían comunicarse. De manera similar, si los dispositivos de una red local no utilizaran los mismos protocolos, no podrían comunicarse.

Los protocolos de red definen muchos aspectos de la comunicación a través de la red local.
# Ejemplo
Si se requiere establecer una conexión web, se activará un protocolo específico para dicho tipo de comunicación. (HTTP y HTTPS)

# Comando Netstat
El comando *netstat* mostrará los protocolos en uso, la dirección local y los números de puerto, la dirección externa y los números de puerto y el estado de la conexión.![[protocolos.png]]

Podemos usar *netstat -r* para ver las rutas actuales conocidas por el equipo en su red, son las rutas contenidas en la tabla de ruteo.