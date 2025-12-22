Un paquete es un conjunto de módulos y su estructura usualmente se ve así:

Siempre tiene el archivo **\_\_init.py__**

![[estructura-paquete-python.png|500]]

Main2.py tendría algo como:

```python
from sys import path

path.append('..∖∖packages')


import extra.good.best.sigma as sig
import extra.good.alpha as alp

print(sig.funS())
print(alp.funA())
```