# Reto
## Descripción
Can you figure out how this program works to get the flag?Connect to the program with netcat:`$ nc saturn.picoctf.net 51576`The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/521/picker-II.py).
## Solución
### Solucion

```
┌──(kali㉿kali)-[~/picoctf/reversingp2/p2]
└─$ open picker-II.py                          
                                                                                                                                                                      
┌──(kali㉿kali)-[~/picoctf/reversingp2/p2]
└─$ nc saturn.picoctf.net 51576
==> win
Illegal input
==> open('flag.txt', 'r')
'_io.TextIOWrapper' object is not callable
                                                                                                                                                                      
┌──(kali㉿kali)-[~/picoctf/reversingp2/p2]
└─$ nc saturn.picoctf.net 51576
==> open('flag.txt', 'r').read
==> print(open('flag.txt', 'r').read())
picoCTF{f1l73r5_f41l_c0d3_r3f4c70r_m1gh7_5ucc33d_b924e8e5}
'NoneType' object is not callable

```
picoCTF{f1l73r5_f41l_c0d3_r3f4c70r_m1gh7_5ucc33d_b924e8e5}

## Notas


## Referencias
