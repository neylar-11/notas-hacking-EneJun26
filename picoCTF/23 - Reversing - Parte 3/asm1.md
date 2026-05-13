# Reto
## Descripción
What does asm1(0x3fa) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://challenge-files.picoctf.net/c_fickle_tempest/6ccb8e41f43acc909f5d4ab56fb3e8f825575db4e33b94da272ce0133fefee87/test.S)
## Solución
### Solucion

```

  GNU nano 8.6                                                                                                   test.S                                                                                                            
        <+7>:   cmp    DWORD PTR [ebp+0x8],0x2a7
        <+14>:  jg     0x11d3 <asm1+38>
        <+16>:  cmp    DWORD PTR [ebp+0x8],0x28
        <+20>:  jne    0x11cb <asm1+30>
        <+22>:  mov    eax,DWORD PTR [ebp+0x8]
        <+25>:  add    eax,0x15
        <+28>:  jmp    0x11ea <asm1+61>
        <+30>:  mov    eax,DWORD PTR [ebp+0x8]
        <+33>:  sub    eax,0x15
        <+36>:  jmp    0x11ea <asm1+61>
        <+38>:  cmp    DWORD PTR [ebp+0x8],0x48b
        <+45>:  jne    0x11e4 <asm1+55>
        <+47>:  mov    eax,DWORD PTR [ebp+0x8]
        <+50>:  sub    eax,0x15
        <+53>:  jmp    0x11ea <asm1+61>
        <+55>:  mov    eax,DWORD PTR [ebp+0x8]
        <+58>:  add    eax,0x15
        <+61>:  pop    ebp
        <+62>:  ret    


┌──(kali㉿kali)-[~/picoctf/crypto3/reversing3/1]
└─$ python3
Python 3.13.9 (main, Oct 15 2025, 14:56:22) [GCC 15.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 0x6fa > 0x3a2
True
>>> 0x6fa != 0x6fa
False
>>> 0x6fa != 0x6fa
False
>>> hex(0x6fa-0x12)
'0x6e8'
>>> hex(0x6fa-0x12)
'0x6e8'
>>> 
KeyboardInterrupt
>>> hex(0x40f-0x12)
'0x40f'
>>> 

```
0x40f
## Notas


## Referencias
