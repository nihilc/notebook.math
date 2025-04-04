## Teorema

#Teorema $a,b \in \Z^+\implies ab=\mcd(a,b)\cdot\mcm(a,b)$

==Demostración==

Realizamos la descomposición de $a$ y $b$ en factores primos:

$a=P_1^{a_1}P_2^{a_2}\cdots P_n^{a_n}$
$b=P_1^{b_1}P_2^{b_2}\cdots P_n^{b_n}$

Donde $P_1,P_2,\dots,P_N$ son primos y $a_1,a_2,\dots,a_n$ y $b_1,b_2,\dots,b_n$ son enteros positivos
Ahora
$\mcd(a,b)=P_1^{\min(a_1,b_1)}P_2^{\min(a_2,b_2)}\cdots P_n^{\min(a_n,b_n)}$
$\mcm(a,b)=P_1^{\max(a_1,b_1)}P_2^{\min(a_2,b_2)}\cdots P_n^{\min(a_n,b_n)}$
Luego
$$
\begin{split}
\mcd(a,b)\cdot\mcm(a,b)
	&= [ P_1^{\min(a_1,b_1)} \cdot P_2^{\min(a_2,b_2)} \cdots P_n^{\min(a_n,b_n)} ] \cdot [ P_1^{\max(a_1,b_1)} \cdot P_2^{\max(a_2,b_2)} \cdots P_n^{\max(a_n,b_n)} ] \\
	&= P_1^{a_1+b_1} \cdot P_2^{a_2+b_2} \cdots P_n^{a_n+b_n} \\
	&= P_1^{a_1}P_1^{b_1} \cdot P_2^{a_2}P_2^{b_2} \cdots P_n^{a_n}P_n^{b_n} \\
	&= ( P_1^{a_1} \cdot P_2^{a_2} \cdots P_n^{a_n} ) \cdot ( P_1^{b_1} \cdot P_2^{b_2} \cdots P_n^{b_n}) \\
	&= a\cdot b
\end{split}
$$

==Ejemplo==

$a=18 \quad b=24$

$$
\begin{split}
18 &= 2^1 \cdot 3^2 \\
24 &= 2^3 \cdot 3 \\
\mcd(18,24) &= 2^1 \cdot 3^1 = 6\\
\mcm(18,24) &= 2^3 \cdot 3^2 = 72\\
\end{split}
$$

Observamos que
$$
\begin{split}
\mcd(18,24)\cdot \mcm(18,24) = 6\cdot 72 &= 432 \\
18\cdot 24 &= 432
\end{split}
$$