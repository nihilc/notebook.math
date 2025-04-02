# Maximo Común Divisor

El mayor entero que divide a 2 enteros se llama máximo común divisor de estos enteros

Sean $a,b \in \Z$ . El mayor entero $c$ tal que $c|a \land c|b$ se llama máximo común divisor y se denota por $\mcd(a,b)$

## Forma básica de hallar MCD

==Ejemplo==

Hallar $\mcd(98,57)$
Divisores de $98 = \{\boxed1,2,7,14,49,98\}$
Divisores de $67 = \{\boxed1,3,19,57\}$
$\mcd(98,57)=1$

==Ejemplo==

Hallar $\mcd(45,120)$
Divisores de $45=\{\boxed1,\boxed3,9,\boxed{15},45\}$
Divisores de $120=\{\boxed1,2,\boxed3,4,5,6,8,10,12,\boxed{15},20,24,30,40,60\}$
$\mcd(45,120)=15$

## Forma avanzada de hallar MCD

Hallamos la descomposición en factores primos de $a$ y $b$ es decir:

$a=P_1^{m_1} \cdot P_2^{m_2} \cdot \dotsc \cdot P_k^{m_k}$
$b=P_1^{n_1} \cdot P_2^{n_2} \cdot \dotsc \cdot P_k^{n_k}$

Donde $P_1,P_2,\dots,P_k$ son números primos y $m_1,m_2,\dots,m_k$ y $n_1,n_2,\dots,n_k$ son enteros no negativos. De modo que:

$\mcd(a,b) = P_1^{\min(m_1,n_1)} \cdot P_2^{\min(m_2,n_2)} \cdot \dotsc \cdot P_k^{\min(m_k,n_k)}$

==Ejemplo==

Hallar $\mcd(68,120)$

$$
\begin{split}
68 &= 2^2\cdot17   &&= 2^2 \cdot 3^0 \cdot 11^0 \cdot 17^1\\
120 &= 3^2 \cdot11 &&= 2^0 \cdot 3^2 \cdot 11^1 \cdot 17^0\\
\mcd(68,120) &= 1  &&= 2^0 \cdot 3^0 \cdot 11^0 \cdot 17^0
\end{split}
$$

## Algoritmo de Euclides para hallar $\mcd(a,b)$

[[cursos/s1/matematicas_discretas/06-algoritmo_euclides|Algoritmo de Euclides]]

Sean $a$ y $b$ enteros positivos con $a \geq b$
Aplicamos el algoritmo de la division sucesivamente
$$
\begin{split}
a       &= bq_1 + r_1   && 0 \leq r_1 < b \\
b       &= r_1q_2 + r_2 && 0 \leq r_2 < r_1 \\
r_1     &= r_2q_3 + r_3 && 0 \leq r_3 < r_2 \\
r_2     &= r_3q_4 + r_4 && 0 \leq r_4 < r_3 \\
\vdots \\
r_{n-3} &= r_{n-2}q_{n-1} + r_{n-1} \quad\quad &&0\leq r_n < r_{n-1}\\
r_{n-2} &= r_{n-1}q_{n} + 0 \\
\end{split}
$$
Siguiendo este proceso hallamos una sucesión de residuos $r_1,r_2,\dots,r_{n-2},r_{n-1},0$ y por el [[cursos/s1/matematicas_discretas/06-algoritmo_euclides#Lema|lema]] tenemos que $\mcd(a,b)=\mcd(b,r_1)=\mcd(r_1,r_2)=\dots=\mcd(r_{n-1},0)=r_{n-1}$

Es decir $\mcd(a,b)$ es el ultimo residuo no nulo de la sucesión de divisiones

==Ejemplo==

Hallar $\mcd(621,512)$
$$
\begin{split}
621 &= 512\cdot1+109 \\
512 &= 109\cdot4+76 \\
109 &= 76\cdot1+33 \\
76 &= 33\cdot2+10 \\
33 &= 10\cdot3+3 \\
10 &= 3\cdot3+1 \\
3 &= 1\cdot3 + 0 \\
\\
\therefore \mcd(621,512) &= \mcd(512,109) \\
	&= \mcd(109,76) \\
	&= \mcd(76,33) \\
	&= \mcd(33,10) \\
	&= \mcd(10,3) \\
	&= \mcd(3,1) \\
	&= 1
\end{split}
$$
## [[cursos/s1/matematicas_discretas/ejercicios/03-mcd.ej|Ejercicios]]
