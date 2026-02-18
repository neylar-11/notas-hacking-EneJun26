# Reto
## Descripción
Can you find the flag in [file](https://challenge-files.picoctf.net/c_fickle_tempest/a35dc624cfda858ed12a4bce57f832dad3b433bad6cde2b98e25fae4bc8ff760/strings) without running it?
## Solución
### Solucion 1
```
neylar11-picoctf@webshell:~$ wget https://challenge-files.picoctf.net/c_fickle_tempest/a35dc624cfda858ed12a4bce57f832dad3b433bad6cde2b98e25fae4bc8ff760/strings
--2026-02-18 01:50:31--  https://challenge-files.picoctf.net/c_fickle_tempest/a35dc624cfda858ed12a4bce57f832dad3b433bad6cde2b98e25fae4bc8ff760/strings
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.18, 3.160.5.95, 3.160.5.40, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 784424 (766K) [application/octet-stream]
Saving to: 'strings'

strings               100%[========================>] 766.04K  1.83MB/s    in 0.4s    

2026-02-18 01:50:31 (1.83 MB/s) - 'strings' saved [784424/784424]

neylar11-picoctf@webshell:~$ file string
string: cannot open `string' (No such file or directory)
neylar11-picoctf@webshell:~$ file strings
strings: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=a0867a67d407f6d2dad90aefc25fd5c89888e12e, for GNU/Linux 3.2.0, not stripped
neylar11-picoctf@webshell:~$  ls -la strings
-rw-rw-r-- 1 neylar11-picoctf neylar11-picoctf 784424 Nov 14 19:58 strings
neylar11-picoctf@webshell:~$ chmod -x strings
neylar11-picoctf@webshell:~$ ls -la strings
-rw-rw-r-- 1 neylar11-picoctf neylar11-picoctf 784424 Nov 14 19:58 strings
neylar11-picoctf@webshell:~$ ./ strings
-bash: ./: Is a directory
neylar11-picoctf@webshell:~$ strings strings | grep pico
picoCTF{5tRIng5_1T_60eA8fdA}
neylar11-picoctf@webshell:~$ 
```
picoCTF{5tRIng5_1T_60eA8fdA}
## Notas
- tuve problemas  porque no se encontro el archivo hasta que utilice el wget para descargar el archivo directamente a la terminal
## Referencias
