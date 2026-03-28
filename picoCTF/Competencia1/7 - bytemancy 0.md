# Reto
## Descripción
Can you conjure the right bytes? The program's source code can be downloaded [here](https://challenge-files.picoctf.net/c_candy_mountain/a32ca0e42d9494e3cf81e345699e8ae50415274c00871b1e8594d0fa0ce7078c/app.py).Connect to the program with netcat:`$ nc candy-mountain.picoctf.net 60006`
## Solución
### Solucion
- cyberchef: https://gchq.github.io/CyberChef/#recipe=From_Hex('%5C%5Cx')&input=XHg2NVx4NjVceDY1
```
┌──(kali㉿kali)-[~/picoctf/competencia1/bytemancy0]
└─$ wget https://challenge-files.picoctf.net/c_candy_mountain/a32ca0e42d9494e3cf81e345699e8ae50415274c00871b1e8594d0fa0ce7078c/app.py
--2026-03-27 22:35:18--  https://challenge-files.picoctf.net/c_candy_mountain/a32ca0e42d9494e3cf81e345699e8ae50415274c00871b1e8594d0fa0ce7078c/app.py
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.161.44.103, 3.161.44.61, 3.161.44.22, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.161.44.103|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 773 [application/octet-stream]
Saving to: ‘app.py’

app.py                                    100%[=====================================================================================>]     773  --.-KB/s    in 0s      

2026-03-27 22:35:19 (18.7 MB/s) - ‘app.py’ saved [773/773]

                                                                                                                                                                        
┌──(kali㉿kali)-[~/picoctf/competencia1/bytemancy0]
└─$ cat app.py   
while(True):
  try:
    print('⊹──────[ BYTEMANCY-0 ]──────⊹')
    print("☍⟐☉⟊☽☈⟁⧋⟡☍⟐☉⟊☽☈⟁⧋⟡☍⟐☉⟊☽☈⟁⧋⟡☍⟐")
    print()
    print('Send me ASCII DECIMAL 101, 101, 101, side-by-side, no space.')
    print()
    print("☍⟐☉⟊☽☈⟁⧋⟡☍⟐☉⟊☽☈⟁⧋⟡☍⟐☉⟊☽☈⟁⧋⟡☍⟐")
    print('⊹─────────────⟡─────────────⊹')
    user_input = input('==> ')
    if user_input == "\x65\x65\x65":
      print(open("./flag.txt", "r").read())
      break
    else:
      print("That wasn't it. I got: " + str(user_input))
      print()
      print()
      print()
  except Exception as e:
    print(e)
    break
                                                                                                                                                                        
┌──(kali㉿kali)-[~/picoctf/competencia1/bytemancy0]
└─$ nc candy-mountain.picoctf.net 60006
⊹──────[ BYTEMANCY-0 ]──────⊹
☍⟐☉⟊☽☈⟁⧋⟡☍⟐☉⟊☽☈⟁⧋⟡☍⟐☉⟊☽☈⟁⧋⟡☍⟐

Send me ASCII DECIMAL 101, 101, 101, side-by-side, no space.

☍⟐☉⟊☽☈⟁⧋⟡☍⟐☉⟊☽☈⟁⧋⟡☍⟐☉⟊☽☈⟁⧋⟡☍⟐
⊹─────────────⟡─────────────⊹
==> eee
picoCTF{pr1n74813_ch4r5_62360bfd}

```
picoCTF{pr1n74813_ch4r5_62360bfd}
## Notas


## Referencias
