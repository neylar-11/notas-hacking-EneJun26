# Reto
## Descripción
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/13/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/13/level2.flag.txt.enc) in the same directory too.
## Solución
### Solucion
```
neylar11-picoctf@webshell:~$ wget -q https://artifacts.picoctf.net/c/14/level2.py
neylar11-picoctf@webshell:~$ wget -q https://artifacts.picoctf.net/c/14/level2.flag.txt.enc
neylar11-picoctf@webshell:~$ nano level2.py
neylar11-picoctf@webshell:~$ python level2.py
Please enter correct password for flag: 4ec9
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_9701e681}
```
picoCTF{tr45h_51ng1ng_9701e681}
## Notas
- Modificamos el archivo .py para poder saber los caracteres por medio de la linea: 'print(chr(0x34) + chr(0x65) + chr(0x63) + chr(0x39))', ya que esos son comandos que puede leer python sin problema y darnos la respuesta correcta.

## Referencias
