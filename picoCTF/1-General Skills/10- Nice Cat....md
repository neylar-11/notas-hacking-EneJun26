# Reto
## Descripción
There is a nice program that you can talk to by using this command in a shell:$ nc wily-courier.picoctf.net 50505, but it doesn't speak English...
## Solución
#### Solución 1
- linux + cyber chef
- https://gchq.github.io/CyberChef/#recipe=From_Decimal('Space',false)&input=MTEyIA0KMTA1IA0KOTkgDQoxMTEgDQo2NyANCjg0IA0KNzAgDQoxMjMgDQoxMDMgDQo0OCANCjQ4IA0KMTAwIA0KOTUgDQoxMDcgDQo0OSANCjExNiANCjExNiANCjEyMSANCjMzIA0KOTUgDQoxMTAgDQo0OSANCjk5IA0KNTEgDQo5NSANCjEwNyANCjQ5IA0KMTE2IA0KMTE2IA0KMTIxIA0KMzMgDQo5NSANCjk3IA0KNTcgDQo1MiANCjEwMSANCjU1IA0KMTI1IA0KMTAg&ieol=CRLF
```
>>>neylar11-picoctf@webshell:~$ nc wily-courier.picoctf.net 50505
----------------
cyberchef:
recipe: from decimal
input: numero que nos dio en linux
```
picoCTF{g00d_k1tty!_n1c3_k1tty!_a94e7}
## Notas
## Referencias
