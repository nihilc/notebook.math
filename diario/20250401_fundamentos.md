# Conjuntos

## Operaciones

- Union
- Intersección
- Complemento
- Diferencia
- Diferencia Simétrica

### Union

$A\cup B=\{x | x\in A \lor x\in B\}$

### Intersección

$A\cap B=\{x|x\in A \land x\in B\}$

### Complemento

$A^C=\{x|x \not\in A\}$
$C_u(A)=\{x\in U | x \not\in A\}$
### Diferencia

$A-B=\{x|x\in A \land x\not\in B\}$

### Diferencia Simétrica

$A\triangle B=\{x|x\in A \underline\lor x\in B\}$

## Diagramas de Venn

![[_files/20250401_fundamentos 20250401]]

# Como usamos el calculo proposicional para mostrar propiedades en conjuntos?

$A \cup (B \cap C)$

$A\cup(B\cap C) = (A\cup B)\cap(A\cup C)$

# Igualdad de conjuntos

$$
\begin{split}
A=B &\iff (\forall x)(x\in A \iff x \in B) \\
&\iff (\forall x)(x\in A \implies x \in B \land x\in B \implies x \in A)
\end{split}
$$

==Ejemplo==

 $A\cup(B\cap C) =(A\cup B)\cap (A\cup C)$
![[_files/20250401_fundamentos 20250401_0]]

Demostración

$$
\begin{split}
x\in A\cup(B\cap C) &\iff x\in A \lor x \in (B\cap C) 
	&&&\text{Definicion}\\
&\iff x\in A \lor (x\in B \land x \in C) 
	&&&\text{Definicion} \\
&\iff (x\in A \lor x \in B) \land (x\in A \lor x\in C) \quad  
	&&&\text{Tautologia} \\
&\iff x \in A \cup B \land x \in A \cup B  
	&&&\text{Definicion}\\
&\iff \boxed {x \in (A \cup B) \cap (A\cup B)}  
	&&&\text{Definicion}
\end{split}
$$

> Se usa la tautologia $p\lor(q\land r)\iff (p\lor q) \land (p \lor r)$

==Probar==

$A\cap(B\cup C) = (A\cap B)\cup(A\cap C)$
![[_files/20250401_fundamentos 20250401_1]]
Demostración

$$
\begin{split}
x\in A \cap(B\cup C) &\iff x\in A \land x\in (B\cup C) 
	&& \text{Definicion}\\
&\iff x\in A \land (x\in B \lor x \in C) 
	&&\text{Definicion} \\
&\iff (x \in A \land x \in ) \lor (x \in A \land x \in B) \quad
	&&\text{Tautologia} \\
&\iff x\in A\cap B \lor x \in A \cap B 
	&&\text{Definicion}\\
&\iff \boxed{x \in (A \cap B) \cup (A \cap B)}
	&&\text{Definicion}
\end{split}
$$

> Se usa la tautologia $p\land(q\lor r)\iff (p\land q) \lor (p \land r)$


# Leyes de Morgan

## $(A\cup B)^c = A^c \cap B^c$

![[_files/20250401_fundamentos 20250401_2]]

Demostración
$$
\begin{split}
x\in (A\cup B)^c
&\iff x\not\in (A \cup B)
  &&\text{Def. complemento} \\
&\iff \lnot(x\in A \cup B)
  &&\text{Def. union} \\
&\iff \lnot(x\in A \lor x \in B)
  &&\text{Tautologia} \\
&\iff x\not\in A \land x\not\in B 
  &&\text{} \\
&\iff x \in A^c \land x \in B^c
  &&\text{} \\
&\iff x \in A^c \cap B^c
\end{split}
$$

## $(A\cap B)^c = A^c \cup B^c$
![[_files/20250401_fundamentos 20250401_3]]
$$
\begin{split}
x \in (A \cap B)^c 
&\iff x \not\in A\cap B \quad\quad\quad\quad\quad
  &&\text{Def. complemento}\\
&\iff \lnot(x\in A\cap B) 
  &&\text{Def. complemento}\\
&\iff \lnot(x \in A \land x \in B) 
  &&\text{Def. interseccion}\\
&\iff \lnot x \in A \lor \lnot x \in B 
  &&\text{Tautologia }\\
&\iff x\not\in A \lor x \not \in B 
  &&\text{Def. complemento}\\
&\iff x \in A^c \lor x \not\in B^c 
  &&\text{Def. complemento}\\
&\iff x \in A^c \cup x \in B^c 
  &&\text{Def. union}\\
\end{split}
$$
# Tarea 

Ejercicios cap 1 libro, solo propiedades y proposiciones