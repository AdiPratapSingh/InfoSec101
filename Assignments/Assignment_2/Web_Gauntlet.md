# PicoGym Web Exploitation Writeup

Author: [Adi Pratap Singh](https://github.com/AdiPratapSingh) 

Challenge Page: [Web Gauntlet]
(http://jupiter.challenges.picoctf.org:29164/) 
(http://jupiter.challenges.picoctf.org:29164/filter.php)

## Walkthrough
Firstly I went on with random input which displayed the corresponding SQL query.

#### For Round 1/5 :-
- I used `admin' OR 1=1;--` in username field and any random thing as password but it didn't worked. 
- Also on the second page it was written 'Round 1: OR'. 
- Then I tried `admin'; --` as username which worked and displayed Round 2/5.
- The query was `SELECT * FROM users WHERE username='admin'; --' AND password='admin'; --'`

#### For Round 2/5 :-
- On refreshing  the second page it displayed `Round2: or and like = --` which seems like it's trying to say that one can't use these operators.
- But then I used username as `admin';/*`.
- Resultant query was `SELECT * FROM users WHERE username='admin'/*' AND password='asfsdf'`

#### For Round 3/5 :-
- On refreshing  the second page it displayed `Round3: or and = like > < --` which seems like it's trying to say that one can't use these operators.
- Still `admin';/*` was valid and it worked too.

#### For Round 4/5 :-
- On refreshing  the second page it displayed `Round4: or and = like > < -- admin` which seems like it's trying to say that one can't use these operators and words.
- The main problem was `admin` being forbidden. Therefore I read about bypassing words filters in SQL.
- I tried to write admin in hex using `as` but it didn't worked.
- Then I got to know about concatination operator `||` which concatinates the two part.
- Final statement was `SELECT * FROM users WHERE username='adm'||'in';' AND password='erfwesds'`

#### For Round 5/5 :-
- On refreshing  the second page it displayed `Round4: or and = like > < -- admin union` which seems like it's trying to say that one can't use these operators and words.
- Since there was no filter on concatination operator , the above worked well here too.

## Flag
`picoCTF{y0u_m4d3_1t_a3ed4355668e74af0ecbb7496c8dd7c5}`

## Useful resources 
> https://www.geeksforgeeks.org/sql-concatenation-operator/
> https://websitesetup.org/wp-content/uploads/2020/08/SQL-Cheat-Sheet-websitesetup.pdf