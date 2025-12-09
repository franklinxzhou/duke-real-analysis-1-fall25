Continuity

## Limits of Functions
**Def** 4.1 Limits of Functions
Let $X$ and $Y$ be metric spaces; suppose $E\subset X$, $f$ maps $E$ into $Y$, and $p$ is a limit point of $E$. We write $f(x)\rightarrow q$ as $x\rightarrow p$, or $$\lim_{x\rightarrow p}f(x)=q$$ if there is a point $q\in Y$ with the following property: For every $\epsilon>0$, $\exists$ a $\delta>0$ s.t. $$d_Y(f(x),q)<\epsilon$$ for all points $x\in E$ for which $$0<d_X(x,p)<\delta.$$
**Thm** 4.2 Let $X$, $Y$, $E$, $f$, and $p$ be as in **Def** 4.1. Then, $$\lim_{x\rightarrow p}f(x) = q$$ if and only if $$\lim_{n\rightarrow \infty} f(p_n) = q$$ for every sequence $\{p_n\}$ in $E$ s.t. $$p_n\ne p, \qquad \lim_{n\rightarrow\infty}p_n = p$$
*Proof*: Suppose $\lim_{x\rightarrow p} f(x) = q$. Fix an arbitrary $\epsilon>0$, then $\exists \delta>0$ s.t. $d_Y(f(x),q)<\epsilon$ if $x\in E$, $d_X(x,p) < \delta$. Find an arbitrary $\{p_n\}\subset E$ s.t. $p_n\ne p$, $\lim_{n\rightarrow \infty}p_n = p$. Then, $\exists N\in \mathbb{N}$ s.t. $n>N\Rightarrow d_X(p_n,p)<\delta\Rightarrow d_Y(f(p_n), q)<\epsilon$. 

Suppose $\lim_{x\rightarrow p}f(x) = q$ is not true. Then, $\exists \epsilon>0$ s.t. $\forall \delta>0$, $\exists x\in E$ for which $0< d_X(x,p)< \delta$ but $d_Y(f(x), q)\ge \epsilon$. We construct $\delta_n = 1/n$, then for each $\delta_n$, we obtain a $x$ satisfies the above condition and let $p_n = x$. For this $\{p_n\}$, $p\ne p_n$, since $d_X(p_n,p)<1/n$, $\lim_{n\rightarrow \infty} 1/n = 0$,$\lim_{n\rightarrow \infty} d_X(p_n,p) = 0\Rightarrow \lim_{n\rightarrow \infty} p_n = p$. However, $d_Y(f(p_n), q)\ge \epsilon$, making $\lim_{n\rightarrow \infty} f(p_n) = q$ false. (QED)

**Thm** 4.4
Suppose $E\subset X$, a metric space, $p$ is a limit point of $E$, $f$ and $g$ are complex functions on $E$, and $$\lim_{x\rightarrow p} f(x) = A, \qquad \lim_{x\rightarrow p} g(x) = B.$$
Then:
(a) $\displaystyle\lim_{x\rightarrow p}(f+g)(x) = A+B$;
(b) $\displaystyle\lim_{x\rightarrow p}(fg)(x) = AB$;
(c) $\displaystyle\lim_{x\rightarrow p}\left(\frac{f}{g}\right)(x) = \frac{A}{B}$, if $B\ne 0$. 

## Continuous Functions
**Def** 4.5 Continuous
Suppose $X$ and $Y$ are metric spaces, $E\subset X$, $p\in E$, and $f: E\rightarrow Y$. Then $f$ is said to be continuous at $p$ if $\forall \epsilon>0$, $\exists \delta>0$ such that $$d_Y(f(x), f(p))<\epsilon$$ for all $x\in E$ for which $d_X(x,p)<\delta$. 

**Thm** 4.6 
In the situation of **Def** 4.5, assume also that $p$ is a limit point of $E$. Then $f$ is continuous at $p$ if and only if $\lim_{x\rightarrow p}f(x) = f(p)$. 

Remark: The direction "$f$ is continuous at $p$ $\Rightarrow$ $\lim_{x\rightarrow p} f(x)=f(p)$" is basically **Def** 4.1. The direction "$f$ is continuous at $p$ $\Leftarrow$ $\lim_{x\rightarrow p} f(x)=f(p)$" is basically **Def** 4.5.

**Thm** 4.7
Suppose $X$, $Y$, $Z$ are metric spaces, $E\subset X$, $f$ maps $E$ into $Y$, $g$ maps the range of $f$, $f(E)$, into $Z$, and $h$ is the mapping of $E$ into $Z$ defined by $$h(x) = g(f(x)) \qquad (x\in E)$$
If $f$ is continuous at a point $p\in E$ and if $g$ is continuous at the point $f(p)$, then $h$ is continuous at $p$. 

*Proof*: Fix an arbitrary $\epsilon>0$. Since $g$ is continuous at $f(p)\in f(E)$, $\exists \zeta>0$ s.t. $\forall y\in f(E)$, $d_Y(y, f(p))< \zeta$ implies $d_Z(g(y), h(p))<\epsilon$.  

Using the same $\zeta$. Since $f$ is continuous at $p\in E$, $\exists \delta>0$ s.t. $\forall x\in E$, $d_X(x,p)<\delta$ implies $d_Y(f(x), f(p))< \zeta$. 

Therefore, $\forall \epsilon>0$, $\exists \delta>0$ s.t. $\forall x\in E$, $d_X(x,p)<\delta \Rightarrow d_Y(f(x), f(p))< \zeta \Rightarrow d_Z(h(x), h(p))< \epsilon$. This proves that $h$ is continuous at $p$. (QED)

