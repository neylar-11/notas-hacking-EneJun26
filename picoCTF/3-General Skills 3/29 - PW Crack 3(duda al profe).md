# Reto
## Descripción
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/18/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/18/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/18/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Solución
### Solucion
```
neylar11-picoctf@webshell:~$ wget -q https://artifacts.picoctf.net/c/16/level3.py
neylar11-picoctf@webshell:~$ wget -q https://artifacts.picoctf.net/c/16/level3.flag.txt.enc
neylar11-picoctf@webshell:~$ wget -q https://artifacts.picoctf.net/c/16/level3.hash.bin
neylar11-picoctf@webshell:~$ nano level3.py
neylar11-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: 865e
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_2b072a90}
```
picoCTF{m45h_fl1ng1ng_2b072a90}
## Notas
- Modificamos el archivo .py para poder saber los caracteres por medio de la linea: 'print(chr(0x34) + chr(0x65) + chr(0x63) + chr(0x39))', ya que esos son comandos que puede leer python sin problema y darnos la respuesta correcta.

## Referencias
