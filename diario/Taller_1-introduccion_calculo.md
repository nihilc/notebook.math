# Taller

![[_files/Taller_1-introduccion_calculo_20250410.pdf]]

# Desarrollo

## 1. Expresar los siguiente números racionales de las formas: como cociente de dos números enteros primos relativos, como expresión decimal, o como porcentaje.

### a. $3.1415$

- Fracción: $\frac{6283}{2000}$
$$
3.1415 \cdot {10000\over10000}= {31415\over10000} = {6283\over2000}
$$
- Porcentaje: $314.15\%$
$$3.1415 \cdot 100 = 314.15\%$$
- Decimal: $3.1415$

### b. $0.00\overline{5}$
$$
\begin{split}
n &= 0.00\overline5 \\
100n &= 0.\overline5 \\
1000n - 100n &= 5.\overline5-0.\overline5 \\
900n &= 5 \\
n &= \frac{5}{900} = \frac{1}{180}
\end{split}
$$

### c. $2.75$
$$
2.75 \cdot \frac{100}{100}= \frac{275}{100} = \frac{55}{20} = \frac{11}{4}
$$

### d. $4.\overline{150}$
$$
\begin{split}
n &= 4.\overline{150} \\
1000n - n &= 4150.\overline{150} - 4.\overline{150} \\
999n &= 4146 \\
n &= \frac{4146}{999} = \frac{1382}{333}
\end{split}
$$

### e. $225\%$
$$
255\% = \frac{255}{100} = \frac{51}{20} = 2.55
$$

### f. $1.23\overline{45}$
$$
\begin{split}
n &= 1.23\overline{45} \\
10000n - 100n &= 12345.\overline{45} - 123.\overline{45} \\
9900n &= 12222 \\
n &= \frac{12222}{9900} = \frac{6111}{4950} = \frac{2037}{1650} = \frac{679}{550}
\end{split}
$$

### g. $7.123\overline{21}$
$$
\begin{split}
n &= 7.123\overline{21} \\
100000n - 1000n &= 712321.\overline{21} - 7123.\overline{21} \\
999000n &= 705198 \\
n &= \frac{705198}{999000} = \frac{352599}{499500} = \frac{117533}{166500}
\end{split}
$$

## 2. Demostrar que $\sqrt3$ y $\sqrt5$ son números irracionales

### Para $\sqrt3\in\I$

Supongamos que $\sqrt3$ es racional, entonces $\exists p,q \in \Z \land \mcd(p,q)=1$ de modo que $\sqrt3=\frac{p}{q}$ Ahora:
$$
\begin{split}
\sqrt3 &= \frac{p}{q} \\
3 &= \frac{p^2}{q^2} \\
3q^2 &=p^2
\end{split}
$$

Esto implica que $3|p^2$ por lo tanto $3|p$
Ahora sea $p=3k$ con $k\in\Z$ . Sustituyendo:
$$
\begin{split}
3q^2 &= (3k)^2 \\
3q^2 &= 9k^2 \\
q^2 &= 3k^2
\end{split}
$$

Esto implica que $3|q^2$ por lo tanto $3|q$
Pero si $p$ y $q$ son divisibles de $3$ esto contradice que $\mcd(p,q)=1$
$\therefore \sqrt{3}$ no puede expresarse como fracción, $\sqrt3$ es irracional

### Para $\sqrt5\in\I$

Supongamos que $\sqrt5$ es racional, entonces $\exists p,q \in\Z \land \mcd(p,q)=1$ de modo que $\sqrt5=\frac{p}{q}$ . Ahora:
$$
\begin{split}
\sqrt5 &= \frac{p}{q} \\
5 &= \frac{p^2}{q^2} \\
5q^2 &= p^2
\end{split}
$$

Esto implica que $5|p^2$ por lo tanto $5|p$ (Por lema de Euclides)
Ahora sea $p=5k$ con $k\in\Z$ . Sustituyendo:
$$
\begin{split}
5q^2 &= (5k)^2 \\
5q^2 &= 25k^2 \\
q^2 &= 5k^2
\end{split}
$$

Esto implica que $5|q^2$ por lo tanto $5|q$
Pero si $5|p \land 5|q$ contradice que $\mcd(p,q)=1$
$\therefore \sqrt5$ no puede expresarse como fracción, $\sqrt5$ es irracional

## 3. Si $\forall a,b,c,d \in \R$ demostrar:

### a. $1^{-1}=1$
$$
\begin{split}
1^{-1} &= \frac{1}{1}\quad &&\text{Definicion}\; a^{-1}=\frac{1}{a} \\
&= 1
\end{split}
$$

### b. $-(a-b-c)=-a-b-c$
$$
\begin{split}
-(a-b-c) &= -1(a-b-c) \\
&= (-1)(a) + (-1)(-b) + (-1)(-c)
  &\quad &A_3 \\
