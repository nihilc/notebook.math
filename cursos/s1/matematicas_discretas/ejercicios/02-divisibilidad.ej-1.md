# Taller

#Incompleto

Realizar los problemas de 1 al 12 de la sección 2.4 del libro de Rosen (paginas 152, 153)

## 1. Divide 17 a los siguientes números:

- $68$ Si porque existe $4 \in Z$ tal que $68 = 17 \cdot 4$
- $84$ No porque no existe $c \in Z$ tal que $84 = 17c$
- $357$ Si porque existe $21 \in Z$ tal que $357= 17 \cdot 21$
- $1001$ No porque no existe $c \in Z$ tal que $1001 = 17c$

## 2. Demuestre que si $a$ es un entero no nulo

1. $1|a$
	H: $a \in Z$ y $a \not= 0$
	T: $1|a$ (Existe $n \in Z$ tal que $a = 1 \cdot n$)
	Supongamos que $a \in Z \land a \not=0$ Entonces $a = 1 \cdot n$ siendo $n \in Z$
	Sabemos que $a = 1 \cdot a$ entonces podemos decir $n = a \in Z$
	Por lo tanto $1|a$

2. $a|0$
	H: $a \in Z$ y $a \not= 0$
	T: $a|0$ (Existe $n \in Z$ tal que $0 = a \cdot n$ siendo $n \in Z$)
	Supongamos que $a \in Z \land a \not= 0$ Entonces $0 = a \cdot n$ para $n \in Z$
	Sabemos que $0 = a \cdot 0$ entonces podemos decir que $n = 0 \in Z$
	Por lo tanto $a|0$

## 3. Demostrar que la parte (2) del Teorema 1 es verdadera

[[cursos/s1/matematicas_discretas/02-divisibilidad#$a b implies a bc$|Demostracion]]

## 4. Demostrar que la parte (3) del Teorema 1 es verdadera

[[cursos/s1/matematicas_discretas/02-divisibilidad#$a b land b c implies a c$|Demostracion]]

## 5. Demostrar que si $a|b$ y $b|a$ donde $a$ y $b \in Z$ entonces $a=b$ o $a=-b$

H: $a|b \land b|a$ donde $a \land b \in Z$
T: $a=b \lor a=-b$
Supongamos que $a|b \land b|a$ donde $a \land b \in Z$, Entonces $\boxed{b = ax}$ siendo $x \in Z$ y también $\boxed{a=by}$ siendo $y \in Z$
Si remplazamos $b$ en $a = by$ tenemos que $a = axy$ simplificamos $a$ dejándonos con $1 = xy$ si y solo si $a \not= 0$
Ahora la unica forma en que $1 = xy$ con $x \land y \in Z$ es con $(x=1 \land y=1) \lor (x=-1 \land y=-1)$
Por lo tanto $\boxed{a = b(\pm1)}$ entones $a = b \lor a = -b$

## 6. Demuestra que si $a,b,c,d$ son enteros tales que $a|c$ y $b|d$, entonces $ab|cd$

H: $a,b,c,d \in Z$ tal que $a|c \land b|d$
T: $ab|cd$ (Existe $k \in Z$ tal que $cd = ab \cdot k$)
Supongamos que $a,b,c,d \in Z$ tal que $a|c \land b|d$ por lo tanto existe $\boxed{c=a\cdot n}$ con $n\in Z$ y también existe $\boxed{d = b \cdot m}$ con $m \in Z$
Si multiplicamos $c(d) = an(bm)$ luego si ordenamos la ecuación $cd = ab \cdot nm$ como sabemos que $n \in Z$ y $m \in Z$ entonces $n \cdot m \in Z$ a esto lo llamamos $k = n \cdot m$ entonces podemos decir que $cd = ab \cdot k$ con $k \in Z$ por lo tanto $ab|cd$

## 7. Demuestra que si $a,b,c$ son enteros tales que $ac|bc$ y $c\not=0$ entonces $a|b$

H: $a,b,c \in Z$ tal que $ac|bc$ y $c\not=0$
T: $a|b$ (Existe un $k \in Z$ tal que $b = a \cdot k$)
Supongamos que $bc = ac \cdot n$ con $n \in Z$ como $c\not=0$ dividimos por $c$ quedando con $b = a \cdot n$ con $n \in Z$ lo tanto $a|b$

## 8. Son primeros estos enteros?

- 19 es primo ya que no existe $n \in Z$ siendo $1<n<19$ tal que $n|19$
- 27 no es primo ya que $\exists n \in Z$ siendo $1<n<27$ tal que $n|27$
- 93 no es primo ya que $\exists n\in Z$ siendo $1<n<93$ tal que $n|93$
- 101 es primo ya que no existe $n\in Z$ siendo $1<n<101$ tal que $n|101$
- 107 es primo ya que no existe $n\in Z$ siendo $1<n<107$ tal que $n|107$
- 113 es primo ya que no existe $n\in Z$ siendo $1<n<113$ tal que $n|113$

## 9. Cual es el cociente y el resto cuando

- 19 se divide entre 7
Tenemos que $19 = 7\cdot2 + 5$
Por lo tanto el cociente es $2 = 19 \div 7$ y el resto es $5 = 19 \% 7$

- -111 se divide entre 11
Tenemos que $-111 = 11 \cdot 10 - 1$ pero como en resto debe cumplir con $0 \leq r < 11$ ajustamos la operación a $-111 = 11 \cdot -11 + 1$
Por lo tanto el cociente es $-11 = -111\div11$ y el resto es $1 = -111\%11$

- 789 se divide entre 23
Tenemos que $789 = 23 \cdot 34 + 7$
Por lo tanto el cociente es $34 = 789\div23$ y el resto es $7=789\%23$

- 1001 se divide entre 13
Tenemos que $1001 = 13 \cdot 77$
Por lo tanto el cociente es $77 = 1001\,\text{div}\,23$ y el resto es $0 = 1001\%13$

- 0 se divide entre 19
- 3 se divide entre 5
- -1 se divide entre 3
- 4 se divide entre 1
