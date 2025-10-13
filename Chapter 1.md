The Real and Complex Number Systems

**Example** 1.1 Proof by contradiction that $\exists p$ rational, $p^2 = 2$.

**Def** 1.3 Member of a set, empty set, nonempty set, subset, proper subset, equal set

**Def** 1.4 The set of all rational numbers, $\mathbb{Q}$

## Ordered Sets
**Def** 1.5 Order, <
Let $S$ be a set. An *order* on $S$ is a relation, denoted by <, such that
(i) If $x\in S$ and $y\in S$ then one and only one of the statements $$x<y, x=y, y<x$$ is true. 
(ii) If $x,y,z\in S$, if $x<y$ and $y<z$, then $x<z$.

**Def** 1.6 Ordered set
An *ordered set* is a set $S$ in which an order is defined.

**Def** 1.7 Upper bound, bounded above, lower bound, bounded under
Suppose $S$ is ordered and $E\subset S$. If $\exists \beta\in S$ s.t. $x\le \beta, \forall x\in E$, we say that $E$ is *bounded above* and call $\beta$ an *upper bound* of $E$.

If $\exists \beta\in S$ s.t. $x\ge \beta, \forall x\in E$, we say that $E$ is *bounded below* and call $\beta$ an *lower bound* of $E$.

**Def** 1.8 Least upper bound/supremum, greatest lower bound/infimum
Suppose $S$ is an ordered set, $E\subset S$, and $E$ is bounded above. Suppose $\exists \alpha \in S$ with the following properties:
(i) $\alpha$ is an upper bound of $E$.
(ii) If $\gamma<\alpha$ then $\gamma$ is not an upper bound of $E$. 

Then, $\alpha$ is called the *least upper bound* of $E$ or the *supremum* of $E$.
$$\alpha = \sup E$$

Suppose $S$ is an ordered set, $E\subset S$, and $E$ is bounded below. Suppose $\exists \alpha \in S$ with the following properties:
(i) $\alpha$ is a lower bound of $E$.
(ii) If $\gamma>\alpha$ then $\gamma$ is not a lower bound of $E$. 

Then, $\alpha$ is called the *greatest lower bound* of $E$ or the *infimum* of $E$.
$$\alpha = \inf E$$

**Def** 1.10 Least-upper-bound property
An ordered set $S$ is said to have the *least-upper-bound property* if the following is true:
If $E\subset S$, $E$ is not empty, and $E$ is bounded above, then $\sup E$ exists in $S$.

**Thm** 1.11
Suppose $S$ is an ordered set with the least-upper-bound property, $B\subset S$, $B$ is not empty, and $B$ is bounded below. Let $L$ be the set of all lower bounds of $B$. Then, 
$$\alpha = \sup L$$ exists in $S$, and $\alpha = \inf B$. In particular, $\inf B$ exists in $S$.

*Proof*: Since $B$ is bounded below, $L$ is not empty. $L$ is bounded above by any element of $B$, because, by definition, $\forall \beta\in B$, $\forall a\in L$, $\beta\ge a$. Therefore, $L$ has a supremum. 

Let $\alpha = \sup L$. Then, $\forall b \in B$, since $\forall \alpha\in L$, $\alpha \le b$. Then, any element of $B$ is an upper bound of $L$. Suppose $\gamma\in B$, if $\gamma < \alpha$ then $\gamma$ is not an upper bound of $L$. Then, $\gamma \ge \alpha$, so $\alpha$ is a lower bound of $B$, i.e., $\alpha\in L$.

Since $\alpha = \sup L$, if $\alpha < \zeta$, then $\zeta\notin L$. Therefore, $\alpha$ is the greatest lower bound of $B$.
$$\alpha = \inf B$$
(QED)