&= -(1a) + 1b + 1c
  &&\text{Teorema}\; (-a)(-b)=ab \\
  &&&\text{Teorema}\; (-a)b = -(ab) \\
&= -a + b + c
 &&A_4
\end{split}
$$
Pero $-a+b+c \not= -a-b-c$
$\therefore -(a-b-c)\not=-a-b-c$

> Comprobar porque como no especifica que las variables no pueden ser $0$ puede darse que $-(a-b-c)=-a-b-c$
### c. $-ax=-a \land a\not=0 \implies x=1$
$$
\begin{split}
-ax &= -a \cdot 1
  &\quad\quad &A_4 \\
-(ax) &= -(a\cdot1)
  &&\text{Teorema}\; (-a)b = -(ab) \\
-(xa) &= -(1\cdot a)
  &&A_1 \\
(-x)a &= (-1)a
  &&\text{Teorema}\; (-a)b = -(ab) \\
(-x)a\cdot a^{-1} &= (-1)a \cdot a^{-1} \\
(-x) &= (-1)
  &&A_6 \\
(-x)(-1) &= (-1)(-1) \\
x\cdot1 &= 1 \cdot 1
  &&\text{Teorema}\; (-a)(-b)=ab \\
x &= 1
  &&A_4
\end{split}
$$

### d. $\frac{-a}{b}-\frac{c}{d}= \frac{-(ad+bc)}{bd}$
$$
\begin{split}
\frac{-a}{b}-\frac{c}{d} &= \left[\frac{-a}{b}-\frac{c}{d}\right] \cdot 1 
  &\quad\quad &A_4 \\
&= \left[\frac{-a}{b}-\frac{c}{d}\right]\cdot [(bd) \cdot (bd)^{-1}]
  & &A_6 \\
&= \left[ \left( \frac{-a}{b}-\frac{c}{d} \right) \cdot (bd) \right] \cdot (bd)^{-1}
  & &A_2 \\
&= \left[ \left(\frac{-a}{b}\right)\cdot(bd) - \left( \frac{c}{d}\right)\cdot (bd)  \right] \cdot (bd)^{-1}
  & &\text{Teorema}\; (a+b)c=ac+bc \\
&= [(-ab^{-1})(bd) - (cd^{-1})(bd)] \cdot (bd)^{-1}
  & &\text{Teorema}\; \frac{a}{b}=ab^{-1} \\
&= (-adb^{-1}b -cbd^{-1}d) \cdot (bd)^{-1}
  & &A_2,A_1 \\
&= (-ad -cb) \cdot (bd)^{-1}
  & &A_6 \\
&= \frac{-ad-cb}{bd}
  & &\text{Teorema}\; \frac{a}{b}=ab^{-1} \\
&= \frac{-1(ad+cb)}{bd}
  & &A_3? \\
&= \frac{-(ad+cb)}{bd}
\end{split}
$$

### e. $a^2=aa \implies a^2-b^2=(a+b)(a-b)$

$$
\begin{split}
(a+b)(a-b) &= a(a-b) + b(a-b) 
  &\quad &\text{Teorema}\; (a+b)c=ac+bc \\
&= aa -ab +ba -bb
  &&A_3 \\
&= aa - bb + (ab - ab) 
  &&A_1,A_2 \\
&= aa - bb
  &&A_5 \\
&= a^2 - b^2
  &&\text{Definicion}
\end{split}
$$

### f. $a^n-b^n=(a-b)( a^{n-1} + a^{n-2}b + a^{n-3}b^2 + \dots + a^2b^{n-3} + ab^{n-2} + b^{n-1} )$
$$
\begin{split}
a^n-b^n &= (a-b)(a^{n-1}+a^{n-2}b+a^{n-3}b^2+\dots+a^2b^{n-3}+ab^{n-2}+b^{n-1}) \\
&=
  a(a^{n-1}+a^{n-2}b+a^{n-3}b^2+\dots+a^2b^{n-3}+ab^{n-2}+b^{})
  -b(a^{n-1}+a^{n-2}b+a^{n-3}b^2+\dots+a^2b^{n-3}+ab^{n-2}+b^{})\\
&=
  a^n + a^{n-1}b + a^{n-2}b^2 + \dots + a^3b^{n-3} + a^2b^{n-2} + ab^{n-1}
  -a^{n-1}b - a^{n-2}b^2 - a^{n-3}b^3 - \dots - a^2b^{n-2} - ab^{n-1} - b^n \\
&= 
  a^n-b^n +
  (a^{n-1}b-a^{n-1}b) + 
  (a^{n-2}b^2-a^{n-2}b^2) + 
  (a^{n-3}b^3-a^{n-3}b^3) + 
  \dots + 
  (a^3b^{n-3}-a^3b^{n-3}) + 
  (a^2b^{n-2}-a^2b^{n-2}) + 
  (ab^{n-1}-ab^{n-1}) \\
