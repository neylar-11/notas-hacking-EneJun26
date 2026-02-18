# Reto
## Descripción
Unzip this archive and find the flag.

- [Download zip file](https://artifacts.picoctf.net/c/503/big-zip-files.zip)

## Solución
### Solución 1
descargamos el zip y lo descomprimimos
```
neylar11-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/503/big-zip-files.zip
neylar11-picoctf@webshell:~$ unzip big-zip-files.zip
```

```
neylar11-picoctf@webshell:~$ ls
Addadshashanammu      big-zip-files.zip  static.ltdis.strings.txt
Addadshashanammu.zip  enc_flag           static.ltdis.x86_64.txt
README.txt            ltdis.sh
big-zip-files         static
neylar11-picoctf@webshell:~$ cd big-zip-files/
neylar11-picoctf@webshell:~/big-zip-files$ /big-zip-files$ grep -r pico
-bash: /big-zip-files$: No such file or directory
neylar11-picoctf@webshell:~/big-zip-files$ ~/big-zip-files$ grep -r pico
-bash: /home/neylar11-picoctf/big-zip-files$: No such file or directory
neylar11-picoctf@webshell:~/big-zip-files$ grep -r pico
folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}
neylar11-picoctf@webshell:~/big-zip-files$ 
```

picoCTF{gr3p_15_m4g1c_ef8790dc}
## Notas

## Referencias