## Fields
**Def** 1.12 Field, addition, multiplication
A *field* is a set $F$ with two operations, *addition* and *multiplication*, which satisfy the following axioms.
**(A)** Axioms for addition
(A1) If $x\in F$ and $y\in F$, then their sum $x+y$ is in $F$.
(A2) Addition is commutative: $x+y=y+x$, $\forall x,y\in F$.
(A3) Addition is associative: $(x+y)+z = x+(y+z)$, $\forall x,y,z\in F$.
(A4) $F$ contains an element 0 such that $0+x=x$, $\forall x\in F$.
(A5) To every $x\in F$ corresponds an element $-x\in F$ such that $x+(-x)=0$.

**(M)** Axioms for multiplication
(M1) If $x\in F$ and $y\in F$, then their product $xy\in F$.
(M2) Multiplication is commutative: $xy=yx$, $\forall x,y\in F$.
(M3) Multiplication is associative: $(xy)z=x(yz)$, $\forall x,y,z\in F$.
(M4) $F$ contains an element 1$\neq $0 such that $1x=x$, $\forall x\in F$.
(M5) If $x\in F$ and $x\neq 0$ then $\exists 1/x\in F$ s.t. $x\cdot (1/x) = 1$.

**(D)** The distributive law
$$x(y+z) = xy + xz$$
holds $\forall x,y,z\in F$.

**Prop** 1.14
The axioms for addition imply
(a) If $x+y=x+z$ then $y=z$.
(b) If $x+y=x$ then $y=0$.
(c) If $x+y = 0$ then $y=-x$.
(d) $-(-x) = x$.

*Proof Roadmap*: (a) For $x\in F$, $\exists -x\in F$ s.t. $x+(-x) = 0$ (A5). Notice, $y = 0+y$ (A4). Then, $y = x+(-x)+y = x+y+(-x)$ (A3). $x+y+(-x) = x+z +(-x) = x+(-x)+z = 0+z=z$ (A3, A4). Therefore, $y=z$. (QED)
(b) $x+y=x = x+0$ (A4). Then, apply (a), $y=0$. (QED)
(c) $x+y=0\Rightarrow \exists -x\in F, x+y=x+(-x)$ (A5). Then, apply (a), $y=-x$. (QED)
(d) Notice that $(-x)+x = 0$ (A5), so $x = -(-x)$. (QED)

**Prop** 1.15 
The axioms of multiplication imply
(a) If $x\neq 0$ and $xy=xz$ then $y=z$.
(b) If $x\neq 0$ and $xy=x$ then $y=1$.
(c) If $x\neq 0$ and $xy=1$ then $y = 1/x$.
(d) If $x\neq 0$ then $1/(1/x)=x$.

**Prop** 1.16
The field axioms imply the following statements, $\forall x,y,z\in F$.
(a) $0x=0$.
(b) If $x\neq 0$ and $y\neq 0$ then $xy\neq 0$.
(c) $(-x)y = -(xy) = x(-y)$.
(d) $(-x)(-y) = xy$.

*Proof*: 
(a) Notice that $0x + 0x = (0+0)x = 0$ (D). Then, by Prop 1.14(b), $0x=0$. (QED)
(b) Assume, BWOC, that $xy=0$. Then, (M5)
$$1 = \left(\frac{1}{x}\right)\left(\frac{1}{y}\right) xy$$
Notice that $xy=0$, apply (a), 
$$\left(\frac{1}{x}\right)\left(\frac{1}{y}\right) xy = \left(\frac{1}{x}\right)\left(\frac{1}{y}\right)0 = 0$$
We have the ridiculous $1=0$. $\Rightarrow \Leftarrow$ (QED)
(c) For $(-x)y=-(xy)$, we need to show that $(-x)y + xy = 0$. Notice that, (D, A5),
$$(-x)y + xy = ((-x)+x)y = 0y$$
Apply (a), $(-x)y + xy = 0$, so $(-x)y = -(xy)$. 
The proof is similar for $-(xy) = x(-y)$. (QED)
(d) Apply Part (c), $(-x)(-y) = -(x(-y)) = -(-(xy))$. Apply Prop 1.14(d), $-(-(xy)) = xy$. Therefore, $(-x)(-y) = xy$. (QED)

