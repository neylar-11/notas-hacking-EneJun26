# Reto
## Descripción
Can you find the flag in the file? This would be really tedious to look through manually, something tells me there is a better way.The flag is in this [file](https://challenge-files.picoctf.net/c_fickle_tempest/d0b2e96347614d19414d591c946a1789fa8bd35487fcbfabf9437d0acfcaa503/file).

### Solucion 1
- usando Python
```
neylar11-picoctf@webshell:~$ python
>>>neylar11-picoctf@webshell:~$ wget https://challenge-files.picoctf.net/c_fickle_tempest/d0b2e96347614d19414d591c946a1789fa8bd35487fcbfabf9437d0acfcaa503/file

neylar11-picoctf@webshell:~$ cat file | grep 'picoCCTF'
>>> picoCTF{grep_is_good_to_find_things_e3C4b360}
```
picoCTF{grep_is_good_to_find_things_e3C4b360}
### Solucion 
descarga
```
descargamos el archivo y al abrirlo buscamos grep y sale
```
## Notas
- 
## Referencias
