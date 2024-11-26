Una zona de seguridad o Security Zone es un segmento de una red que protege la red interna, del internet. Hacen parte de una técnica o práctica de seguridad que divide una red en segmentos llamada *segmentación de redes*/[[Qué Es Subnetting|subnetting]].

Esta técnica de seguridad permite mantener la privacidad y seguridad de una red. Por ejemplo, un hotel puede dar acceso gratuito a sus huéspedes, esa red abierta e insegura la va a mantener separada de sus redes encriptadas usadas por el personal del hotel. 

Segmentar en subredes también ofrece privacidad entre departamentos de una organización, por ejemplo, en una red universitaria, la red de la facultad estará separada de la red de estudiantes, si la red de estudiantes se ve vulnerada, los administradores de red pueden aislar la red y mantener el resto de la red libre.

# Tipos de zonas de seguridad
## Zona sin control
Cualquier red fuera del control de la organización.
## Zona controlada
Subred que protege la red interna de la zona sin control.

### Áreas en la zona controlada
#### DMZ (Demilitarized Zone/Zona Desmilitarizada)
Contiene servicios públicos que pueden acceder a internet.
- Servidores web
- Servidores Proxy que ofrecen sitios web al público
- Servidores DNS que proveen IP's a usuarios de internet

Actúa como red de perímetro a la red interna.

#### Red interna
Contiene servidores privados que la organización quiere proteger. 

Dentro de esta red se encuentra la zona restringida.

##### Zona restringida
Esta zona protege la información altamente confidencial a la que sólo pueden acceder los empleados con determinados privilegios.

![[zonasControladas.png]]