**Def** 1.17 Ordered field
An *ordered field* is a field $F$ which is also an ordered set, s.t.
(i) $x+y<x+z$ if $x,y,z\in F$ and $y<z$.
(ii) $xy>0$ if $x\in F, y\in F$, $x>0$, and $y>0$.

**Prop** 1.18 The following statements are true in every ordered field.
(a) If $x>0$ then $-x<0$, and *vice versa*.
(b) If $x>0$ and $y<z$ then $xy<xz$.
(c) If $x<0$ and $y<z$ then $xy>xz$.
(d) If $x\neq 0$ then $x^2>0$. In particular $1>0$.
(e) If $0<x<y$ then $0<1/y<1/x$.

*Proof*: 
(a) If $x>0$, then $x+(-x)>0+(-x)$. By A5, Left hand side $=0$. By A4, Right hand side $=-x$. Then, $-x<0$. (QED)
(b) Since $y<z$, $0= y + (-y) < z + (-y)$ (A5), $x>0$, we have $x(z+(-y))>0$. By D, $xz + (-xy)>0$. Then, $xz = xz + (-xy) +xy >xy$. Therefore, $xz>xy$. (QED)
(c) Similar to (b).
(d) If $x>0$, $x^2>0$. (trivial) If $x<0$, then by (a), $-x>0$. $x^2 =(-x)^2>0$ according to Prop 1.16(d).  (QED)
(e) Notice that since $x(\frac{1}{x}) = 1>0$, $x>0$, $\frac{1}{x}>0$. Similarly, $\frac{1}{y}>0$. Then, $$\left(\frac{1}{x}\right)\left(\frac{1}{y}\right)>0$$
Since $x<y$, $y-x>0$. Then, $$(y-x)\left(\frac{1}{x}\right)\left(\frac{1}{y}\right)>0$$
$$\frac{1}{x} - \frac{1}{y}>0$$
$$\frac{1}{x}>\frac{1}{y}$$
(QED)

## The Real Field

**Thm** 1.19 There exists an ordered field $\mathbb{R}$ which has the least-upper-bound property. Moreover, $\mathbb{R}$ contains $\mathbb{Q}$ as a subfield.

**Thm** 1.20 
(a) If $x\in \mathbb{R}$, $y\in \mathbb{R}$, and $x>0$, then there is a positive integer $n$ s.t. $$nx>y.$$(b) If $x\in \mathbb{R}$, $y\in \mathbb{R}$, and $x<y$, then there exists a $p\in \mathbb{Q}$ s.t. $x<p<y$. 

*Proof*: (a) Assume, BWOC, that there is not such a positive integer $n$. Then, $y$ is larger than all elements of $A=\{nx\}_{n\in \mathbb{N}}$, i.e., $A$ is bounded above by $y$. Notice that $\mathbb{R}$ has the least-upper-bound property, so $\exists k\in \mathbb{R}$ such that $$k = \sup A$$
Then, notice that $k-x< k$ is not a upper bound of $A$, so $\exists m\in \mathbb{N}$ s.t. $k-x<mx$. However, $k<(m+1)x\in A$. This means that $k$ is not the supremum. $\Rightarrow \Leftarrow$
(b) $x<y \Rightarrow y-x>0$. Apply (a), $$n(y-x)>1\Rightarrow ny>1+nx$$
Apply (a) again, we get integers $m_1$, $m_2$, $$m_1>nx$$ and $$m_2>-nx.$$
Then, we see $$-m_2<nx<m_1,$$ which bounds $nx$ inside the interval of two integers $-m_2$ and $m_1$. $\exists m$ with $-m_2\le m \le m_1$ such that $m-1\le nx < m$. Notice that 
$$nx<m\le 1+nx$$
Since $ny>1+nx$, it follows that $$nx<m<ny$$
Then, divide the inequality by $n$, $$x<\frac{m}{n}<y.$$
**Thm** 1.21 $\forall x>0$ and $\forall n>0, n\in \mathbb{Z}$, $\exists$ one and only one positive $y\in \mathbb{R}$ s.t. $y^n=x$.

