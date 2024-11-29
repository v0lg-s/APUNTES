## Comando cp
Este comando nos permite copiar un archivo desde un origen hacia un destino. Se puede especificar una ruta como destino y al final de la ruta el nuevo nombre de la copia del archivo
- cp → Copy
### cp archivos
```bash
cp archivo.txt archivo-copia.txt
```
- Lo anterior copia el archivo.txt en un archivo llamado archivo-copia.txt dentro del directorio en el que se está trabajando.
```bash
cp archivo.txt /home/volg/Downloads/archivo-copia.txt
```
- Lo anterior copia el archivo.txt en un archivo llamado archivo-copia.txt en el directorio Downloads.
### cp directorios
Para copiar un directorio junto a su contenido hacemos uso del argumento -r en el comando cp, de la siguiente manera:
```bash
cp -r directorio/ copia_directorio/
```
