La contraseña de bandit 17 nos la dan pasando la contraseña de bandit16 a algún puerto entre el 31.000 y el 32.000.

Debemos encontrar en el rango de estos puertos, los que estén escuchando. Posteriormente de los que están escuchando encontrar los que 'hablan' SSL/TLS y cuales no. Solo uno de esos nos devolverá la contraseña de bandit 17 cuando pasemos la contraseña de bandit16, el resto nos enviara devuelta lo que mandemos.

Con el escaneo:
```bash
nmap localhost -p31000-32000
```


Encontré que los puertos:

```plaintext
31046/tcp open  unknown
31518/tcp open  unknown
31691/tcp open  unknown
31790/tcp open  unknown
31960/tcp open  unknown
```


Están abiertos. Con el comando *'netstat -l'* confirmé que están escuchando.

Usando el script: *'ssl-enum-ciphers'* de nmap, intenté encontrar cuales 'hablan' SSL/TLS. 

```bash
nmap localhost -p31000-32000 --script ssl-enum-ciphers
```

*(No fue muy útil en realidad, simplemente podía empezar a probar cada uno. Con lo anterior solo descarté 1 y si ese script se ejecuta es bastante ruidoso.)*

**EL resultado es:**

```plaintext
PUERTO
31046
31518
31691
31790
```

Por prueba y error encontré que el puerto que devuelve la flag es el `31790`.

Le envío: `kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx`.

(En este punto tuve problemas porque me devolvía el mensaje *'KEYUPDATE'* se soluciona poniendo la opción *-quiet* al comando) Según un blog que encontré, debido a que la clave empieza por *'k'* puede que el servidor interprete esto como un comando. Con la opción *-quiet* todo lo que entra en el servidor no se interpreta, solo se procesa.

La respuesta es una clave privada RSA que guardé en el directorio.

**Password for bandit17:**
EReVavePLFHtFlFsjn3hyzMlvSuSAcRD (Se consigue tras iniciar sesión con la llave privada)
