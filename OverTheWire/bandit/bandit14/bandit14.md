Para ingresar a bandit 14 nos dan una llave SSH privada desde bandit 13. Esta llave privada la ponemos en un archivo de texto y la usaremos posteriormente para acceder al host remoto.

El comando que usamos será *'ssh'* este tiene una opción para indicar que le daremos una llave privada para acceder en vez de una contraseña esta es *'-i'*.

```bash
ssh bandit14@bandit.labs.overthewire.org -p 2220 -i privateKeyRSA.txt
```

Hay que tener en cuenta que el archivo que contiene la llave privada debe tener los mínimos privilegios. [[1. Tipos de permisos y Usuarios#3. Otros/Other|Otros]] no pueden acceder a este archivo.

**Password for bandit 14:**
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS

Esta contraseña solo fue accesible una vez entramos al usuario bandit14.

**Temas relacionados:** [[Auth con llave pública y privada]], [[Protocolo SSH]].