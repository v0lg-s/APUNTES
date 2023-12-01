En sistemas Linux, la estructura de archivos y directorios sigue un diseño jerárquico organizado de manera lógica y coherente, como se muestra en la siguiente imagen:

![[directorios-estructura.png|600]]
Todo parte desde el directorio raíz que está representado por la barra inclinada **/**.

---

- **/ (Raíz del Sistema)** 
	- Es el nivel más alto en la jerarquía de directorios, es el que contiene a todos los demás archivos y directorios en Linux.
- **bin/ (Binarios)** 
	- Contiene los binarios de usuario, es decir, los ficheros o archivos (binarios) ejecutables necesarios para el arranque y el funcionamiento básico del sistema. Son comandos y utilidades en lenguaje máquina que utiliza el sistema.

---

- **boot/ (Arranque)** 
	- Contiene archivos relacionados al proceso de arranque, como el kernel del sistema operativo y los archivos de configuración de arranque.
- **dev/ (Dispositivos)** 
	- En este directorio se encuentran los archivos especiales que representan dispositivos físicos y virtuales del sistema. Por ejemplo, los discos duros, las impresoras y otros dispositivos son accesibles a través de archivos en este directorio.

---

- **/etc (Configuración)** 
	- Almacena archivos de configuración del sistema y de las aplicaciones. Aquí se encuentran los archivos de configuración del sistema, como `/etc/passwd` para usuarios y `/etc/network/` para la configuración de red. Se pueden iniciar servicios como el FTP desde aquí.
- **/home (Hogar)** 
	- Este directorio es el lugar donde residen los directorios de usuario personal. Cada usuario tiene su propio directorio de inicio en este lugar, donde puede almacenar sus archivos personales y configuraciones.

---

- **/lib (Bibliotecas)** 
	- Contiene las bibliotecas compartidas esenciales que requieren los programas en `/bin` y `/sbin` para su funcionamiento. También puede haber subdirectorios, como `/lib64`, en sistemas de 64 bits.
- **/media (Extraíbles)
	- Se utiliza para montar temporalmente dispositivos de almacenamiento extraíbles, como unidades USB, discos ópticos (CD y DVD), tarjetas SD y otros medios extraíbles. Cuando conectas un dispositivo de almacenamiento extraíble a tu sistema Linux, este directorio se usa para montar automáticamente el dispositivo y hacer que su contenido sea accesible desde el sistema.

---

- **/opt (Opcionales)** 
	- Este directorio se utiliza para instalar software adicional no incluido en la distribución principal del sistema. Las aplicaciones y paquetes de software adicionales a menudo se instalan en subdirectorios de `/opt`.
- **/sbin (Binarios del sistema)** 
	- Al igual que `/bin`, contiene archivos binarios, pero estos están relacionados con la administración del sistema y, por lo general, solo pueden ser ejecutados por el super usuario (root).

---

- **/srv (Datos de servicio)** 
	- Este directorio se utiliza para almacenar datos de servicios proporcionados por el sistema, como archivos de sitios web o repositorios de datos de servidores.
- **/tmp (Temporal):** 
	- Es un directorio utilizado para almacenar archivos temporales. Los archivos aquí son efímeros y se borran automáticamente durante el reinicio.

---

- **/usr (Recursos del sistema):** 
	- Contiene la mayoría de los archivos y programas del sistema, incluyendo aplicaciones, bibliotecas y archivos de datos. La estructura de `/usr` es similar a la del directorio raíz, con subdirectorios como `/usr/bin`, `/usr/lib`, `/usr/share`, entre otros.
- **/var (Variables):** 
	- Almacena datos variables, como archivos de registro, archivos de spool de impresión y otros datos que pueden cambiar con el tiempo. O logs de servidores y servicios.

---
