# Reto
## Descripción
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/18/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/18/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/18/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Solución
### Solucion
```
neylar11-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/18/level3.py
--2026-02-18 04:10:16--  https://artifacts.picoctf.net/c/18/level3.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.16, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1337 (1.3K) [application/octet-stream]
Saving to: 'level3.py'

level3.py             100%[=======================>]   1.31K  --.-KB/s    in 0s      

2026-02-18 04:10:16 (350 MB/s) - 'level3.py' saved [1337/1337]

neylar11-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/18/level3.flag.txt.enc
--2026-02-18 04:10:31--  https://artifacts.picoctf.net/c/18/level3.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.92, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level3.flag.txt.enc'

level3.flag.txt.enc   100%[=======================>]      31  --.-KB/s    in 0s      

2026-02-18 04:10:31 (32.4 MB/s) - 'level3.flag.txt.enc' saved [31/31]

neylar11-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/18/level3.hash.bin
--2026-02-18 04:10:46--  https://artifacts.picoctf.net/c/18/level3.hash.bin
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.43, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16 [application/octet-stream]
Saving to: 'level3.hash.bin'

level3.hash.bin       100%[=======================>]      16  --.-KB/s    in 0s      

2026-02-18 04:10:46 (20.6 MB/s) - 'level3.hash.bin' saved [16/16]

neylar11-picoctf@webshell:~$ nano level3.py
neylar11-picoctf@webshell:~$ vim level3.py

[1]+  Stopped                 vim level3.py
neylar11-picoctf@webshell:~$ python level3.py
Please enter correct password for flag: 
That password is incorrect
neylar11-picoctf@webshell:~$ vim level3.py

[2]+  Stopped                 vim level3.py
neylar11-picoctf@webshell:~$ python level3.py
Please enter correct password for flag: a9de
That password is incorrect
neylar11-picoctf@webshell:~$ python level3.py
Please enter correct password for flag: 8799
That password is incorrect
neylar11-picoctf@webshell:~$ python level3.py
Please enter correct password for flag: d3ab
That password is incorrect
neylar11-picoctf@webshell:~$ python level3.py
Please enter correct password for flag: 1ea2
That password is incorrect
neylar11-picoctf@webshell:~$ python level3.py
Please enter correct password for flag: acaf
That password is incorrect
neylar11-picoctf@webshell:~$ python level3.py
Please enter correct password for flag: 2295
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_6f98a49f}
```
picoCTF{m45h_fl1ng1ng_6f98a49f}
## Notas
- entre igual a vim y para no modificar nada intente con todas las opciones que me daban

## Referencias
