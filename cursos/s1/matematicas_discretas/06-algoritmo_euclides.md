# Algoritmo Euclides

## Lema

#Lema $\forall a,b,q,r\in\Z \land a=bq+r \implies \mcd(a,b)=\mcd(b,r)$

==Demostración==

Tenemos que 
$$
\begin{split}
a=bq+r \\
r=a-bq
\end{split}
$$
Probemos que $a$ y $b$ tienen los mismos divisores comunes que $b$ y $r$ . Así $\mcd(a,b)=\mcd(b,r)$
- Supongamos $d|a \land d|b$ Luego por [[cursos/s1/matematicas_discretas/02-divisibilidad#Teorema|teorema]] $d|a-bq$ y como $r=a-bq$
  $\therefore d|r$
- Supongamos $d|b\land d|r$ Luego $d|bq+r$ y como $a=bq+r$
  $\therefore d|a$ 
Por lo tanto hemos probado que cualquier divisor común de $b$ y $r$ también es divisor común de $a$ y $b$
$\therefore \mcd(a,b)=\mcd(b,r)$

## Ejemplo

Hallar el $mcd(287,91)$

Dividir mas grande entre mas pequeño  $287/91$ por algoritmo de la division $287=91\cdot 3+14$
Fijémonos que cualquier divisor de $91$ y $287$ debe ser un divisor de $14=287-91\cdot3$ de modo que si $d$ es un divisor de $91$ y $287$ entonces
$$
287=d\cdot q_1 \land 91 = d\cdot q_2
$$
Luego
$$
\begin{split}
14 &= 287-91\cdot3 \\
&= d\cdot q_1 - d\cdot q_2 \cdot 3 \\
&= d(q_1 - q_2 \cdot 3)
\end{split}
$$
Es decir, $d$ es un divisor de 14
De igual forma se prueba que cualquier divisor de $91$ y $14$ debe ser un divisor de $287$

Por lo tanto el $\mcd(287,91)=\mcd(91,14)$

Hallar el $mcd(91,14)$
$$
\begin{split}
91&=14\cdot6+7 \\
7&=91-14\cdot6
\end{split}
$$
Cualquier divisor de 91 y 14 también divide a 7 y cualquier divisor común de 14 y 7 divide a 91, luego
$$
\mcd(91,14)=\mcd(14,7)
$$
Y continua de la misma forma:
$$
14=7\cdot2
$$
luego $\mcd(14,7)=7$

Por lo tanto
$$
\mcd(287,91)=\mcd(91,14)=\mcd(14,7)=7
$$
En conclusion, el algoritmo de Euclides para hallar el $\mcd$ de dos enteros  $a$ y $b$ utiliza divisiones sucesivas hasta que uno de los enteros se haga cero (residuo $0$)