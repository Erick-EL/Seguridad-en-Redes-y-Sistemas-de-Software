## Descripción 
We have several pages hidden. Can you find the one with the flag? The website is running [here](http://chatelaine.cylabacademy.net:32204/)
## Solución 
```
Son69-academy@webshell:~$ URL="http://chatelaine.cylabacademy.net:32204/"
Son69-academy@webshell:~$ curl -s "$URL/" | grep -i "href"
    <link href="vendor/bootstrap/css/bootstrap.min.css" rel="stylesheet" />
    <link href="secret/assets/index.css" rel="stylesheet" />
      <a class="active" href="#home">Home</a>
      <a href="about.html">About</a>
      <a href="contact.html">Contact</a>
Son69-academy@webshell:~$ curl -s "$URL/secret/" | grep -i "href"
    <link rel="stylesheet" href="hidden/file.css" />
Son69-academy@webshell:~$ curl -s "$URL/secret/hidden/" | grep -i "href"
    <link href="superhidden/login.css" rel="stylesheet" />
              <a href="#" class="fb btn">
              <a href="#" class="twitter btn">
              <a href="#" class="google btn">
            <a href="#" style="color: white" class="btn">Sign up</a>
            <a href="#" style="color: white" class="btn">Forgot password?</a>
Son69-academy@webshell:~$ curl -s "$URL/secret/hidden/superhidden/" | grep -E -o '(picoCTF|academy)\{.*\}'
academy{succ3ss_@h3n1c@10n_7d8bae24}
```
## Notas adicionales 
* Los recursos estáticos como CSS, imágenes y JavaScript siempre deben revelar sus rutas para poder cargarse en el navegador del usuario. Esconder una página web dentro de la misma ruta que los recursos estáticos públicos siempre expondrá su existencia
## Referencias
* https://webshell.cylabacademy.org/