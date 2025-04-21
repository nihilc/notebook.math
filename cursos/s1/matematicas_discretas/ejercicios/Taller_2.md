# Taller

Desarrollar puntos 1,13,20,26,36,42,48,55,60 de la sección 2.4 del Libro de Rosen

# Desarrollo

## 1. Divide 17 a los siguientes números?

1. $68$ Si, porque $\exists4\in\Z$ tal que $68=17\cdot4$
2. $84$ No, porque $\not\exists c\in\Z$ tal que $84=17\cdot c$
3. $357$ Si, porque $\exists21\in\Z$ tal que $357=17\cdot21$
4. $1001$ No, porque $\not\exists c\in\Z$ tal que $1001=17\cdot c$

## 13. Obtenga la descomposición en primos de $10!$

$$
\begin{split}
10! 
&= 1\cdot2\cdot3\cdot4\cdot5\cdot6\cdot7\cdot8\cdot9\cdot10 \\
&= 1\cdot2\cdot3\cdot(2\cdot2)\cdot5\cdot(2\cdot3)\cdot7\cdot(2\cdot2\cdot2)\cdot(3\cdot3)\cdot(2\cdot5) \\
&= \boxed{2^8\cdot3^4\cdot5^2\cdot7} \\
&= 3628800
\end{split}
$$

## 20. Decimos que un entero positivo es perfecto si es igual a la suma de sus divisores positivos que no son el mismo.

1. Comprobar que 6 y 28 son perfectos

$$
\begin{split}
n|28 &\implies n=\{1,2,4,7,17,28\} \\
&\implies 1+2+4+7+14=28 \\
&\therefore 28 \;\text{es perfecto} \\
\\
n|6 &\implies n=\{1,2,3,6\} \\
&\implies 1+2+3=6 \\
&\therefore 6 \;\text{es perfecto}
\end{split}
$$

2. Demuestra que $2^{p-1}(2^p-1)$ es un numero perfecto cuando $2^p-1$ es primo

$2^p-1\;\text{es primo} \implies 2^{p-1}(2^p-1)\;\text{es perfecto}$

Supongamos que $2^p-1$ es primo
Ahora llamemos $n=2^{p-1}(2^p-1)$
Como $2^p-1$ es primo los divisores de $n$ son de la forma $2^k$ y $2^k(2^p-1)$ con $0 \leq k \leq p-1$ 
Ósea los divisores de $n$ serian $2^0,2^1,2^2,\dots,2^{p-1}$ y $2^0(2^p-1), 2^1(2^p-1),2^2(2^p-1),\dots,2^{p-2}(2^p-1),2^{p-1}(2^p-1)$ .

Sumando los divisores de la forma $2^k$
$$
1+2+2^2+\dots+2^{p-1} = \sum_{k=0}^{p-1} 2^k
$$

Nos damos cuenta que es una suma geométrica entonces podemos usar
$$
\sum_{k=0}^{m} r^k = 1 + r + r^2 + \dots+r^m = \frac{r^{m+1}-1}{r-1}
$$

Aplicando:
$$
\sum_{k=0}^{p-1} 2^k = \frac{2^{(p-1)+1}-1}{2-1} = 2^p-1
$$

Sumando también los divisores de la forma $2^k(2^p-1)$ sin incluir al propio $n$
$$
\begin{split}
&(2^P-1)+2(2^p-1)+2^2(2p-1)+\dots+2^{p-2}(2^p-1) \\ 
= &(2^p-1)(1+2+2^2+\dots+2^{p-2}) \\
= &(2^p-1)\sum_{k=0}^{p-2}2^k \\ 
\end{split}
$$

Resolvemos la suma geométrica
$$
\sum_{k=0}^{p-2} 2^k = \frac{2^{(p-2)+1}-1}{2-1} = 2^{p-1}-1
$$

Remplazando
$$
(2^p-1)\sum_{k=0}^{p-2}2^k = (2^p-1)(2^{p-1}-1)
$$

Ahora sumamos ambas sumas
$$
\begin{split}
&(2^p-1) + (2^p-1)(2^{p-1}-1) \\
= &(2^p-1)[1+(2^{p-1}-1)] \\
= &(2^p-1)(2^{p-1}) \\
= &2^{p-1}(2^p-1)
\end{split}
$$

Lo cual es igual a $n$
$\therefore n \;\text{es un numero perfecto}$

## 26. Demuestra que $n$ es primo si y solo si $\phi(n)=n-1$

$n\;\text{es primo}\implies \phi(n)=n-1$

Supongamos que $n$ es un numero primo. Por definición un primo tiene únicamente dos divisores positivos $1$ y $n$ mismo.
La función $\phi(n)$ de Euler cuenta la cantidad de enteros positivos menores o iguales a $n$ que son primos relativos con $n$ 
Consideremos los enteros positivos $1,2,3,\dots,n-1,n$
Dado que $n$ es primo su único divisor positivo mayor que $1$ es $n$ mismo.
Por lo tanto cualquier entero positivo $k$ tal que $0< k < n$ no puede tener ningún factor primo en común con $n$ Esto implica que $\mcd(k,n)=1$ para todo $k$ en el rango $0<k<n$
Los enteros positivos menores o iguales a $n$ que son primos relativos con $n$ son, por lo tanto $1,2,3,\dots,n-1$. Hay exactamente $n-1$ de estos enteros.
$\therefore$ si $n$ es primo, entonces $\phi(n)=n-1$

$\phi(n)=n-1 \implies n\;\text{es primo}$

