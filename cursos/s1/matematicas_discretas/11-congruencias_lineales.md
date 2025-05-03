# Congruencias Lineales

Una congruencia de la forma $ax \equiv b(\mod m)$ donde $a,b\in\Z$ y $m\in\Z^+$ y $x$ es una variable se llama una congruencia lineal

Ejemplo: $2x \equiv 5(\mod 3)$

$$
3 | 2x-5 \iff 2x-5=3k \quad k\in\Z
$$

La idea es encontrar todos los valores de $x$ que satisfaga esta igualdad.

Vamos a ver un metodo para realizar esto:

## Teorema

#Teorema Sean $a$ y $m$ primos relativos y $m>1$ entonces existe el inverso de $a\mod m$, denotado por $\bar a$, el cual es único modulo $m$

==Demostración==

Como $\mcd(a,m)=1$ pues $a$ y $m$ son primos relativos por hipótesis entonces por un teorema anterior (existen entonces $s$ y $t$ tales que: $sa + tm = 1$)

Así también podemos decir que $sa + tm \equiv 1 (\mod m)$

Fijémonos que $tm \equiv 0 (\mod m)$ entonces necesariamente $sa \equiv 1 (\mod m)$ Es decir $s$ es el inverso de $a \mod m$

==Ejemplo==

Halle el inverso de $5 \mod 8$

En este caso $a=5 \land m=8 \implies \mcd(a,m)=1$

Aplicamos el algoritmo de Euclides:

![[_files/11-congruencias_lineales_20250502.png]]

$$
\begin{split}
&8 = 5 \cdot 1 + 3 &\implies 3 = 8-5\\
&5 = 3 \cdot 1 + 2 &\implies 2 = 5-3\\
&3 = 2 \cdot 1 + \boxed1 &\implies 1 = 3-2\\
&2 = 1 \cdot 2 + 0 \\
\\
&1 = 3-2 \\
&1 = (8-5) - (5-3) \\
&1 = (8-5) - (5-(8-5)) \\
&1 = (8-5) - (5-8+5)) \\
&1 = 8-5-5+8-5 \\
&1 = 8+8-5-5-5 \\
&1 = 8\cdot2-5\cdot3 \\
&1 = (8\cdot2)+(5\cdot(-3)) \\
\end{split}
$$

Como $8\cdot2 \equiv 0 (\mod 8) \implies 5\cdot-3 \equiv 1 (\mod 8)$
Es decir $-3$ es el inverso de $5\mod8$
Tambien $5$ es inverso de $5\mod8$

==Ejercicio==

Calcular $s$ y $t$ tales que $sa+tm=1$ donde $a=4$ y $m=9$

Hallar el inverso de $4\mod9$

Aplicando algoritmo Euclides:
$$
\begin{split}
9 &= 4\cdot 2 + \boxed1 &\implies 1 = 9-4\cdot2\\
4 &= 1 \cdot4 + 0 \\
\\
1 &= 9 - 4\cdot2 \\
 &= 9\cdot 1 - 4\cdot2 \\
 &= 9\cdot 1 + 4\cdot-2 \\
\\
&\therefore s=-2 \land t=1 
\end{split}
$$

Ahora $9\cdot 1 \equiv 0 (\mod 9) \implies 4\cdot-2 \equiv 1 (\mod 9)$
Es decir $-2$ es el inverso de $4\mod9$
Es decir $4$ es el inverso de $4\mod9$

## Como resolver una congruencia $ax\equiv b(\mod m)$ usando el inverso de $a$?

==Ejemplo==

Resolver $5x=2(\mod 8)$

Sabemos que el inverso de $5\mod8$$ es $5$. Multiplicados a ambos lados de la congruencia por $5$:
$$ 5\cdot 5x \equiv 5\cdot2 (\mod 8) $$
Como $5\cdot5 \equiv 1(\mod8)$ y $5\cdot2 \equiv 2(\mod8)$ entonces se cumple que:
$$ 1\cdot x \equiv 2 (\mod 8) $$
Es decir $X=2(\mod 8)$ son las soluciones buscadas; es decir $8|(x-2)$ o $x=2+8k$ para cualquier entero $k$

==Ejercicio==

Resolver $4x\equiv 5(\mod 9)$

## Como resolver un sistema de congruencias lineales?


$$
\begin{cases}
x\equiv 2(\mod 5) \\
x\equiv 3(\mod 9) \\
x\equiv 0(\mod 4) \\
\end{cases}
$$

Se trata de resolver, es decir, hallar los valores de $x$ que satisfagan un sistema de congruencias como este. Para esto, usaremos el Teorema chino del resto

### Teorema Chino del resto

#Teorema Sean $m_1,m_2,\dots,m_n$ enteros positivos primos relativos dos a dos. El sistema de congruencias

$$
\begin{split}
x &= a_1(\mod m_1) \\
x &= a_2(\mod m_2) \\
x &= a_3(\mod m_3) \\
&\;\;\vdots \\
x_n &= a_n(\mod m_n)
\end{split}
$$

Tiene solucion unica $m=m_1 m_2 m_3 \dots m_n$; es decir, existe un $0<x<m-1$ que es solucion y todas las demas son soluciones son congruentes modulo $m$