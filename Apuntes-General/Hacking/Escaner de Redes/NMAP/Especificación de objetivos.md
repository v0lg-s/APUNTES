En Nmap podemos especificar los objetivos de cuatro maneras:

1. Lista de IP's a escanear. **`192.168.0.3 scanme.nmap.org example.com` -> Escanea 3 IP's.**
2. Rango de IP's a escanear. **`10.11.12.15-20` Escanea desde la *10.11.12.15* hasta la *10.11.12.20*.**
3. Subred. **`IP/30` Se especifica una IP y una mascara. Esto escaneará todos los hosts en el segmento de red.**
4. Mediante un archivo usando la opción `-iL`.

```bash
nmap -iL list_of_hosts.txt
```

