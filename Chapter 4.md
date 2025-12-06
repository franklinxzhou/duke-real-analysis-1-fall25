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

**Thm** 4.9
Let $f$ and $g$ be complex continuous functions on a metric space $X$. Then $f+g$, $fg$, and $f/g$ are continuous on $X$.

**Thm** 4.10


