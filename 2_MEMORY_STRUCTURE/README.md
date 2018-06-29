# 2. MEMORY STRUCTURE

#### Stack & Heap

| Address | Value |
|:----:|:----:|
| 0x0 | &nbsp; |
| 0x1 | &nbsp; |
| 0x2 | &nbsp; |
| 0x3 | &nbsp; |
| 0x4 | &nbsp; |
| 0x5 | &nbsp; |
| 0x6 | &nbsp; |
| 0x7 | &nbsp; |
| 0x8 | &nbsp; |
| 0x9 | &nbsp; |
| 0xA | &nbsp; |
| 0xB | &nbsp; |
| 0xC | &nbsp; |
| 0xD | &nbsp; |
| 0xE | &nbsp; |
| 0xF | &nbsp; |

#### Stack
- saved registers
- passed arguments --> $ebp+?
- Return address --> $ebp+4
- stack frame, stack frame pointer --> $ebp
- local variables --> $ebp-?
- current stack pointer --> $esp


