# Reto
## Descripción
If I told you a word started with 0x70 in hexadecimal, what would it start with in ASCII?
## Solución
### Solucion 1
- Usando cyberchef
- https://gchq.github.io/CyberChef/#recipe=From_Hex('0x')&input=MHg3MA
### Solucion
- usando Python
```
neylar11-picoctf@webshell:~$ python
>>> int(0x70)
112
>>> chr(112)
'p'
>>> 
```
picoCTF{p}
## Notas
- US
## Referencias
