![[Controles de seguridad]]

Los controles pueden ser *físicos, técnicos y administrativos*. *Detectan, previenen o corrigen* los problemas de seguridad.

# Tipos de controles
## Preventivos
Diseñados para prevenir que ocurra un incidente en primer lugar.
## Correctivos
Usados para restaurar un activo tras un incidente.
## Detectores
Implementados para determinar si un incidente ya ocurrió o se encuentra en progreso.
## Disuasorio
Diseñados para desalentar/disuadir un ataque.

# Categorías de controles
## Controles físicos
Usados para limitar el acceso a activos físicos por parte de personal no autorizado.
- Puertas, vallas y cerraduras
- Guardias de seguridad
- Circuito cerrado de Televisión (CCTV), sensores de movimiento y cámaras de vigilancia
- Tarjetas de acceso o distintivos para entrar a los espacios de oficina

|                                   **Nombre del Control**                                   | **Tipo de Control ** |                                                                                                                        **Propósito del Control **                                                                                                                         |
| :----------------------------------------------------------------------------------------: | :------------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|                                  Caja fuerte temporizada                                   |       Disuasor       |                                                                                                Reducir la superficie de ataque y el impacto global de las amenazas físicas                                                                                                |
|                                    Iluminación adecuada                                    |       Disuasor       |                                                                                                              Disuadir las amenazas limitando los «escondites                                                                                                              |
|                            Circuito cerrado de Televisión(CCTV)                            | Preventivo/Detector  | El circuito cerrado de televisión es a la vez un control preventivo y de detección, ya que su presencia puede reducir el riesgo de que se produzcan determinados tipos de sucesos, y puede utilizarse después de un suceso para informar sobre las condiciones del mismo. |
|                        Armarios con cerradura (para equipos de red)                        |      Preventivo      |                                                      Reforzar la integridad impidiendo que personal no autorizado y otras personas accedan físicamente a los equipos de la infraestructura de red o los modifiquen.                                                       |
|                Señalización que indica el proveedor de servicios de alarma                 |       Disuasor       |                                                                                    Disuadir ciertos tipos de amenazas haciendo que la probabilidad de éxito de un ataque parezca baja.                                                                                    |
|                                          Candados                                          | Disuasor/Preventivo  |                                                                               Reforzar la integridad disuadiendo e impidiendo que personal no autorizado acceda físicamente a los activos.                                                                                |
| Detección y prevención de incendios (alarma contra incendios, sistema de rociadores, etc.) | Detector/Preventivo  |                                                                               Detectar incendios en ubicaciones físicas y evitar daños a activos físicos como inventarios, servidores, etc.                                                                               |

## Controles Técnicos
Soluciones como:
- Firewalls
- MFA
- Software Antivirus

|             **Nombre del Control**             | **Tipo de Control ** |                                 **Propósito del Control **                                  |
| :--------------------------------------------: | :------------------: | :-----------------------------------------------------------------------------------------: |
|                    Firewall                    |      Preventivo      |           Filtrar el tráfico no deseado o malicioso y evitar que entre en la red            |
|                    IDS/IPS                     |       Detector       |          Detectar e impedir el tráfico anómalo que coincida con una firma o regla           |
|                  Encriptación                  |       Disuasor       |                  Garantizar la confidencialidad de la información sensible                  |
|                    Backups                     |      Correctivo      |                             Restaurar/recuperarse de un suceso                              |
|             Gestión de contraseñas             |      Preventivo      |                              Reducir la fatiga de contraseñas                               |
|            Antivirus (AV) software             |      Correctivo      |                    Detectar y poner en cuarentena las amenazas conocidas                    |
| Monitoreo manual, mantenimiento e intervención |      Preventivo      | Identificar y gestionar las amenazas, riesgos o vulnerabilidades de los sistemas obsoletos. |
## Controles administrativos
Están relacionados con el componente humano de la ciberseguridad. Incluye políticas y procedimientos que definen como una organización gestiona la información y define claramente las responsabilidades se sus empleados. Aunque son típicamente controles basados en políticas, el cumplimiento de ellas puede requerir el uso de controles técnicos o físicos.

|       **Nombre del Control**        | **Tipo de Control ** |                                                                           **Propósito del Control **                                                                           |
| :---------------------------------: | :------------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|          Menor privilegio           |      Preventivo      |                                                Reducir el riesgo y el impacto global de las cuentas maliciosas o comprometidas.                                                |
| Planes de recuperación de desastres |      Correctivo      |                                                                   Garantizar la continuidad de la actividad                                                                    |
|      Políticas de contraseñas       |      Preventivo      |                          Reducir la probabilidad de que una cuenta se vea comprometida mediante técnicas de ataque de fuerza bruta o de diccionario.                           |
|   Políticas de control de acceso    |      Preventivo      |                                 Reforzar la confidencialidad y la integridad definiendo qué grupos pueden acceder a los datos o modificarlos.                                  |
|   Políticas de gestión de cuentas   |      Preventivo      | Gestionar el ciclo de vida de las cuentas, reducir la superficie de ataque y limitar el impacto global de los antiguos empleados descontentos y el uso de cuentas por defecto. |
|       Separación de funciones       |      Preventivo      |                                                Reducir el riesgo y el impacto global de las cuentas maliciosas o comprometidas.                                                |
