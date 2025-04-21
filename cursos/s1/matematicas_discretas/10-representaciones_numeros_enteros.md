# Representaciones de Numero Enteros

(Sección 2.5 libro Rosen)
Usualmente para representar numero enteros usamos la *notación* decimal
Ejemplo: $2586 = 2 \cdot 10^3 + 5 \cdot 10^2 + 8 \cdot 10^1 + 6 \cdot 10^0 = 2000 + 500 + 80 + 6$

Sea $b$ un entero positivo mayor que 1, Sea $n$ un entero positivo cualquiera, entonces
$$
\boxed{
n=a_kb^k+a_{k-1}b^{k-1}+\cdots+a_1b+a_0
}\quad\text{(*)}
$$
de forma unica donde $k$ es un entero no negativo y $a_0,a_1,\dots,a_k$ son enteros no negativos menores que $b$ y $a_k\not=0$

A la representación (\*) de $n$ se le llama *expresión de $n$ en base $b$* y se representa por
$$
\boxed{
n_b=(a_xa_{x-1}\cdots a_1a_0)_b
}
$$

==Ejemplo==

Halle el numero entero representado por $(314)_5$
$$
\begin{split}
(314)_5 
&= 5(62)+4 \\
&= 5(5(12)+2)+4 \\
&= 5(5(5(2)+2)+2)+4 \\
&= 5(5(2\cdot5^1 + 2)+2)+4 \\
&= 5(2\cdot5^2 + 2\cdot5^1 + 2)+4 \\
&= 2\cdot5^3 + 2\cdot5^2 + 2\cdot5^1 + 4\cdot5^0 \\
&= \boxed{2224}
\end{split}
$$
![[_files/10-representaciones_numeros_enteros 20250411]]
$\therefore (314)_5$ es la representación de $2224$ en base $5$

==Ejemplo==

Halle $1583$ en base 2, 4 y 8

$$
\begin{split}
(1583)_4 &= 4(395)+3 \\
&= 4(4(98)+3)+3 \\
&= 4(4(4(24)+2)+3)+3 \\
&= 4(4(4(4(6)+0)+2)+3)+3 \\
&= 4(4(4(4(4(1)+2)+0)+2)+3)+3 \\
&= 4(4(4(4(1\cdot4^1+2)+0)+2)+3)+3 \\
&= 4(4(4(1\cdot4^2+2\cdot4^1+0)+2)+3)+3 \\
&= 4(4(1\cdot4^3+2\cdot4^2+0\cdot4^1+2)+3)+3 \\
&= 4(1\cdot4^4+2\cdot4^3+0\cdot4^2+2\cdot4^1+3)+3 \\
&= 1\cdot4^5+2\cdot4^4+0\cdot4^3+2\cdot4^2+3\cdot4^1+3\cdot4^0 \\
&= 120233
\end{split}
$$

$$
\begin{split}
(1583)_8 &= 8(197)+7 \\
&= 8(8(24)+5)+7 \\
&= 8(8(8(3))+5)+7 \\
&= 8(8(3\cdot8^1)+5)+7 \\
&= 8(3\cdot8^2+5)+7 \\
&= 3\cdot8^3+5\cdot8^1+7\cdot8^0 \\
&= 3\cdot8^3+0\cdot8^2+5\cdot8^1+7\cdot8^0 \\
&= 3057
\end{split}
$$

[[cursos/s1/matematicas_discretas/ejercicios/04-representaciones_numeros_enteros.ej|Ejercicios]]

## Expresiones hexadecimal

La base principal usada en informatica es la base 2, es decir la expresión binaria, los símbolos utilizados son 0 y 1
Otras bases también son las potencias de 2: 4, 8, 16

- Base 4: 0,1,2,3
- Base 8 u octal: 0,1,2,3,4,5,6,7
- Base 16 o hexadecimal: 0,1,2,3,4,5,6,7,8,9,A,B,C,D,F

==Ejemplo==

Halle 1543 en base hexadecimal

$$
\begin{split}
(1543)_{16} &= 16(96)+7 \\
&= 16(16(6)+0)+7 \\
&= 16(6\cdot16^1+0)+7 \\
&= 6\cdot16^2+0\cdot16^1+7\cdot16^0 \\
&= 607
\end{split}
$$

==Ejemplo==

Encuentre la expresión decimal de $n_{16}=9C1AB$

$$
\begin{split}
n &= 9\cdot16^4 + 12\cdot16^3 + 1\cdot16^2 + 10\cdot16^1 + 11\cdot16^0 \\
&= 589824 + 49152 + 256 + 160 + 11 \\
&= 639403
\end{split}
$$

## Conversion de una base a otra