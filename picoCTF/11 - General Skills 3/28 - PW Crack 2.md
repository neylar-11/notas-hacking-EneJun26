# Reto
## Descripción
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/13/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/13/level2.flag.txt.enc) in the same directory too.
## Solución
### Solucion
```
neylar11-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/13/level2.py
--2026-02-18 03:58:43--  https://artifacts.picoctf.net/c/13/level2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.128, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 914 [application/octet-stream]
Saving to: 'level2.py'

level2.py             100%[=======================>]     914  --.-KB/s    in 0s      

2026-02-18 03:58:43 (404 MB/s) - 'level2.py' saved [914/914]

neylar11-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/13/level2.flag.txt.enc
--2026-02-18 03:58:58--  https://artifacts.picoctf.net/c/13/level2.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.128, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level2.flag.txt.enc'

level2.flag.txt.enc   100%[=======================>]      31  --.-KB/s    in 0s      

2026-02-18 03:58:58 (11.9 MB/s) - 'level2.flag.txt.enc' saved [31/31]

neylar11-picoctf@webshell:~$ nano level2.py
neylar11-picoctf@webshell:~$ vim level2.py

[1]+  Stopped                 vim level2.py
neylar11-picoctf@webshell:~$ python
Python 3.10.12 (main, Feb  4 2025, 14:57:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print(chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36))
de76
>>> cd
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'cd' is not defined. Did you mean: 'id'?
>>> exit()
neylar11-picoctf@webshell:~$ python level2.py
Please enter correct password for flag: de76
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_489dea9a}
neylar11-picoctf@webshell:~$ 
```
picoCTF{tr45h_51ng1ng_489dea9a}
## Notas
- entre a editor de texto con vim y tome la linea: 'print(chr(0x34) + chr(0x65) + chr(0x63) + chr(0x39))', ya que esos son comandos que puede leer python  despues sali con con ctrl + z y entre a python y imprimi  la linea print(...) y me dio la contraseña

## Referencias
