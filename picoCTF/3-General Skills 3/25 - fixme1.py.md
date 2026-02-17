# Reto
## Descripción
Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/27/fixme1.py)
## Solución
### Solucion
- Se ejecutó el archivo python mediante la terminal.
```
neylar11-picoctf@webshell:~$ wget -q https://artifacts.picoctf.net/c/27/fixme1.py
neylar11-picoctf@webshell:~$ python fixme1.py 
  File "/home/VictorCervantes-picoctf/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
neylar11-picoctf@webshell:~$ nano fixme1.py 
neylar11-picoctf@webshell:~$ python fixme1.py 
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_182342f7}
neylar11-picoctf@webshell:~$ 

```
picoCTF{1nd3nt1ty_cr1515_182342f7}
## Notas

## Referencias
