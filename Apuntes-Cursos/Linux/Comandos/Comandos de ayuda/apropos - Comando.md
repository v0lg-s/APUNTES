Busca las descripciones de una página del manual para un string especificado.

**Por ejemplo:** 
Tenemos una tarea que implica cambiar una contraseña pero no sabemos como, escribimos:
```bash
apropos password
```
![[aproposComando1.1.png]]
Nos muestra muchos comandos con la palabra password. Puede no ser de mucha ayuda, pero usando la opción -a, podemos filtrar comandos que contengan dos cadenas de string que especificamos.

```bash
apropos -a change password
```

![[aproposComando.png]]