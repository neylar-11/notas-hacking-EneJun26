# Reto
## Descripción
Our flag printing service has started glitching!
`$ nc saturn.picoctf.net 49929`
## Solución
#### Solución 1
- linux + python
```
>>>neylar11-picoctf@webshell:~$ nc saturn.picoctf.net 49929
>>>'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'
'picoCTF{gl17ch_m3_n07_9c42a45d}'
```
picoCTF{gl17ch_m3_n07_9c42a45d}
## Notas
primero en la consola sin entrar a python se pego lo que se solicita, luego se copia la respuesta y se entra a python para pegarla
 - chr convierte a caracter
 


## Referencias
