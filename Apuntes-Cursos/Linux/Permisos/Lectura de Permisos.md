
![[permisos.png]]

Los permisos van de izquierda a derecha en pares de tres.

* -*rwx rwx rwx* : El primer grupo de tres indica los permisos que el dueño "[[Tipos de permisos y Usuarios#1. Usuario/User|User]]" del archivo tiene, el segundo grupo indica los permisos que el grupo "[[Tipos de permisos y Usuarios#2. Grupo/Group|Group]]" especificado tiene sobre el archivo y el último indica los permisos que otros "[[Tipos de permisos y Usuarios#3. Otros/Other|Other]]" usuarios tienen sobre dicho archivo.
* El primer espacio cuando se encuentra una "d" indica que se trata de un directorio.
* Cuando en vez de una de las letras se encuentra un guión, por ejemplo:
	* -rw-r--r--: indica que ese permiso no se encuentra dado. En este caso, "[[Tipos de permisos y Usuarios#1. Usuario/User|User]]" no tiene permiso para ejecutar, "[[Tipos de permisos y Usuarios#2. Grupo/Group|Group]]" no tiene permiso para escribir ni ejecutar al igual que "[[Tipos de permisos y Usuarios#3. Otros/Other|Other]]".

*Permisos:* 
- r → [[Tipos de permisos y Usuarios#1. Read/Leer|read]]
- w → [[Tipos de permisos y Usuarios#2. Write/Escribir|write]]
- x → [[Tipos de permisos y Usuarios#3. Execute/Ejecutar|execute]]

Se pueden leer como binarios y pasarlos a decimal para usarlos junto al comando [[Apuntes-Cursos/Linux/Permisos/Cambiar Permisos#Comando chmod|chmod]]. Es decir, los siguientes permisos se pueden ver como:

*-rw-r---w-.* → *110 100 010* 

Si pasamos a decimal cada 3 bits obtenemos:

6 4 2