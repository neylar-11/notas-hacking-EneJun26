# Reto
## Descripción
Resuelve el cuestionario.Descargue el código fuente para responder preguntas [aquí](https://challenge-files.picoctf.net/c_lonely_island/1839946f94d93b9ea33fcda2307feffc5567f00412c8e26d23430d137d8f0d00/vuln.c) .Descargue el binario para responder preguntas [aquí](https://challenge-files.picoctf.net/c_lonely_island/1839946f94d93b9ea33fcda2307feffc5567f00412c8e26d23430d137d8f0d00/vuln) .Conéctate con la instancia del desafío aquí:`nc lonely-island.picoctf.net 53883`
## Solución
### Solucion

```
┌──(kali㉿kali)-[~/picoctf/competencia1]
└─$ wget https://challenge-files.picoctf.net/c_lonely_island/1839946f94d93b9ea33fcda2307feffc5567f00412c8e26d23430d137d8f0d00/vuln.c
--2026-03-12 02:06:24--  https://challenge-files.picoctf.net/c_lonely_island/1839946f94d93b9ea33fcda2307feffc5567f00412c8e26d23430d137d8f0d00/vuln.c
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.161.44.61, 3.161.44.84, 3.161.44.103, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.161.44.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 434 [application/octet-stream]
Saving to: ‘vuln.c’

vuln.c                                    100%[=====================================================================================>]     434  --.-KB/s    in 0s      

2026-03-12 02:06:24 (81.8 MB/s) - ‘vuln.c’ saved [434/434]

                                                                                                                                                                        
┌──(kali㉿kali)-[~/picoctf/competencia1]
└─$ wget https://challenge-files.picoctf.net/c_lonely_island/1839946f94d93b9ea33fcda2307feffc5567f00412c8e26d23430d137d8f0d00/vuln  
--2026-03-12 02:06:43--  https://challenge-files.picoctf.net/c_lonely_island/1839946f94d93b9ea33fcda2307feffc5567f00412c8e26d23430d137d8f0d00/vuln
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.161.44.22, 3.161.44.103, 3.161.44.84, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.161.44.22|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16136 (16K) [application/octet-stream]
Saving to: ‘vuln’

vuln                                      100%[=====================================================================================>]  15.76K  --.-KB/s    in 0s      

2026-03-12 02:06:44 (83.5 MB/s) - ‘vuln’ saved [16136/16136]

                                                                                                                                                                        
┌──(kali㉿kali)-[~/picoctf/competencia1]
└─$ ls
vuln  vuln.c
                                                                                                                                                                        
┌──(kali㉿kali)-[~/picoctf/competencia1]
└─$ cat vuln.c
#include <stdio.h>
#include <stdlib.h>

/*
This is not the challenge, just a template to answer the questions.
To get the flag, answer all the questions. 
There are no bugs in the quiz.
There are 0xD questions in total.

*/

void win(){
        system("cat flag.txt");
}

void vuln(){
        char buffer[0x15] = {0};
        fprintf(stdout, "\nEnter payload: ");
        fgets(buffer, 0x90, stdin);
}

void main(){
        vuln();
}
                                                                                                                                                                        

┌──(kali㉿kali)-[~/picoctf/competencia1]
└─$ nc lonely-island.picoctf.net 57432

=========================================================================================================                                                               
                                   ELF BINARY ANALYSIS QUIZ                                                                                                             
=========================================================================================================                                                               
                                                                                                                                                                        

◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉
◉                                                                                                       ◉
◉  This is a simple questionnaire to analyze the binary characteristics.                                ◉
◉                                                                                                       ◉
◉  When compiling C/C++ source code in Linux, an ELF (Executable and Linkable Format) file is           ◉
◉  created. The flags added when compiling can affect the binary in various ways, like the              ◉
◉  protections.                                                                                         ◉
◉                                                                                                       ◉
◉  Dynamic Linking:                                                                                     ◉
◉  Dynamic linking is a process where a program uses external code libraries (called shared             ◉
◉  libraries or dynamic link libraries) that are loaded into memory at runtime, rather than             ◉
◉  being built directly into the executable file.                                                       ◉
◉                                                                                                       ◉
◉  Static Linking:                                                                                      ◉
◉  The code for all the routines called by your program becomes part of the executable file.            ◉
◉                                                                                                       ◉
◉  Stripped:                                                                                            ◉
◉  The binary does not contain debugging information which can be used with debuggers                   ◉
◉  like GDB.                                                                                            ◉
◉                                                                                                       ◉
◉  Non Stripped:                                                                                        ◉
◉  The binary contains no debuggig information which makes it difficult for analysis.                   ◉
◉                                                                                                       ◉
◉  Canary: A random/specific value which is stored on the stack for protection against                  ◉
◉  buffer overflow.                                                                                     ◉
◉                                                                                                       ◉
◉  Run 'file' and 'checksec' commands on the binary to answer the questions.                            ◉
◉                                                                                                       ◉
◉  Find out what are 'pwntools' and how can this library be used for exploit creation.                  ◉
◉                                                                                                       ◉
◉  To run the binary: chmod +x ./vuln , followed by ./vuln                                              ◉
◉                                                                                                       ◉
◉  Analyze the provided C program and the corresponding binary to answer the questions.                 ◉
◉                                                                                                       ◉
◉  Answer the questions about this binary to get the flag.                                              ◉
◉                                                                                                       ◉
◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉

[*] Question number 0x1:

Is this a '32-bit' or '64-bit' ELF? (e.g. 100-bit)

💡 Hint: Check if the system is x86_64 or x86. No compilation flag specified means default.

>> 64-bit


✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅                                                                                                                                                 
✅                    ✅                                                                                                                                                
✅      Correct!      ✅                                                                                                                                                
✅                    ✅                                                                                                                                                
✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅                                                                                                                                                 
                                                                                                                                                                        

[*] Question number 0x2:

What's the linking of the binary? (e.g. static, dynamic)

💡 Hint: The program uses standard library functions like fprintf, fgets, and system.

>> dynamic


✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅                                                                                                                                                 
✅                    ✅                                                                                                                                                
✅      Correct!      ✅                                                                                                                                                
✅                    ✅                                                                                                                                                
✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅                                                                                                                                                 
                                                                                                                                                                        

[*] Question number 0x3:

Is the binary 'stripped' or 'not stripped'?

💡 Hint: By default, binaries compiled without the -s flag contain debugging symbols.

>> not stripped


✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅                                                                                                                                                 
✅                    ✅                                                                                                                                                
✅      Correct!      ✅                                                                                                                                                
✅                    ✅                                                                                                                                                
✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅                                                                                                                                                 
                                                                                                                                                                        

[*] Question number 0x4:

Looking at the vuln() function, what is the size of the buffer in bytes? (e.g. 0x10)

💡 Hint: Check the declaration in the function and answer in either hex or decimal

>> 0x15


✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅                                                                                                                                                 
✅                    ✅                                                                                                                                                
✅      Correct!      ✅                                                                                                                                                
✅                    ✅                                                                                                                                                
✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅                                                                                                                                                 
                                                                                                                                                                        

[*] Question number 0x5:

How many bytes are read into the buffer? (e.g. 0x10)

💡 Hint: Check the fgets

>> 0x90


✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅                                                                                                                                                 
✅                    ✅                                                                                                                                                
✅      Correct!      ✅                                                                                                                                                
✅                    ✅                                                                                                                                                
✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅                                                                                                                                                 
                                                                                                                                                                        

[*] Question number 0x6:

Is there a buffer overflow vulnerability? (yes/no)

💡 Hint: Compare buffer size and input size

>> yes


✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅                                                                                                                                                 
✅                    ✅                                                                                                                                                
✅      Correct!      ✅                                                                                                                                                
✅                    ✅                                                                                                                                                
✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅                                                                                                                                                 
                                                                                                                                                                        

[*] Question number 0x7:

Name a standard C function that could cause a buffer overflow in the provided C code.

💡 Hint: (e.g. fprintf)

>> fgets


✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅                                                                                                                                                 
✅                    ✅                                                                                                                                                
✅      Correct!      ✅                                                                                                                                                
✅                    ✅                                                                                                                                                
✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅                                                                                                                                                 
                                                                                                                                                                        

[*] Question number 0x8:

What is the name of function which is not called any where in the program?

💡 Hint: Analyze the source

>> win


✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅                                                                                                                                                 
✅                    ✅                                                                                                                                                
✅      Correct!      ✅                                                                                                                                                
✅                    ✅                                                                                                                                                
✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅                                                                                                                                                 
                                                                                                                                                                        

[*] Question number 0x9:

What type of attack could exploit this vulnerability? (e.g. format string, buffer overflow, etc.)

💡 Hint: Try interpreting the information gathered so far

>> buffer overflow


✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅                                                                                                                                                 
✅                    ✅                                                                                                                                                
✅      Correct!      ✅                                                                                                                                                
✅                    ✅                                                                                                                                                
✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅                                                                                                                                                 
                                                                                                                                                                        

[*] Question number 0xa:

How many bytes of overflow are possible? (e.g. 0x10)

💡 Hint: Subtract values

>> 0x7b


✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅                                                                                                                                                 
✅                    ✅                                                                                                                                                
✅      Correct!      ✅                                                                                                                                                
✅                    ✅                                                                                                                                                
✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅                                                                                                                                                 
                                                                                                                                                                        

[*] Question number 0xb:

What protection is enabled in this binary?

💡 Hint: Learn to use checksec

>> NX


✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅                                                                                                                                                 
✅                    ✅                                                                                                                                                
✅      Correct!      ✅                                                                                                                                                
✅                    ✅                                                                                                                                                
✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅                                                                                                                                                 
                                                                                                                                                                        

[*] Question number 0xc:

What exploitation technique could bypass NX? (e.g. shellcode, ROP, format string)

💡 Hint: Choose from the options

>> ROP


✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅                                                                                                                                                 
✅                    ✅                                                                                                                                                
✅      Correct!      ✅                                                                                                                                                
✅                    ✅                                                                                                                                                
✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅                                                                                                                                                 
                                                                                                                                                                        




[*] Question number 0xd:

What is the address of 'win()' in hex? (e.g. 0x4011eb)

💡 Hint: Use gdb/objdump to find the address

>> 0x401176
-----------------------------------------------------------
 otra terminal: ┌──(kali㉿kali)-[~/picoctf/competencia1]
└─$ objdump -d vuln | grep "<win>"
0000000000401176 <win>:
------------------------------------------------------------
✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅                                                                                                                                                 
✅                    ✅                                                                                                                                                
✅      Correct!      ✅                                                                                                                                                
✅                    ✅                                                                                                                                                
✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅                                                                                                                                                 
                                                                                                                                                                        

=========================================================================================================
QUIZ COMPLETE!
=========================================================================================================

🎉 PERFECT SCORE! 🎉
You got 13/13 questions correct!

Flag: picoCTF{my_bIn@4y_3xpl0it_fL@g_0353e5a1}


```
picoCTF{my_bIn@4y_3xpl0it_fL@g_0353e5a1}

## Notas
- objdump -d vuln | grep "<win"
- objdump` es una utilidad disponible en sistemas Linux que permite **examinar el contenido interno de archivos binarios**, especialmente ejecutables en formato **ELF (Executable and Linkable Format). Durante el análisis del binario fue necesario identificar la dirección de algunas funciones dentro del ejecutable. Para esto se utilizó la herramienta `objdump`.
- ambos win llevan <> pero se mueve el documento
## Referencias
