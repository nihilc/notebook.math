# Negación de cuantificadores

## Cuantificador Universal

> La negación de $\forall$ es $\exists$ seguido de la negación de la proposición

- Afirmación *"Para todo $x$ en $A$, se cumple $P(x)$"* 
  En lenguaje matemático: $(\forall x)(P(x))$
- Negación *"No es cierto que para todo $x$ en $A$, se cumple $P(x)$"* $\iff\lnot(\forall x)(P(x))$
  Esto significa que existe al menos un elemento en $A$ para el cual $P(x)$ no se cumple.
  En lenguaje matemático: $\lnot(\forall x)(P(x)) \iff (\exists x)(\lnot P(x))$

==Ejemplo==



## Cuantificador Existencial

> La negación de $\exists$ es $\forall$ seguido de la negación de la proposición

- Afirmación *Existe x en $A$ tal que se cumple $P(x)$*
  En lenguaje matemático: $(\exists x)(P(x))$
- Negación *No es cierto que existe $x$ en $A$ tal que se cumple $P(x)$*
  Esto significa que para ningún elemento en $A$ se cumple $P(x)$, o equivalentemente, para todos los elementos en $A$ no se cumple $P(x)$
  En lenguaje matematico: $\lnot(\exists x)(P(x)) \iff (\forall x)(\lnot P(x))$

==Ejemplo==