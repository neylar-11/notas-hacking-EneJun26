# Reto
## Descripción
After logging in, you will find multiple file parts in your home directory. These parts need to be combined and extracted to reveal the flag.SSH to `dolphin-cove.picoctf.net`:`61690` and login as `ctf-player` with password `8d076785`.
## Solución
### Solucion

```
┌──(kali㉿kali)-[~/picoctf/competencia1/piece]
└─$ ssh -p 61690 ctf-player@dolphin-cove.picoctf.net
The authenticity of host '[dolphin-cove.picoctf.net]:61690 ([3.13.34.175]:61690)' can't be established.
ED25519 key fingerprint is: SHA256:rdvWhF7Klwlu1EivysxTh/FjeqFI0dSEK5gaelaW9t8
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[dolphin-cove.picoctf.net]:61690' (ED25519) to the list of known hosts.
** WARNING: connection is not using a post-quantum key exchange algorithm.
** This session may be vulnerable to "store now, decrypt later" attacks.
** The server may need to be upgraded. See https://openssh.com/pq.html
ctf-player@dolphin-cove.picoctf.net's password: 
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 6.17.0-1007-aws x86_64)

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

ctf-player@pico-chall$ ls
instructions.txt  part_aa  part_ab  part_ac  part_ad  part_ae
ctf-player@pico-chall$ cat part_* > combined.zip
ctf-player@pico-chall$ file combined.zip
combined.zip: Zip archive data, at least v1.0 to extract
ctf-player@pico-chall$ ls
combined.zip  instructions.txt  part_aa  part_ab  part_ac  part_ad  part_ae
ctf-player@pico-chall$ unzip combined.zip
Archive:  combined.zip
[combined.zip] flag.txt password: 
 extracting: flag.txt                
ctf-player@pico-chall$ cat flag.txt
picoCTF{z1p_and_spl1t_f1l3s_4r3_fun_4e5c49a8}ctf-player@pico-chall$ 

```
picoCTF{z1p_and_spl1t_f1l3s_4r3_fun_4e5c49a8}
## Notas
contraseña: supersecret

## Referencias
