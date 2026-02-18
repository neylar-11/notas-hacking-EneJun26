# Reto
## Descripción
Can you look at the data in this binary? The bash script might help![static](https://challenge-files.picoctf.net/c_wily_courier/418e2775a501eaabeb99a96c5c467a83539369fe9649e8234644250cfb72d717/static), [ltdis.sh](https://challenge-files.picoctf.net/c_wily_courier/418e2775a501eaabeb99a96c5c467a83539369fe9649e8234644250cfb72d717/ltdis.sh)
## Solución
### Solución 1

```
neylar11-picoctf@webshell:~$ wget https://challenge-files.picoctf.net/c_wily_courier/418e2775a501eaabeb99a96c5c467a83539369fe9649e8234644250cfb72d717/static
--2026-02-18 02:00:09--  https://challenge-files.picoctf.net/c_wily_courier/418e2775a501eaabeb99a96c5c467a83539369fe9649e8234644250cfb72d717/static
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.64, 3.160.5.95, 3.160.5.40, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16776 (16K) [application/octet-stream]
Saving to: 'static'

static                100%[=======================>]  16.38K  --.-KB/s    in 0.006s  

2026-02-18 02:00:09 (2.58 MB/s) - 'static' saved [16776/16776]

neylar11-picoctf@webshell:~$ wget https://challenge-files.picoctf.net/c_wily_courier/418e2775a501eaabeb99a96c5c467a83539369fe9649e8234644250cfb72d717/ltdis.sh
--2026-02-18 02:00:25--  https://challenge-files.picoctf.net/c_wily_courier/418e2775a501eaabeb99a96c5c467a83539369fe9649e8234644250cfb72d717/ltdis.sh
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.95, 3.160.5.40, 3.160.5.18, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.95|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 785 [application/octet-stream]
Saving to: 'ltdis.sh'

ltdis.sh              100%[=======================>]     785  --.-KB/s    in 0s      

2026-02-18 02:00:25 (575 MB/s) - 'ltdis.sh' saved [785/785]

neylar11-picoctf@webshell:~$ file *
README.txt: ASCII text, with escape sequences
ltdis.sh:   Bourne-Again shell script, ASCII text executable
static:     ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=9a00d4dca6b92d22aa0cd1fceffa4ed7495b8534, for GNU/Linux 3.2.0, not stripped
neylar11-picoctf@webshell:~$ ./ltdis.sh
-bash: ./ltdis.sh: Permission denied
neylar11-picoctf@webshell:~$ chmod +x ltdis.sh
neylar11-picoctf@webshell:~$ ./ltdis.sh
Attempting disassembly of  ...
objdump: 'a.out': No such file
objdump: section '.text' mentioned in a -j option, but not found in any input file
Disassembly failed!
Usage: ltdis.sh <program-file>
Bye!
neylar11-picoctf@webshell:~$ ./ltdis.sh static
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
neylar11-picoctf@webshell:~$ strings static | grep pico
picoCTF{d15a5m_t34s3r_20335e41} 
```

picoCTF{d15a5m_t34s3r_20335e41}
## Notas

## Referencias
