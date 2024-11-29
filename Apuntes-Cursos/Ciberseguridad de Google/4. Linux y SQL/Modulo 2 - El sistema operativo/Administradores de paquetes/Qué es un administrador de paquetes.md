Un paquete puede ser una pieza de información, que al combinarse con otros paquetes forme una aplicación.
- Algunos paquetes pueden ser lo suficientemente grandes como para formar aplicaciones por sí solos.
- Los paquetes contienen los archivos necesarios para instalar una aplicación. Estos archivos incluyen dependencias, que son archivos suplementarios utilizados para ejecutar una aplicación.

Un **administrador de paquetes** es una herramienta que ayuda a instalar, gestionar y eliminar paquetes o aplicaciones.

**Nota:** Es importante utilizar la versión más reciente de un Paquete siempre que sea posible. La versión más reciente tiene las correcciones de errores y los parches de seguridad más actualizados. Estos ayudan a mantener su sistema más seguro.

# Tipos de administradores de paquetes
Algunos administradores de paquetes funcionan con determinadas distribuciones. Por ejemplo:
- *RPM* es el administrador de paquetes de distribuciones Red Hat y sus derivadas. 
	- Tiene archivos que utilizan la extensión **.rpm**. 
- *dpkg* es el administrado de paquetes de distribuciones Debian y sus derivadas.
	- Tiene archivos que utilizan la extensión de archivo .deb.

# Herramientas de Gestión de paquetes
Existen herramientas de gestión de paquetes que permiten trabajar fácilmente con los paquetes desde la terminal/shell.

Se utilizan a veces en vez de los administradores de paquetes porque permiten a los usuarios realizar tareas básicas fácilmente.
- **APT**
- **YUM**

## APT (Advanced Packet Tool)
Es una herramienta de gestión de paquetes que se utiliza con las distribuciones derivadas de Debian. Gestiona, busca e instala paquetes.

- `apt list --installed` lista las apps instaladas

## YUM (Yellowdog Updater Modified)
Es una herramienta utilizada con las distribuciones derivadas de Red Hat. Se ejecuta desde la interfaz de línea de comandos para gestionar, buscar e instalar paquetes. YUM trabaja con archivos .rpm.
