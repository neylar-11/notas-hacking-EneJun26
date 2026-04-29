# Reto
## Descripción
This vault uses some complicated arrays! I hope you can make sense of it, special agent. The source code for this vault is here: [VaultDoor1.java](https://challenge-files.picoctf.net/c_fickle_tempest/eb2eaca69cb975c96a289b4db182ed439cf7f6bc542b135b8a9a1e9834c068c1/VaultDoor1.java)
## Solución
### Solucion

```
┌──(kali㉿kali)-[~/picoctf/reversingp1/vaultdoor1]
└─$ grep "password.charAt" VaultDoor1.java > salida.txt
                                                                                                                                                                      
┌──(kali㉿kali)-[~/picoctf/reversingp1/vaultdoor1]
└─$ open salida.txt     
                                                                                                                                                                      
┌──(kali㉿kali)-[~/picoctf/reversingp1/vaultdoor1]
└─$ grep "password.charAt" archivo.java | sort -t'(' -k2 -n > ordenado.txt
grep: archivo.java: No such file or directory
                                                                                                                                                                      
┌──(kali㉿kali)-[~/picoctf/reversingp1/vaultdoor1]
└─$ grep "password.charAt" VaulDoor1.java | sort -t'(' -k2 -n > ordenado.txt
grep: VaulDoor1.java: No such file or directory
                                                                                                                                                                      
┌──(kali㉿kali)-[~/picoctf/reversingp1/vaultdoor1]
└─$ grep "password.charAt" VaultDoor1.java | sort -t'(' -k2 -n > ordenado.txt
                                                                                                                                                                      
┌──(kali㉿kali)-[~/picoctf/reversingp1/vaultdoor1]
└─$ open ordenado.txt
                                                                                                                                                                      
┌──(kali㉿kali)-[~/picoctf/reversingp1/vaultdoor1]
└─$ cat flag | sort -t'(' -k2 -n
cat: flag: No such file or directory
                                                                                                                                                                      
┌──(kali㉿kali)-[~/picoctf/reversingp1/vaultdoor1]
└─$ cat ordenado.txt \
| sed "s/.*== '\(.*\)'.*/\1/" \
| tr -d '\n'
d35cr4mbl3_tH3_cH4r4cT3r5_29e8d8       
```
picoCTF{d35cr4mbl3_tH3_cH4r4cT3r5_29e8d8}
## Notas


## Referencias
