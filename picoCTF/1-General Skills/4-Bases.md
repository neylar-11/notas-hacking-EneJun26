# Reto
## Descripción
What does this bDNhcm5fdGgzX3IwcDM1 mean? I think it has something to do with bases.
## Solución
### Solucion 1
- Usando cyberchef
- https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=YkROaGNtNWZkR2d6WDNJd2NETTE
-  recipe: from base: A-Za-z0-9+/=
- input: bDNhcm5fdGgzX3IwcDM1
### Solucion 2
- usando Python
```
neylar11-picoctf@webshell:~$ python
>>> import base64
>>> base64.b64decode('bDNhcm5fdGgzX3IwcDM1')
b'l3arn_th3_r0p35'
>>>
```
picoCTF{l3arn_th3_r0p35}
### Solucion 3
usando linux
```
neylar11-picoctf@webshell:~$ echo 'bDNhcm5fdGgzX3IwcDM1' | base64 -d
l3arn_th3_r0p35neylar11-picoctf@webshell:~$
```
## Notas
- se uso la consola linux para resolverlo
## Referencias
