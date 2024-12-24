# Listar procesos y entenderlos
- Si hay varios procesos en segundo plano, el comando **`job -l`** lista los procesos con sus identificadores.
	- La primer columna indica el *identificador interno* del proceso o *número de trabajo*.
	- La tercer columna muestra el *identificador global* del proceso.
	- El signo *'+'* antes del ID de proceso indica que es el *proceso preseleccionado*. Es decir cualquier comando que ejecutemos sin especificar un identificador interno o global se ejecutará sobre el proceso con el *'+'*.

![[comandoJobs.png]]
- Para hacer referencia al *identificador interno* o *número de trabajo* de un proceso con un comando se usa el signo *'%'*, por ejemplo, si quiero que el proceso [1] vaya a primer plano:

```bash
fg %1
```

# Comandos

![[ControlDeProcesos.png]]


### Comandos para procesos en Foreground (Primer plano)

- **Suspender comando en ejecución:** Se usa la combinación de teclas **`ctrl+z`**.
- **Detener o matar proceso en ejecución:** Se usa la combinación de teclas **`ctrl+c`**.

### Comandos para procesos Suspended
%# Es la referencia al identificador interno del trabajo.

- **Reanudar el proceso en primer plano:** Se usa el comando **`fg %#`**.
- **Reanudar el proceso en segundo plano:** Se usa el comando **`bg %#`**.
- **Detener o matar el proceso:** Se usa el comando **`kill %#`** (Número de trabajo) ó **`kill #`** (Identificador global del proceso).

### Comandos para procesos en Background

- **Ejecutar comando en segundo plano:** Para ejecutar un comando en segundo plano se utiliza el símbolo *'&'* al final del comando.

```bash
ping localhost &
```

- **Poner el proceso en primer plano:** Se usa el comando **`fg %#`**.
- **Suspender proceso en segundo plano:** Se usa el comando **`kill -STOP %#`**
- **Detener o matar el proceso:** Se usa el comando **`kill %#`** (Número de trabajo) ó **`kill #`** (Identificador global del proceso).

