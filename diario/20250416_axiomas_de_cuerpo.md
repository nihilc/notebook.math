# Axiomas de cuerpo

Sea $\R$ un conjunto. Supongamos que en $\R$ definimos dos operaciones $+$ y $\cdot$ que cumplen los siguientes axiomas:
- $A_0\quad \forall x,y \in\R \implies x+y \in \R \land xy\in\R$
- $A_1\quad \forall x,y\in\R \implies x+y=y+x \land xy=yx$
- $A_2\quad \forall x,y,z \in\R \implies x+(y+z)=(x+y)+z \land x(yz)=(xy)z$
- $A_3\quad \forall x,y,z\in\R \implies x(y+z)=xy+xz$
- $A_4\quad \exists0,1\in\R \land \forall x \in\R \implies x+0=x \land x\cdot1=x$
- $A_5\quad \forall x\in\R \implies \exists y\in\R \land x+y=0$
- $A_6\quad \forall x\in\R \land x\not=0 \implies \exists z\in\R \land xz=1$
## Teoremas

- $\forall a,b,c \in\R \land a+b=a+c \implies b=c$
- $\forall a,b \in\R \land \exists! x\in\R \implies a+x=b$

## Definición Inverso Aditivo

Al numero $x$ solución de la ecuación $a+x=b$ lo notaremos por $b-a$. En particular, si $b=0$ ($A_5$), entonces $a+x=0$ y así $x=0-a=-a$, al cual llamaremos el inverso aditivo de $a$, o el opuesto de $a$

## Teoremas

- $\forall a,b \in\R \implies a-b=a+(-b)$
- $\forall a \in \R \implies -(-a)=a$
- $\forall a \in\R \implies a\cdot0=0$
- $\forall a,b \in\R \implies -(ab)=(-a)\cdot b$
- $\forall a,b,c \in\R \implies (a+b)c=ac+bc$
- $\forall a,b,c \in\R \implies a(b-c)=ab-ac$
- $a,b,c \in\R \land a\not=0 \land ab=ac \implies b=c$
- $a,b\in\R \land a\not=0 \land \exists!x\in\R \implies ax=b$

## Definición Inverso Multiplicativo

Al numero $x$ solución de la ecuación $ax=b$, $a\not=0$ lo notaremos por $\frac{b}{a}$. En particular, si $b=1$ ($A_6$), entonces $ax=1$ y así $x=\frac{1}{a}$ que notaremos por $a^{-1}$ y lo llamaremos el inverso multiplicativo de $a$ o el reciproco de $a$

## Teoremas

- $\forall a,b\in\R \land a\not=0 \implies \frac{b}{a}=ba^{-1}$
- $a\in\R \land a\not=0 \land a^{-1}\;\text{es inversible}  \implies (a^{-1})^{-1}=a$
- $\forall a,b \in\R \land ab=0 \implies a=0 \lor b=0$
- $\forall a,b \in\R \implies (-a)(-b)=ab$
- $a,b\in\R \land ab\not=0 \implies (ab)^{-1}=a^{-1}b^{-1}$
- $a,b,c,d \in\R \land b\not=0 \land d\not=0 \implies \frac{a}{b}+\frac{c}{d}=\frac{ad+bc}{bd}$
- $a,b,c,d\in\R \land b\not=0 \land d\not=0 \implies \frac{a}{b}\cdot \frac{c}{d} = \frac{ac}{bd}$