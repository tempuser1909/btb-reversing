# 4. ASSEMBLY CODE

#### Syntax

#### Intel
```
add eax, 1
```
- <instruction> <destination>, <source>

#### Instruction Set
- mov
- jmp
- jl
- jg
- jz
- call --> main thing to remember in order to get a faster overview of the program
- cmp
- add
- sub
- [...] --> accessing memory address to get the value at that location
- and many more

#### Registers and Flags

##### 32-bit registers
- eax
- ebx
- ecx
- edx
- esp --> stack pointer
- eip --> instruction pointer
- esi --> source index
- edi --> destination index

##### 64-bit registers
- rax
- rbx
- rcx
- rdx
- rsp
- rip
- rsi
- rdi

#### C Calling conventions
- cdecl (aka right to left order, and that return values are passed with $eax)
- stdcall (aka Windows API, right to left order, return values are also passed with $eax)
- fastcall (not standard across compilers, first 2/3 32-bit arguments are passed with $eax, $ecx, $edx, also often found to be right to left order)

#### C++ Calling conventions
- thiscall --> pointer to class object is passed via $ecx, right to left order, return value passed via $eax
- name mangling --> it is just how C++ function names are being added with more information
- extern "C"

#### Reference links
- https://en.wikibooks.org/wiki/X86_Disassembly/Calling_Conventions