El **Crowdsourcing** es la práctica de recopilar información utilizando las aportaciones y la colaboración del público. Las plataformas de Inteligencia sobre amenazas utilizan el crowdsourcing para recopilar información de la comunidad mundial de ciberseguridad.

El crowdsourcing permite a las personas y organizaciones de la comunidad mundial de ciberseguridad compartir abiertamente y acceder a una colección de datos de inteligencia sobre amenazas, lo que ayuda a mejorar continuamente las tecnologías y metodologías de detección.

Entre los ejemplos de organizaciones que comparten información se incluyen los Centros de Análisis e Intercambio de Información (ISAC), que se centran en recopilar y compartir inteligencia sobre amenazas específica del sector con empresas de sectores concretos como la energía, la sanidad y otros. La **Inteligencia de fuentes abiertas (OSINT** ) es la recopilación y el análisis de información procedente de fuentes de acceso público para generar inteligencia utilizable. La OSINT también puede utilizarse como método para recopilar información relacionada con los actores de las amenazas, las amenazas, las vulnerabilidades y mucho más.

# Virustotal
Es un servicio que permite a cualquiera analizar archivos, dominios, URL y direcciones IP sospechosos en busca de contenido malicioso. VirusTotal también ofrece servicios y herramientas adicionales para uso empresarial. Esta lectura se centra en el sitio web de VirusTotal, que está disponible para uso gratuito y no comercial.

![[virusTotal.png]]

1. **Detección**: La pestaña Detección proporciona una Lista de Proveedores de Seguridad de terceros y sus veredictos de detección sobre un IoC. Por ejemplo, los Proveedores pueden listar su veredicto de detección como malicioso, sospechoso, inseguro y más.

2. **Detalles**: La pestaña Detalles proporciona información adicional extraída de un análisis estático del IoC. Información como diferentes hashes, tipos de archivo, tamaños de archivo, cabeceras, hora de creación e información sobre el primer y último envío pueden encontrarse en esta pestaña.    

3. **Relaciones**: La pestaña Relaciones proporciona IoCs relacionados que están de alguna manera conectados a un artefacto, como URLs contactadas, dominios, direcciones IP y archivos descartados si el artefacto es un ejecutable.
 
4. **Comportamiento**: La pestaña Comportamiento contiene información relacionada con la actividad y los comportamientos observados de un artefacto tras ejecutarlo en un entorno controlado o sandboxed. Esta información incluye tácticas y técnicas detectadas, comunicaciones de red, acciones de registro y sistemas de archivos, procesos y mucho más.

5. **Comunidad:** La pestaña Comunidad es donde los miembros de la comunidad de VirusTotal, como profesionales de la Seguridad o investigadores, pueden dejar comentarios y estadísticas sobre el IoC.

6. **Proporción de Proveedores y** puntuación de la comunidad: La puntuación que aparece en la parte superior del Informe es la proporción de Proveedores. El ratio de proveedores muestra cuántos proveedores de Seguridad han marcado el IoC como malicioso en general. Debajo de esta puntuación, se encuentra también la puntuación de la comunidad, basada en las aportaciones de la comunidad de VirusTotal. Cuantas más detecciones tenga un archivo y mayor sea su puntuación de la comunidad, más probable es que el archivo sea malicioso.

**Nota**: Los Datos subidos a VirusTotal serán compartidos públicamente con toda la comunidad de VirusTotal. Tenga cuidado con lo que envía y asegúrese de no subir información personal.

# Otras herramientas

Existen otras herramientas de investigación que pueden utilizarse para analizar IoC. Estas herramientas también pueden compartir los datos que se les cargan con la comunidad de seguridad.

## **Escaneo de software malicioso de Jotti**

El análisis de[software malicioso](https://virusscan.jotti.org/) de Jotti es un servicio gratuito que le permite analizar archivos sospechosos con varios programas antivirus. Existen algunas limitaciones en cuanto al número de archivos que puede enviar.

## **Urlscan.io**

[Urlscan](https://urlscan.io/).io es un servicio gratuito que escanea y analiza las URL y proporciona un informe detallado que resume la información de la URL.

## **MalwareBazaar**

[MalwareBazaar](https://bazaar.abuse.ch/browse/) es un repositorio gratuito de muestras de software malicioso. Las muestras de software malicioso son una gran fuente de Inteligencia sobre amenazas que puede utilizarse con fines de investigación.