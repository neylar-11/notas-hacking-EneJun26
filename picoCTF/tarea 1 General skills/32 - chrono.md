# Reto
## Descripción
How to automate tasks to run at intervals on linux servers?Use ssh to connect to this server:

```
Server: saturn.picoctf.net
Port: 62437
Username: picoplayer 
Password: emrdK96SGH
```
## Solución
### Solucion

```
neylar11-picoctf@webshell:~$ ssh picoplayer@saturn.picoctf.net -p 63842     
The authenticity of host '[saturn.picoctf.net]:63842 ([13.59.203.175]:63842)' can't be established.
ED25519 key fingerprint is SHA256:dMTscRrUiURy7uMu5eGWwEKdd2FzqLzx6LfWhssWnNQ.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:20: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:63842' (ED25519) to the list of known hosts.
picoplayer@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.8.0-1044-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

picoplayer@challenge:~$ cat /etc/crontab
# picoCTF{Sch3DUL7NG_T45K3_L1NUX_0bb95b71}
picoplayer@challenge:~$ Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.
```
picoCTF{Sch3DUL7NG_T45K3_L1NUX_0bb95b71}
## Notas
- `cat` → muestra el contenido de un archivo  
- `/etc/crontab` → archivo donde se configuran tareas programadas (cron jobs)

## Referencias
https://www.youtube.com/watch?v=K9H6i73ydMM