**Thm** 4.8
A mapping $f$ of a metric space $X$ into a metric space $Y$ is continuous on $X$ if and only if $f^{-1}(V)$ is open in $X$ for every open set $V$ in $Y$. 

*Proof*: Suppose $f^{-1}(V)$ is open in $X$ for every open set $V$ in $Y$. Fix an arbitrary $p\in X$, s.t. $f(p)\in Y$. Then, fix an arbitrary $\epsilon>0$, let the open ball $B_\epsilon(f(p))\subset Y$ be an example of an open set in $Y$. Then, $f^{-1}(B_\epsilon(f(p)))$ is open. By the definition of openness, $\forall x\in f^{-1}(B_\epsilon(f(p)))$, $\exists \delta >0$, $B_\delta(x)\subset f^{-1}(B_\epsilon(f(p)))$. Hence, $\exists \delta>0$, $\forall x$, $d_X(x,f^{-1}(f(p))) = d_X(x,p)< \delta$ implies $x\in B_\delta(x)$. This follows that $x\in f^{-1}(B_\epsilon(y))$ and $f(x)\in B_\epsilon(f(p))$. This implies that $d_Y(f(x), f(p))<\epsilon$, so $f$ is continuous on $f^{-1}(B_\epsilon(y))$. 

Suppose $f$ is continuous. Fix an arbitrary open set $V\subset Y$. Find an arbitrary $p\in f^{-1}(V)$, then $f(p)\in V$. Since $V$ is open, $\exists \epsilon>0$ s.t. $B_\epsilon(f(p))\subset V$. Since $f$ is continuous at $p$, for this $\epsilon$, $\exists$ a $\delta>0$ s.t. if $d_X(x,p)<\delta$, then $d_Y(f(x), f(p))<\epsilon$. This follows that $f(B_\delta(p))\subset B_\epsilon(f(p))$. We have known that $B_\epsilon(f(p))\subset V$, so $f(B_\delta(p))\subset V$. This follows $B_\delta(p)\subset f^{-1}(V)$. Therefore, $f^{-1}(V)$ is an open set. (QED)

One equivalent form of **Thm** 4.8 is:
**Corr** of **Thm** 4.8
A mapping $f$ of a metric space $X$ into a metric space $Y$ is continuous if and only if $f^{-1}(C)$ is closed in $X$ for every closed set $C$ in $Y$. 

**Thm** 4.9
Let $f$ and $g$ be complex continuous functions on a metric space $X$. Then $f+g$, $fg$, and $f/g$ are continuous on $X$.

**Thm** 4.10
(a) Let $f_1, \dots, f_k$ be real functions on a metric space $X$, and let $\mathbf{f}$ be the mapping of $X$ into $\mathbb{R}^k$ defined by $$\mathbf{f}(x) = (f_1(x), \dots, f_k(x))\qquad (x\in X)$$
then $\mathbf{f}$ is continuous if and only if each of the functions $f_1, \dots, f_k$ is continuous. 
(b) If $\mathbf{f}$ and $\mathbf{g}$ are continuous mappings of $X$ into $\mathbb{R}^k$, then $\mathbf{f}+\mathbf{g}$ and $\mathbf{f}\cdot \mathbf{g}$ are continuous on $X$. 

*Remark*: The part (a) extends the concepts to the vector world and part (b) is an extension of **Thm** 4.9 for vector-valued functions. 

## Continuity and Compactness; Uniform Continuity
**Def** 4.13 Bounded
A mapping $\mathbf{f}: E\to \mathbb{R}^k$ is said to be *bounded* if $\exists M\in \mathbb{R}$ s.t. $|\mathbf{f}(x)|\le M$, $\forall x\in E$. 

**Thm** 4.14 Continuity preserves compactness
Suppose $f$ is a continuous mapping of a compact metric space $X$ into a metric space $Y$. Then $f(X)$ is compact. 

*Proof*: We want to show that $f(X)$ is compact. Then, we discuss its open cover $\{\mathscr{O}_n\}$. We are very much aware that, due to **Thm** 4.8, $\{f^{-1}(\mathscr{O}_n)\}$ is a set of open sets. What is more, $$f(X) \subset \bigcup_n \mathscr{O}_n$$
This follows that $$X\subset f^{-1}\left(\bigcup_n \mathscr{O}_n\right) = \bigcup_n f^{-1}(\mathscr{O}_n)$$
At this stage, we should declare that $\{f^{-1}(\mathscr{O}_n)\}$ is an open cover of $X$. Due to compactness of $X$, it admits a subcover $\{f^{-1}(\mathscr{O}_{n_k})\}_{k=1}^m$. This follows $$f(X)\subset f\left(\bigcup_{k=1}^m f^{-1}(\mathscr{O}_{n_k})\right)\subset \bigcup_{k=1}^m \mathscr{O}_{n_k}$$
This means the open cover of $f(X)$ admits a finite subcover, so $f(X)$ is compact.

**Thm** 4.15 Heine Borel Theorem $\times$ Continuity
If $\mathbf{f}$ is a continuous mapping of a compact metric space $X$ into $\mathbb{R}^k$, then $\mathbf{f}(X)$ is closed and bounded. Thus, $\mathbf{f}$ is bounded. 

**Thm** 4.16 Extreme Value Theorem
Suppose $f$ is a continuous real function on a compact metric space $X$, and $$M = \sup_{p\in X} f(p), \qquad m = \inf_{p\in X}f(p)$$ Then $\exists$ points $p,q\in X$ s.t. $f(p) = M$ and $f(q) = m$. 

