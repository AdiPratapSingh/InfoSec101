# PicoGym Web Exploitation Writeup

Author: [Adi Pratap Singh](https://github.com/AdiPratapSingh) 

Challenge Page: [Where Are The Robots](https://jupiter.challenges.picoctf.org/problem/56830/)

## Walkthrough
- The bot related info of website is stored in `robots.txt` file which stores info about whether the site is allowed to be indexed by Search Engines (bots) and other stuff.
- Then I went to `https://jupiter.challenges.picoctf.org/problem/56830/robots.txt` which displayed `Disallow: /1bb4c.html`.
- Compelled by my nature of doing things which are disallowed , I went to `https://jupiter.challenges.picoctf.org/problem/56830/1bb4c.html` and there I found the flag :p.

## Flag
`picoCTF{ca1cu1at1ng_Mach1n3s_1bb4c}`

## Useful resources (if any)
- A mere google search will be enough.