# Reto
## Descripción
Can you read the flag? I think you can!`ssh -p 56788 ctf-player@green-hill.picoctf.net` using password `61ecc684`
### Solucion

```
┌──(kali㉿kali)-[~/picoctf/competencia1/SANDWICH]
└─$ ssh -p 49671 ctf-player@green-hill.picoctf.net
The authenticity of host '[green-hill.picoctf.net]:49671 ([3.18.205.4]:49671)' can't be established.
ED25519 key fingerprint is: SHA256:6yCIZ8GT1zu0g1/pjVc7t+aLNpxCPniM/MF6w7pTUx0
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:1: [hashed name]
    ~/.ssh/known_hosts:3: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[green-hill.picoctf.net]:49671' (ED25519) to the list of known hosts.
** WARNING: connection is not using a post-quantum key exchange algorithm.
** This session may be vulnerable to "store now, decrypt later" attacks.
** The server may need to be upgraded. See https://openssh.com/pq.html
ctf-player@green-hill.picoctf.net's password: 
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 6.17.0-1007-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

ctf-player@challenge:~$ ls
flag.txt
ctf-player@challenge:~$ cat flag.txt
cat: flag.txt: Permission denied
ctf-player@challenge:~$ strings flag.txt
-bash: strings: command not found
ctf-player@challenge:~$ sudo cat flag.txt
[sudo] password for ctf-player: 
Sorry, try again.
[sudo] password for ctf-player: 

Sorry, try again.
[sudo] password for ctf-player: 
sudo: 3 incorrect password attempts
ctf-player@challenge:~$ grep picoCTF flag.txt
grep: flag.txt: Permission denied
ctf-player@challenge:~$ vim flag.txt

[1]+  Stopped                 vim flag.txt
ctf-player@challenge:~$ bash flag.txt
bash: flag.txt: Permission denied
ctf-player@challenge:~$ sudo emacs flag.txt

```
picoCTF{ju57_5ud0_17_4c6f730f}
## Notas
GNU Emacs es un **editor de texto muy potente** que se usa mucho en Linux:
- - abrir el archivo `flag.txt`
- mostrar su contenido en el editor

## Referencias
