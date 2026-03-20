# Reto
## Descripción
I made a cool website where you can announce whatever you want! Try it out!I heard templating is a cool and modular way to build web apps! Check out my website [here](http://rescued-float.picoctf.net:64113/)!
## Solución
### Solucion

```

```
picoCTF{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_dcdca99a}
## Notas
Añadimos esta función `request.application.__globals__.__builtins__`porque nuestro código original `__import__('os')`estaba bloqueado por un filtro. Para sortearlo, necesitábamos una ruta diferente para acceder indirectamente a las funciones integradas de Python.

### Así es como funciona la cadena:

1. `**request.application**`  
    En Flask, el `request`objeto nos da acceso a la instancia de la aplicación a través de `request.application`.
2. `**__globals__**`  
    La aplicación (a menudo una función u objeto) almacena referencias a sus variables globales mediante el `__globals__`atributo. Esto nos da acceso al ámbito interno de Python.
3. `**__builtins__**`  
    Dentro de `__globals__`, hay `__builtins__`, que contiene todas las funciones integradas de Python, incluyendo`__import__`

Pulsa Intro o haz clic para ver la imagen a tamaño completo.

## Referencias
