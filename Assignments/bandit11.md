# Bandit Level 11 to 12 Writeup

Author: [Adi Pratap Singh](https://github.com/AdiPrartapSingh)

Problem Page: [bandit11](https://overthewire.org/bandit/bandit11)

## List of Commands Used
```
ls - list files in a directory
cat - view contents of a readable file
tr - traranforming input on the basis of desired rules
```

## Walkthrough
I searched and got to know about ROT-13 cipher. Then I searched for how to do it on a text file. Then I felt the use of piping operators.

## Password
`5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu`

## Bash/Python script to automate the process
```
cat data.txt
tr 'A-Za-z' 'N-ZA-Mn-za-m' < data.txt

```

## Suggested modifications [Optional]
It was a short step hence not much can be thought of.
Changing the cipher algo can be done.
The idea of tr can be made more clearer by imposing addition rules to cipher such as deletion etc. 
