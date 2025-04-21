# Aritmética Modular

Sean $a$ y $b$ enteros y $m$ entero positivo, Decimos que $a$ es **congruente** con $b$ modulo $m$ y se representa por $a \equiv b(\mod m)$ . Si $m$ divide a $a-b$; es decir $m|(a-b)$. Si $a$ no es congruente con $b$ modulo $m$ es decir $a\not\equiv b(\mod m)$

==Ejemplo==

$8\equiv2(\mod 3)$?

Veamos si $3|8-2$ es decir $3|6$
Es cierto que $3|6$ porque $6=3\cdot2$
$\therefore 8\equiv2(\mod 3)$

==Ejemplo==

$10\equiv4(\mod8)$?

$$
\begin{split}
10 \not\equiv 4(\mod8) &\iff 8|10-4\\
&\iff 8|6 \\
&\iff 6 \not= 8\cdot c \land c \in \Z \\ \\
\therefore 10\not&\equiv4(\mod8)
\end{split}
$$

## Teoremas
### Teorema

#Teorema $a,b \in \Z \land m \in\Z^+ \implies (a\equiv b(\mod m) \iff a \mod m = b \mod m)$

==Demostración==

$(p \iff q)\iff (p\implies q) \land (q\implies p)$

1. $a \equiv b(\mod m) \implies a\mod m = b\mod m$
Supongamos que $a\equiv b(\mod m)$; es decir $m|a-b$
Luego, existe un entero $c$ tal que $a-b=m\cdot c$
Así, $a=m\cdot c + b$ y $b=-m\cdot c + a$

2. $a \mod m = b \mod m \implies a\equiv b(\mod m)$ 


==Ejemplo==

$8\equiv2(\mod3)$

$8\mod3=\boxed2$ porque $8=3\cdot2+\boxed2$
$2\mod3=\boxed2$ porque $2=3\cdot0+\boxed2$

En efecto $8\mod3=2\mod3$

### Teorema

#Teorema $a,b,c,d\in\Z \land m\in\Z^+ \land a\equiv b(\mod m) \land c\equiv d(\mod m) \implies a+c \equiv b+d(\mod m) \land ac\equiv bd(\mod m)$

==Demostración==

Supongamos que $a\equiv b(\mod m)$ y $c\equiv d(\mod m)$ entonces $m|a-b$ y $m|c-d$ es decir:
$a-b=mk$ con $k\in\Z$
$c-d=mp$ con $p\in\Z$
Luego, $a=b+mk$ y $c=d+mp$ sumamos estas igualdades termino a termino
$$
\begin{split}
a+c &= (b+mk) + (d+mp) \\
&= (b+d) + (mk + mp) \\
&= (b+d) + m(k+p)
\end{split}
$$
Como $k$ y $p$ son enteros entonces $k+p$ también es entero, Sea $n=k+p \in\Z$ por lo tanto:
$$
\begin{split}
a+c &= (b+d)+mn \\
(a+c)-(b+d)&= mn
\end{split}
$$
Ósea $m|(a+c)-(b+d)$
$\therefore a+c\equiv(b+d)(\mod m)$

Ahora también si multiplicamos termino a termino $a=b+mk$ y $c=d+mp$ tenemos que
$$
\begin{split}
ac &= (b+mk)(d+mp) \\
&= bd + bmp + mkd + m^2kp \\
&= bd + m(bp + kd + mkp)
\end{split}
$$
Ahora como $b,d,p,k,m \in \Z$ entonces $bp+kd+mkp$ también es entero, llamémoslo $n$ entonces
$$
\begin{split}
ac &= bd + mn \\
ac - bd &= mn
\end{split}
$$
Ósea $m|ac-bd$
$\therefore ac\equiv bd(\mod m)$

==Ejemplos==

## Aplicaciones de las convergencias

### Funciones de dispersion

Memoria de un computador <- Información
Por ejemplo la universidad debe guardar la información de todos los estudiantes, guarda sus datos personales y academicos. Como hacer para poder acceder a la información de cada estudiante de forma efectiva?
Para esto se usan las funciones de dispersion:
La información se almacena en ficheros cada uno de ellos se localiza usando una clave, que identifica de forma unica el fichero de cada estudiante. En particular la identificación puede ser el código estudiantil. Una función de dispersion $h$ asigna una posición de memoria $h(k)$ al fichero que tiene a $k$ como clave. Existen muchas funciones de dispersion, una de ellas es $h(k)=k(\mod m)$ donde $m$ es el numero de posiciones de memoria existentes.
![[_files/09-aritmetica_modular_20250410.png]]
$h(k)=k\mod m$ Residuo de dividir $k$ por $m$

