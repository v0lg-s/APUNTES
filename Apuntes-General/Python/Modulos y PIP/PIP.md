Repositorio *PyPI* (es la abreviatura de Python Package Index) es **un repositorio centralizado** de todos los paquetes de software disponibles. Lo mantiene un grupo de trabajo llamado Packaging Working Group, una parte de la Python Software Foundation. https://pypi.org/

La herramienta para acceder a este repositorio se llama *pip*. Algunas instalaciones de Python vienen con *pip* instalado otras no.

# Comandos

## Ayuda
```python
pip help 
```

Muestra ayuda del comando.

---
## Mostrar paquetes instalados
```python
pip list
```

Muestra los paquetes instalados y su versión.

---
## Mostrar información de paquete
```python
pip show package_name
```

Muestra más información acerca de un paquete, como dependencias y qué paquetes dependen de él.

---
## Instalar paquetes
```python
pip install --user pygame
```

Instala el paquete especificado, la opción --user indica que solo será instalado para el usuario actual y no en todo el S.O.

```bash
pip install nombre_del_paquete==versión_del_paquete
```
Instala la versión especificada del paquete.

---
## Actualizar paquetes

```bash
pip install -U nombre_del_paquete
```

Actualiza el paquete especificado.

---
## Desinstalar paquetes

```bash
pip uninstall package
```

Desinstalar el paquete especificado,