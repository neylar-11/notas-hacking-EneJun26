# Reto
## Descripción
Can you figure out how this program works to get the flag?Connect to the program with netcat:`$ nc saturn.picoctf.net 50361`The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/527/picker-IV.c). The binary can be downloaded [here](https://artifacts.picoctf.net/c/527/picker-IV).
## Solución
### Solucion

```
┌──(kali㉿kali)-[~/picoctf/reversingp2/p4]
└─$ nc saturn.picoctf.net 50361                        
Enter the address in hex to jump to, excluding '0x': 
j 
You input 0x7ffe
Segfault triggered! Exiting.

o
                                                                                                                                                                      
┌──(kali㉿kali)-[~/picoctf/reversingp2/p4]
└─$ wget https://artifacts.picoctf.net/c/527/picker-IV.c  
--2026-05-06 13:40:37--  https://artifacts.picoctf.net/c/527/picker-IV.c
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.225.222.105, 13.225.222.125, 13.225.222.28, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.225.222.105|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 839 [application/octet-stream]
Saving to: ‘picker-IV.c’

picker-IV.c                               100%[===================================================================================>]     839  --.-KB/s    in 0s      

2026-05-06 13:40:38 (8.38 MB/s) - ‘picker-IV.c’ saved [839/839]

                                                                                                                                                                      
┌──(kali㉿kali)-[~/picoctf/reversingp2/p4]
└─$ wget https://artifacts.picoctf.net/c/527/picker-IV  
--2026-05-06 13:40:48--  https://artifacts.picoctf.net/c/527/picker-IV
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.225.222.105, 13.225.222.120, 13.225.222.28, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.225.222.105|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 17272 (17K) [application/octet-stream]
Saving to: ‘picker-IV’

picker-IV                                 100%[===================================================================================>]  16.87K  --.-KB/s    in 0.001s  

2026-05-06 13:40:49 (20.9 MB/s) - ‘picker-IV’ saved [17272/17272]

                                                                                                                                                                      
┌──(kali㉿kali)-[~/picoctf/reversingp2/p4]
└─$ ls
picker-IV  picker-IV.c
                                                                                                                                                                      
┌──(kali㉿kali)-[~/picoctf/reversingp2/p4]
└─$ file picker-IV   
picker-IV: ELF 64-bit LSB executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=12b33c5ff389187551aae5774324da558cee006c, for GNU/Linux 3.2.0, not stripped
                                                                                                                                                                      
┌──(kali㉿kali)-[~/picoctf/reversingp2/p4]
└─$ objdump -help    
objdump: 'a.out': No such file
                                                                                                                                                                      
┌──(kali㉿kali)-[~/picoctf/reversingp2/p4]
└─$ objdump --help
Usage: objdump <option(s)> <file(s)>
 Display information from object <file(s)>.
 At least one of the following switches must be given:
  -a, --archive-headers    Display archive header information
  -f, --file-headers       Display the contents of the overall file header
  -p, --private-headers    Display object format specific file header contents
  -P, --private=OPT,OPT... Display object format specific contents
  -h, --[section-]headers  Display the contents of the section headers
  -x, --all-headers        Display the contents of all headers
  -d, --disassemble        Display assembler contents of executable sections
  -D, --disassemble-all    Display assembler contents of all sections
      --disassemble=<sym>  Display assembler contents from <sym>
  -S, --source             Intermix source code with disassembly
      --source-comment[=<txt>] Prefix lines of source code with <txt>
  -s, --full-contents      Display the full contents of all sections requested
  -Z, --decompress         Decompress section(s) before displaying their contents
  -g, --debugging          Display debug information in object file
  -e, --debugging-tags     Display debug information using ctags style
  -G, --stabs              Display (in raw form) any STABS info in the file
  -W, --dwarf[a/=abbrev, A/=addr, r/=aranges, c/=cu_index, L/=decodedline,
              f/=frames, F/=frames-interp, g/=gdb_index, i/=info, o/=loc,
              m/=macro, p/=pubnames, t/=pubtypes, R/=Ranges, l/=rawline,
              s/=str, O/=str-offsets, u/=trace_abbrev, T/=trace_aranges,
              U/=trace_info]
                           Display the contents of DWARF debug sections
  -Wk,--dwarf=links        Display the contents of sections that link to
                            separate debuginfo files
  -WK,--dwarf=follow-links
                           Follow links to separate debug info files (default)
  -WN,--dwarf=no-follow-links
                           Do not follow links to separate debug info files
  -L, --process-links      Display the contents of non-debug sections in
                            separate debuginfo files.  (Implies -WK)
      --ctf[=SECTION]      Display CTF info from SECTION, (default `.ctf')
      --sframe[=SECTION]   Display SFrame info from SECTION, (default '.sframe')
  -t, --syms               Display the contents of the symbol table(s)
  -T, --dynamic-syms       Display the contents of the dynamic symbol table
  -r, --reloc              Display the relocation entries in the file
  -R, --dynamic-reloc      Display the dynamic relocation entries in the file
  @<file>                  Read options from <file>
  -v, --version            Display this program's version number
  -i, --info               List object formats and architectures supported
  -H, --help               Display this information

 The following switches are optional:
  -b, --target=BFDNAME           Specify the target object format as BFDNAME
  -m, --architecture=MACHINE     Specify the target architecture as MACHINE
  -j, --section=NAME             Only display information for section NAME
  -M, --disassembler-options=OPT Pass text OPT on to the disassembler
  -EB --endian=big               Assume big endian format when disassembling
  -EL --endian=little            Assume little endian format when disassembling
      --file-start-context       Include context from start of file (with -S)
  -I, --include=DIR              Add DIR to search list for source files
  -l, --line-numbers             Include line numbers and filenames in output
  -F, --file-offsets             Include file offsets when displaying information
  -C, --demangle[=STYLE]         Decode mangled/processed symbol names
                                   STYLE can be "none", "auto", "gnu-v3",
                                   "java", "gnat", "dlang", "rust"
      --recurse-limit            Enable a limit on recursion whilst demangling
                                  (default)
      --no-recurse-limit         Disable a limit on recursion whilst demangling
  -w, --wide                     Format output for more than 80 columns
  -U[d|l|i|x|e|h]                Controls the display of UTF-8 unicode characters
  --unicode=[default|locale|invalid|hex|escape|highlight]
  -z, --disassemble-zeroes       Do not skip blocks of zeroes when disassembling
      --start-address=ADDR       Only process data whose address is >= ADDR
      --stop-address=ADDR        Only process data whose address is < ADDR
      --no-addresses             Do not print address alongside disassembly
      --prefix-addresses         Print complete address alongside disassembly
      --[no-]show-raw-insn       Display hex alongside symbolic disassembly
      --insn-width=WIDTH         Display WIDTH bytes on a single line for -d
      --adjust-vma=OFFSET        Add OFFSET to all displayed section addresses
      --show-all-symbols         When disassembling, display all symbols at a given address
      --special-syms             Include special symbols in symbol dumps
      --inlines                  Print all inlines for source line (with -l)
      --prefix=PREFIX            Add PREFIX to absolute paths for -S
      --prefix-strip=LEVEL       Strip initial directory names for -S
      --dwarf-depth=N            Do not display DIEs at depth N or greater
      --dwarf-start=N            Display DIEs starting at offset N
      --dwarf-check              Make additional dwarf consistency checks.
      --ctf-parent=NAME          Use CTF archive member NAME as the CTF parent
      --visualize-jumps          Visualize jumps by drawing ASCII art lines
      --visualize-jumps=color    Use colors in the ASCII art
      --visualize-jumps=extended-color
                                 Use extended 8-bit color codes
      --visualize-jumps=off      Disable jump visualization
      --disassembler-color=off       Disable disassembler color output. (default)
      --disassembler-color=terminal  Enable disassembler color output if displaying on a terminal.
      --disassembler-color=on        Enable disassembler color output.
      --disassembler-color=extended  Use 8-bit colors in disassembler output.

objdump: supported targets: elf64-x86-64 elf32-i386 elf32-iamcu elf32-x86-64 pei-i386 pe-x86-64 pei-x86-64 elf64-little elf64-big elf32-little elf32-big pe-bigobj-x86-64 pe-i386 pdb srec symbolsrec verilog tekhex binary ihex plugin
objdump: supported architectures: i386 i386:x86-64 i386:x64-32 i8086 i386:intel i386:x86-64:intel i386:x64-32:intel iamcu iamcu:intel

The following i386/x86-64 specific disassembler options are supported for use
with the -M switch (multiple options should be separated by commas):
  x86-64      Disassemble in 64bit mode
  i386        Disassemble in 32bit mode
  i8086       Disassemble in 16bit mode
  att         Display instruction in AT&T syntax
  intel       Display instruction in Intel syntax
  att-mnemonic  (AT&T syntax only)
              Display instruction with AT&T mnemonic
  intel-mnemonic  (AT&T syntax only)
              Display instruction with Intel mnemonic
  addr64      Assume 64bit address size
  addr32      Assume 32bit address size
  addr16      Assume 16bit address size
  data32      Assume 32bit data size
  data16      Assume 16bit data size
  suffix      Always display instruction suffix in AT&T syntax
  amd64       Display instruction in AMD64 ISA
  intel64     Display instruction in Intel64 ISA

Options supported for -P/--private switch:
For PE files:
  header      Display the file header
  sections    Display the section headers
Report bugs to <https://sourceware.org/bugzilla/>.
                                                                                                                                                                      
┌──(kali㉿kali)-[~/picoctf/reversingp2/p4]
└─$ objdump -D picker-IV | grep win
000000000040129e <win>:
  4012d2:       75 16                   jne    4012ea <win+0x4c>
  4012f9:       eb 1a                   jmp    401315 <win+0x77>
  401319:       75 e0                   jne    4012fb <win+0x5d>
                                                                                                                                                                      
┌──(kali㉿kali)-[~/picoctf/reversingp2/p4]
└─$ nc saturn.picoctf.net 50361                        
Enter the address in hex to jump to, excluding '0x': 40129e
You input 0x40129e
You won!
picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_01672a61}

```
picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_01672a61}
## Notas


## Referencias
