# Level_2 Sydney (15 points)

- Password was directly compared in check_password function
- But it will not work because the comparison was performed in little endian system and also the hardware has 16 bit architecture.
- For the storage of values more than byte, in this system values will be stored in reverse order.
- The system stores the hex form of input. As it is greater than 1 byte, the values will be stored in reverse order in a 16 - bit space.
- For example lets say we have to store 12345678 in little endian system of 16 bit then we will make 16 bits section in the input.
- Here those will be '1234' and '5678' . Now these both will be stored in reverse order byte wise i.e as '34 12' and '78 56'.
- Hence the password hex which we get from the assembly code (7745 627a 6e23 392d) is actually stored in little endian way. so in order to get the password hex, we have to reverse it again.

`` Password hex = 4577 7a62 236e 2d39 ``