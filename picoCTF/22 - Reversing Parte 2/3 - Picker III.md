# Reto
## Descripción
Can you figure out how this program works to get the flag?Connect to the program with netcat:`$ nc saturn.picoctf.net 55149`The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/525/picker-III.py).
## Solución
### Solucion
cyberchef: https://gchq.github.io/CyberChef/#recipe=From_Hex('Auto')&input=MHg3MCAweDY5IDB4NjMgMHg2ZiAweDQzIDB4NTQgMHg0NiAweDdiIDB4MzcgMHg2OCAweDMxIDB4MzUgMHg1ZiAweDMxIDB4MzUgMHg1ZiAweDc3IDB4NjggMHgzNCAweDM3IDB4NWYgMHg3NyAweDMzIDB4NWYgMHg2NyAweDMzIDB4MzcgMHg1ZiAweDc3IDB4MzEgMHgzNyAweDY4IDB4NWYgMHg3NSAweDM1IDB4MzMgMHg3MiAweDM1IDB4NWYgMHgzMSAweDZlIDB4NWYgMHg2MyAweDY4IDB4MzQgMHg3MiAweDY3IDB4MzMgMHg1ZiAweDYxIDB4MzEgMHgzOCAweDM2IDB4NjYgMHgzOSAweDYxIDB4NjMgMHg3ZCANCg&ieol=CRLF&oeol=CRLF
```
┌──(kali㉿kali)-[~/picoctf/reversingp2/p3]
└─$ open picker-III.py                                   
                                                                                                                                                                      
┌──(kali㉿kali)-[~/picoctf/reversingp2/p3]
└─$ nc saturn.picoctf.net 55149
==> ?

This program fixes vulnerabilities in its predecessor by limiting what
functions can be called to a table of predefined functions. This still puts
the user in charge, but prevents them from calling undesirable subroutines.

* Enter 'quit' to quit the program.
* Enter 'help' for this text.
* Enter 'reset' to reset the table.
* Enter '1' to execute the first function in the table.
* Enter '2' to execute the second function in the table.
* Enter '3' to execute the third function in the table.
* Enter '4' to execute the fourth function in the table.

Here's the current table:
  
1: print_table
2: read_variable
3: write_variable
4: getRandomNumber
==> 3
Please enter variable name to write: getRandomNumber
Please enter new value of variable: win
==> 2
Please enter variable name to read: getRandomNumber
<function win at 0x7f57840c3dc0>
==> 4
0x70 0x69 0x63 0x6f 0x43 0x54 0x46 0x7b 0x37 0x68 0x31 0x35 0x5f 0x31 0x35 0x5f 0x77 0x68 0x34 0x37 0x5f 0x77 0x33 0x5f 0x67 0x33 0x37 0x5f 0x77 0x31 0x37 0x68 0x5f 0x75 0x35 0x33 0x72 0x35 0x5f 0x31 0x6e 0x5f 0x63 0x68 0x34 0x72 0x67 0x33 0x5f 0x61 0x31 0x38 0x36 0x66 0x39 0x61 0x63 0x7d
```
picoCTF{7h15_15_wh47_w3_g37_w17h_u53r5_1n_ch4rg3_a186f9ac}
## Notas


## Referencias
