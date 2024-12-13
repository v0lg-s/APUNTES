Las claves o llaves de un algoritmo de encriptación, son la manera de desencriptar el mensaje cifrado. Existen llaves privadas para poder descifrar un mensaje encriptado, debemos tener en nuestro poder esta llave *única* para hacerlo. Sin embargo, el uso de múltiples llaves privadas es poco manejable a gran escala.

Para esto se creo la Infraestructura de llave pública (PKI), esta infraestructura asegura el intercambio de información en línea. Hace que acceder a información sea rápido, fácil y seguro.

# Proceso de PKI

## 1. Intercambio de información cifrada
Puede involucrar cifrado simétrico, asimétrico o ambos.

De acuerdo a la prioridad PKI elegirá una u otra, o ambas. 
### Cifrado asimétrico
El uso de un par de llaves, una llave pública y una llave privada para el cifrado y descifrado del mensaje.
*Ejemplo:* Una caja con 2 llaves. 
- La llave pública permite agregar artículos a la caja pero no permite retirarlos. Puede ser copiada y compartida con todo el mundo para agregar artículos. 
- La llave privada abre la caja por completo, de manera que los artículos adentro pueden ser removidos, solo el dueño de la caja tiene acceso a la llave privada que la desbloquea.

La clave pública se utiliza para la encriptación de los Datos y la privada para su desencriptación. La clave privada sólo se entrega a los usuarios con acceso autorizado.
### Cifrado simétrico
El uso de una sola llave secreta para intercambiar información. Dado que utiliza una sola clave para la encriptación y la desencriptación, el emisor y el receptor deben conocer la clave secreta para bloquear o desbloquear el cifrado.

*Ejemplo:* Una caja con una sola llave. El dueño puede compartir la llave con servidores para que ellos también puedan acceder a la información, Esto hace la comunicación más rápida pero menos segura.

## 2. Establecimiento de confianza mediante sistema digital de certificados digitales

En la PKI, los Datos pueden cifrarse mediante criptografía asimétrica, criptografía simétrica o ambas. A continuación, un certificado digital enlaza la clave pública de los datos con la identidad verificada de un sitio web, individuo, organización, dispositivo o servidor.

### Certificado digital
Es un archivo que verifica la identidad del poseedor de la llave pública.