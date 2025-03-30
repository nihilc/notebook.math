# Números Primos

Todo numero entero positivo es divisible por $1$ y por si mismo
Un entero positivo $p>1$ se llama primo si los únicos divisores positivos de $p$ son $1$ y $p$
Si un entero positivo no es primo se llama compuesto

$\P=\{2,3,5,7,11,13,17,19,23,29,\dots\}$

==Ejemplo==
Determine si un numero dado es primo o compuesto:
1. 121
   No Primo porque $11|121$
2. 53
   Primo porque $\forall n\in\Z,(n|53 \implies n=1 \lor n=53)$
3. 259
   No Primo porque $7|259$
4. 641
   Primo porque $\forall n\in\Z,(n|641 \implies n=1 \lor =n=641)$

## Teoremas

### Teorema Fundamental de la Aritmética FTA 

#Teorema Todo entero positivo mayor que $1$ se puede escribir de forma unica como un primo o como el producto de dos o mas primos, en el que los factores primos se escriben de forma no decreciente

==Ejemplo==
Descomponga en primos:
1. $89=89$
2. $256=2^8$
3. $525=3\cdot5^2\cdot7$
4. $1000=2^3\cdot5^3$

### Teorema

#Teorema Si $n$ es un entero compuesto entonces $n$ tiene un divisor primo menor o igual $\sqrt{n}$

==Demostración==

Supongamos que $n$ es un entero compuesto, Es decir $\exists k \in \Z \land k\not=1 \land k=not=n$ tal que $k|n$ de modo que $n=k\cdot l$ donde $l\in\Z$
Observemos que $k\leq\sqrt{n}$ y $l\leq\sqrt{n}$ , dado que si no fuera asi, es decir si $k\geq\sqrt{n}$ o $l\geq\sqrt{n}$ entonces $k \cdot l > \sqrt{n}\cdot\sqrt{n}$ luego $k\cdot l > n$ lo cual es falso

Si $k$ es primo entonces queda probado que $n$ tiene un divisor primo menor o igual que $\sqrt{n}$

Si $k$ y $l$ no son primos entonces por el [[#Teorema Fundamental de la Aritmética FTA|FTA]] poseen al menos un divisor primo, y como $k$ o $l$ son menores o iguales que $\sqrt{n}$ este divisor también lo sera

==Ejemplo==

Para saber si 817 es primo o compuesto buscamos si es divisible por un entero menor o igual que $\sqrt{817} \approx 28.58$

Buscamos los primos menores que $P<28=\{2,3,5,7,11,13,17,19,23\}$
Encontramos que $817=19\cdot43$ por lo que $817$ es compuesto

==Observe==

Por el teorema anterior, si un entero positivo $n$ no tiene divisores primos menores o iguales que $\sqrt{n}$ entonces $n$ es primo

### Teorema

#Teorema Existen infinitos números primos

==Demostración== (*Por reducción al absurdo*)

Supongamos que existen un numero finito de primos $\{P_1,P_2,P_3\dots,P_n\}$, Sea $Q=P_1\cdot P_2\cdot P_3\cdot \dotsc \cdot P_n + 1$

Observe que $P_1,P_2,P_3,\dots,P_n$ no son divisores de $Q$ #_duda

Además $Q$ puede ser primo o compuesto y por [[#Teorema Fundamental de la Aritmética FTA|FTA]] si $Q$ es compuesto se puede descomponer en factores primos

- Si $Q$ fuera primo entonces $Q$ seria otro primo fuera de $\{P_1,P_2,P_3,\dots,P_n\}$ lo cual no puede ocurrir
- Si $Q$ fuera compuesto debe existir algún $P_j \in \{P_1,P_2,P_3,\dots,P_n\}$ tal que $P_j|Q$
  Pero también $P_j|P_1\cdot P_2\cdot P_3\cdot \dotsc \cdot P_n$
  Luego $P_j|Q-P_1\cdot P_2\cdot P_3\cdot \dotsc \cdot P_n$ Es decir $P_J|1$

## Primos Relativos

Los enteros positivos $a$ y $b$ se llaman primos relativos si su [[cursos/s1/matematicas_discretas/05-maximo_comun_divisor|MCD]] $\mcd(a,b)=1$

Los enteros $a_1,a_2,\dots,a_n$ son primos relativos dos a dos si $\mcd(a_i,a_j)=1$ para $i=1,\dots,n$ y $j=1,\dots,n$ con $i\not=j$

==Ejemplo==

$68,99,5,7$ son primos relativos dos a dos porque:
$$
\begin{split}
\mcd(68,99)=1 \\
\mcd(68,5)=1 \\
\mcd(68,7)=1 \\
\mcd(99,5)=1 \\
\mcd(99,7)=1 \\
\mcd(5,7)=1 \\
\end{split}
$$