*Proof roadmap*: Since $X$ is compact, by **Thm** 4.14, $f(X)$ is compact. By Heine-Borel Theorem (**Thm** 2.41), $f(X)$ is closed and bounded. Therefore, $f(X)$ contains its supremum and infimum. 

**Thm** 4.17 Continuous, bijective $f: X$ compact $\to Y$ implies continuous $f^{-1}$
*The original Rudin text is so old-school and confusing to me, so this is a modern way of saying this:*
Suppose continuous, bijective $f: X\to Y$, where $X$ is compact, then the inverse mapping $f^{-1}$ defined on $Y$ by $$f^{-1}(f(x)) = x, \qquad x\in X$$ is continuous. 

*Proof*: With the **Corr** of **Thm** 4.8, for all $C\subset X$ closed, if $f(C) = f^{-1}(f^{-1})(C)$ is closed, then $f^{-1}$ is continuous. Therefore, it is sufficient to show $f(C)$ is closed in $Y$. Since $C$ is a closed set in a compact set $X$, according to **Thm** 2.35, $C$ is compact. Then, according to **Thm** 4.14, $f(C)$ is compact. Lastly, using Heine-Borel/**Thm** 2.41, $f(C)$ is closed. Therefore, the inverse mapping $f^{-1}$ is continuous. (QED)

**Def** 4.18 Uniform continuity
Let $f$ be a mapping of a metric space $X$ into a metric space $Y$. We say that $f$ is *uniformly continuous* on $X$ if $\forall \epsilon>0$, $\exists \delta>0$, s.t. $$d_Y(f(p), f(q))<\epsilon$$ for all $p$ and $q$ in $X$ for which $d_X(p,q)<\delta$. 

*Remark*: Continuity vs. uniform continuity
1. While continuity can be defined for a specific point $p$, uniform continuity is a property of a function. 
2. If $f$ is continuous, for each $\epsilon>0$, we find a $\delta>0$ that is dependent on $\epsilon$ and a particular $p\in X$; if $f$ is uniformly continuous, for each $\epsilon>0$, we find a $\delta>0$ that *only depends on* $\epsilon$ and will work $\forall p\in X$.
3. Uniform continuity $\Rightarrow$ Continuity.

**Thm** 4.19 Continuity on compact metric space $\Rightarrow$ uniform continuity
Let $f$ be a continuous mapping of a compact metric space $X$ and a metric space $Y$. Then $f$ is uniformly continuous on $X$.

*Proof*: Fix an arbitrary $\epsilon>0$, since $f$ is continuous, choose $\delta(p)$ for each $p\in X$ s.t. if $q\in B_{\delta(p)}(p)$, then $f(q)\in B_\epsilon(f(p))$. Let's now shift our focus onto open balls with half the parameter, $\delta(p)/2$. Notice that the set of open balls $\{B_{\delta(p)/2}(p)\}$ is an open cover of $X$. $$X \subset \bigcup_{p\in X}B_{\delta(p)/2}(p)$$
Since $X$ is compact, this open set admits a finite subset. We therefore, obtain a finite sequence $\{p_n\}_{n=1}^m$ such that $$X\subset \bigcup_{n=1}^m B_{\delta(p_n)/2}(p)$$
With finiteness, we can choose $\delta = \frac{1}{2}\inf_{p}\delta(p_n)$. Choose two points $p,q\in X$ s.t. $d_X(p,q)<\delta < \delta(p_n)/2$, $\forall n$. Assume for some $k$, $d_X(p,p_k)< \delta(p_k)/2 < \delta(p_k)$, then we wonder if it is possible to put $q$ into the same ball: It turns out that while it is unsure if we have a full-delta ball containing $p,q$, as $$d_X(q,p_k)\le d_X(p,q) + d_X(p,p_k)< \delta(p_k)$$
With $d_X(p,p_k)<\delta(p_k)$, $$d_Y(f(p), f(p_k))<\epsilon$$
With $d_Y(q,p_k)<\delta(p_k)$, $$d_Y(f(q), f(p_k))<\epsilon$$
This follows $$d_Y(f(p), f(q))\le d_Y(f(p), f(p_k)) + d_Y(f(q), f(p_k)) < 2\epsilon,$$ so $f$ is uniformly continuous on $X$. (QED)

**Thm** 4.20
Let $E$ be a noncompact set in $\mathbb{R}$. Then,
(a) there exists a continuous function on $E$ which is not bounded;
(b) there exists a continuous and bounded function on $E$ which has no maximum. 
If, in addition, $E$ is bounded, then 
(c) there exists a continuous function on $E$ which is not uniformly continuous. 

*Example*: 
(a) Consider $$f(x) = \frac{1}{x-x_0} \qquad (x\in E)$$
Let $x_0$ be a limit point of $E$ that is not in $E$. It is continuous, but the value of the function explodes toward infinity around the missing point $x_0$. 

(b) Consider $$g(x) = \frac{1}{1+(x-x_0)^2} \qquad (x\in E),$$ a function with a "bell curve" shape centered at the missing point $x_0\notin E$. 

It is continuous, bounded ($0<g(x)<1$). However, it does not attain its maximum, as $$\sup_{x\in E}g(x) = 1.$$
(c) Consider $$h(x) = \frac{x^2}{x^2+1}$$ where $E$ is a bounded set. Therefore, $h(x)$ is continuous, but it never has the chance to attain its maximum as $h(x)<1$ for all bounded $E$. 

## Continuity and Connectedness

**Thm** 4.22 Continuity Preserves Connectedness
If $f$ is a continuous mapping of a metric space $X$ into a metric space $Y$, and if $E$ is a connected subset of $X$, then $f(E)$ is connected.

**Remark** If $f: X\rightarrow Y$ is continuous and surjective, where $X$ is connected, then $Y$ is connected. 

*I personally don't like the $\sqcup$ sign, but this is how the professor started it in the lecture.*

*Proof*: Assume, BWOC, that it is not connected. Then, $\exists Y_1, Y_2$ both open and nonempty, $Y = Y_1\sqcup Y_2$. Then, notice that $f^{-1}(Y_1)$ and $f^{-1}(Y_2)$ also open. Since $Y_1\cap Y_2 = \varnothing$, we claim that $f^{-1}(Y_1)\cap f^{-1}(Y_2) = \varnothing$: If otherwise, $\exists x\in f^{-1}(Y_1)\cap f^{-1}(Y_2)$, then $f(x)\in Y_1$ and $f(x) \in Y_2$, then $f(x)\in Y_1\cap Y_2\ne \varnothing$. Since $Y_1, Y_2$ are both nonempty, their preimages must also be nonempty. $\forall y\in Y$, since the mapping is surjective, $\exists x\in X$, $f(x) =y$. Notice that $$f^{-1}(Y_1) \cup f^{-1}(Y_2) = f^{-1}(Y_1 \cup Y_2) = f^{-1}(Y) = X,$$so $X$ is covered by $f^{-1}(Y_1)\cup f^{-1}(Y_2)$. This makes $X$ disconnected. $\Rightarrow \Leftarrow$ (QED)

**Thm** 4.23 Intermediate Value Theorem (IVT)
Let $f$ be a continuous real function on the interval $[a,b]$. If $f(a)<f(b)$ and if $c$ is a number s.t. $f(a)<c<f(b)$, then there exists a point $x\in (a,b)$ s.t. $f(x)=c$. 

*Remark*: As we know, closed interval on $\mathbb{R}$ is connected. Then, this is a direct result of **Thm** 4.22.
## Discontinuities

**Def** 4.25 Upper and Lower bound
Let $f$ be defined on $(a,b)$. Consider any point $x$ s.t. $a\le x<b$, we write $$f(x^+) = q$$ if $f(t_n)\to q$ as $n\to \infty$, for all sequences $\{t_n\}$ in $(x,b)$ such that $t_n\to x$. 

Consider any point $x$ s.t. $a < x\le b$, we write $$f(x^-) = p$$ if $f(t_n)\to p$ as $n\to \infty$, for all sequences $\{t_n\}$ in $(a,x)$ such that $t_n\to x$. 

**Def** 4.26 Discontinuity
Let $f$ be defined on $(a,b)$. If $f$ is discontinuous at a point $x$, and if $f(x^+)$ and $f(x^-)$ exist, then $f$ is said to have a discontinuity of the *first kind*, or *simple discontinuity*, at $x$; this simple discontinuity is in the form of either $f(x^+) \ne f(x^-)$, with $f(x)$ undefined, or $f(x^+)=f(x^-)\ne f(x)$. Otherwise the discontinuity is said to be of *second kind*.

**Example** Let $$f(x) = \begin{cases} -1 & \text{ if }x<0\\ 1 & \text{ if }x>0 \\ \pi & \text{ if }x=0\end{cases}$$ Then, $$\lim_{t\rightarrow 0^+}f(t) = 1$$ $$\lim_{t\rightarrow 0^-}f(t) = -1$$ Sometimes we write $$f(x^+) = \lim_{t\rightarrow x^+}f(t)$$ $$f(x^-) = \lim_{t\rightarrow x^-}f(t)$$ and say $f$ is upper continuous at $x$ if $f(x^+)$ exists and is equal to $f(x)$.

**Example** Let $$f(x) = \begin{cases} 1 & \text{ if }x\text{ rational}\\ 0 &\text{ otherwise}\end{cases}$$ then $f(x)$ is not upper or lower continuous at any point. 

**Example** Let $$f(x) = \begin{cases} x & \text{ if }x\text{ rational}\\ 0 &\text{ otherwise}\end{cases}$$ is continuous at $x = 0$, discontinuous at every other point. 

Piecewise linear functions have upper and lower limits at every point. $$(a,b) = (a,a_1)\sqcup\{a_1\}\sqcup(a_1, a_2)\sqcup\{a_2\}\sqcup\dots$$ ask that $f\mid_{(a_i, a_{i+1})}$ is linear $\forall i$. 
## Monotonic Functions

**Def** 4.28 Monotonically increasing/decreasing
Let $f$ be real on $(a,b)$. Then $f$ is said to be *monotonically increasing* on $(a,b)$ if $a<x<y<b$ implies $f(x)\le f(y)$. 

**Thm** 4.29
Let $f$ be monotonically increasing on $(a,b)$. Then $f(x^+)$ and $f(x^-)$ exist at every point of $x\in (a,b)$. More precisely, $$\sup_{a<t<x} f(t) = f(x^-) \le f(x) \le f(x^+) = \inf_{x<t<b} f(t)$$
Furthermore, if $a<x<y<b$, then $$f(x^+)\le f(y^-)$$
*Proof*:

**Thm** 4.30
Let $f$ be monotonic on $(a,b)$. Then the set of points of $(a,b)$ at which $f$ is discontinuous is at most countable.

*Proof*:

The last section of the chapter, *Infinite Limits and Limits at Infinity*, is more or less in place to ensure the rigor of the language.

## Exercises
### Question 1
Consider $$f(x) = \begin{cases} 1 & x\in \mathbb{Q}\\ 0 & x\notin \mathbb{Q}\end{cases}$$ This function shouts "NO".

### Question 2
If $y\in f(\overline{E})$, then $\exists p\in X$ s.t. $y=f(p)$. $p\in \overline{E}$. Since $\overline{E} = E\cup E'$, if $p\in E$, then $y\in f(E)\subset \overline{f(E)}$. If $p\in E'$, fix an arbitrary $\epsilon>0$: $\exists \delta>0$, $\exists x_0\in E$ s.t. $x_0\in B_\delta(p)$. This implies $\exists f(x_0)\in f(E)$ s.t. $f(x_0)\in B_\epsilon(y)$. Then, $y\in (f(E))'\subset \overline{f(E)}$.

### Question 3
$Z(f) = f^{-1}(\{0\})$. Proof done by **Corr** of **Thm** 4.8. 

### Question 4
(Question 2, Homework 4)
For the first conclusion, since $E$ is a dense subset of $X$, $\forall x\in X$, either $x\in E$ or $x$ is a limit point of $E$. In the former case, $f(x)\in f(E)$. In the latter case, $\exists x'\in E$, $x'\neq x$, such that $x'\in B_\delta(x)$. As $f$ is continuous, $f(x')\in B_\epsilon(f(x))$. Notice that $f(x')\in f(E)$, so $f(x)\in (f(E))'$. To sum up, $\forall y\in f(X)$, either $y\in f(E)$ or $y$ is a limit point of $f(E)$.

For the second conclusion, since $E$ is dense in $X$, for this $p$, either $p\in E$ or $p$ is a limit point of $E$. In the former case, $g(p)=f(p)$ still holds. In the latter case, fix an arbitrary $\epsilon>0$, then $\exists \delta_1 >0$, $x\in B_{\delta_1}(p)$ implies $f(x)\in B_\epsilon(f(p))$; $\exists \delta_2 >0$, $x\in B_{\delta_2}(p)$ implies $f(x)\in B_\epsilon(f(p))$. Let $\delta = \min\{\delta_1, \delta_2\}$. With the definition of a limit point, we can always find $x_0\in B_\delta(p)\cap E$. Then, $f(x_0)\in B_\epsilon(f(p))$. With a similar argument, $g(x_0) \in B_\epsilon(g(p))$. Notice $f(x_0) = g(x_0)$, then $d_Y(f(x_0), g(x_0)) = 0$. Also, $d_Y(f(p), f(x_0))<\epsilon$, $d_Y(g(p), g(x_0))<\epsilon$. This follows that $$d_Y(f(p), g(p)) \le d_Y(f(p), f(x)) + d_Y(f(x), g(x)) + d_Y(g(x), g(p))<2\epsilon$$
Since $\epsilon$ is arbitrary, $g(p) = f(p)$ if $p$ is a limit point of $X$. 

### Question 5
(Question 2, Homework 5)
We firstly prove the existence of such a function.

If $E$ is a closed subset of $\mathbb{R}$, then $\mathbb{R} - E$ is open. According to Exercise 29 in Chapter 2, every open set in $\mathbb{R}$ is the union of an at most countable collection of disjoint segments.
$$\mathbb{R} - E = \bigcup_{n\in \mathbb{N}}(a_n, b_n),$$
where the boundary points $a_n$, $b_n$ are guaranteed to be in $E$ because $E$ is closed and $\mathbb{R} - E$ is not closed.

Now, I can apply the idea of interpolation,
$$g(x) = \begin{cases}
    f(x) & x\in E\\
    f(a_n)+\frac{f(b_n) - f(a_n)}{b_n - a_n} & x\in (a_n, b_n), \text{ where }\lvert a_n\rvert <\infty, \lvert b_n\rvert<\infty\\
    f(b_n) & x\in (a_n, b_n), \text{ where }a_n = - \infty, \lvert b_n\rvert<\infty\\
    f(a_n) & x\in (a_n, b_n), \text{ where }\lvert a_n\rvert <\infty, b_n = \infty\\
\end{cases}$$

On $E$, $g(x)$ is continuous because as $f(x)$ is continuous, $\forall \epsilon>0$, $\exists \delta>0$ such that $\lvert x - x'\rvert <\delta$ implies $\lvert f(x) - f(x')\rvert <\epsilon$. One more step, this in turn implies that $\lvert g(x) - g(x')\rvert < \epsilon$. 

The reason that $g$ is continuous is that it is continuous on $E$, linear functions are continuous on their respective segments, and all segments have boundary values matched. 

Then, to consider the case of an open $E$, we raise the following counterexample. Let 
$$f(x) = \frac{1}{x}$$
defined on the open $E = (-\infty, 0)\cup (0,\infty)$. It is impossible, as $$\lim_{x\rightarrow 0^-}f(x) = -\infty$$
and 
$$\lim_{x\rightarrow 0^+}f(x) = \infty,$$
to find some continuous $g(x)$ no matter how we define $g(0)$. From another perspective, the segments cannot have the boundary values matched.

Therefore, the result is false without requiring a closed $E$.

All the discussion above are based on real-valued functions. For vector-valued functions, the proof is straightforward because a vector-valued function is continuous if and only if its components are all continuous. 

### Question 6
Suppose that $f$ is continuous on $E$. Since $E$ is compact, it is also bounded and closed, so $\exists M_1\in \mathbb{R}$, $$|x|\le M_1, \qquad \forall x\in E.$$On a compact set $E$, if $f$ is continuous on $E$, then $f(E)$ is closed and bounded (**Thm** 4.15). This follows that $\exists M_2\in \mathbb{R}$,  $$|f(x)|\le M_2, \qquad \forall f(x)\in f(E).$$
In light of that, the euclidean norm of a point $(x,f(x))$ is $$\lVert (x,f(x))\rVert = \sqrt{x^2+(f(x))^2}\le \sqrt{M_1^2+M_2^2},$$ which shows that the graph is bounded. 

Next, we want to show it is closed. Suppose that $(x_0, y_0)$ is an arbitrary limit point, to which a sequence of points $\{(x_n, f(x_n))\}$ converges. Since $E$ is compact, $x_0\in E$. Then, piecewise, $x_n\to x_0$, $f(x_n)\to y_0$. We fix an arbitrary $\epsilon>0$, then $\exists \delta >0$, $$|x_n - x_0|<\delta \Rightarrow |f(x_n) - f(x_0)|<\epsilon.$$
Notice that for this $\delta$, $\exists N_1\in \mathbb{N}$, $n>N_1$ implies $|x_n - x_0|<\delta$. Then, $$n>N_1\Rightarrow |f(x_n) - f(x_0)|<\epsilon.$$
Meanwhile, $\exists N_2\in \mathbb{N}$, $$n>N_2\Rightarrow |f(x_n) - y_0|<\epsilon.$$
Owing to the uniqueness of limit for the sequence $\{f(x_n)\}$, $y = f(x_0)$. This follows the arbitrary limit point $(x_0, f(x_0))\in (E, f(E))$, then the graph is closed. 

Therefore, the graph is compact.

Suppose that f(x) is not continuous at some particular $x_0\in E$, and assume, BWOC, that the graph is still compact. Construct a sequence of points $\{P_n\}$, where $P_n = (x_n, f(x_n))$ on the graph and $x_n\to x_0$, but $\exists \epsilon>0$, $|f(x_n) - f(x_0)|\ge \epsilon$ for all $n$. Since the graph is compact, it is closed, so $\exists$ a subsequence of $\{P_n\}$, say $\{P_{n_k}\}$, that converges to some $(x_0, f(x_0))$ in the graph (as $x_n\to x_0$). As part of $\{P_n\}$, $|f(x_n) - f(x_0)|\ge \epsilon$; however, since $f(x_{n_k})\to f(x_0)$, for this $\epsilon$, $\exists N\in \mathbb{N}$ s.t. $k>N$ implies $|f(x_n) - f(x_0)|<\epsilon$. $\Rightarrow \Leftarrow$.

### Question 7
First, we prove that $f$ is bounded on $\mathbb{R}^2$. Notice that $$(|x| - y^2)^2\ge 0$$ $$x^2 - 2|x|y^2 + y^4 \ge 0$$ $$\frac{|x|y^2}{x^2+y^4}\le \frac{1}{2}$$
Second, we assess the behavior of $f$ and $g$ around (0,0): For $g$, to balance the powers in the denominator, substitute $x=y^3$ into $g(x,y)$: $$g(y^3, y) = \frac{(y^3)(y^2)}{(y^3)^2+y^6} = \frac{1}{2y}$$ As $y\to 0$, $g\to \infty$. Then, it is clearly not continuous around $(0,0)$.

For $f$, to balance the powers in the denominator, substitute $x=y^2$ into $f(x,y)$: $$f(y^2,y) = \frac{(y^2)(y^2)}{(y^2)^2+y^4} = \frac{1}{2}$$ Along this path, $f(x,y)\to 1/2$, but $f(0,0) = 0$, so $f$ is not continuous around $(0,0)$.

The restriction of $f$ to an arbitrary straight line on $\mathbb{R}^2$, provided the line is represented as $x = ay$, $a\in \mathbb{R}$ (notice it needs to pass through the origin), is $$f(ay,y) = \frac{(ay)(y^2)}{(ay)^2+y^4}$$
As $y\to 0$, $$\lim_{y\to 0}f(ay) = \lim_{y\to 0} \frac{0}{y} = 0,$$ which proves that the restriction of $f$ to any straight line is continuous in the neighborhood of $(0,0)$.

The restriction of $g$ to an arbitrary straight line on $\mathbb{R}^2$, provided the line is represented as $x = ay$, $a\in \mathbb{R}$, is $$g(ay, y) = \frac{(ay)(y^2)}{(ay)^2+y^6}$$
As $y\to 0$, $$\lim_{y\to 0} g(ay) = \lim_{y\to 0}\frac{0}{y^3} = 0,$$ which proves that the restriction of $g$ to any straight line is continuous in the neighborhood of $(0,0)$.

### Question 8
(Idea of [Amit Rajaraman](https://math.stackexchange.com/users/447210/amit-rajaraman) on Math Stack Exchange)

Assume, BWOC, that $f$ is not bounded. WLOG, assume that it is not bounded above. Then, $\forall n\in \mathbb{N}$, $\exists x_n\in E$ s.t. $f(x_n)>n$. Also notice that since $E$ is bounded, there is a convergent subsequence of $\{x_n\}$, denoted as $\{x_{n_k}\}$. This subsequence is therefore, Cauchy, so $\forall \delta>0$, $\exists N\in \mathbb{N}$ s.t. $r,s\ge N$ implies $|x_{n_r} - x_{n_s}| <\delta$.

In the meantime, $f$ is uniformly continuous. Then, for $\epsilon = 1$, $\exists \delta>0$ s.t. $\forall x_n$ in the sequence described above, $$|x_{n_r} - x_{n_s}|<\delta \quad \Rightarrow \quad |f(x_{n_r}) - f(x_{n_s})|< 1$$
Now, fix a specific index $j>N$, $\forall k>j$, $$|f(x_{n_k}) - f(x_{n_j})|<1$$ This implies $$f(x_{n_k})<f(x_{n_j}) + 1;$$ i.e., $\{f(x_{n_k})\}_{k>j}$ is bounded by $f(x_{n_j})+1$. Notice that $f(x_{n_k})>n_k$, which goes to infinity. $\Rightarrow\Leftarrow$.

If the condition of bounded $E$ is omitted, then the above proof will fail because it is not guaranteed that $\{x_{n_k}\}$ is convergent/Cauchy.

### Question 9
We can prove that To every $\epsilon>0$ there exists a $\delta>0$ such that $\mathrm{diam} f(E)<\epsilon$ for all $E\subset X$ with $\mathrm{diam} E<\delta$ $\Leftrightarrow$ **Def** 4.18.

Suppose the new condition holds. Fix an arbitrary $\epsilon>0$, then $\exists$ a corresponding $\delta>0$. For any arbitrary $E\subset X$ with $\mathrm{diam} E<\delta$, $$\sup_{p,q\in E}d_X(p,q)<\delta.$$ Then, we can find $x,y\in E$ s.t. $d_X(x,y)<\delta$. This results in $\mathrm{diam} f(E)<\epsilon$, which means $$\sup_{p,q\in E}d_Y(f(p), f(q))<\epsilon.$$ For our $x,y\in E$, $d_Y(f(x), f(y))<\epsilon$. 

Therefore, $\forall \epsilon>0$, $\exists \delta >0$, $d_Y(f(x),f(y))<\epsilon$ whenever $d_X(x,y)<\delta$, $x,y\in E$. This is **Def** 4.18. 

Suppose **Def** 4.18 holds. Fix an arbitrary $\epsilon>0$. Then, we choose some $0< \zeta < \epsilon$, $\exists \delta>0$, so that $d_X(x,y)<\delta$ implies $d_Y(f(x), f(y))<\zeta$. Under this scenario, in any subset $E\subset X$, if $\mathrm{diam} E<\delta$, $\forall p,q\in E$, $d_X(p,q)<\delta$. This follows $d_Y(f(p), f(q))<\zeta$, so $\sup \{d_Y(f(p), f(q)): p,q\in E\} \le \zeta < \epsilon$. This is equivalent to say, $\mathrm{diam} f(E) < \epsilon$. Thus, the condition in this question holds.
### Question 10
Assume, BWOC, that $f$ is not uniformly continuous. Construct $\{p_n\}$, $\{q_n\}$. **Thm** 2.37 guarantees, based on the compactness of $X$, that $\exists p,q\in X$, $p_n\to p$, $q_n\to q$. 

We construct $d_X(p_n, q_n)\to 0$. 

By definition of convergence, $\forall \delta>0$, $\exists N_1\in \mathbb{N}$ s.t. $n\ge N_1$ implies $d_X(p_n, q_n)< \delta/3$; $\exists N_2\in \mathbb{N}$ s.t. $n\ge N_2$ implies $d_X(p_n, p)<\delta/3$; $\exists N_3\in \mathbb{N}$ s.t. $n\ge N_3$ implies $d_X(q_n, p)<\delta/3$. By the triangle inequality, $$d_X(p,q) \le d_X(p,p_n) + d_X(p_n, q_n) + d_X(q_n,q)<\delta$$ Since $\delta$ is arbitrary, as $n\to \infty$, $d_X(p,q)=0$. We therefore have $p=q$. 

Following this, let $r\in Y$, then **Thm** 4.2 says $f(p_n)\to r$, $f(q_n)\to r$. $$d_Y(f(p_n), f(q_n))\le d_Y(f(p_n), r) + d_Y(f(q_n), r)$$ In the same way of using the triangle inequality, $d_Y(f(p_n), f(q_n))\to 0$. 

A direct result of non-uniform continuity is that $\exists \epsilon>0$, when $d_X(p_n, q_n)\to 0$, $d_Y(f(p_n), f(q_n))>\epsilon$. $\Rightarrow\Leftarrow$
### Question 11
Suppose $f$ is uniformly continuous. Then, fix an arbitrary $\epsilon>0$, $\exists \delta>0$ s.t. $x,y\in X$ and $d_X(x,y)<\delta$ implies $d_Y(f(x), f(y))<\epsilon$. For this $\delta$, since $\{x_n\}\subset X$ is Cauchy, $\exists N\in \mathbb{N}$ s.t. $m,n>N$, $m,n\in \mathbb{N}$ implies $d_X(x_m, x_n)<\delta$. Then, this implies that $d_Y(f(x_m), f(x_n))<\epsilon$. Restating the logic flow, $\exists N\in \mathbb{N}$ s.t. $m,n>N$, $m,n\in \mathbb{N}$ implies $d_Y(f(x_m), f(x_n))<\epsilon$. Thus, $\{f(x_n)\}$ is a Cauchy sequence.
### Question 12
*Statement*: If $g: X\to Y$ and $f: Y\to Z$ are both uniformly continuous, then $h: X\to Z$, where $h(x) = f(g(x))$, is uniformly continuous. 
*Proof*: Since $f$ is uniformly continuous, then fix an arbitrary $\zeta>0$, $\exists \epsilon>0$ s.t. $y_1, y_2\in Y$, $d_Y(y_1, y_2)<\epsilon$ implies $d_Z(f(y_1), f(y_2))<\zeta$. Since $g$ is uniformly continuous, then to make $d_Y(y_1, y_2)<\epsilon$, $\exists \delta>0$, we need $d_X(x_1, x_2)<\delta$, $x_1, x_2\in X$, $y_1 = f(x_1)$, $y_2 = f(x_2)$. 

Therefore, $\forall \zeta>0$, $\exists \delta>0$, $x_1, x_2\in X$, $d_X(x_1,x_2)<\delta$ implies $d_Z(f(g(x_1)), f(g(x_2))) = d_Z(h(x_1), h(x_2))$. This proves that $h$ is uniformly continuous.

### Question 13
Following the hint, for each $p\in X$ and each $n\in \mathbb{N}$, let $V_n(p) = \{q\in E: q\in B_{1/n}(p)\}$. Under this construction, the diameter of the domain sets is very small. $$\mathrm{diam}(V_n(p))\le \frac{2}{n}$$ $$\mathrm{diam}(V_n(p))\to 0$$
 Since $f$ is uniformly continuous, **Exercise 9** says that $$\mathrm{diam}(f(V_n(p)))\to 0.$$
 Notice that $\overline{f(Y_n(p))}$ shares the diameter with $f(V_n(p))$ and if $\mathrm{diam}\left(\overline{f(V_n(p))}\right)\to 0$, there is only one single point in the intersection (**Thm** 3.10). Let's denote this point as $g(p)$. 

  Next, I will show that $g(p)$ is continuous. Fix an arbitrary $\epsilon>0$, then since $f$ is uniformly continuous, $\exists \delta>0$ s.t. $\forall x,y\in E$, $d_X(x,y)<\delta$ implies $d_Y(f(x), f(y))<\epsilon/3$. We find $p,q$ with $d_X(p,q)<\delta$. Then, as $x\to p$, $g(p)$ is the limit of $f(x)$; as $y\to q$, $g(q)$ is the limit of $f(y)$. Fix $x,y\in E$ s.t. $d_X(x,p)<\delta$, $d_X(y,q)<\delta$, $d_X(x,y)< \delta$. Then, we have $d_Y(f(x), g(p))< \epsilon/3$, $d_Y(f(y), g(q))<\epsilon/3$. Then, $$d_Y(g(p), g(q))\le d_Y(g(p), f(x))| + d_Y(f(x), f(y) + d_Y(f(y), g(q)))<\epsilon.$$
  This follows that $g(p)$ is continuous. Notice that $g(p)$ is defined as the intersection of the closures, it must cover the rest of $X$. Also, $$g(p) = f(p)$$ whenever $p\in E$. It is hence a valid continuous extension of $f$. 

### Question 14
(Question 3, Hom. work 5)
Let $g(x) = f(x) - x$. Then, we check for the signs of the values at $x=0$ and $x=1$.
$$g(0) = f(0) - 0$$

Since $f(0)\in I$, $f(0)\geq 0$, so $g(0)\geq 0$.

$$g(1) = f(1) - 1$$

Since $f(1)\in I$, $f(1)\leq 1$, so $g(1)\leq 0$.

Therefore, with $g(0) \geq 0$ and $g(1)\leq 0$, $0\in [g(1), g(0)]$. Apply **Thm** 4.23 (Intermediate Value Theorem), since $0\in [g(1), g(0)]$, $\exists x\in (0,1)$ such that $g(x) = 0$. Equivalently, this $x\in I$ makes $f(x) = x$.
### Question 15
(Question 4, Homework 5)
We approach this question by proving the contrapositive. Suppose $f: \mathbb{R}\rightarrow \mathbb{R}$ is not monotonic. Then, $\exists x_1, x_2, \Delta\in \mathbb{R}$, $\Delta>0$, 
$$f(x_1)>f(x_1+\Delta)$$
$$f(x_2)<f(x_2+\Delta)$$

Without the loss of generality, assume that $x_1<x_2$. The case of $x_1>x_2$ is similar.

Now, we have defined a compact subset $[x_1, x_2+\Delta]\subset \mathbb{R}$. We can apply Rudin theorem 4.16, 
$$m = \inf_{x\in[x_1,x_2+\Delta]}f(x),$$
then there exists $p\in [x_1,x_2+\Delta]$ such that $m = f(p)$. Observe that $p\neq x_2+\Delta$ nor $p\neq x_1$. Therefore, $p\in (x_1, x_2+\Delta)$, an open set. 
$$f(p) = \inf_{x\in(x_1,x_2+\Delta)}f(x)$$

Now we discuss if $f((x_1,x_2+\Delta))$ is an open set. Centered at $f(p)$, find a neighborhood $B_\epsilon(f(p))$. Clearly, for some elements $q\in B_\epsilon(f(p))$, $q<f(p)$. Thus, $q\notin f((x_1,x_2+\Delta))$. 

This negates that $f((x_1,x_2+\Delta))$ is an open set, and further negates that $f$ is an open mapping. 

Therefore, every continuous open mapping of $\mathbb{R}\rightarrow \mathbb{R}$ is monotonic.
### Question 16
$[x]$: Both $f(n^+)=n$ and $f(n^-)=n-1$ exist, so discontinuity of the first kind.
$(x)$: Both $f(n^+) = 0$ and $f(n^-) = 1$ exist, so discontinuity of the first kind.

### Question 17

### Question 18

### Question 19

### Question 20

### Question 21
(Question 5, Homework 5)

### Question 22

### Question 23
(Question 6, Homework 5)

### Question 24

### Question 25
(Question 7, Homework 5)

### Question 26
