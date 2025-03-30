# Divisibilidad

Sea $a,b \in \Z\; a,b \not= 0$ decimos que $a$ divide a $b$ si existe un numero entero $c$ tal que $b=a \cdot c$ y se representa por $a/b$.

También se dice que:

- $b$ es divisible po $a$
- $b$ es múltiplo de $a$
- $a$ es un factor de $b$
- $a$ es divisor de $b$

==Ejemplo==
Determine si es Verdadero o Falso y justifique:
- $3$ divide a $15$ ? Verdadero porque existe $5\in \mathbb{Z}$ tal que $15 = 3 \cdot 5$

## [[cursos/s1/matematicas_discretas/ejercicios/02-divisibilidad.ej|Ejercicios 1]]

## Enteros divisibilidad y multiplicidad

1. Escriba todos los divisores de 100:
$$
\{1,2,3,4,5,10,20,25,50,100\}
$$
2. Escriba los 10 primeros múltiplos de 4:
$$
\{0,4,8,12,16,20,24,28,32,36\}
$$
3. Determine si $6|120$ , $120|6$ , $3|12$ , $12|3$
$$
\begin{split}
&V: 6|120 &&\implies 120=6\cdot20 \\
&F: 120|6 &&\implies 6=120\cdot c \land c \not\in \Z \\
&V: 3|12 &&\implies 12=3\cdot4 \\
&F: 12|3 &&\implies 3=12\cdot c \land c \not\in \Z
\end{split}
$$

Obs:
- Un divisor de un entero $n$ siempre es menor o igual que $n$ . Además $1$ es divisor de cualquier entero $n$ pues $n=n\cdot1$
$$
100=1\cdot100 \lor 100=2\cdot50 \lor 100=4\cdot25 \lor 100=5\cdot20 \lor 100=10\cdot10
$$

- Un múltiplo de un entero $n$ siempre es mayor o igual que $n$ y son de la forma $n,2n,3n,\dotsc$ o también $\dotsc,-3n,-2n,-n$
  ![[_files/02-divisibilidad_20250314.png]]
  Observe que hay una cantidad infinita de múltiplos de un numero. Además $0$ es múltiplo de cualquier entero distinto de $0$: Si $n\in \Z \implies 0=0\cdot n$ 

## Teorema 

>Es una afirmación verdadera que debe ser probada por medio de una demostración matemática

#Teorema Sean $a,b,c\in \Z$ se cumple que:
1. $a|b$ y $a|c \implies a|(b+c)$
2. $a|b \implies a|bc$
3. $a|b \land b|c \implies a|c$

==Demostración==

### $a|b$ y $a|c \implies a|(b+c)$

H: $a|b$ y $a|c$
T: $a|(b+c)$ (Existe $n \in \Z$ tal que $b+c = a \cdot n$)

Supongamos que $a|b$ y $a|c$. Es decir, existe $k \in \Z$ tal que $\boxed{b=a \cdot k}$ y también existe $m \in \Z$ tal que $\boxed{c=a \cdot m}$

Sumando estas igualdades termino a termino obtenemos

$$
\begin{gather}
b+c &= ak + am \\
  &= a (k+m)
\end{gather}
$$

Como $k \in \Z$ y $m \in \Z$ entonces $k+m \in \Z$. Sea $\boxed{n=k+m}$. Luego:

$$
b+c = a \cdot n \quad \text{donde} \quad n \in \Z
$$

Por lo tanto, $a|(b+c)$

### $a|b \implies a|bc$

H: $a|b$
T: $a|bc$ para cualquier entero $c$ (Existe un numero $n \in \Z$ tal que $bc=an$)

Supongamos que $a|b$. Es decir, existe $k \in \Z$ tal que $b=ak$ Si lo multiplicamos por $c$ tememos

$$
\begin{split}
b \cdot c &= ak \cdot c\\
bc &= a (kc) \quad \text{por prop. asociativa}
\end{split}
$$

Como $k \in \Z$ y $c \in \Z$ entonces $kc \in \Z$ entonces llamamos $n = kc$. Luego $bc = an$ con $n \in \Z$ Es decir $a|bc$ para cualquier entero $c$

### $a|b \land b|c \implies a|c$

H: $a|b$ y $b|c$
T: $a|c$ (Existe un numero $n \in \Z$ tal que $c = an$)

Supongamos que $a|b$ y $b|c$. Es decir, existe $x \in \Z$ tal que $\boxed{b = ax}$ y también existe $y \in \Z$ tal que $\boxed{c = by}$

Ahora si sustituimos $b$ en $c=by$ tenemos que $c= (ax)y$ que por prop. asociativa podemos expresar como $c=a(xy)$

Como $x \in \Z$ y $y \in \Z$ entonces $x \cdot y \in \Z$ esto lo podemos llamar $n = xy$

Luego $c = an$ con $n \in \Z$ es decir $a|c$

## [[cursos/s1/matematicas_discretas/ejercicios/02-divisibilidad.ej-1|Ejercicios 2]]

## Corolario

> Es una afirmación que es consecuencia de un teorema

#Corolario $\forall a,b,c \in \Z \land a|b \land a|c \implies a|(bm+cn) \land m\in\Z \land n\in\Z$

Dem:

Supongamos que $a|b \land a|c$ 
Por la parte 2 del teorema anterior tenemos que $a|bm$ para cualquier entero $m$
Por la parte 2 del teorema anterior tenemos que $a|cn$ para cualquier entero $n$
Luego como $a|bm \land a|cn$ por la parte 1 del teorema anterior se obtiene $a|(bm + cn)$