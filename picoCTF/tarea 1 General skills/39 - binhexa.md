# Reto
## Descripción
How well can you perfom basic binary operations?Start searching for the flag here `nc titan.picoctf.net 52299`
## Solución
### Solucion

```
neylar11-picoctf@webshell:~$ nc titan.picoctf.net 52299

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 00110100
Binary Number 2: 00001100


Question 1/6:
Operation 1: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 1000000
Correct!

Question 2/6:
Operation 2: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 00111100
Correct!

Question 3/6:
Operation 3: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 00000100
Correct!

Question 4/6:
Operation 4: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 00000110
Correct!

Question 5/6:
Operation 5: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 01101000
Correct!

Question 6/6:
Operation 6: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 1001110000
Correct!

Enter the results of the last operation in hexadecimal: 270

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_6862762d}
```
picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_6862762d}
## Notas


## Referencias
https://www.youtube.com/watch?v=6qASsWoyw7g