*Proof*: This theorem has two parts: Uniqueness and existence of such $y\in \mathbb{R}$. For uniqueness, note that $0<y_1<y_2$ implies $y_1^n<y_2^n$. 

For existence, we let $E$ be the set of all positive $t\in \mathbb{R}$ s.t. $t^n<x$. Such $E$ is nonempty: Let $t = \frac{x}{1+x}$, then $t^n\le t$ for all $n\in \mathbb{N}$ and $t<x$. Therefore, $t^n<x$ and $t\in E$. Such $E$ is bounded above: If $t>1+x$, then $t^n\ge t > x$. This $t\notin E$ but is an upper bound of $E$. Notice that $\mathbb{R}$ has the least-upper-bound property, which guarantees the existence of $$\alpha = \sup E.$$
Before we proceed on, notice that
$$\begin{align*}
b^n-a^n &= (b-a)(b^{n-1}+b^{n-2}a + \dots + a^{n-1})\\
&< (b-a)nb^{n-1}
\end{align*}$$
Assume, BWOC, $\alpha^n<x$. Let $$0<h<\frac{x-\alpha^n}{n(\alpha+1)},$$ $(\alpha+h)^n - \alpha^n < nh(\alpha+h)^{n-1} < nh(\alpha+1)^{n-1}<x-\alpha^n$. Then, $(\alpha+h)^n < x$. Then, $\alpha + h\in E$. Notice $\alpha + h>\alpha$, so $\alpha$ cannot be an upper bound of $E$. $\Rightarrow\Leftarrow$

Assume, BWOC, $a^n<x$. Let $$0<k<\frac{\alpha^n-x}{n(\alpha+1)}.$$ Notice that $$k < \frac{y^n - xy^{n-1}}{ny^{n-1}} = \frac{y-x}{n}<y.$$ Then, $$\alpha^n - (\alpha - k)^n < kn\alpha^{n-1}<\alpha^n - x,$$ so $(\alpha - k)^n>x$. Hence, $\alpha - k$ is also an upper bound of $E$, so $\alpha$ cannot be the least upper bound of $E$. $\Rightarrow\Leftarrow$

The only choice left is $\alpha^n=x$. We have thereby proven the existence of $\alpha$. (QED)

## The Extended Real Number System

**Def** 1.23 
The *extended real number system* consists of the real field $\mathbb{R}$ and two symbols, $+\infty$ and $-\infty$. We preserve the original order in $\mathbb{R}$, and define $$-\infty < x < +\infty$$ for all $x\in \mathbb{R}$.

## The Complex Field

**Def** 1.24 Complex number 
A *complex number* is an ordered pair $(a,b)$ of real numbers.

**Thm** 1.25 - **Thm** 1.29 Trivial stuff

**Def** 1.30 Conjugate, real part, imaginary part
If $a$, $b$ are real and $z=a+bi$, then $\overline{z} = a-bi$ is called the *conjugate* of $z$. $a$ is the *real part* and $b$ is the *imaginary part*. 

**Thm** 1.31
If $z$ and $w$ are complex, then
(a) $\overline{z+w} = \overline{z}+\overline{w}$.
(b) $\overline{zw} = \overline{z}\cdot\overline{w}$.
(c) $z+\overline{z} = 2\Re(z)$, $z-\overline{z} = 2i\Im(z)$.
(d) $z\overline{z}$ is real and positive (unless $z=0$).

Notice that $z\overline{z} = a^2+b^2$. 

**Def** 1.32 Absolute value

**Thm** 1.33 
Let $z$ and $w$ be complex numbers. Then
(a) $\lvert z \rvert>0$ unless $z=0, \lvert 0\rvert = 0$.
(b) $\lvert \overline{z}\rvert = \lvert z \rvert$.
(c) $\lvert zw\rvert = \lvert z\rvert \lvert w\rvert$.
(d) $\lvert \Re(z)\rvert \le \lvert z \rvert$.
(e) $\lvert z+w\rvert \le \lvert z\rvert + \lvert w\rvert$.

