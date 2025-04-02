# Mínimo Común Múltiplo

El mínimo común múltiplo de dos enteros positivos $a$ y $b$ es el menor entero positivo que es divisible tanto por $a$ como por $b$ y se representa por $\mcm(a,b)$

Sean $a,b\in\Z$ . El menor entero $c$ tal que $a|c\land b|c$ se llama máximo común divisor y se denota por $\mcm(a,b)$

## Formas básica de hallar MCM

==Ejemplo==

Hallar $\mcm(9,6)$

### Por múltiplos

Múltiplos de $9=\{0,9,\boxed{18},27,\boxed{36},45,\boxed{54},63,72,81\cdots\}$
Múltiplos de $6=\{0,6,12,\boxed{18},24,30,\boxed{36},42,48,\boxed{54},\cdots\}$
$\therefore \mcd(9,6)=18$

### Por divisibilidad

$18$ es divisible por $9$ si porque $18=9\cdot2$
$18$ es divisible por $6$ si porque $18=6\cdot3$
$\therefore mcm(9,6)=18$

## Forma avanzada de hallar MCM

Lo mismo que la [[cursos/s1/matematicas_discretas/05-maximo_comun_divisor#Forma avanzada de hallar MCD|forma avanzada para hallar MCD]] pero en vez de buscar el exponente mínimo buscamos el maximo

Hallamos la descomposición en factores primos de $a$ y $b$ es decir:

$a=P_1^{m_1} \cdot P_2^{m_2} \cdot \dotsc \cdot P_k^{m_k}$
$b=P_1^{n_1} \cdot P_2^{n_2} \cdot \dotsc \cdot P_k^{n_k}$

Donde $P_1,P_2,\dots,P_k$ son números primos y $m_1,m_2,\dots,m_k$ y $n_1,n_2,\dots,n_k$ son enteros no negativos. De modo que:

$\mcd(a,b) = P_1^{\max(m_1,n_1)} \cdot P_2^{\max(m_2,n_2)} \cdot \dotsc \cdot P_k^{\max(m_k,n_k)}$

==Ejemplo==

Hallar $\mcm(9,6)$

$$
\begin{split}
9 &= 3^2 &&= 2^0\cdot3^2\\
6 &= 2\cdot3 &&= 2^1\cdot3^1\\
\mcm(9,6) &= 18  &&= 2^1\cdot3^2
\end{split}
$$

## [[cursos/s1/matematicas_discretas/ejercicios/04-mcm.ej|Ejercicios]]
