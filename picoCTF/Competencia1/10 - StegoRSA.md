# Reto
## Descripción
A message has been encrypted using RSA. The public key is gone… but someone might have been careless with the private key. Can you recover it and decrypt the message?Download the [flag](https://challenge-files.picoctf.net/c_plain_mesa/5b62df520d0762ee68a7a8e4fc39b4584d68c8be61ca062848fe2f3943af21d9/flag.enc) and [image](https://challenge-files.picoctf.net/c_plain_mesa/5b62df520d0762ee68a7a8e4fc39b4584d68c8be61ca062848fe2f3943af21d9/image.jpg).
## Solución
### Solucion
- cyberchef: https://gchq.github.io/CyberChef/#recipe=From_Hex('None')&input=MmQyZDJkMmQyZDQyNDU0NzQ5NGUyMDUwNTI0OTU2NDE1NDQ1MjA0YjQ1NTkyZDJkMmQyZDJkMGE0ZDQ5NDk0NTc2Njc0OTQyNDE0NDQxNGU0MjY3NmI3MTY4NmI2OTQ3Mzk3NzMwNDI0MTUxNDU0NjQxNDE1MzQzNDI0YjY3
- cyberchef: https://gchq.github.io/CyberChef/#recipe=From_Hex('None')&input=MmQyZDJkMmQyZDQyNDU0NzQ5NGUyMDUwNTI0OTU2NDE1NDQ1MjA0YjQ1NTkyZDJkMmQyZDJkMGE0ZDQ5NDk0NTc2Njc0OTQyNDE0NDQxNGU0MjY3NmI3MTY4NmI2OTQ3Mzk3NzMwNDI0MTUxNDU0NjQxNDE1MzQzNDI0YjY3Nzc2NzY3NTM2YjQxNjc0NTQxNDE2ZjQ5NDI0MTUxNDMzMDM0N2E3OTMyNjg3NzY5NDY1ODQ5NDQ2ODBhNTA3Mjc3NmI2MjMyNzcyZjQ5MzA0NzM1MmIzMTY0NjU1NjdhNDQ2ODQ2NTM1OTY1NGI2NTU3NjQ2Nzc4NWE1MDczMzc3NzcyNGYzMDM5NjkzNDM5NTk2ODMzNTU2ZTU1NjUzNjRhNzYzMzVhMmI3MjQzNGUzNTdhMmI1OTY1MzMwYTc4Njc0YzMzNjkzODQzNzY0NzQ5NGI0NTUzNGUzMTcyNjg1YTQ3NGI0YjY3NmU1YTcxNGM2NTZjNjk0ZTRjMzg1MTM5MzI2NTQ3NTE0MzUzNTI0YTZjNTU2Njc3MzE2YjU4NDU1MjM1Nzg3MTY5NTEzMDQ4NTY2NzUwMzk0NjQzMGE3NzMyNTczNjM4NWE0MjQzN2EzODc1NDQ3MDU0NzgyYjM2Mzg1NzM2NTg0ZTM2NzI0Njc1MmY0ZjRiMzE1NjZjNzc2YzMxNzA1ODQzNjU1NTU2NzU1MDRjNWE1NzYzNGM0YTJmMzQ2ODJmNGY0ZDZhNGI0ZTYyMzI1MzYyNjc2YjBhMzE1OTc2MzY0NjQ3Njg2YTRhNzE0YTYxNjU1MDVhNDU2YTY3NTEzNTU2NzM0NjY0NmM2NzU2NTQ2ZjRhMmI2MzcxMzY0NjM4Nzk3YTdhNTI2MTM0NzA3NzQyNWE2ODMyNTk1MTYyNDI1ODRmNjc0YTM4NzU2NTU5NzY2NTZiNDcwYTYyNDY2ZTU5MzU1MzcxMzAzMjcxNTI0NDU1Nzc1MjYxNDIzNTRkMzMzNzUyNTU3ODQ2NjI3ODY1NjYzNzMyNDk1MTZlNTk0MzVhNDM3OTRiNzMzMTUyNjQ3MjdhNDkzOTRlNzY0ZDdhNTM1NjZjMzE0NzM0NTQ1Nzc2Njc1YTQ4MGE0NjUzNGY2NjUzNTA2YTJmNDE2NzRkNDI0MTQxNDU0MzY3Njc0NTQxNDI0MjY3MzI3NTY4MzA0MjVhNGUzOTczNzI1Nzc5NWE2ZTcxNzU0NjQyNDU0YzYzNmE0OTUzN2E2NjQyNjUzMjRjNDE2ZjcxNDI0NDZlNDg2YjQ2NGIzMDBhMzA1MjU5NGQzOTc0MmI1MDU1NzY2ZjM4NTU1MzU0NzM3NDQ3NmY2NTQzNjI0NTMzNDc1OTc5NDk1NzRhNDMzMzM4NTU0NzQzNzQ0YjM3NGU3MjQ1NmEyYjUwMzE2NDU1MzUzODY1NzM3NjU0NjQ3MDVhNGI3NDczNjk0ZDczMzUwYTZjMzI3NDQ0MzIzMzMzNGY1YTUxNDUzMzY4NTY0NzY3Mzg0ODZmNmI0ZTRiNzQzNjQzNmM2YjZjNzA3NzZkNjE3ODM0NzU2Mjc4NDc2YjRmNjI2ZDc5Mzg3NTc4Nzk2YjM2MzI3OTU0MzIzNzMyNWE2MjcyMzg0NTcxMzY0YjQ3MGE3MzZmNTE0ZjM0NzQ3MzY2MzI2MTRhNDg3MzcwNGQ2ZTM1NjIzMjU4NzUzNDY1NmYzNjcyNDM2YzMzNjIzMzQxMzI0ZTRkNmM0YzcyNDY1OTQ0NDE1MjUyNGU2NTMyNjg2MjU1NTc0NDU2NTI0MTc3NmQ0NDY1NTI0NTYxNzE2NjBhNTk1OTc5NzU0ZjYxNzM0YTRhNzU3NzMyNjc2Njc1NDU1NTY0NGUzNTQ3MzA1YTYzNTk0NzczNmM1YTZhNjI3NTcxNzc2MTQ5MzA0NDdhNjM3MjM0MzQ0NTU1NmI2NTY2NTM0ZjU4NDUzMzYzNzY0MTQ4Njk2ODYzNmE2ZTRkNjEwYTY2NTk0OTZkNDMzNjUyNDIzOTQ0NzgzMzM0NDI3MDY2NTY3NTY4NTU1YTZhNzM3NDMxNjE2MTUxNjY0NDQyNmU0YjU2NjU1NDU5NWE2NzUyMzk1MTRiNDI2NzUxNDQ0NTY3NTI3YTUxN2E1NDM2NjE1OTZiMzczMDRkMzY2ZjMzMGEzMjZmNGU1YTU2NTQ0NTQ3NzQyZjc1MzQzODdhNzYzNDVhNDQ2ODU0NDg1MjY5NjYzNTMyNjU1ODRlNDczNDc2NzU0NDZhNjQ1Mzc3NDQ1MTdhMzE0NjVhNmQ2NjM2NWE0OTU2NDg0NzQ3NTkyYjU1MzE3MzQ2NGY2ZDY2NTY3NzBhNjM2YjMyMzYzNjYzNzE0YjMyNTU2NzM2MzQ0ZTM4NTIzNzM0NmI2NTUxNzQ0NDMzNmY3YTRhNGU3NTM3NzA0YjMwNDY0MTQyMzY0YzQxNjI1MDUzMzc3MTQ3MmI3MjJiNWE0ODYzNDczMDZlNTk2MzM3NmU0ODU0NzUzNjY4NjIwYTQ2Nzc3NDczNTE1MzVhNTI3NjQxNzEzNTcxNTI0NzY4NjU1MzQ1NDE3MDVhNDk0ZjY2NTE0YjQyNjc1MTQ0NzI3MDM2MmY3MjY5NTE3NTUyNzU1NTc5NmM1NjQyNzg3NDM3MzI3MDUzNTM3NjU3MzM2ZDY4NzA0ZDUyMzA2ODUyMGEzMDRiNmUzOTZlNTg2ZDY3NzU3OTJmNzk3MzQ0NTU3MTU0NzI3YTQzNWE2ODY1NDg3NjUyNjQyYjM1MzQ0MzRiNDg2ZjQxNjU2NDQ5NjY2NjM1NjI2OTM5NzY2ZDcyNjY2YjRlNWEzNjZiNDg3MzRiNzAyYjY1MzE0ZDcxMzM3NzBhNGU0ODRiNTQ1ODJmNGQ1NTY5Njg0YjZmNzk3Mjc2NzE3NDc5MzIzNjZmNGI3MzczNjgzNzU0MmYzMjU5NzczMzQ0NWE2OTYxNzkzODZmMzg3NjRjNTk2YTQ2Nzk2NjUwNjEyZjQ2MmI0NDQ2NzA3MDY3NzE0ZjRhNTk3YTQxNTcwYTRiNGIzNjRlMzczNzYyNTM0Yjc3NGI0MjY3NTE0Mzc0NTQzOTcyNmI1YTZiNDc1MzMxNGI1OTY5NTIyZjYzNTg2MzQxNjg3NDQ4MmY0MTc2NzA3NDQ4NDQ1NzJmNTI0NzcyNjMzMzZlNzM0NDJmNzA3NTRiNTQ3MTJmNTg2YjM1MGE2MTU2NjY3NTQyNWE3MjY3NmI0MjZkNDYzMTM0NWE3NjM5NGIzMDMwMzk1YTRhNmU2OTYzNmU1MTMwMzQ1NjY2MmI2NDQzNDk3YTQ3MzY3ODYxMzk2MTQzMzUzNTYxNTg0ZDUyNjQ1NTczMzA1Nzc2NTI0MzYxMzMzMzRhMzA0MTBhNDk3ODM2NGU3MzQ4NjE3OTYyMzU0OTU0NGU1NDQyNjIzMDcxNzc1MTUwNmI3NTY5NTY0ZDUwNjM0YTUzNTQ2Yzc3NmE3NDMyMzc1NDYzNmYzMjM1NzI3OTQzNTM1ODY0NzI3NzQ4NmQ2ZDY5NDY3MDMyNTE0YjQyNjc1MTQzNmIwYTY3NGE0NjY3NmM1ODQ2NjI0NDM0NTEyYjZmNTM0NzYyNjE0YTYyNGI3YTU5NGQ0YzM0NGY3MDYzNzQ3OTQ4MzMzNDc2NjI1ODZiNTA2NDU4Nzk1ODUwNmQ0ZDU0NTY2MjdhNDUzMDY1NTUzMTQxMzM3NDQ0NzQ1NDZlNmMzMTc2MGE2YTU3MzA1OTU2NTg2MTQ5NTM0ODJiNTg0NDUwNjI2YjQzMmI0YTM4MmI3MTQzMzU3ODZmMzQ0ZDUxNmIzMjQ0NzM2MzZiNGU3MzY0Nzc3MDUzNTYzMTUwNGQ1MDM3NTA0NTU5NDkzOTZjNmQzMDQ4NmEzOTQxMzk0NDY1NzQ0MTBhNjY3OTQxMzU1YTc1NzQ0ZTU0NGU3MjQ1NTU2OTUzMzc0ZjY2NmY0MjYxNGM1MTc3NmM1NDM1MzkzNjRhNzk2ZTc5MzA3ODU3N2E3MjQ0NGM3Mzc3NGI0MjY3NDU3MzQ2NmYyZjJiNzYzNDZkNjY1MzU2NjQ2YzM5NjU1MTMyNmMwYTMyNDI2NTcxMmY2ZDY1NDM3ODZhNTczMjY4NTQzNTYyNzg2YjY2NGY0ZDU3NjM3OTc0NmE3NzRhMzI3MjU5NDYyZjU4NmM0YTY5NzMzNTVhNWE1MzczNDU1NzRlMzA3NTcwNDc0MTUwNDg2YTY1Njg0YTUwMzc2MzQ5NDY0MjcxMGE0ZjM5NDE1NTM4NmQ0YzcxNWE0ZjQyMzk0ZDM2MzgzMjc2NDYzODY0NTI0NjJmNGQ0ZjU4NzE2MTRlNGYzOTQ5MmYzNDc0Nzc0YjZmMzYzOTZhMzg0YzQ0MmYzMjY3NmI3MjU5NTE0OTZjNGU3MjM5NmQ2NjM2NDQ1MjdhMzI0YjBhNjc2ODcwNjM3MjUwMzgzMDcxNTI2YzRlMzA1MjRkNjkzMDcwNGE1MzY5NjY3ODJiMGEyZDJkMmQyZDJkNDU0ZTQ0MjA1MDUyNDk1NjQxNTQ0NTIwNGI0NTU5MmQyZDJkMmQyZDBh
```
┌──(kali㉿kali)-[~/picoctf/competencia1/StegoRSA]
└─$ wget https://challenge-files.picoctf.net/c_plain_mesa/5b62df520d0762ee68a7a8e4fc39b4584d68c8be61ca062848fe2f3943af21d9/flag.enc  
--2026-03-27 22:56:42--  https://challenge-files.picoctf.net/c_plain_mesa/5b62df520d0762ee68a7a8e4fc39b4584d68c8be61ca062848fe2f3943af21d9/flag.enc
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.161.44.61, 3.161.44.22, 3.161.44.84, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.161.44.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 256 [application/octet-stream]
Saving to: ‘flag.enc’

flag.enc                                  100%[=====================================================================================>]     256  --.-KB/s    in 0s      

2026-03-27 22:56:43 (70.0 MB/s) - ‘flag.enc’ saved [256/256]

                                                                                                                                                                        
┌──(kali㉿kali)-[~/picoctf/competencia1/StegoRSA]
└─$ wget https://challenge-files.picoctf.net/c_plain_mesa/5b62df520d0762ee68a7a8e4fc39b4584d68c8be61ca062848fe2f3943af21d9/image.jpg
--2026-03-27 22:56:57--  https://challenge-files.picoctf.net/c_plain_mesa/5b62df520d0762ee68a7a8e4fc39b4584d68c8be61ca062848fe2f3943af21d9/image.jpg
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.161.44.103, 3.161.44.84, 3.161.44.22, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.161.44.103|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 20794 (20K) [application/octet-stream]
Saving to: ‘image.jpg’

image.jpg                                 100%[=====================================================================================>]  20.31K  --.-KB/s    in 0s      

2026-03-27 22:56:57 (47.9 MB/s) - ‘image.jpg’ saved [20794/20794]

                                                                                                                                                                        
┌──(kali㉿kali)-[~/picoctf/competencia1/StegoRSA]
└─$ file image.jpg   
image.jpg: JPEG image data, JFIF standard 1.01, aspect ratio, density 1x1, segment length 16, comment: "2d2d2d2d2d424547494e2050524956415445204b45592d2d2d2d2d0a4d494945766749424144414e42676b71686b6947397730424151454641415343424b67", baseline, precision 8, 512x512, components 3
                                                                                                                                                                        
┌──(kali㉿kali)-[~/picoctf/competencia1/StegoRSA]
└─$ file flag.enc 
flag.enc: data
                                                                                                                                                                        
┌──(kali㉿kali)-[~/picoctf/competencia1/StegoRSA]
└─$ cat flag.enc
&l��D�D�/eZ����&i��L��s� ?�G}>��5Oݙ]a��
�;,܊���p�;K�{[�D�2r�V/m�;�T�wrτ)��w/���s;▒�l���Գ�|����Sk�Q��M��|�?Am!>#"=�0_ŖoY(g���&�?9�K�y���n�ϟߩy�����M�
   ��1ls����帀���pX��/n�l���O;�w��UYR>����S�r�+� R��H����3 
t��ˆ                                                                                                                                                                        
┌──(kali㉿kali)-[~/picoctf/competencia1/StegoRSA]
└─$ exiv2 image.jpg      
File name       : image.jpg
File size       : 20794 Bytes
MIME type       : image/jpeg
Image size      : 512 x 512
image.jpg: No Exif data found in the file
                                                                                                                                                                        
┌──(kali㉿kali)-[~/picoctf/competencia1/StegoRSA]
└─$ nano solve.pem                     
                                                                                                                                                                        
┌──(kali㉿kali)-[~/picoctf/competencia1/StegoRSA]
└─$ nano solve.pem
                                                                                                                                                                        
┌──(kali㉿kali)-[~/picoctf/competencia1/StegoRSA]
└─$ openssl rsautl -decrypt -inkey solve.pem -in flagenc -out key.bin
The command rsautl was deprecated in version 3.0. Use 'pkeyutl' instead.
Can't open "flagenc" for reading, No such file or directory
40D7A986CF7F0000:error:80000002:system library:BIO_new_file:No such file or directory:../crypto/bio/bss_file.c:67:calling fopen(flagenc, rb)
40D7A986CF7F0000:error:10000080:BIO routines:BIO_new_file:no such file:../crypto/bio/bss_file.c:75:
                                                                                                                                                                        
┌──(kali㉿kali)-[~/picoctf/competencia1/StegoRSA]
└─$ openssl rsautl -decrypt -inkey solve.pem -in flag.enc -out key.bin
The command rsautl was deprecated in version 3.0. Use 'pkeyutl' instead.
                                                                                                                                                                        
┌──(kali㉿kali)-[~/picoctf/competencia1/StegoRSA]
└─$ openssl rsautl -decrypt -inkey solve.pem -in flag.enc -out decrypted_file.txt
The command rsautl was deprecated in version 3.0. Use 'pkeyutl' instead.
                                                                                                                                                                        
┌──(kali㉿kali)-[~/picoctf/competencia1/StegoRSA]
└─$ ls
decrypted_file.txt  flag.enc  image.jpg  key.bin  solve.pem
                                                                                                                                                                        
┌──(kali㉿kali)-[~/picoctf/competencia1/StegoRSA]
└─$ cat decrypted_file.txt
picoCTF{rs4_k3y_1n_1mg_66388eb3}

```
picoCTF{rs4_k3y_1n_1mg_66388eb3}
## Notas


## Referencias
