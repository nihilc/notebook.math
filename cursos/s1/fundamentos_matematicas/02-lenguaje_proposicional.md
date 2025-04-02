# Lenguaje Proposicional

Una proposición es una afirmación a la cual se puede decir que es **Verdadera** o **Falsa**

## Syntaxis

### Proposiciones Atómicas

Son las mas sencillas que se puede construir y carecen de [[cursos/s1/fundamentos_matematicas/01-lenguaje_matematico#Conectivos|Conectivos]] lógicos

Notación: $p,q,r,...$

Ejemplos:

- $p$ : "El cielo es azul" ✔️ Atómica
- $q$ : "Hoy es lunes" ✔️Atómica
- "Hoy no hay clase"
	- $r$ : "Hoy hay clase" ✔️Atómica
	- $\lnot r$: "Hoy no hay clase" ✖️ No Atómica

### Proposiciones Moleculares

Son obtenidas a partir de [[#Proposiciones Atómicas]] usando [[cursos/s1/fundamentos_matematicas/01-lenguaje_matematico#Conectivos|Conectivos]] lógicos

Ejemplos:

$$
\begin{gather}
\text{Si hoy es lunes va a llover} \\
p: \text{Hoy es lunes} \quad q: \text{Hoy va a llover} \\
p \implies q \\
\\
\text{Como empanada y me voy a pie} \\
p: \text{Como empanada} \quad q: \text{Me voy a pie} \\
p \land q \\
\\
\end{gather}
$$

 > En este ejemplo dependiendo de donde se encuentre la "," puede cambiar a el como se usan los símbolos de [[cursos/s1/fundamentos_matematicas/01-lenguaje_matematico#Agrupación|agrupacion]] o si no tuviera una coma seria ambiguo

$$
\begin{gather}
\text{"Si tengo clase de fundamentos entonces hay quiz y no estudie"} \\
	p: \text{Tengo clase de fundamentos} \quad
	q: \text{Hay quiz} \quad
	r: \text{Estudie} \\
p \implies q \land \lnot r \\
\\
\text{"Si tengo clase de fundamentos entonces hay quiz\color{red},\color{default} y no estudie"} \\
	p: \text{Tengo clase de fundamentos} \quad
	q: \text{Hay quiz} \quad
	r: \text{Estudie} \\
(p \implies q) \land \lnot r \\
\\
\text{"Si tengo clase de fundamentos entonces\color{red},\color{default} hay quiz y no estudie"} \\
	p: \text{Tengo clase de fundamentos} \quad
	q: \text{Hay quiz} \quad
	r: \text{Estudie} \\
p \implies (q \land \lnot r)
\end{gather}
$$

### Formulas Bien Formadas (FBF or WFF)

1. Las proposiciones atómicas son FBF.
2. La negación de una FBF es una FBF ($\lnot p$)
3. Si $p$ y $q$ son FBF entonces $\begin{Bmatrix} p \land q \\ p \lor q \\ p \implies q \\ p \iff q \end{Bmatrix}$ Son FBF
4. Si $x$ es una variable y $p(x)$ es una FBF entonces $(\forall{x})(p(x))$ y $(\exists{x})(p(x))$ son FBF

> Cualquier FBF debe obtenerse a partir de 1-4

## Semántica

"Sentido" valor de (V o F)

### Evaluar valor de verdad de una proposición

En lenguaje proposicional una proposición solamente puede tener dos valor $\T$ de *true/verdad* o $\F$ de *false/falso* 

==Ejemplo==

Evaluar los valores de verdad de la proposición *"Hoy es miércoles"*
Entonces si es verdad que *Hoy es miércoles* $p=\T$  mientras que si no es verdad que *Hoy es miércoles* $p=\F$
Por lo tanto los valores de verdad de $p$ podrían ser:
$$\begin{array}{|c|c|}\hline p \\ \hline \T \\ \F \\\hline\end{array}$$

==Ejemplo==

Evaluar los valores de verdad de la proposición *Hoy no tengo clase entonces no estudie*

Como es una proposición [[#Proposiciones Moleculares|molecular]] lo mas sencillo es siempre sacar las proposiciones [[#Proposiciones Atómicas|atómicas]] (tener en cuenta que siempre deben ser verdaderas) y luego organizar los [[cursos/s1/fundamentos_matematicas/01-lenguaje_matematico#Conectivos|conectivos]]

$$
\begin{gather}
p:\text{"Hoy tengo clase"} \\
q:\text{"Estudié"} \\[5pt]
\lnot p \implies \lnot q
\end{gather}
$$
Ahora obtenemos todos los valores de verdad posibles de la proposición $\lnot p \implies \lnot q$

$$
\begin{array}{|c|c|} \hline
p & q & \lnot p & \lnot q & \lnot p \implies \lnot q \\ \hline
\T & \T & \F & \F & \T \\
\T & \F & \F & \T & \T \\
\F & \T & \T & \F & \F \\
\F & \F & \T & \T & \T \\ \hline
\end{array}
$$

### Tablas De Verdad

- Siendo $p$ una [[#Proposiciones Atómicas|proposición atómica]] $p$ puede tomar un valor de $V$ o $F$
- Siendo $p$ y $q$ [[#Proposiciones Atómicas]] tenemos que

$$
\begin{array}{|c|c|c|c|c|c|c|}
	\hline
	p & q & \lnot p & p \land q & p \lor q & p \implies q & p \iff q \\
	\hline
	\T & \T & \F & \T & \T & \T & \T \\
	\T & \F & \F & \F & \T & \F & \F \\
	\F & \T & \T & \F & \T & \T & \F \\
	\F & \F & \T & \F & \F & \T & \T \\
	\hline
\end{array}
$$

## [[cursos/s1/fundamentos_matematicas/ejercicios/02-lenguaje_proposicional.ej|Ejercicios]]
