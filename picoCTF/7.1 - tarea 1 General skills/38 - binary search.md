# Reto
## Descripción
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/17/challenge.zip)

`ssh -p 63983 ctf-player@atlas.picoctf.net`Using the password `f3b61b38`. Accept the fingerprint with `yes`, and `ls` once connected to begin. Remember, in a shell, passwords are hidden!
## Solución
### Solucion

```
neylar11-picoctf@webshell:~$ ssh -p 63983 ctf-player@atlas.picoctf.net
The authenticity of host '[atlas.picoctf.net]:63983 ([18.217.83.136]:63983)' can't be established.
ED25519 key fingerprint is SHA256:M8hXanE8l/Yzfs8iuxNsuFL4vCzCKEIlM/3hpO13tfQ.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[atlas.picoctf.net]:63983' (ED25519) to the list of known hosts.
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 453
Lower! Try again.
Enter your guess: 400
Lower! Try again.
Enter your guess: 300
Lower! Try again.
Enter your guess: 100
Lower! Try again.
Enter your guess: 20
Higher! Try again.
Enter your guess: 30
Higher! Try again.
Enter your guess: 50
Higher! Try again.
Enter your guess: 70
Higher! Try again.
Enter your guess: 90
Higher! Try again.
Enter your guess: 95
Higher! Try again.
Sorry, you've exceeded the maximum number of guesses.
Connection to atlas.picoctf.net closed.
neylar11-picoctf@webshell:~$ ssh -p 63983 ctf-player@atlas.picoctf.net
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 98
Higher! Try again.
Enter your guess: 99
Higher! Try again.
Enter your guess: 100
Higher! Try again.
Enter your guess: 120
Higher! Try again.
Enter your guess: 150
Higher! Try again.
Enter your guess: 190
Higher! Try again.
Enter your guess: 210
Higher! Try again.
Enter your guess: 250
Higher! Try again.
Enter your guess: 300
Higher! Try again.
Enter your guess: 400
Higher! Try again.
Sorry, you've exceeded the maximum number of guesses.
Connection to atlas.picoctf.net closed.
neylar11-picoctf@webshell:~$ ssh -p 63983 ctf-player@atlas.picoctf.net
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Lower! Try again.
Enter your guess: 400
Higher! Try again.
Enter your guess: 460
Lower! Try again.
Enter your guess: 456
Lower! Try again.
Enter your guess: 453
Lower! Try again.
Enter your guess: 451
Lower! Try again.
Enter your guess: 450
Lower! Try again.
Enter your guess: 430
Lower! Try again.
Enter your guess: 410
Higher! Try again.
Enter your guess: 420
Higher! Try again.
Sorry, you've exceeded the maximum number of guesses.
Connection to atlas.picoctf.net closed.
neylar11-picoctf@webshell:~$ ssh -p 63983 ctf-player@atlas.picoctf.net
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 425
Higher! Try again.
Enter your guess: 430
Higher! Try again.
Enter your guess: 450
Lower! Try again.
Enter your guess: 440
Lower! Try again.
Enter your guess: 435
Lower! Try again.
Enter your guess: 432
Higher! Try again.
Enter your guess: 434
Lower! Try again.
Enter your guess: 433
Congratulations! You guessed the correct number: 433
Here's your flag: picoCTF{g00d_gu355_6dcfb67c}
Connection to atlas.picoctf.net closed.
neylar11-picoctf@webshell:~$ ^C
neylar11-picoctf@webshell:~$ 
```
picoCTF{g00d_gu355_6dcfb67c}
## Notas


## Referencias
