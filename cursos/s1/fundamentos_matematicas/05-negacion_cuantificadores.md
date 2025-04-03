# Negación de cuantificadores

## Cuantificador Universal

> La negación de $\forall$ es $\exists$ seguido de la negación de la proposición

- Afirmación *"Para todo $x$ en $A$, se cumple $P(x)$"* 
  En lenguaje matemático: $(\forall x)(P(x))$
- Negación *"No es cierto que para todo $x$ en $A$, se cumple $P(x)$"* $\iff\lnot(\forall x)(P(x))$
  Esto significa que existe al menos un elemento en $A$ para el cual $P(x)$ no se cumple.
  En lenguaje matemático: $\lnot(\forall x)(P(x)) \iff (\exists x)(\lnot P(x))$

==Ejemplo==

"Para todo entero $a,b$ se cumple que $a+b=c$ siendo $c$ también es entero"
$$
\begin{split}
(\forall a)(\forall b)(a\in\Z \land b\in\Z \implies a+b\in\Z)
\end{split}
$$

"No es cierto que para todo entero $a,b$ se cumple que $a+b=c$ siendo $c$ también es entero"
$$
\begin{split}
&\lnot((\forall a)(\forall b)(a\in\Z \land b\in\Z \implies a+b\in\Z)) \\
&(\exists a)(\exists b)(\lnot(a\in\Z \land b\in\Z \implies a+b\in\Z)) \\
&(\exists a)(\exists b)(a\in\Z \land b\in\Z \land \lnot(a+b\in\Z)) \\
&(\exists a)(\exists b)(a\in\Z \land b\in\Z \land a+b\not\in\Z)) \\
\end{split}
$$
En lenguaje natural:
"Existe algún entero $a,b$ tal que $a+b$ no es un entero"

## Cuantificador Existencial

> La negación de $\exists$ es $\forall$ seguido de la negación de la proposición

- Afirmación *Existe x en $A$ tal que se cumple $P(x)$*
  En lenguaje matemático: $(\exists x)(P(x))$
- Negación *No es cierto que existe $x$ en $A$ tal que se cumple $P(x)$*
  Esto significa que para ningún elemento en $A$ se cumple $P(x)$, o equivalentemente, para todos los elementos en $A$ no se cumple $P(x)$
  En lenguaje matemático: $\lnot(\exists x)(P(x)) \iff (\forall x)(\lnot P(x))$

==Ejemplo==

Afirmación: 

- En lenguaje natural: *"Existe un número natural n tal que n es mayor que 10"*
- En lenguaje proposicional:
$$
p \land q \quad
\begin{cases}
p:\text{"n es numero natural"}\\
q:\text{"n es mayor que 10"}
\end{cases}
$$
> No es posible expresarlo en lenguaje proposicional puro ya que los cuantificadores $\forall, \exists$ no pertenecen a este si no al Lenguaje de predicados (o Logica de primer orden). 
> Pero esto nos sirve para saber como se debe negar la proposición ya que sabemos que $\lnot(p\land q)$ es igual que $\lnot p \lor \lnot q$ por leyes de Morgan
- En lenguaje matemático:
$$
(\exists n)(n\in\N \land n > 10)
$$

Negación: 

- En lenguaje natural sin transformar: *"No es cierto que Existe un número natural n tal que n es mayor que 10"*
- En lenguaje proposicional: 
$$
\lnot(p\land q)\iff \lnot p\lor \lnot q \quad
\begin{cases}
\lnot p:\text{"n no es un numero natural"} \\
\lnot q:\text{"n es menor igual que 10"}
\end{cases}
$$
- En lenguaje matemático:
$$
\begin{split}
&\lnot((\exists n)(n\in\N \land n > 10)) \\
&(\forall n)(\lnot(n\in\N \land n>10)) \\
&(\forall n)(\lnot(n\in\N) \lor \lnot(n>10)) \\
&(\forall n)(n\not\in\N \lor n\leq10) \\
\end{split}
$$
- En lenguaje natural transformado: *"Para todo $n$, $n$ no es numero natural o $n$ menor o igual que 10"*