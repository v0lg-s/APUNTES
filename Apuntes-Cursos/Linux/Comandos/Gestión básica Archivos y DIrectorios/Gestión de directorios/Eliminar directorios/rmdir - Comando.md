## Comando rmdir
*rmdir* nos permite eliminar un directorio vacío especificado.
- rmdir → Remove Directory

```bash
rmdir carpeta_nueva
```

Para eliminar un directorio con contenido debemos usar el comando rm con el argumento -r.

```bash
rm -r carpeta_nueva
```

Si se agrega el modificador f tras r, es decir, *-rf* se borrará el directorio sin ninguna confirmación adicional en terminal. Es necesario tener precaución porque puede borrar directorios y subdirectorios de manera forzada.

```bash
rm -rf carpeta_nueva
```

