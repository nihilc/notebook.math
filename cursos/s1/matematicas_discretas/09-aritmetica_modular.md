# Aritmética Modular

Sean $a$ y $b$ enteros y $m$ entero positivo, Decimos que $a$ es **congruente** con $b$ modulo $m$ y se representa por $a \equiv b(\mod m)$ . Si $m$ divide a $a-b$; es decir $m|(a-b)$. Si $a$ no es congruente con $b$ modulo $m$ es decir $a\not\equiv b(\mod m)$

==Ejemplo==

$8\equiv2(\mod 3)$?

Veamos si $3|8-2$ es decir $3|6$
Es cierto que $3|6$ porque $6=3\cdot2$
$\therefore 8\equiv2(\mod 3)$

==Ejemplo==

$10\equiv4(\mod8)$?

$$
\begin{split}
10 \not\equiv 4(\mod8) &\iff 8|10-4\\
&\iff 8|6 \\
&\iff 6 \not= 8\cdot c \land c \in \Z \\ \\
\therefore 10\not&\equiv4(\mod8)
\end{split}
$$

## Teorema

#Teorema $a,b \in \Z \land m \in\Z^+ \implies (a\equiv b(\mod m) \iff a \mod m = b \mod m)$

==Demostración==

$(p \iff q)\iff (p\implies q) \land (q\implies p)$

1. $a \equiv b(\mod m) \implies a\mod m = b\mod m$
Supongamos que $a\equiv b(\mod m)$; es decir $m|a-b$
Luego, existe un entero $c$ tal que $a-b=m\cdot c$
Así, $a=m\cdot c + b$ y $b=-m\cdot c + a$

2. $a \mod m = b \mod m \implies a\equiv b(\mod m)$ 


==Ejemplo==

$8\equiv2(\mod3)$

$8\mod3=\boxed2$ porque $8=3\cdot2+\boxed2$
$2\mod3=\boxed2$ porque $2=3\cdot0+\boxed2$

En efecto $8\mod3=2\mod3$