&= a^n-b^n + 0 + 0 + 0 + \dots + 0 + 0 + 0 \\
&= a^n-b^n
\end{split}
$$

### g. $0$ del axioma $4$ es único.

## 4. $\forall a,b,c,d \in \R$ demostrar:

### a. $a>0 \iff a \in \P$

$a>0 \implies a\in\P$

Por definición de orden $a>0$ equivale a $a-0\in\P$ ahora por $A_4$ $a\in\P$ 

$a\in\P \implies a>0$

==Duda==

### b. $a>0 \implies -a\in\P$

Por definición de orden $a>0 \implies a\in\P$, ahora por tricotomía $a\in\P \veebar a=0 \veebar -a\in\P$
$\therefore \text{Es falso que si}\; a>0 \implies -a\in\P$

### c. $0<a<b \land 0<c<d \implies ac<bd$

Por hipótesis $b-a\in\P \land b\in\P$ también $d-c\in\P \land c\in\P$. Ahora
$$
\begin{split}
c(b-a) + b(d-c) &\in\P &\quad &A_7 \\
cb-ca +bd-bc &\in\P &&A_3 \\
bd-ac+bc-bc &\in\P &&A_1 \\
bd-ac &\in\P &&A_5,A_4 \\
\therefore ac<bd &&&\text{Def. orden}
\end{split}
$$

### d. $a>0 \land b<0 \implies ab < 0$

Por hipótesis $a\in\P \land -b\in\P$ ahora
$$
\begin{split}
a(-b) &\in \P &\quad &A_7\\
-(ab) &\in \P &&\text{Teorema}\; (-a)b=-(ab) \\
\end{split}
$$
Como sabemos que $ab\not=0$ ya que $a\not=0\land b\not=0$, entonces $-(ab)\in\P \implies ab\not\in\P$ por tricotomía
$\therefore ab<0$

### e. $a<0 \land b>0 \implies ab<0$

Por hipótesis $-a\in\P\land b\in\P$ ahora
$$
\begin{split}
(-a)b &\in\P &\quad &A_7 \\
-(ab) &\in\P &&\text{Teorema}\; (-a)b=ab \\
\end{split}
$$
Como $ab\not=0$ ya que $a\not=0\land b\not=0$ entonces por $-(ab)\in\P\implies ab\not\in\P$ por tricotomía
$\therefore ab< 0$

### f. $a-b=b-a \implies a=b$

$$
\begin{split}
a-b &= b-a \\
a-b + (a+b) &= b-a + (a+b) &\quad&A_0 \\
a+a +b-b &= b+b+a-a &&A_1 \\
a+a &= b+b &&A_5,A_4 \\
2^{-1}\cdot2a &= 2^{-1}\cdot2b &&A_0\\
1a &= 1b &&A_6 \\
a &= b &&A_4
\end{split}
$$

## 5. $\forall a,b\in\R$ demostrar:

### a. $|ab|=|a||b|$

### b. $|a-b|\geq |a| - |b|$

### c. $-|a| \leq a \leq |a|$

## 6. Resolver la siguientes inecuaciones, justifique con axioma, definición o teorema cada paso:

### a. $$2x^2-7x-15\geq 0$$

### c.  $$3(2x+1)-(3-4x)+6 \leq 5x + (5-2x) - 6$$

### d. $$\frac{5x+3}{4}-\frac{4x-7}{5} \geq 3\left( \frac{2x}{3} - \frac{2}{5} \right)$$

### e.  $$(2x-3)(x+5)(3x-2) \leq 0$$

### f.   $$ \frac{5x+8}{3x^2-5x-2} \geq 0$$

### h. $$\frac{x^2+1}{9x-5} > 0$$

### i. $$\frac{x^3-1}{(x^2+x+1)(x^2-1)} < 0$$

### j. $$\frac{5x+8}{3x^2-5x-2}$$

### k. $$\frac{3 - \frac{7x}{3}}{8-x} \leq -\frac{3}{4}(x-7)$$

### l. $$\frac{(2x-5)(4-x)}{2-3x} > 0$$

### m. $$\left|\frac{1}{2}x-\frac{3}{4}\right| < \frac{4}{3}$$

### n. $$\left|\frac{3x-2}{x+5}-\frac{3}{4}\right| < \frac{4}{3}$$

### o. $$\left|\frac{3x-1}{2-4x}\right| \geq 4$$

### p. $$|5x-7| + |2x+9| < 7$$

### q. $$|3x+5| + |2x+8| \leq \frac{2}{5}$$

### r. $$|12-3x| - |9+11x| \geq 8$$

### s. $$|2x-7| < |5x+9|$$

### t. $$\left|\frac{5x-3}{8-9x}\right| \geq 10$$