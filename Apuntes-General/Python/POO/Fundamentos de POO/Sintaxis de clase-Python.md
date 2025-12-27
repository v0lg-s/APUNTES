# Básica
**Definir una clase**

```python
class NombreDeLaClase:
	pass
```

**Instanciar un objeto**

```python
primer_objeto = NombreDeLaClase()
```

**Método constructor**

Las propiedades deben agregarse a la clase manualmente.  El constructor es una función de la clase, su propósito general es construir un nuevo objeto.

- Tiene que ser nombrada de forma estricta. \_\_init__
- Se ejecuta implícitamente cuando se crea un nuevo objeto.

El constructor debe saber todo acerca de la estructura del objeto y debe realizar todas las inicializaciones necesarias.

**Herencia**
```python
class ClaseHija(ClasePadre):
	def __init__(self):
		ClasePadre.__init__(self)
```
---

**Ejemplo:** Pila con Programación OO.

```python
class Stack:
	def __init__ (self):
		self.stack_list = [] # Atributo
		
stack_object = Stack()
print(len(stack_object.stack_list)) # salida 0
```

> Cualquier cambio que se realice dentro del constructor que modifique el estado del parámetro *self* se verá reflejado en el objeto recién creado.

Debemos hacer privado el atributo *stack_list*. **ENCAPSULACIÓN**

**Definición de la clase**

```python
class Stack:
	def __init__ (self):
		self.__stack_list = [] # Atributo privado - solo accesible desde la clase
		
	def push(self, val):
		self.__stack_list.append(val)
	
	def pop(self):
		val = self.__stack_list[-1]
		del self.__stack_list[-1]
		return val
```

**Instanciación**

```python
stack_object = Stack()

stack_object.push(3)
stack_object.push(2)
stack_object.push(1)

print(stack_object.pop())
print(stack_object.pop())
print(stack_object.pop())

# salida
# 1
# 2
# 3
```

**Herencia**

```python
class Stack:
	def __init__ (self):
		self.__stack_list = [] # Atributo privado - solo accesible desde la clase
		
	def push(self, val):
		self.__stack_list.append(val)
	
	def pop(self):
		val = self.__stack_list[-1]
		del self.__stack_list[-1]
		return val
		
class AddingStack(Stack):
	def __init__ (self):
		super().__init__(self)
		self.__sum = 0
		
	def push(self, val): # método anulado
		self.__sum += val
		Stack.push(self, val)
		
	def pop(self): # método anulado
		val = Stack.pop(self)
	    self.__sum -= val
	    return val
	    
	 def get_sum(self):
		 return self.__sum
```

>Al hacer un método con el mismo nombre en la clase hija y añadirle código se hizo anulación de métodos (method overriding) que permite a una clase hija (subclase) redefinir o especializar un método que ya existe en su clase padre (superclase), manteniendo el mismo nombre, firma (parámetros) y tipo de retorno, para ofrecer una implementación propia y específica
## Parámetro self

Permite que el método acceda a entidades (propiedades y actividades / métodos) del objeto. Cada vez que Python invoca un método, envía implícitamente el objeto actual como el primer argumento.

- La primera etapa entrega el objeto como un todo → `self`.
- A continuación, debe llegar a la lista ``__stack_list`` → ``self.__stack_list``.
- Con ``__stack_list`` lista para ser usada, puedes realizar el tercer y último paso → ``self.__stack_list.append(val)``.

