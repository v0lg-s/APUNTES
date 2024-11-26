Es un dispositivo o ordenador que funciona como intermediario entre un usuario y un sitio web, permitiendo que el usuario se conecte a Internet de forma indirecta.

Los servidores proxy utilizan la traducción de direcciones de red (NAT) para servir de barrera entre los clientes de la red y las amenazas externas. Los proxies directos gestionan las consultas de los clientes internos cuando acceden a Recursos externos a la red. Los proxies inversos funcionan de forma opuesta a los proxies directos; gestionan las peticiones de sistemas externos a servicios de la red interna. Algunos servidores proxy también pueden configurarse con reglas, como un firewall. Por ejemplo, puede crear filtros para bloquear los sitios web identificados por contener software malicioso.

- También son usados para bloquear sitios web inseguros que usuarios de una red organizacional no tienen permitido acceder.
- Usa memoria temporal para almacenar información que solicitan regularmente los servidores externos, así no tiene que buscar la información en el servidor interno, esto reduce el contacto del servidor interno con exterior mejorando la seguridad.

# Tipos de servidores proxy
## Servidor Proxy de reenvío
Regula y restringe el acceso de una persona a internet.
- Objetivo: Ocultar la dirección IP del usuario y aprobar las solicitudes salientes.
	- **Ejemplo:** Recibe el tráfico saliente de un empleado, lo aprueba y lo reenvía al destino en internet.

## Servidor Proxy Inverso
Regula y restringe el acceso de internet a un servidor interno. Funciona, cómo lo dice su nombre, de manera inversa al de reenvío.
- Objetivo: Aceptar el tráfico de terceros, aprobarlo y reenviarlo a los servidores internos.
- Útil para proteger servidores internos con datos confidenciales para que no expongan su dirección IP a terceros. 

## Servidor Proxy de Correo Electrónico
Filtra el spam verificando si la dirección del remitente fue falsificada. Reduce el riesgo de ataques de suplantación de identidad.

# Diferencia con un firewall
Un firewall es como un guardia de seguridad que protege la puerta de tu red, mientras que un proxy es como un mensajero que envía y recibe información en tu nombre, ocultando tu identidad.

**Firewall:**
- Actúa como una barrera entre tu red y el mundo exterior (internet).
- Examina el tráfico de red entrante y saliente en busca de actividades sospechosas basándose en reglas predefinidas.
- Bloquea cualquier tráfico que considere peligroso.
- Opera a nivel de red, analizando las direcciones IP y los puertos.

**Proxy:**
- Actúa como un intermediario entre tu dispositivo y el internet.
- Oculta tu dirección IP real, lo que proporciona un nivel adicional de anonimato.
- Puede almacenar en caché el contenido web para acelerar los tiempos de carga.
- Puede filtrar el contenido web, bloqueando sitios web específicos o tipos de contenido.
- Opera a nivel de aplicación, analizando el tráfico web, FTP, etc.