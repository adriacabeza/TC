## Examens

### Exam on CFGs, March 27th, 2015

Exercici 1
```c 
S-> aSa|bSb|b|
```

Exercici 2
```c 
S-> bSO| aYO
Y -> bYO| aXO
X -> c|bXO
O -> a|b
```


Exercici 3
```c 
S->aaAb|bCcc|aAbCc|aaAbbCcc|
A->aaAb|
C->bCcc|
```

Exercici 4
```c 
S -> T | BbD
T -> aTa | BbDb | Tb
D -> aD | E
E -> Eb |

B -> aCa | Bb |
C -> aCa | Cb | b
```

### Exam on CFGs, March 29th, 2016

Exercici 1
```c 
S -> aRb | bRa | aSa | bSb 
R -> XRX |
X -> a | b
```

Exercici 2
```c 
S -> BaBaSbAbA | BcA
B -> bB|
A -> aA|
```
### Exam on CFGs, October 22nd, 2014
Exercici 1
```c 
S -> aXa|bYb
X -> bXb|a
Y-> bSb|aXa
```

Exercici 2
```c 
S-> A | B 

A-> aAc|L
L-> Lbb|N
N-> aN|a

B->aBc|bM
M->bbM|R
R->Rc|c
```
### Exam on CFGs, October 22nd, 2015
Exercici 1
```c
S-> aNb
N-> aMb
M-> aMb|
```
Exercici  2
```c
S-> AX|bS|c
X-> bSa|bSb|c
A-> aA|a
```

Exercici 5
```c
S-> X|
X-> (X)S|()(X)S|()
```

### Exame on REG+CFG+PDA, April 25th, 2016
Exercici  5
```c
main
{
  
  multiple5 =
    " 0 1
    0 0 1 +
    1 2 3
    2 4 0
    3 1 2
    4 3 4
    ";
  
  cicle = 
    " x 
    0 1 
    1 2
    2 3 +
    3 0
    ";
    cicler = substitution(cicle, "x"-> ("0"|"1"));
  output multiple5 | cicler;
}
```

Exam on REG+CFG+PDA, November 19th, 2014
Exercici 2
```c
main
{
	L="     a    b   
I    1    1    +
1    2    2    +
2    POZO I    +
POZO POZO POZO";
	  
	  T="   a    b   
I    1    1    +
1    2    2    +
2    3    3    +
3    4    4    +
4    I    POZO +
POZO POZO POZO";
	    
	    output T & L; 
}
```
Exercici 5
```c
main
{
 L=  "   a  b 
I  1  p  +
1  2  I 
10 p  9 
2  3  1 
3  4  2 
4  5  3 
5  6  4 
6  7  5 
7  8  6 
8  9  7 
9  10 8 
p  p  p " ;
  
  L2 = substitution(L, "a"->"(", "b"->")");
  x = "("|")";
  L3 = x x x x x x x x x x x x x x x x x x x x;
  output L2 & L3;
}
```