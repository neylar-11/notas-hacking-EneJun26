# Reto
## Descripción
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames.[Addadshashanammu.zip](https://challenge-files.picoctf.net/c_wily_courier/730d9106a6ce1d52c6463b90937ec89f5eb661388954fbd15cfa0c8a2eec012f/Addadshashanammu.zip)

## Solución
### Solución 1
Primero, descargamos y descomprimimos la carpeta zip:
```
neylar11-picoctf@webshell:~$ wget https://challenge-files.picoctf.net/c_wily_courier/730d9106a6ce1d52c6463b90937ec89f5eb661388954fbd15cfa0c8a2eec012f/Addadshashanammu.zip
--2026-02-18 02:16:00--  https://challenge-files.picoctf.net/c_wily_courier/730d9106a6ce1d52c6463b90937ec89f5eb661388954fbd15cfa0c8a2eec012f/Addadshashanammu.zip
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.18, 3.160.5.64, 3.160.5.95, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 5166 (5.0K) [application/octet-stream]
Saving to: 'Addadshashanammu.zip'

Addadshashanammu.zip  100%[=======================>]   5.04K  --.-KB/s    in 0s      

2026-02-18 02:16:00 (1.27 GB/s) - 'Addadshashanammu.zip' saved [5166/5166]

neylar11-picoctf@webshell:~$ unzip Addadshashanammu.zip 
Archive:  Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
 extracting: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet.c  
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet
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

picoCTF{l3v3l_up!_t4k3_4_r35t!_fc588427}
## Notas

## Referencias
