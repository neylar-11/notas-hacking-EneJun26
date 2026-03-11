# Reto
## Descripción
Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin.Login via `ssh` as `ctf-player` with the password, `8c606eb1` on the host `wily-courier.picoctf.net` and port `50582`.

## Solución
### Solución 1
Primero, nos conectamos al servidor ssh:
```
neylar11-picoctf@webshell:~$ ssh ctf-player@wily-courier.picoctf.net -p50582
The authenticity of host '[wily-courier.picoctf.net]:50582 ([18.189.99.27]:50582)' can't be established.
ED25519 key fingerprint is SHA256:ErlUUvYlrAxfSW1tIdzfOnGTBSr5OFkZvz0nMN4Vodw.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[wily-courier.picoctf.net]:50582' (ED25519) to the list of known hosts.
ctf-player@wily-courier.picoctf.net's password: 
Welcome to Ubuntu 18.04.6 LTS (GNU/Linux 6.14.0-1012-aws x86_64)

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
```
Despues, hacemos tab hasta encontrar el ultimo archivo y lo ejecutamos
```
neylar11-picoctf@webshell:~$ ls
Addadshashanammu      README.txt  static                    static.ltdis.x86_64.txt
Addadshashanammu.zip  ltdis.sh    static.ltdis.strings.txt
neylar11-picoctf@webshell:~$ cd Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
neylar11-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissi
neylar11-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Ma
neylar11-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabita
shpi/Maelkashishi/Onnissiralis/Ularradallaku$ Addadshashanammu/Almurbalarammi/Ashalmi
-bash: Addadshashanammu/Almurbalarammi/Ashalmi: No such file or directory
neylar11-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabita
shpi/Maelkashishi/Onnissiralis/Ularradallaku$ /Addadshashanammu/Almurbalarammi/Ashalmi
-bash: /Addadshashanammu/Almurbalarammi/Ashalmi: No such file or directory
neylar11-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabita
shpi/Maelkashishi/Onnissiralis/Ularradallaku$ ls
fang-of-haynekhtnamet  fang-of-haynekhtnamet.c
neylar11-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabita
shpi/Maelkashishi/Onnissiralis/Ularradallaku$ /Addadshashanammu/Almurbalarammi/Ashalmi
-bash: /Addadshashanammu/Almurbalarammi/Ashalmi: No such file or directory
neylar11-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabita
shpi/Maelkashishi/Onnissiralis/Ularradallaku$ Addadshashanammu/Almurbalarammi/Ashalmi
-bash: Addadshashanammu/Almurbalarammi/Ashalmi: No such file or directory
neylar11-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabita
shpi/Maelkashishi/Onnissiralis/Ularradallaku$ ~/Addadshashanammu/Almurbalarammi/Ashalmi
-bash: /home/neylar11-picoctf/Addadshashanammu/Almurbalarammi/Ashalmi: No such file or directory
neylar11-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabita
shpi/Maelkashishi/Onnissiralis/Ularradallaku$ /Addadshashanammu/Almurbalarammi/Ashalmi
-bash: /Addadshashanammu/Almurbalarammi/Ashalmi: No such file or directory
neylar11-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabita
shpi/Maelkashishi/Onnissiralis/Ularradallaku$ Addadshashanammu/Almurbalarammi/Ashalmi
-bash: Addadshashanammu/Almurbalarammi/Ashalmi: No such file or directory
neylar11-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabita
shpi/Maelkashishi/Onnissiralis/Ularradallaku$ /Addadshashanammu/Almurbalarammi/Ashalmi
-bash: /Addadshashanammu/Almurbalarammi/Ashalmi: No such file or directory
neylar11-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabita
shpi/Maelkashishi/Onnissiralis/Ularradallaku$ Addadshashanammu/Almurbalarammi/Ashalmi
-bash: Addadshashanammu/Almurbalarammi/Ashalmi: No such file or directory
neylar11-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabita
shpi/Maelkashishi/Onnissiralis/Ularradallaku$ file fang-of-haynekhtnamet
fang-of-haynekhtnamet: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=4fdc1b4e898a0612ce5aa28e5012209f20bfc0ca, for GNU/Linux 3.2.0, not stripped
neylar11-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabita
shpi/Maelkashishi/Onnissiralis/Ularradallaku$ ./fang-of-haynekhtnamet 
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_fc588427}
neylar11-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabita
shpi/Maelkashishi/Onnissiralis/Ularradallaku$ cd
```
Despues, una vez dentro hacemos un ls:
```
ctf-player@pico-chall$ ls
1of3.flag.txt  instructions-to-2of3.txt
ctf-player@pico-chall$ cat 1of3.flag.txt
picoCTF{xxsh_
ctf-player@pico-chall$ cat instructions-to-2of3.txt 
Next, go to the root of all things, more succinctly `/`
ctf-player@pico-chall$ cd /
ctf-player@pico-chall$ ls
2of3.flag.txt  challenge  home                      lib64  opt   run   sys  var
bin            dev        instructions-to-3of3.txt  media  proc  sbin  tmp
boot           etc        lib                       mnt    root  srv   usr
ctf-player@pico-chall$ cat 2of3.flag.txt
0ut_0f_//4t3r_
ctf-player@pico-chall$ cat instructions-to-3of3.txt
Lastly, ctf-player, go home... more succinctly `~`
ctf-player@pico-chall$ cd ~
ctf-player@pico-chall$ ls
3of3.flag.txt  drop-in
ctf-player@pico-chall$ cat 3of3.flag.txt 
0b24fc4f}ctf-player@pico-chall$ Connection to wily-courier.picoctf.net closed by remote host.
Connection to wily-courier.picoctf.net closed.
neylar11-picoctf@webshell:~$ 
```

picoCTF{xxsh_0ut_0f_//4t3r_0b24fc4f}
## Notas
- Se usa cat para concatenar osea mostrar el contenido
## Referencias
