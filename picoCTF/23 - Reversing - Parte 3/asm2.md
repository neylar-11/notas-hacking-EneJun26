# Reto
## Descripción
What does asm2(0xa,0x15) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://challenge-files.picoctf.net/c_fickle_tempest/1b461fce4f77f2756ffeade3af119ec77d49db6fd9831387af61f9e3dec7a839/test.S)
## Solución
### Solucion

```
local_4 = 0x15 (21) local_8 = 0xa (10) while (local_8 <= 0x84ab): # 0x84ab = 33963 local_4 += 1 local_8 += 0x37 # 0x37 = 55 return local_4
n*55 > 33953
n > 617.32...
n = 618 

local_4 = 21 + 618 = 639 = 0x27f
```

## Notas


## Referencias
