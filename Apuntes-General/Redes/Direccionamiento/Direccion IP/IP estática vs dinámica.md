# Dirección IP Estática Vs Dinámica

**Dirección IP Estática:**

1. **Características:**
    - Una dirección IP estática es una dirección IP que se asigna permanentemente a un dispositivo en una red.
    - No cambia con el tiempo, a menos que se realice una reconfiguración manual.
    - Suele asignarse manualmente por un administrador de red o configurarse en el propio dispositivo.
    - Es constante y predecible.
2. **Casos de Uso:**
    - Se utiliza en servidores y dispositivos de red que deben estar siempre disponibles en la misma dirección, como servidores web, servidores de correo, cámaras de seguridad, etc.
    - Es útil para servicios que necesitan ser accesibles de manera consistente a través de la misma dirección IP, como aplicaciones remotas o VPN.
    - Se emplea en situaciones donde es importante tener un control total sobre la asignación de direcciones IP.

**Dirección IP Dinámica:**

1. **Características:**
    - Una dirección IP dinámica es una dirección IP que se asigna automáticamente a un dispositivo por un servidor [[Protocolo DHCP|DHCP (Protocolo de Configuración Dinámica de Host)]] en la red.
    - Puede cambiar con el tiempo cuando un dispositivo se conecta o desconecta de la red, pero la asignación es temporal y se libera cuando el dispositivo no está en uso.
    - Es eficiente en la gestión de direcciones IP, ya que permite compartir un grupo limitado de direcciones IP entre varios dispositivos en función de su disponibilidad.
2. **Casos de Uso:**
    - Es ampliamente utilizado en redes domésticas y entornos empresariales para dispositivos cotidianos como computadoras, teléfonos, tabletas y otros dispositivos móviles.
    - Es eficiente en la asignación de direcciones IP en redes con muchos dispositivos, ya que permite que los dispositivos compartan direcciones IP de manera dinámica sin requerir una dirección IP única para cada uno.
    - Facilita la administración de la red al eliminar la necesidad de configurar manualmente cada dispositivo con una dirección IP específica.