# Reto
## Descripción
There is some interesting information hidden around this site. Can you find it?http://wily-courier.picoctf.net:54228/
## Solución
### Solucion

```
nos logueamos y despues modificamos con debugger el token
┌──(kali㉿kali)-[~]
└─$ nanq hash
Command 'nanq' not found, did you mean:
  command 'nano' from deb nano
Try: sudo apt install <deb name>
                                                                             
┌──(kali㉿kali)-[~]
└─$ nano hash
                                                                             
┌──(kali㉿kali)-[~]
└─$ cat hash
cat: hash: No such file or directory
                                                                             
┌──(kali㉿kali)-[~]
└─$ nano hash
                                                                             
┌──(kali㉿kali)-[~]
└─$ cat hash 
cat: hash: No such file or directory
                                                                             
┌──(kali㉿kali)-[~]
└─$ nano hash
                                                                             
┌──(kali㉿kali)-[~]
└─$ nano hash
                                                                             
┌──(kali㉿kali)-[~]
└─$ cat hash 
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoibHVpcyJ9.RWB3HG8tPP1ls6UchXtNE0kspyED-E_Ds9Fsd9QCzj4
                                                                             
┌──(kali㉿kali)-[~]
└─$ ls usr/share/wordlist
ls: cannot access 'usr/share/wordlist': No such file or directory
                                                                             
┌──(kali㉿kali)-[~]
└─$ ls /usr/share/wordlist
ls: cannot access '/usr/share/wordlist': No such file or directory
                                                                             
┌──(kali㉿kali)-[~]
└─$ ls /usr/share/wordlists
dirb        fasttrack.txt  legion      rockyou.txt.gz  wifite.txt
dirbuster   fern-wifi      metasploit  sqlmap.txt
dnsmap.txt  john.lst       nmap.lst    wfuzz
                                                                             
┌──(kali㉿kali)-[~]
└─$ gzip -d /usr/share/wordlists/rockyou.txt.gz 

gzip: /usr/share/wordlists/rockyou.txt: Permission denied
                                                                             
┌──(kali㉿kali)-[~]
└─$ sudo gzip -d /usr/share/wordlists/rockyou.txt.gz
[sudo] password for kali: 
                                                                             
┌──(kali㉿kali)-[~]
└─$ ls /usr/share/wordlists                    
dirb        fasttrack.txt  legion      rockyou.txt  wifite.txt
dirbuster   fern-wifi      metasploit  sqlmap.txt
dnsmap.txt  john.lst       nmap.lst    wfuzz
                                                                             
┌──(kali㉿kali)-[~]
└─$ head /usr/share/wordlists/rockyou.txt.
head: cannot open '/usr/share/wordlists/rockyou.txt.' for reading: No such file or directory
                                                                             
┌──(kali㉿kali)-[~]
└─$ head /usr/share/wordlists/rockyou.txt 
123456
12345
123456789
password
iloveyou
princess
1234567
rockyou
12345678
abc123
                                                                             
┌──(kali㉿kali)-[~]
└─$ sudo apt install john                           
john is already the newest version (1.9.0-Jumbo-1+git20211102-0kali10).
john set to manually installed.
Summary:                    
  Upgrading: 0, Installing: 0, Removing: 0, Not Upgrading: 0
                                                                             
┌──(kali㉿kali)-[~]
└─$ john hash -w-/usr/share/wordlists/rockyou.txt  
Unknown option: "-w-/usr/share/wordlists/rockyou.txt"
                                                                             
┌──(kali㉿kali)-[~]
└─$ john hash -w=/usr/share/wordlists/rockyou.txt
Using default input encoding: UTF-8
Loaded 1 password hash (HMAC-SHA256 [password is key, SHA256 256/256 AVX2 8x])
Will run 4 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
ilovepico        (?)     
1g 0:00:00:01 DONE (2026-03-02 22:45) 0.6024g/s 4456Kp/s 4456Kc/s 4456KC/s ilovetitor..ilovemymother@
Use the "--show" option to display all of the cracked passwords reliably
Session completed. 

```
picoCTF{jawt_was_just_what_you_thought_bbb82bd4a57564aefb32d69dafb60583}
## Notas


## Referencias
https://www.youtube.com/watch?v=iaKbvrbcSko