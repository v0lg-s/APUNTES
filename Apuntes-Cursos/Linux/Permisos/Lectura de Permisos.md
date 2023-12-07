
![[permisos.png]]

Los permisos van de izquierda a derecha en pares de tres.

* - *rwx rwx rwx* : El primer par de tres indica los permisos que el dueño "User" del archivo tiene, el segundo par indica los permisos que el grupo "Group" especificado tiene sobre el archivo y el último par indica los permisos que otros "Others" usuarios tienen sobre dicho archivo.
* El primer espacio cuando se encuentra una "d" indica que se trata de un directorio.
* Cuando en vez de una de las letras se encuentra un guión, por ejemplo:
	* -rw-r--r--: indica que ese permiso no se encuentra dado. En este caso, "User" no tiene permiso para ejecutar, "Group" no tiene permiso para escribir ni ejecutar al igual que "Others".

*Permisos:* 
- r → read
- w → write
- x → execute

Se pueden leer como binarios y pasarlos a decimal para usarlos junto al comando [[Cambiar Permisos#Comando chmod|chmod]]. Es decir, los siguientes permisos se pueden ver como:

*-rw-r---w-.* → *110 100 010* 

Si pasamos a decimal cada 3 bits obtenemos:

6 4 2