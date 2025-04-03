# Lista de Tautologias

## Lista Rápida

1. $p \land q \iff q\land p$
2. $p \lor q \iff q \lor p$
3. $p \land (q\land r) \iff (p \land q)\land r$
4. $p \lor (q \lor r) \iff (p\lor q)\lor r$
5. $p\land p\iff p$ #_duda 
6. $p \lor p \iff p$ #_duda 
7. $p \land (q \lor r) \iff (p \land q) \lor (p \land r)$
8. $p \lor (q \land r) \iff (p \lor q) \land (p \lor r)$
9. $\lnot(\lnot p)\iff p$
10. $\lnot(p\land q)\iff \lnot p \lor \lnot q$
11. $\lnot(p\lor q)\iff \lnot p \land \lnot q$
12. $\lnot(p \implies q) \iff p \land \lnot q$
13. $(p \implies q) \iff \lnot p \lor q$
14. $(p \implies q \lor r) \iff p \land \lnot q \implies r$
15. $(p \implies q \lor r) \iff p \land \lnot r \implies q$
16. $(p \implies q \land r) \iff (p \implies q)\land(p \implies r)$

## Completas

### Ley de identidad

$p \implies p$
Una proposición siempre se implica a si misma
$$
\begin{array}{|c|c|}\hline
	p & p \implies p \\ \hline
	\T & \T \\
	\F & \T \\ \hline
\end{array}
$$

### Ley de no contradicción

$\lnot(p \land \lnot p)$
Una proposición y su negación no pueden ser verdaderas al mismo tiempo 
$$
\begin{array}{|c|c|}\hline
	p & \lnot p & p \land \lnot p & \lnot(p \land \lnot p) \\ \hline
	\T & \F & \F & \T \\
	\F & \T & \F & \T \\ \hline
\end{array}
$$

### Ley de no contradicción

$p \lor \lnot p$
Una proposición es verdadera o su negación es verdadera; no hay una tercera posibilidad
$$
\begin{array}{|c|c|}\hline
	p & \lnot p & p \lor \lnot p \\ \hline
	\T & \F & \T \\
	\F & \T & \T \\ \hline
\end{array}
$$
