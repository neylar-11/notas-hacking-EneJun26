# Reto
## Descripción

## Solución
### Solucion

```
import struct
arg1 = 0xb58568e8
arg2 = 0xc63ab2a1
arg3 = 0xf9d33ef4
stack = struct.pack('<III', arg1, arg2, arg3)
eax = 0
ah = stack[3]
ax = (ah << 8) & 0xFFFF
ax = (ax << 16) & 0xFFFF
al = ((ax & 0xFF) - stack[5]) & 0xFF
ah = (((ax >> 8) & 0xFF) + stack[4]) & 0xFF
ax = (ah << 8) | al
word_at_10 = struct.unpack_from('<H', stack, 8)[0]
ax = ax ^ word_at_10
print(hex(ax))
```
0x9fba
## Notas


## Referencias
