Este proceso se realiza mediante software analizador de protocolos. Que intercepta y ve los paquetes enviados a través de una red.
# (P-cap) o Packet Capture
Es un archivo que contiene paquetes de datos interceptados de una interfaz o red.

Los archivos P-cap pueden tener muchos formatos dependiendo de la biblioteca de captura de paquetes que se utilice. Cada formato tiene diferentes usos y las herramientas de red pueden utilizar o soportar formatos específicos de archivos de captura de paquetes por defecto.

1. **Libpcap** es una biblioteca de captura de paquetes diseñada para ser utilizada por sistemas tipo Unix, como Linux y MacOS®. Herramientas como tcpdump utilizan Libpcap como formato de archivo de captura de paquetes por defecto.
2. **WinPcap** es una biblioteca de captura de paquetes de código abierto diseñada para dispositivos con sistemas operativos Windows. Se considera un formato de archivo más antiguo y no se utiliza predominantemente.
3. **Npcap** es una biblioteca diseñada por la herramienta de exploración de puertos Nmap que se utiliza habitualmente en los sistemas operativos Windows.
4. **PCAPng** es un formato de archivo moderno que puede capturar paquetes y almacenar datos simultáneamente. Su capacidad para hacer ambas cosas explica la "ng", que significa "próxima generación"
# Cómo funcionan los analizadores de protocolos de red

Los analizadores de protocolos de red utilizan tanto software como hardware para capturar el tráfico de red y mostrarlo para que los analistas de seguridad lo examinen y analicen. He aquí cómo:

1. En primer lugar, los paquetes deben recogerse de la red a través de la **tarjeta de interfaz de red (NIC)**, que es el hardware que conecta las computadoras a una red, como un router. Las NIC reciben y transmiten tráfico de red, pero por defecto sólo escuchan el tráfico de red dirigido a ellas. Para capturar todo el tráfico de red que se envía a través de la red, una NIC debe conmutarse a un modo que tenga acceso a todos los paquetes de datos de red visibles. En las interfaces inalámbricas, esto suele denominarse modo monitor, y en otros sistemas puede llamarse modo promiscuo. Este modo permite al NIC tener acceso a todos los paquetes de datos de red visibles, pero no ayudará a los analistas a acceder a todos los paquetes de una red. Un analizador de protocolos de red debe colocarse en un segmento de red adecuado para acceder a todo el tráfico entre los distintos hosts.
    
2. El analizador de protocolos de red recoge el tráfico de red en formato binario sin procesar. El formato Binario consiste en 0s y 1s y no es tan fácil de interpretar para los humanos. El analizador de protocolos de red toma el binario y lo convierte para que se muestre en un formato legible para el ser humano, de modo que los analistas puedan leer y comprender la información con facilidad.