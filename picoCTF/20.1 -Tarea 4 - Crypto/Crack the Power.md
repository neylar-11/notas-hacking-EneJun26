# Reto
## Descripción
We received an encrypted message. The modulus is built from primes large enough that factoring them isn’t an option, at least not today. See if you can make sense of the numbers and reveal the flag.Download the [message](https://challenge-files.picoctf.net/c_amiable_citadel/d75bf3f0753b354c1fabcaec0bdeb5902d67448835d57a0b0b268560a19f16a3/message.txt).
## Solución
### Solucion

```
import gmpy2

e = 20
c = 64063743081040685750056670209627408039666134432614898981914985563770727598347289989275044441930023407989265333336298950685280168500876225113087283274419764646685>

root , exact = gmpy2.iroot(c,e)

if  not exact:
        print ("Not found")
print("root")
print(int(root).to_bytes((root.bit_length()+7)//8,'big').decode())

```
picoCTF{t1ny_e_9b88056f}
## Notas


## Referencias
