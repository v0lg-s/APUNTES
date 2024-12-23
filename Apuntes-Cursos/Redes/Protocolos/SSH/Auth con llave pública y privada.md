Esta alternativa de autenticación es más segura que el uso de una contraseña, ya que las contraseñas pueden ser fácilmente hackeadas y adivinadas por fuerza bruta.

- No se debe recordar ninguna contraseña.
- Se pueden revisar las llaves autorizadas para ingresar al servidor.
- Las llaves son claves criptográficas.

# Funcionamiento
Se basa en el uso de dos archivos o llaves, llave o clave privada y llave o clave pública.
- **Llave privada:** Es una llave única que no puede ser compartida con nadie, y debería estar muy asegurada. 
- **Llave pública:** Esta llave esta hecha para ser compartida con el servidor al que nos queremos conectar.

La llave privada se almacena en el computador host autorizado para ingresar al servidor. La llave pública debe ser agregada a un archivo llamado *"Authorized_keys"* en el servidor.

**Nota:** Tener en cuenta que con la llave privada se puede generar la llave pública aportando la 'passphrase' que protege la llave, si es que fue configurada.

## 1. Generación de claves
Es necesario generar el par de claves que serán usadas para autenticarse. Esto se realiza con herramientas como *ssh-keygen*.

```bash
ssh-keygen -t rsa -b 4096
```

- La opción '-t' indica el tipo de clave a generar. En este caso RSA, que es un sistema comúnmente usado y seguro.
- '-b' define el número de bits de la clave a generar. *claves de 4096 bits son más seguras pero más lentas en procesos de criptografía como cifrado y descifrado o firmas digitales.*

## 2. Compartir clave pública
La clave pública se comparte al servidor remoto y se guarda en el archivo *authorized_keys* usualmente está en el directorio oculto *.ssh/*.

- Se puede compartir manualmente copiándola en este archivo.
- O usando el comando:

```bash
ssh-copy-id usuario@direccionServidor
```


## 3. Proceso de autenticación con llaves

### 1. Inicio de conexión
1. El cliente inicia la conexión con el comando `ssh usuario@servidor`.
2. El cliente y el servidor "se ponen de acuerdo" en cuanto al algoritmo de cifrado, compresión y autenticación que van a utilizar. Puede ser AES para cifrado y RSA para autenticación. 
3. Se establece un canal seguro temporal con criptografía de clave simétrica.

### 2. Identificación del servidor
Este proceso se realiza siempre que se pueda, pero no es obligatorio para realizar la conexión. Es más una manera de verificar que nos estamos comunicando con el servidor correcto y no hay alguien tratado de suplantarlo.

1. El servidor envía la clave pública al cliente.
2. El cliente verifica la clave del servidor comparándola con las claves almacenadas en el archivo `~/.ssh/known_hosts`.
3. Si la clave coincide, el cliente confía en que está hablando con el servidor correcto.

### 3. Autenticación del cliente

1. **Solicitud de autenticación:** 
	1. El cliente le dice al servidor "Me autenticaré con una clave pública."
	2. El cliente envía al servidor un hash o identificador de la clave pública almacenada en el servidor. Esto lo hace para que el servidor sepa qué clave pública se usará para el proceso.
2. **Desafío del servidor:**
	1. El servidor busca la clave pública que corresponde con el hash recibido en el archivo `~/.ssh/authorized_keys`.
	2. Si la clave está en el archivo, el servidor cifra un mensaje aleatorio con esta clave y lo envía al cliente que solicita la conexión.
3. **Respuesta del cliente:** 
	1. El cliente descifra el mensaje usando su clave privada.
	2. Envía un hash del mensaje descifrado con la firma de la clave privada al servidor. (Cifra el hash del mensaje con su clave privada)
4. **Verificación del servidor:**
	1. El servidor usa la clave pública para verificar que la respuesta sea correcta. (Descifra el mensaje con la clave pública y obtiene el hash. En esta parte ya comprobó que el cliente tiene la clave privada, posteriormente compara el hash recibido con el hash del desafío original y comprueba si el contenido del desafío se modificó.)
	2. Si coincide, la autenticación es exitosa.

### 4. Establecimiento de la sesión SSH
Cuando la autenticación finaliza con éxito, el cliente y el servidor establecen una clave simétrica compartida para cifrar las comunicaciones que se generen durante la sesión.

La clave simétrica se envía con RSA para mantenerla secreta.
