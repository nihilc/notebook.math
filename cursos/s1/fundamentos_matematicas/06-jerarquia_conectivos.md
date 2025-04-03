# Jerarquía de conectivos

1. Implicación ==$\implies$== es el conectivo mas fuerte
$p \implies q \land r$ Es una implicación, como sabemos que tiene prioridad $\implies$ es lo mismo que decir $p\implies(q\land r)$
$(p \implies q) \land r$ es una conjunción
> Doble implicación también se podría decir que esta al mismo nivel pero como se puede ver como $(p \implies) q \land (q\implies p)$ no es necesario 

2. Conjunción y Disyunción ==$\land, \lor$== son igual de fuertes
$p \land q \lor r$ No es una [[cursos/s1/fundamentos_matematicas/02-lenguaje_proposicional#Formulas Bien Formadas (FBF or WFF)|FBF]]
$(p \land q) \lor r$ Es una Disyunción
$p \land (q \lor r)$ Es una Conjunción

3. La negación ==$\lnot$== es el termino de enlace mas débil, actúa solamente sobre la mas cercana
$\lnot p \land q$ Es una Conjunción
$\lnot(p\land q)$ Es una Negación