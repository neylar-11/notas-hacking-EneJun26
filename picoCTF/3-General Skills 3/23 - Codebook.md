# Reto
## Descripción
Run the Python script `code.py` in the same directory as `codebook.txt`.

- [Download code.py](https://artifacts.picoctf.net/c/3/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/3/codebook.txt)
## Solución
### Solucion
- Se ejecutó el archivo python mediante la terminal.
```
neylar11-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/3/code.py
--2026-02-18 03:42:29--  https://artifacts.picoctf.net/c/3/code.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.43, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1278 (1.2K) [application/octet-stream]
Saving to: 'code.py'

code.py               100%[=======================>]   1.25K  --.-KB/s    in 0s      

2026-02-18 03:42:29 (1.14 GB/s) - 'code.py' saved [1278/1278]

neylar11-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/3/codebook.txt
--2026-02-18 03:42:49--  https://artifacts.picoctf.net/c/3/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.128, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: 'codebook.txt'

codebook.txt          100%[=======================>]      27  --.-KB/s    in 0s      

2026-02-18 03:42:49 (6.18 MB/s) - 'codebook.txt' saved [27/27]

neylar11-picoctf@webshell:~$ ls
README.txt  code.py  codebook.txt  files  files.zip
neylar11-picoctf@webshell:~$ python code.py 
picoCTF{c0d3b00k_455157_197a982c}
```

picoCTF{c0d3b00k_455157_197a982c}
## Notas
- Usando el comando 'wget', si le agregamos un '-q', descarga el archivo pero no muestra en la terminal el porcentaje ni la información del archivo, simplemente lo descarga y muestra la siguiente linea para ejecutar comando
## Referencias
