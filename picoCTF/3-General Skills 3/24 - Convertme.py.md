# Reto
## Descripción
Run the Python script and convert the given number from decimal to binary to get the flag.[Download Python script](https://artifacts.picoctf.net/c/23/convertme.py)
## Solución
### Solucion
- Se ejecutó el archivo python mediante la terminal.
```
neylar11-picoctf@webshell:~$ wget -q https://artifacts.picoctf.net/c/23/convertme.py
neylar11-picoctf@webshell:~$ ls
README.txt  code.py.1     codebook.txt.1  file  runme.py
code.py     codebook.txt  convertme.py    flag
neylar11-picoctf@webshell:~$ python convertme.py
If 73 is in decimal base, what is it in binary base?
Answer: 00110111 00110011
That isn't a binary number. Binary numbers contain only 1's and 0's
neylar11-picoctf@webshell:~$ python convertme.py
If 52 is in decimal base, what is it in binary base?
Answer: 110100
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_9c3b7d4d}
neylar11-picoctf@webshell:~$
```
- para cambiar de base decimal a binario en cyberchef:https://gchq.github.io/CyberChef/#recipe=To_Base(2)&input=NTI
picoCTF{4ll_y0ur_b4535_9c3b7d4d}
## Notas
- - En CyberChef, utilizamos el 'to base' con radix en 2, para obtener la respuesta ingresando solo el numero solicitado.
## Referencias