**Thm** 1.35
If $a_1,\dots, a_n$ and $b_1, \dots, b_n$ are complex numbers, then $$\left \lvert \sum_{j=1}^n a_j\overline{b}_j\right\rvert ^2\le \sum_{j=1}^n\lvert a_j\rvert^2\sum_{j=1}^n\lvert b_j\rvert^2 $$
*Proof*: Let $$A = \sum_{j=1}^n \lvert a_j\rvert ^2,$$ $$B = \sum_{j=1}^n \lvert b_j\rvert ^2,$$ $$C = \sum_{j=1}^n a_j\overline{b}_j.$$
$$\begin{align*}
\sum \left\lvert Ba_j - Cb_j\right\rvert^2 &= \sum(Ba_j - Cb_j)(B\overline{a}_j - \overline{Cb_j})\\
&= \sum(B^2a_j\overline{a}_j - B\overline{C}\overline{b}_ja_j - BC\overline{a}_jb_j - C\overline{C}b_j\overline{b}_j)\\
&= B^2\sum\lvert a_j \rvert^2 - B\overline{C}\sum a_j\overline{b}_j - BC\sum \overline{a}_j b_j - \lvert C\rvert^2 \sum\lvert b_j\rvert^2\\
&= B^2A - \lvert C\rvert^2B\\
&= B(AB - \lvert C\rvert^2) >0
\end{align*}$$

Therefore, $AB>\lvert C\rvert^2$. (QED)

## Euclidean Spaces

**Def** 1.36 Coordinates, vector space over the real field, origin, inner product, norm

**Thm** 1.37 Suppose $\mathbf{x}, \mathbf{y}, \mathbf{z}\in \mathbb{R}^k$, and $\alpha\in \mathbb{R}$, then
(a) $\lvert \mathbf{x}\rvert \ge 0$.
(b) $\lvert \mathbf{x}\rvert = 0$ if and only if $\mathbf{x} = 0$.
(c) $\lvert \alpha \mathbf{x}\rvert = \lvert \alpha \rvert \lvert \mathbf{x} \rvert$.
(d) $\lvert \mathbf{x} \cdot \mathbf{y} \rvert \le \lvert \mathbf{x} \rvert \lvert \mathbf{y} \rvert$.
(e) $\lvert \mathbf{x} + \mathbf{y} \rvert \le \lvert \mathbf{x} \rvert + \lvert \mathbf{y} \rvert$.
(f) $\lvert \mathbf{x} - \mathbf{z} \rvert \le  \lvert \mathbf{x} - \mathbf{y} \rvert + \lvert \mathbf{y} - \mathbf{z} \rvert$.

## EXERCISES

### Question 1
*Proof*: Assume, BWOC, that $r+x$ is rational. Then, $\exists m,n, m_1, n_1\in \mathbb{Z}$ s.t. $$r+x = \frac{m}{n} \text{ and }r = \frac{m_1}{n_1}.$$ We can write $$x = \frac{m}{n} - \frac{m_1}{n_1} = \frac{mn_1 - m_1n}{nn_1},$$ where $mn_1 - m_1n, nn_1\in \mathbb{Z}$ and they do not have a common factor larger than 1. Therefore, $x\in \mathbb{Q}$. $\Rightarrow\Leftarrow$ 

Assume, BWOC, that $rx$ is rational. Then, Then, $\exists m,n, m_1, n_1\in \mathbb{Z}$ s.t. $$rx = \frac{m}{n} \text{ and }r = \frac{m_1}{n_1}.$$ We can write $$x = \frac{rx}{x} = \frac{mn_1}{nm_1},$$ where $mn_1, nm_1\in \mathbb{Z}$ and they do not have a common factor larger than 1. Therefore $x\in \mathbb{Q}$. $\Rightarrow\Leftarrow$ (QED)

