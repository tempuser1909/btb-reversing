# 1. ELF STRUCTURE

### File layout
File header + file data

#### File header
It is just mainly used to define what type of file this is. It also tells us if its 32-bit or 64-bit.

For 32-bit, the file header is 52 bytes long.
For 64-bit, the file header is 64 bytes long.

#### Sections
- .text --> the actual instructions
- .data --> global read/write data
- .rdata --> read-only data, eg. strings
- .bss --> uninitialised data
- .idata
- .edata

#### Analyzing
You can also use ```readelf``` to analyze ELF files to get more information.

#### Reference links:
- https://en.wikipedia.org/wiki/Executable_and_Linkable_Format 
- https://resources.infosecinstitute.com/complete-tour-of-pe-and-elf-part-1/#article
