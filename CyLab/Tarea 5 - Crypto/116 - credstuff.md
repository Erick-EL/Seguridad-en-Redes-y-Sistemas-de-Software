## Descripción 
We found a leak of a blackmarket website's login credentials. Can you find the password of the user `cultiris` and successfully decrypt it? Download the leak [here](https://challenge-files.cylabacademy.net/library/7f760cee144ac7237469fd6bfab7c748d6f1d101ca47c101187ca7d8f5c721f0/leak.tar).

The first user in `usernames.txt` corresponds to the first password in `passwords.txt`. The second user corresponds to the second password, and so on.
## Solución 
```
academy{C7r1F_54V35_71M3}
```
## Notas adicionales 
* En lugar de buscar el número de línea manualmente, podemos unir ambos archivos columna por columna con el comando `paste`, filtrar el usuario `cultiris` y aplicar la rotación de caracteres con `tr`:
## Referencias