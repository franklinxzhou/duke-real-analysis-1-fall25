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

