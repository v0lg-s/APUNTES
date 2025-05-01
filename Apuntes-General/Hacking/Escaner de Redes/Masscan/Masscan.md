Usa un acercamiento similar al escaneo de nmap usando UDP, sin embargo, para finalizar el escaneo más rápido, Masscan es más agresivo en el ratio de envío de paquetes. 

Ejemplos de sintaxis:

```bash
masscan MACHINE_IP/24 -p443
masscan MACHINE_IP/24 -p80,443
masscan MACHINE_IP/24 -p22-25
masscan MACHINE_IP/24 ‐‐top-ports 100
```

