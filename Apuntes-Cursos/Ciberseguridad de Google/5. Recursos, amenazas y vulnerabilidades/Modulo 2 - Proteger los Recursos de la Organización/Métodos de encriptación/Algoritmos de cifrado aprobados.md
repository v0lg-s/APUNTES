### **Algoritmos simétricos**

- _Triple DES (3DES)_ se conoce como un algoritmo de cifrado por bloques por la forma en que convierte el texto plano en texto cifrado en "bloques" Sus orígenes se remontan al Data Encryption Standard (DES), desarrollado a principios de la década de 1970. DES fue uno de los primeros algoritmos de encriptación simétrica que generaba claves de 64 bits. Un **bit** es la unidad más pequeña de medida de datos en una computadora. Como podrá imaginar, Triple DES genera claves de 192 bits, es decir, tres veces más largas. A pesar de que las claves son más largas, muchas organizaciones están dejando de utilizar Triple DES debido a las limitaciones en la cantidad de datos que pueden encriptarse. Sin embargo, es probable que Triple DES siga utilizándose por motivos de retrocompatibilidad.
- _Estándar de encriptación avanzada (AES_) es uno de los algoritmos simétricos más seguros de la actualidad. AES genera claves de 128, 192 o 256 bits. Se considera que las claves criptográficas de este tamaño están a salvo de ataques de fuerza bruta. Se calcula que forzar por la fuerza bruta una clave AES de 128 bits podría llevarle a una computadora moderna ¡miles de millones de años!

### **Algoritmos asimétricos**

- _Rivest Shamir Adleman (RSA_) recibe el nombre de sus tres creadores, que lo desarrollaron mientras estaban en el Instituto Tecnológico de Massachusetts (MIT). RSA es uno de los primeros algoritmos de criptografía asimétrica que produce un par de claves pública y privada. Los algoritmos asimétricos como el RSA producen longitudes de la clave aún más largas. En parte, esto se debe al hecho de que estas funciones crean dos claves. Los tamaños de la clave RSA son de 1.024, 2.048 o 4.096 bits. El RSA se utiliza principalmente para proteger datos altamente sensibles.
- _Algoritmo de firma digital (DSA_) es un algoritmo asimétrico estándar que fue introducido por el NIST a principios de la década de 1990. DSA también genera longitudes de la clave de 2.048 bits. Este algoritmo se utiliza mucho hoy en día como complemento de RSA en infraestructuras de clave pública.

### **Generación de claves**

Estos algoritmos deben implementarse cuando una organización elige uno para proteger sus datos. Una forma de hacerlo es utilizando OpenSSL, que es una herramienta de línea de comandos de código abierto que puede utilizarse para generar claves públicas y privadas. OpenSSL se utiliza habitualmente en las computadoras para verificar los certificados digitales que se intercambian como parte de la infraestructura de clave pública.

**Nota:** A principios de 2014, OpenSSL reveló una vulnerabilidad, conocida como el [error Heartbleed](https://en.wikipedia.org/wiki/Heartbleed), que exponía datos confidenciales en la memoria de sitios web y aplicaciones. Aunque todavía existen versiones de OpenSSL sin parchear, el error Heartbleed fue parcheado a finales de ese mismo año (2014).

**Consejo profesional:** Un sistema criptográfico _no debe_ considerarse seguro si requiere secreto sobre su funcionamiento.