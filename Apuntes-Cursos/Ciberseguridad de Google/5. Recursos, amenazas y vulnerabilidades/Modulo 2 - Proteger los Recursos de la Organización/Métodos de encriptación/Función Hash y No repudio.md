Es un algoritmo que produce un código que no puede ser descifrado. 
Ayudan a determinar la integridad de los archivos.

Son códigos únicos que se generan de acuerdo al contenido de un archivo.

**Por ejemplo:** Si usted envía un correo electrónico a un amigo diciendo "Hola soy Juan." se genera un código hash único. Si en el camino un atacante lo intercepta y cambia el contenido a "¡Hola Yo soy Juan!" el código hash cambia por completo. 

Si al final de la comunicación el código hash generado por el correo enviado inicialmente no coincide con el código hash generado por el correo recibido por su amigo, quiere decir que el mensaje fue corrompido en el camino.

---
Para evitar el riesgo de colisiones de hash, se necesitaban funciones que generaran valores más largos. Las deficiencias de MD5 dieron paso a un nuevo grupo de funciones conocidas como algoritmos hash seguros, o SHA.

El Instituto Nacional de Estándares y Tecnología (NIST) aprueba cada uno de estos algoritmos. Los números que aparecen junto a cada función SHA indican el tamaño de su valor hash en bits. Excepto SHA-1, que produce un compendio de 160 bits, se considera que estos algoritmos son resistentes a las colisiones. Sin embargo, eso no los hace invulnerables a otros exploits.

**Cinco funciones componen la familia de algoritmos SHA:**

- SHA-1
- SHA-224
- SHA-256
- SHA-384
- SHA-512
# Principio de no repudio
El no repudio es un principio de seguridad informática que garantiza que las partes involucradas en una comunicación o transacción no puedan negar su participación. Es un servicio que permite probar que una acción se llevó a cabo y que no se puede repudiar.

También puede entenderse cómo el concepto de que la autenticidad de la información no puede ser negada.

### **Tablas rainbow**

Una **tabla rainbow** es un archivo de valores hash pregenerados y su texto plano asociado. Son como diccionarios de contraseñas débiles. Los atacantes capaces de obtener la base de datos de contraseñas de una organización pueden utilizar una tabla rainbow para compararlas con todos los valores posibles.

**El salting** es una salvaguarda adicional que se utiliza para reforzar las funciones hash. Una _sal_ es una cadena aleatoria de caracteres que se añade a los Datos antes de hacer el hash. Los caracteres adicionales producen un valor hash más único, lo que hace que los datos salados sean resistentes a los ataques de tabla rainbow.

Por ejemplo, una Base de datos que contenga contraseñas podría tener varias entradas con hash para la contraseña "password" Si todas esas contraseñas estuvieran saladas, cada entrada sería completamente diferente. Eso significa que un atacante que utilizara una tabla rainbow sería incapaz de encontrar valores coincidentes para "password" en la base de datos.