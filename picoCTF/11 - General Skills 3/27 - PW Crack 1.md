# Reto
## Descripción
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/10/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/10/level1.flag.txt.enc) in the same directory too.
## Solución
### Solucion
- Se ejecutó el archivo python mediante la terminal.
```
neylar11-picoctf@webshell:~$ wget -q https://artifacts.picoctf.net/c/10/level1.py
neylar11-picoctf@webshell:~$ wget /q https://artifacts.picoctf.net/c/10/level1.flag.txt.enc
/q: Scheme missing.
--2026-02-18 03:55:52--  https://artifacts.picoctf.net/c/10/level1.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.128, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 30 [application/octet-stream]
Saving to: 'level1.flag.txt.enc'

level1.flag.txt.enc   100%[=======================>]      30  --.-KB/s    in 0s      

2026-02-18 03:55:53 (31.4 MB/s) - 'level1.flag.txt.enc' saved [30/30]

FINISHED --2026-02-18 03:55:53--
Total wall clock time: 0.1s
Downloaded: 1 files, 30 in 0s (31.4 MB/s)
neylar11-picoctf@webshell:~$ ls
README.txt  files  level1.flag.txt.enc  level1.py
neylar11-picoctf@webshell:~$ nano level1.py
neylar11-picoctf@webshell:~$ python level1.py
Please enter correct password for flag: 
That password is incorrect
neylar11-picoctf@webshell:~$                 
neylar11-picoctf@webshell:~$ python level1.py
Please enter correct password for flag: 691d
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_56891419}
neylar11-picoctf@webshell:~$ 

```
picoCTF{545h_r1ng1ng_56891419}
## Notas
- entre al vim para saber la contraseña

## Referencias