==Ejemplo==
$m=100$ (cantidad maxima de posiciones de memoria)

- $k_1=20251167000$ Código estudiantil
  $h(k_1)=20251167000 \mod m = \boxed 0$
  $\therefore$ al estudiante de código $k_1$ se le asigna la posición de memoria $0$
- $k_2=20251167826$
  $h(k_2)=20251167826 \mod m = \boxed{26}$
  $\therefore$ al estudiante de código $k_2$ se le asigna la posición de memoria $26$
- $k_3=20251167100$
  $h(k_3)=20251167100 \mod m = \boxed 0$
  Como la posición de memoria $0$ se encuentra ocupada por $k_1$ se le asigna la siguiente
  $\therefore$ al estudiante de código $k_3$ se le asigna la posición de memoria $1$

> Nota: Puede ocurrir que dos códigos estudiantiles dejen el mismo residuo al dividirse por m. En este caso se dice que ha ocurrido una colisión. Una forma de solucionar esta situación es asignar al código que genera repetición del residuo, la siguiente posición de memoria que esté libre en ese momento.

### Numero pseudoaleatorios (Método de congruencia lineal)

Para generar numero pseudoaleatorios usaremos el método de congruencia lineal. Elegimos cuatro numero enteros:

- El modulo $m$
- El multiplicador $a$
- El incremento $c$
- La semilla $x_0$

Que satisfaga $2\leq a <m,\; 0\leq c < m,\; 0\leq x_0<m$

Generamos una sucesión de números pseudoaleatorios $x_n$ , $0\leq n < m$ así; aplicando reiteradamente la congruencia:

$$\boxed{x_{n+1}=(ax_n+c)\mod m}$$

==Ejemplo==
$m=8 ,\quad a=5 ,\quad c=3 ,\quad x_0=2$

- $x_1=(5x_0+3)\mod 8 = (5 \cdot 2 + 3)\mod 8 = 13 \mod 8$
  $\boxed{x_1=5}$
- $x_2=(5x_1+3)\mod 8 = (5\cdot5+3)\mod 8 = 28 \mod 8$
  $\boxed{x_2=4}$
- $x_3=(5x_2+3)\mod 8 = (5\cdot4+3)\mod 8 = 23 \mod 8$
  $\boxed{x_3=7}$
- $x_4=(5x_3+3)\mod 8 = (5\cdot7+3)\mod 8 = 38 \mod 8$
  $\boxed{x_4=6}$
- $x_5=(5x_4+3)\mod 8 = (5\cdot6+3)\mod 8 = 33 \mod 8$
  $\boxed{x_5=1}$
- $x_6=(5x_5+3)\mod 8 = (5\cdot1+3)\mod 8 = 2 \mod 8$
  $\boxed{x_6=2}$

Aquí como volvimos a llegar a la semilla $x_0=x_6$ se repetiría por lo tanto nuestra sucesión de numero aleatorios es: $5,4,7,6,1,2$

### Criptología

La congruencias tienen muchas aplicaciones, en particular en las ciencias de la computación. Una de ellas es la criptología o criptografía, que es el estudio de los mensajes secretos.

==Ejemplo==

$$
\begin{array}{|c|c|} \hline
A & B & C & D & E & F & G & H & I & J & K & L & M & N \\
0 & 1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 & 9 & 10 & 11 & 12 & 13 \\ \hline
Ñ & O & P & Q & R & S & T & U & V & W & X & Y & Z \\
14 & 15 & 16 & 17 & 18 & 19 & 20 & 21 & 22 & 23 & 24 & 25 & 26 \\ \hline
\end{array}
$$

Encriptar el mensaje "La próxima semana tendremos vacaciones"
Usando la numeración dada el mensaje es: 
"11 0  16 18 15 24 8 12 0  19 4 12 0 13 0  20 4 13 3 18 4 12 15 19  22 0 2 0 2 8 15 13 4 19"

Este método de encriptación se basa en reemplazar cada uno de los números del mensaje por:
$f(p)=(p+3)\mod 27$
Así, el mensaje encriptado es 
"14 3  19 21 18 0 11 15 3  22 7 15 3 16 3 23 7 16 6 21 7 15 18 22  25 3 5 3 5 11 18 16 7 22"

Para recuperar el mensaje original del mensaje encriptado debemos usar la función inversa de $f$

$f^{-1}(p)=(p-3)\mod 27$ donde $0\leq p< 27$

Se puede generalizar este método se puede desplazar $k$ lugares en lugar de 3 letras en el alfabeto; es decir $f(p)=(p+k)\mod27$ A este método se le llama cifrado por traslación. Y se descifra con la función inversa $f^{-1}(p)=(p-k)\mod 27$ A este proceso se llama descifrado o descodificación