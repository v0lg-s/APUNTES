*OWASP* es una comunidad dedicada a determinar y combatir las causas que hacen que el software sea inseguro.
Es una sigla en inglés (Open Web Applications Security Project).

# Principios
## 1. Minimizar el área de la superficie de ataque
Implica reducir el número de flancos por dónde pueden atacar a la organización.
- *Superficie de ataque:* Se refiere a todas las posibles vulnerabilidades que un atacante puede aprovechar y explotar.
- Los equipos de seguridad pueden:
	- Deshabilitar características específicas de un software.
	- Restringir el acceso a ciertos activos.
	- Establecer requerimientos de contraseña más complejos.
## 2. Principio de privilegio mínimo
Implica asegurarse de que los usuarios tienen la menor cantidad de privilegio o acceso. Lo mínimo para que pueda realizar su trabajo.
- Esto puede *reducir* la cantidad de daño que una violación de seguridad pueda ocasionar.
### Ejemplo
Un analista de seguridad Jr puede tener acceso a los datos de registro pero puede no tener acceso a cambiar los permisos de usuario. Si un atacante compromete este usuario no podrá desplegar un ataque de mayor magnitud.

## 3. Defensa en profundidad
Implica que una organización debe tener múltiples controles de seguridad que aborden riesgos y amenazas de diferentes maneras.

Realizar esto pone múltiples obstáculos en el camino de un atacante.
### Ejemplo
- MFA (Multifactor Authentication)
- Firewalls
- Sistemas de detección y prevención ([[Sistemas De Detección y Prevención|IDS]])

## 4. Separación de privilegios
Implica dividir los privilegios y responsabilidades de un sistema informático entre diferentes componentes o entidades. 
*"A nadie se le deberían dar tantos privilegios que pueda hacer mal uso del sistema."*
### Ejemplo
La persona encargada de firmar cheques no debería estar también encargada de hacerlos. Esto le da el poder de usar de manera inapropiada sus responsabilidades.

## 5. Mantener la seguridad simple
Las soluciones innecesariamente complicadas deberían ser evitadas, estas se pueden volver inmanejables.
*"Mantener los controles de seguridad lo más simples posibles"* Entre más complicados sean más difícil hará la colaboración entre personas.

## 6. Arreglar correctamente los problemas de seguridad
Incluye:
- Asegurarse que las medidas y reparaciones realizadas para corregir un problema de seguridad funcionan. Se deben llevar a cabo evaluaciones para garantizar que estas reparaciones son efectivas.
- Encontrar rápidamente la raíz del problema de seguridad cuando ocurre un incidente.

## 7. Establecer valores predeterminados seguros
El estado de seguridad por defecto de una aplicación debería ser *óptimo*. Debilitar la seguridad del sistema debería implicar un esfuerzo adicional. 

## 8. Fallar con seguridad
Cuando un control falla o se detiene, debe fallar pasando al modo por defecto más seguro.
### Ejemplo
Cuando un firewall falla, debería cerrar todas las conexiones y rechazar las nuevas. *NO* empezar a aceptar todas las conexiones.

## 9. No confíes en los servicios
Muchas veces las organizaciones usan servicios de terceros que pueden tener políticas de seguridad distintas. Es importante que la aplicación/organización realice sus propios controles y no confiar explícitamente en la seguridad de sus socios.
### Ejemplo
Si un proveedor externo realiza el seguimiento de los puntos de recompensa de los clientes de una aerolínea, ésta debería asegurarse de que el saldo es exacto antes de compartir esa información con sus clientes.

## 10. Evitar la seguridad por oscuridad u ocultamiento
La seguridad de una aplicación no se debe fundamentar en mantener el código fuente en secreto. Se deben implementar medidas adicionales. 
Debemos siempre pensar en que el código será visible, porque en alguna violación se puede exponer este, y si la seguridad se basó simplemente en ocultarlo, ese detalle será la perdición de esa aplicación. 
- Políticas de contraseñas razonables
- Defensa en profundidad
- Límites de transacciones comerciales
- Arquitectura de red sólida
- Controles de fraude y auditoría.