### Question 2
Assume, BWOC, that $\exists p\in \mathbb{Q}$, $$p^2 = 12.$$ Let $m,n\in \mathbb{Z}$, $$p=\frac{m}{n},$$ so $$\left(\frac{m}{n}\right)^2 = 12,$$ which follows $$m^2 = 12n^2.$$ Notice that $m^2$ is even, so $m$ must be even (divisible by 2); $m^2$ is divisible by 3, so $m$ must be divisible by 3. This leads to the fact that $m$ is divisible by 6 and $m^2$ is divisible by 36. Then, $12n^2$ must be divisible by 36. Hence, $n^2$ is divisible by 3, so $n$ is divisible by 3. Hence, $m, n$ shares a common factor 3. $\Rightarrow\Leftarrow$ (QED)

### Question 3
(a) As $x=0$, $\exists \frac{1}{x}\in F$ s.t. $x(\frac{1}{x}) = 1$ (M5). Then, notice $y = 1\cdot y$ (M4), so $y = x(\frac{1}{x})y = \frac{1}{x}xy$ (M3). It follows that $\frac{1}{x}xy = \frac{1}{x}xz = 1\cdot z = z$. (QED)
(b) Apply (a), let $z = 1$, $xy = xz\Rightarrow y=z \Rightarrow y=1$. (QED)
(c) $xy = 1\Rightarrow xy = x(1/x)$ (M5). Then, apply (a), let $z = 1/x$, $xy=xz\Rightarrow y=z\Rightarrow y = 1/x$. (QED)
(d) $x\cdot (1/x) = 1$ (M5). Then, $x = 1/(1/x)$. (QED)

### Question 4
Since $\alpha$ is a lower bound of $E$, $\forall \epsilon \in E$, $\alpha \le \epsilon$. Since $\beta$ is an upper bound of $E$, $\forall \epsilon \in E$, $\beta\ge \epsilon$. Therefore, $\forall \epsilon\in E$, $$\alpha \le \epsilon \le \beta.$$ (QED)

### Question 5
Since $A$ is bounded below, $\exists \beta \in \mathbb{R}$, s.t. $\forall a\in A$, $\beta\le a$. By the definition of $-A$, $\forall -a\in -A$ s.t. $a\in A$, $-\beta \ge -\alpha$. Therefore, $-A$ is bounded above. Since $A$ is nonempty, $-A$ is nonempty. Thus, the supremum of $-A$ exists. Let $$\alpha = \sup (-A),$$ $\forall -a\in -A$, $\alpha \ge -a$; if $\gamma < \alpha$, then $\exists -a\in -A$ s.t. $\gamma < -a$. For the former condition, $\forall a\in A$, $-\alpha \le a$. Then, $-\alpha$ is a lower bound of $A$. For the latter condition, if $-\gamma > -\alpha$, then $\exists a\in A$ s.t. $-\gamma > a$. Then, $-\alpha$ is the greatest lower bound of $A$. $$-\alpha = \inf A, $$ or $$ \inf A = -\sup(-A). $$ (QED)
### Question 6
(a) With $$r = \frac{m}{n} = \frac{p}{q},$$ we know that $mq = pn$. Note that if $x = (b^m)^{1/n}$, then $x^n = b^m$. We can even raise both sides to the power of $q$, $(x^n)^q = (b^m)^q$. Thus, $$x^{nq} = b^{mq}$$ Similarly, let $y = (b^p)^{1/q}$, then $y^q = b^p$. We raise both sides to the power of $n$, $(y^q)^n = (b^p)^n$. Thus, $$y^{nq} = b^{pn}$$ Then, since $pn = mq$, $b^{pn} = b^{mq}$, so $x^{nq} = y^{nq}$. This follows $x = y$. Therefore, $$(b^m)^{1/n} = (b^p)^{1/q}$$ (QED)
(b) Let $r = m/n, s = p/q$, where $m,n,p,q$ are all integers. Let $x = b^{r+s} = b^{m/n+p/q} = (b^{mq+np})^{1/nq}$. Now, raise both sides to the power of $nq$, $$x^{nq} = b^{mq+np},$$ with $mq+np\in \mathbb{Z}$. 

