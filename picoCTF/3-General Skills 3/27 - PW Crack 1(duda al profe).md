# Reto
## Descripción
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/10/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/10/level1.flag.txt.enc) in the same directory too.
## Solución
### Solucion
- Se ejecutó el archivo python mediante la terminal.
```
neylar11-picoctf@webshell:~$ wget -q https://artifacts.picoctf.net/c/11/level1.py
neylar11-picoctf@webshell:~$ wget -q https://artifacts.picoctf.net/c/11/level1.flag.txt.enc
neylar11-picoctf@webshell:~$ ls
README.txt  code.py.1     codebook.txt.1  file       flag                 level1.py
code.py     codebook.txt  convertme.py    fixme1.py  level1.flag.txt.enc  runme.py
neylar11-picoctf@webshell:~$ nano level1.py
neylar11-picoctf@webshell:~$ python level1.py
Please enter correct password for flag: 
That password is incorrect
neylar11-picoctf@webshell:~$ python level1.py
Please enter correct password for flag: 1e1a
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_fa343060}

```
picoCTF{545h_r1ng1ng_fa343060}
## Notas
- Modificamos el archivo .py para saber la contraseña correcta al estar escrita de manera explícito en el código.

## Referencias
