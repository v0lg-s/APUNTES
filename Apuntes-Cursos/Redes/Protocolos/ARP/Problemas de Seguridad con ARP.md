En algunos casos, el uso de ARP puede ocasionar ciertos riesgos de seguridad.
# Envenenamiento ARP

Es posible "envenenar" ARP para suplantar la dirección MAC de un dispositivo, e interceptar las comunicaciones entre dos hosts. Básicamente el atacante emite una respuesta ARP falsa para que el dispositivo que necesita actualizar su tabla ARP tenga información falsa en ella.

## Mitigación de Problemas

Los switches modernos mitigan problemas relacionados a comunicaciones de tipo Broadcast.