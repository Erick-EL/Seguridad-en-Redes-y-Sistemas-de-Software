## Descripción 
Connect to this PostgreSQL server and find the flag! `psql -h xebec.cylabacademy.net -p 40517 -U postgres pico`

Password is `postgres`
## Solución 
Son69-academy@webshell:~$ psql -h xebec.cylabacademy.net -p 40517 -U postgres pico
Password for user postgres: 
psql (14.22 (Ubuntu 14.22-0ubuntu0.22.04.1), server 18.6 (Debian 18.6-1.pgdg13+2))
WARNING: psql major version 14, server major version 18.
         Some psql features might not work.
Type "help" for help.

pico=# Select * from flag
pico-# select * from flags; 
ERROR:  syntax error at or near "select"
LINE 2: select * from flags;
        ^
pico=# Select * from flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | academy{L3arN_S0m3_5qL_t0d4Y_412c85d9}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
academy{L3arN_S0m3_5qL_t0d4Y_412c85d9}
## Notas adicionales 
solo use el Select * from flags; y me dio la flag y listo
## Referencias