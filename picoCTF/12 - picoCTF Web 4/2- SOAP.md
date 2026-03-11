# Reto
## Descripción
The web project was rushed and no security assessment was done. Can you read the /etc/passwd file?[Web Portal](http://saturn.picoctf.net:57810/)
## Solución
### Solucion

```
usamos un payloads xxe para saber la contraseña con buit suites  y repear
```
picoCTF{XML_3xtern@l_3nt1t1ty_e5f02dbf}
## Notas

Un **XXE (XML External Entity)** se usa cuando una aplicación procesa **XML** y permite declarar **entidades externas**. Con eso se puede probar si el parser es vulnerable leyendo archivos locales o haciendo peticiones externas.
## Referencias