Let $y = b^{m/n}b^{p/q} = (b^m)^{1/n}(b^p)^{1/q}$. We raise both sides to the power of $nq$, $$y^{nq} = b^{mq}b^{np} = b^{mq+np}$$
It follows that $x^{nq}=y^{nq}$, so $x=y$, i.e., $$b^{r+s}=b^rb^s$$ (QED)

 (c) When $r$ is rational, $r = m/n$ where $m,n\in \mathbb{Z}$. Then, $B(r)$ is the set of all numbers $b^t$ with $t\in \mathbb{Q}, t\le r$. What we need to prove is that for $p,q\in \mathbb{Q}$, if $p\le q$, then $b^p\le b^q$ ($b>1$). Let $q=p+s$, where $s\in\mathbb{Q}_{\ge 0}$, we can apply (b): $b^q = b^pb^s$. Then, notice that $\forall s\in \mathbb{Q}_{\ge 0}$, $b^s\ge 1$. Therefore, $b^q = b^pb^s\ge b^p$. 

Then, $\forall t\le r$, $b^t\le b^r$, so $b^r$ is an upper bound. If $\gamma < r$, then $\exists t'\le r, t\in \mathbb{Q}$ s.t. $t'> \gamma$. Therefore, if $b^\gamma \le b^r$, then $\exists $b^{t'}\le b^r$ s.t. $b^{t'}>b^\gamma$. This proves that $b^r$ is the least upper bound. $$b^r = \sup B(r)$$
(d) For this part, I prove two conclusions: (i) $b^{x+y}\le b^xb^y$; (ii) $b^xb^y\le b^{x+y}$, where $b>1, x,y\in \mathbb{R}$. In Part (c), we have proven that $b^x = \sup B(x)$, $\forall x\in \mathbb{R}$. Let $r\in \mathbb{Q}$, $r\le x+y$. Then, $r-y\le x$. We can find $r-y\le t\le x$ where $t\in \mathbb{Q}$ because $\mathbb{Q}$ is dense in $\mathbb{R}$. Then, $b^t\in B(x)$. As $b^x = \sup B(x)$, $b^t\le b^x$. From $r-y\le t$, we can let $s = r-t\le y$. Similarly, $b^s\in B(y)$. As $b^y = \sup B(y)$, $b^s\le b^y$. Apply Part (b), $b^r = b^{s+t} = b^sb^t$. Then, since $b^s\le b^x$, $b^t\le b^y$, $b^r = b^sb^t\le b^xb^y$. Then, since our $r$ is arbitrary, $b^xb^y$ is the upper bound of $B(x+y$). Notice that $\sup B(x+y) = b^{x+y}$, $b^{x+y}\le b^xb^y$.

In the other direction, let $s\le x$, $t\le y$. Then, $b^s\in B(x)$, $b^t\in B(y)$. Since $\sup B(x) = b^x$, $b^s\le b^x$;  Since $\sup B(y) = b^y$, $b^t\le b^y$. Define a new set of all possible products $\{b^sb^t\}$ where $b^s\in B(x)$, $b^t\in B(y)$. Then, $\sup \{b^sb^t\} = b^xb^y$. Applt (b), $b^{s}b^{t}=b^{s+t}$. Notice $s+t\le x+y$, so $b^sb^t = b^{s+t}\in B(x+y)$. Therefore, $b^sb^t\le b^{x+y}$, which means $b^{x+y}$ is an upper bound of $\{b^sb^t\}$. Then, $b^xb^y\le b^{x+y}$.

Combine the two directions, $$b^{x+y} = b^xb^y$$ (QED)

### Question 7
(a) Notice that 
 
