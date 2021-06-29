# Reykjavik level_4 (35 points)

> cmp #0xda6f, -0x24(r4)

### Register State
> pc  2448  sp  43da  sr  0000  cg  0000
> r04 43fe  r05 5a08  r06 0000  r07 0000
> br08 0000  r09 0000  r10 0000  r11 4534
> r12 00f8  r13 00c4  r14 0002  r15 0200

### Live Memory Dump
> 43c0:   0000 0000 0000 0000 0000 0000 0000 7824   ..............x$
> 43d0:   0100 4424 0200 da43 1f00 7a7a 7a7a 7a7a   ..D$...C..zzzzzz   // I entered zzzzzzzzzzzzzz as password
> 43e0:   7a7a 7a7a 7a7a 7a7a 0000 0000 0000 0000   zzzzzzzz........   // when prompted for purpose of testing
> 43f0:   0000 0000 0000 0000 0000 0000 0000 4e44   ..............ND

- So basically its just comparing da64 with 1st and 2nd input character. 
- Hence keeping in mind the little endianness of system,
- Our 2nd character's hex will be da and 1st character's hex will be 6f.

` One among passwords =>"6fda"`