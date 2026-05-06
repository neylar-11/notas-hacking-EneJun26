# Reto
## Descripción
This service can provide you with a random number, but can it do anything else?Connect to the program with netcat:`$ nc saturn.picoctf.net 63721`The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/513/picker-I.py).
## Solución
### Solucion
cyberchef: https://gchq.github.io/CyberChef/#recipe=From_Hex('Auto')&input=MHg3MCAweDY5IDB4NjMgMHg2ZiAweDQzIDB4NTQgMHg0NiAweDdiIDB4MzQgMHg1ZiAweDY0IDB4MzEgMHgzNCAweDZkIDB4MzAgMHg2ZSAweDY0IDB4NWYgMHgzMSAweDZlIDB4NWYgMHgzNyAweDY4IDB4MzMgMHg1ZiAweDcyIDB4MzAgMHg3NSAweDY3IDB4NjggMHg1ZiAweDYyIDB4MzUgMHgzMiAweDMzIDB4NjIgMHgzMiAweDYxIDB4MzEgMHg3ZCA
```
┌──(kali㉿kali)-[~/picoctf/reversingp2/p1]
└─$ open picker-I.py 
                                                                                                                                                                      
┌──(kali㉿kali)-[~/picoctf/reversingp2/p1]
└─$ nc saturn.picoctf.net 63721
Try entering "getRandomNumber" without the double quotes...
==> getRandomNumber
4
Try entering "getRandomNumber" without the double quotes...
==> win
0x70 0x69 0x63 0x6f 0x43 0x54 0x46 0x7b 0x34 0x5f 0x64 0x31 0x34 0x6d 0x30 0x6e 0x64 0x5f 0x31 0x6e 0x5f 0x37 0x68 0x33 0x5f 0x72 0x30 0x75 0x67 0x68 0x5f 0x62 0x35 0x32 0x33 0x62 0x32 0x61 0x31 0x7d 
Try entering "getRandomNumber" without the double quotes...
==> 

```
picoCTF{4_d14m0nd_1n_7h3_r0ugh_b523b2a1}
## Notas


## Referencias
