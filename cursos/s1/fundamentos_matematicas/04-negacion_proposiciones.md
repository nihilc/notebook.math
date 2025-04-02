# Negación de proposiciones

$$
\boxed{
\begin{split}
	\lnot (\lnot p) &\iff p\\ 
	\lnot (p \lor q) &\iff \lnot p \land \lnot q \\
	\lnot (p \land q) &\iff \lnot p \lor \lnot q \\
	\lnot (p \implies q) &\iff p \land \lnot q \\
	\lnot (p \iff q) &\iff (p \land \lnot q) \lor (\lnot p \land q)
\end{split}
}
$$

## Tablas de verdad de negaciones

### $\lnot (\lnot p) \iff p$

$$
\begin{array}{|c|c|} \hline
p & \lnot p & \lnot(\lnot p) \\ \hline
\T & \F & \T \\
\F & \T & \F  \\ \hline
\end{array}
$$

### $\lnot(p \lor q) \iff \lnot p \land \lnot q$

$$
\begin{array}{|c|c|} \hline
p & q & p \lor q & \lnot(p \lor q) & \lnot p & \lnot q & \lnot p \land \lnot q \\ \hline
\T & \T & \T & \F & \F & \F & \F \\
\T & \F & \T & \F & \F & \T & \F \\
\F & \T & \T & \F & \T & \F & \F \\
\F & \F & \F & \T & \T & \T & \T \\ \hline
\end{array}
$$

### $\lnot(p \land q) \iff \lnot p \lor \lnot q$

$$
\begin{array}{|c|c|} \hline
p & q & p \land q & \lnot(p \land q) & \lnot p & \lnot q & \lnot p \lor \lnot q \\ \hline
\T & \T & \T & \F & \F & \F & \F \\
\T & \F & \F & \T & \F & \T & \T \\
\F & \T & \F & \T & \T & \F & \T \\
\F & \F & \F & \T & \T & \T & \T \\ \hline
\end{array}
$$

### $\lnot(p \implies q) \iff p \land \lnot q$

$$
\begin{array}{|c|c|} \hline
p & q & p \implies q & \lnot(p \implies q) & \lnot q & p \land \lnot q \\ \hline
\T & \T & \T & \F & \F & \F \\
\T & \F & \F & \T & \T & \T \\
\F & \T & \T & \F & \F & \F \\
\F & \F & \T & \F & \T & \F \\ \hline
\end{array}
$$

### $\lnot(p \iff q) \iff (p \land \lnot q)\lor(\lnot p \land q)$

$$
\begin{array}{|c|c|} \hline
p & q & p \iff q & \lnot(p \iff q) & \lnot p & \lnot q & p \land \lnot q & \lnot p \land q & (p \land \lnot q)\lor(\lnot p \land q) \\ \hline
\T & \T & \T & \F & \F & \F & \F & \F & \F \\
\T & \F & \F & \T & \F & \T & \T & \F & \T \\
\F & \T & \F & \T & \T & \F & \F & \T & \T \\
\F & \F & \T & \F & \T & \T & \F & \F & \F \\ \hline
\end{array}
$$