Supongamos que $\phi(n)=n-1$, esto significa que todos los numeros desde $1$ hasta $n-1$ son coprinos con $n$
Si $n$ no fuera primo, existiría un divisor $d$ de $n$ tal que $1<d<n$.
Pero entonces $d$ y $n$ compartirían un divisor común mayor que $1$ (El propio $d$), por lo que $\mcd(d,n)=d$ y $d\not=1$
Esto implicaría que $\phi(n)<n-1$ pues al menos $d$ no es coprino con $n$, contradiciendo la hipótesis
$\therefore$ La unica posibilidad es que $n$ no tenga divisores propios, es decir, que $n$ sea primo, ya que para un primo $p$ todos los números $1,2,3,\dots,p-1$ son coprinos con $p$

## 36. Evalúa estas expresiones

1. $-17\mod2=1$
2. $-101\mod13=3$
3. $144\mod7=4$
4. $199\mod19=9$

## 42. Demuestre que si $a\equiv b(\mod m)$ y $c \equiv d(\mod m)$ donde $a,b,c,d,m \in \Z$ y $m\geq2$ entonces $a-c\equiv (b-d)(\mod m)$

$a,b,c,d,m \in\Z \land a \equiv b(\mod m) \land c\equiv d(\mod m) \land  m\geq 2 \implies a-c\equiv(b-d)(\mod m)$

Supongamos que $a\equiv b(\mod m)$ por definición $m|a-b$ ósea $a-b=m\cdot k$ con $k\in\Z$
Tambien $c\equiv d(\mod m)$ por definición $m|c-d$ ósea $c-d=m\cdot q$ con $q\in\Z$
Ahora $a=b+mk$ y $c=d+mq$ Luego restamos estas igualdades termino a termino
$$
\begin{split}
a-c &= (b+mk)-(d+mq) \\
	&= b-d+mk+mq \\
	&= (b-d) + m(k+q)
\end{split}
$$

Como $k\in\Z$ y $q\in\Z$ entonces $k+q\in\Z$ llamemos $n=k+q$ por lo tanto
$$
\begin{split}
a-c &= (b-d) + mn \\
(a-c)-(b-d) &= mn
\end{split}
$$

Por lo tanto $m|(a-c)-(b-d)$
$\therefore a-c\equiv(b-d)(\mod m)$

## 48. Que posiciones de memoria asigna la función de dispersion $h(k)=k\mod101$ a las fichas de los estudiantes con los numero de documento nacional de identidad siguientes?

1. $104578690\mod101=58$
2. $432222187\mod101=60$
3. $37201919\mod101=84$
4. $501338753\mod101=3$

## 55. Los primeros nueve dígitos del ISBN de la tercera edición de este libro son 0-07-053965. Cual es el digito de control para este libro?

El código de control de un ISBN es el decimo digito de este, en caso de $\text{0-07-053965}\boxed k$
Para encontrarlo podemos usar
$$
k = 11-\left[\sum_{i=1}^{10}x_i(11-i)\right]\mod 11
$$

donde $x$ es cada cifra del código ISBN sin contar el digito de control.
Entonces tenemos
$$
\begin{split}
k &= 11 - (0\cdot10 + 0\cdot9 + 7\cdot8 + 0\cdot7 + 5\cdot6 + 3\cdot5 + 9\cdot4 + 6\cdot3 + 5\cdot2 + k\cdot1) \mod 11 \\
&= 11 - (0 + 0 + 56 + 0 + 30 + 15 + 36 + 18 + 10) \mod 11 \\
&= 11 - 165 \mod 11 \\
&= 11 - 0 \\
&= 11
\end{split}
$$

En este caso como nos da $11$

- Si $k=11$ remplazamos por $0$
- Si $k=10$ remplazamos por $X$
- En cualquier otro caso ese es el digito de control

$\therefore \text{El digito de control es 0} \implies \text{El ISBN completo seria 0-07-0539650}$

## 60. Puedes encontrar una formula o regla para el termino enésimo de una sucesión relacionada con números primos o con la descomposición en factores primos de tal forma que los primos términos de estas sucesiones sean los siguientes?

1. $2,2,3,5,5,7,7,11,11,11,11,13,13,\dots$
   $a_n$ es igual a la repetición de un numero de primo la cantidad de números que hay entre el y su número primo antecesor
   > No dependiente de orden, el orden es el listado de primos

2. $0,1,2,2,3,3,4,4,4,4,5,5,6,6,\dots$
   $a_n$ es igual a la cantidad de números primos menores o iguales a $n$
   
3. $1,0,0,1,0,1,0,1,1,1,0,1,0,1,\dots$
$$
a_n \begin{cases}
  1 \;\text{Si no es primo} \\
  0 \;\text{Si es primo}
\end{cases}
$$
   
4. $1,-1,-1,0,-1,1,-1,0,0,1,-1,0,-1,1,1,\dots$
$$
a_n \begin{cases}
  -1 &\text{Si es primo} \\
  1 &\text{Si en su descomposicion tiene 5 o 7} \\
  0 &\text{Si en su descomposicion tiene 3, 4 o 6}
\end{cases}
$$
> En caso de que se cumplan $a_n=1$ y $a_n=0$ tiene prioridad $a_n=1$
   
5. $1,1,1,1,1,0,1,1,1,0,1,0,1,0,0,\dots$
$$
a_n \begin{cases}
  0 &\text{Si en su lista de divisores tiene un par y un impar} \\
  1 &\text{En cualquier otro caso}
\end{cases}
$$
   
6. $4,9,25,49,121,179,289,361,529,841,961,1369,\dots$
   $a_n$ es igual a la lista de primos elevados al cuadrado
   > No dependiente de orden, el orden es el listado de primos

# Entregas/Correcciones

## Entrega

![[_files/Taller_2_20250420.pdf]]

## Corrección

![[_files/Taller_2_20250420-1.pdf]]