# Reto
## Descripción
Why search for the flag when I can make a bookmarklet to print it for me?Browse [here](http://titan.picoctf.net:59004/), and find the flag!
## Solución
### Solucion

```
javascript:(function() { var encryptedFlag = "àÒÆÞ¦È¬ëÙ£ÖÓÚåÛÑ¢ÕÓË¨ËÓ§Èí"; var key = "picoctf"; var decryptedFlag = ""; for (var i = 0; i < encryptedFlag.length; i++) { decryptedFlag += String.fromCharCode((encryptedFlag.charCodeAt(i) - key.charCodeAt(i % key.length) + 256) % 256); } alert(decryptedFlag); })();

Ese código **desencripta una cadena usando una clave repetida** (`picoctf`). Básicamente resta el valor ASCII de cada carácter de la clave al carácter cifrado.

Si ejecutamos el script, el resultado que muestra el `alert()` es:

picoCTF{p@g3_turn3r_e8b2d43b}
```
picoCTF{p@g3_turn3r_e8b2d43b}
## Notas


## Referencias
