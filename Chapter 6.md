The Riemann-Stieltjes Integral
## Definition and Existence of the Integral
**Def** 6.1 Partition; Upper and Lower Riemann Integrals
Let $[a,b]$ be a given interval. By a *partition* $P$ of $[a,b]$ we mean a finite set of points $x_0, x_1, \dots, x_n$, where $$a = x_0\le x_1 \le \dots \le x_{n-1} \le x_n = b$$
We write $\Delta x_i = x_i - x_{i-1}$, $i = 1, \dots, n$. Suppose $f$ is a bounded real function defined on $[a,b]$. Corresponding to each partition $P$ of $[a,b]$ we put $$M_i = \sup f(x) \qquad x_{i-1}\le x \le x_i$$ $$m_i = \inf f(x) \qquad x_{i-1}\le x \le x_i$$
$$U(P,f) = \sum_{i=1}^n M_i\Delta x_i,$$ $$L(P,f) = \sum_{i=1}^n m_i\Delta x_i$$ and finally $$\overline{\int_a^b} f\,dx = \inf U(P,f),$$ $$\underline{\int_a^b}f\,dx = \sup L(P,f).$$
The two integrals are called the *upper* and *lower Riemann integrals* of $f$ over $[a,b]$. 

If the upper and lower Riemann integrals are equal, then $f$ is Riemann integrable on $[a,b]$. We write $f\in \mathscr{R}$. The Riemann integral is defined as the simple $$\int_a^b f(x)\,dx.$$

*Remark*: This definition should belong to Darboux integral. However, the Rudin book does not put too much emphasis on differentiating Riemann/Darboux integrable and the two are actually equivalent. 

*Remark*: Since $f$ is bounded, $\exists m, M$, s.t. $$m\le f(x)\le M, \qquad a\le x \le b$$
Therefore, $\forall P$, $$m(b-a)\le L(P,f) \le U(P,f) \le M(b-a).$$ This proves that for all bounded function $f$, $L(P,f)$ and $U(P,f)$ are bounded. 

**Def** 5.2 Riemann-Stieltjes Integral
Let $\alpha$ be a monotonically increasing function on $[a,b]$ (since $\alpha(a)$ and $\alpha(b)$ are finite, it follows that $\alpha$ is bounded on $[a,b]$). Corresponding to each partition $P$ of $[a,b]$, we write $$\Delta \alpha_i = \alpha(x_i) - \alpha(x_{i-1}).$$
It is clear that $\Delta\alpha_i\ge 0$. $\forall$ real-valued function $f$ bounded on $[a,b]$, we put $$U(P,f,\alpha) = \sum_{i=1}^n M_i\Delta\alpha_i$$ $$L(P,f,\alpha) = \sum_{i=1}^n m_i\Delta\alpha_i$$ where $M_i = \sup f(x)$ for $x_{i-1}\le x \le x_i$, $m_i = \inf f(x)$ for $x_{i-1}\le x \le x_i$. Let $$\overline{\int_a^b}f\,d\alpha = \inf U(P,f,\alpha)$$ $$\underline{\int_a^b}f\,d\alpha = \sup L(P,f,\alpha)$$
If the upper and lower Riemann-Stieltjes integrals are equal, then their common value, $$\int_a^b f\,d\alpha,$$ is the *Riemann-Stieltjes integral*, and $f$ is integrable wrt $\alpha$, $f\in \mathscr{R}(\alpha)$. The standard Riemann integral is the case when $\alpha = x$. 

**Def** 6.3 Refinement (of a partition); common refinement
We say that the partition $P^*$ is a *refinement* of $P$ if $P*\supset P$. Given two partitions, $P_1$ and $P_2$, we say that $P^*$ is their *common refinement* if $P^* = P_1\cup P_2$. 

**Thm** 6.4 
If $P^*$ is a refinement of $P$, then $$L(P,f,\alpha)\le L(P^*,f,\alpha)$$ and $$U(P^*,f,\alpha)\le U(P,f,\alpha)$$
*Proof*: For the first inequality, take an arbitrary section $[x_{i-1}, x_i]$ that admits a new point $x^*$. The lower integral of this section, before adding the refinement, is $$m_i(\alpha(x_i) - \alpha(x_{i-1}))$$Notice that $\forall x\in [x_{i-1}, x_i]$, $f(x)\ge m_i$, so suppose the infimum of $f$ on $[x_{i-1}, x^*]$ be $m_{i1}$, the infimum of $f$ on $[x^*, x_i]$ be $m_{i2}$, we have $m_{i1}\ge m_i$, $m_{i2}\ge m_i$, resulting the new lower integral $$m_{i2}(\alpha(x_i) - \alpha(x^*)) + m_{i1}(\alpha(x^*) - \alpha(x_{i-1}))\ge m_i(\alpha(x_i) - \alpha(x_{i-1}))$$ because $\alpha(x_i) - \alpha(x_{i-1}) = (\alpha(x_i) - \alpha(x^*)) + (\alpha(x^*) - \alpha(x_{i-1}))$. 

Summing up, we have $$L(P,f,\alpha)\le L(P^*, f, \alpha).$$
The argument for the second inequality is similar. 

**Thm** 6.5 $$\underline{\int_a^b}f\,d\alpha \le \overline{\int_a^b}f\, d\alpha$$
*Remark*: This can be proven by using the fact that if $P^*$ is the common refinement of two partitions $P_1$ and $P_2$, then $L(P_1, f, \alpha)\le L(P^*, f, \alpha) \le U(P^*, f, \alpha) \le U(P_2, f, \alpha)$. Also, $\underline{\int}f\, d\alpha$ is the supremum of $L$ taken over all partitions, $\overline{\int}f\,d\alpha$ is the infimum of $U$ taken over all partitions. 

**Thm** 6.6 
$f\in \mathscr{R}(\alpha)$ on $[a,b]$ if and only if $\forall \epsilon>0$, $\exists$ a partition $P$ s.t. $$U(P,f,\alpha) - L(P,f,\alpha)<\epsilon.$$
*Proof*: Suppose $U(P,f,\alpha) - L(P,f,\alpha)<\epsilon$. The definition of lower/upper integrals and the **Thm** 6.5 suggest $$L(P,f,\alpha)\le \underline{\int}f\,d\alpha \le \overline{\int}f\,d\alpha
 \le U(P,f,\alpha)$$
 In light of that, $$\overline{\int}f\,d\alpha - \underline{\int}f\,d\alpha\le U(P,f,\alpha) - L(P,f,\alpha)<\epsilon$$
 Since $\epsilon$ is arbitrary, this concludes that $$\overline{\int }f\,d\alpha = \underline{\int}f\,d\alpha,$$ which means $f\in \mathscr{R}(\alpha)$ on $[a,b]$. 

Suppose $f\in \mathscr{R}(\alpha)$ on $[a,b]$. Let $\epsilon>0$, suppose $P_1, P_2$ are partitions with $$U(P_2,f,\alpha) - \int f\,d\alpha < \frac{\epsilon}{2}$$ $$\int f\, d\alpha - L(P_1, f, \alpha) < \frac{\epsilon}{2}$$
Let $P$ be a common refinement for $P_1, P_2$, then $$U(P,f,\alpha)\le U(P_2, f, \alpha) < \int f\,d\alpha + \frac{\epsilon}{2} < L(P_1, f, \alpha) + \epsilon \le L(P_1, f, \alpha) + \epsilon$$
Then, $U(P, f, \alpha) - L(P,f, \alpha) < \epsilon$. 

**Thm** 6.7 
Suppose for some partition $P$ and some $\epsilon>0$, $$U(P,f, \alpha) - L(P,f,\alpha) <\epsilon,$$
(a) It holds with the same $\epsilon$ for every refinement $P$. 
(b) If the above inequality holds for $P = \{x_0, \dots, x_n\}$ and if $s_i$, $t_i$ are arbitrary points in $[x_{i-1}, x_i]$, then $$\sum_{i=1}^n |f(s_i) - f(t_i)|\Delta \alpha_i <\epsilon$$
(c) If the above inequality holds for $P = \{x_0, \dots, x_n\}$ and if $s_i$, $t_i$ are arbitrary points in $[x_{i-1}, x_i]$, $f\in \mathscr{R}(\alpha)$, $$\left\lvert \sum_{i=1}^n f(t_i)\Delta \alpha_i - \int_a^b f\,d\alpha\right\rvert <\epsilon$$
*Remark*: Refinement only makes $U$ smaller and $L$ larger, so the difference will be smaller anyway. (a) is done.

*Proof* of (b-c): 
(b) Notice that $$\begin{align*}
U(P,f,\alpha) - L(P,f,\alpha) &= \sum_{i=1}^n \sup_{x\in[x_{i-1}, x_i]}f(x)\Delta \alpha_i - \sum_{i=1}^n \inf_{x\in[x_{i-1}, x_i]}f(x)\Delta \alpha_i\\
&= \sum_{i=1}^n \left(\sup_{x\in [x_{i-1},x_i]}f(x) - \inf_{x\in[x_{i-1},x_i]}f(x)\right)\Delta \alpha_i < \epsilon
\end{align*}$$
Notice that $\sup f(x) \ge \max\{f(s_i), f(t_i)\}$, $\inf f(x) \le \min\{f(s_i), f(t_i)\}$, so $|f(s_i) - f(t_i)|\le \sup f(x) - \inf f(x)$. Then $$\sum_{i=1}^n |f(s_i) - f(t_i)|\Delta \alpha_i \le \sum_{i=1}^n \left( \sup f(x) - \inf f(x) \right) \Delta \alpha_i< \epsilon$$
(c) If $f\in \mathscr{R}(\alpha)$, since $$\int_a^b f\, d\alpha = \inf U(P, f, \alpha) = \sup L(P, f, \alpha),$$ $$L(P,f, \alpha)\le \int_a^b f\, d\alpha \le U(P, f, \alpha)$$
Since $t_i$ is an arbitrary point in $[x_{i-1}, x_i]$, $$L(P,f, \alpha)\le \sum_{i=1}^n f(t_i)\Delta \alpha_i \le U(P,f,\alpha)$$
Since $U(P,f, \alpha) - L(P,f, \alpha)<\epsilon$, the set of everything between the two is bounded by $\epsilon$. This follows that $$\left\lvert \sum_{i=1}^n f(t_i)\Delta \alpha_i - \int_a^b f\,d\alpha\right\rvert <\epsilon$$

**Thm** 6.8 
If $f$ is continuous on $[a,b]$ then $f\in \mathscr{R}(\alpha)$ on $[a,b]$. 
*Proof*: Fix an arbitrary $\epsilon>0$, then find some $\eta>0$ s.t. $\alpha(b) - \alpha(a)<\epsilon/\eta$. For closed interval $[a,b]\subset \mathbb{R}$, it is compact. Therefore, $f$ is uniformly continuous on $[a,b]$. Then, $\exists \delta>0$ s.t. $d_X(x,y)<\delta$, $x,y\in [a,b]$ implies $d_Y(f(x), f(y))<\eta$. 

It is possible to control $P$ s.t. $x_i - x_{i-1}<\delta$ for each $i$, then on $[x_{i-1}, x_i]$, $\sup f(x) - \inf f(x)\le \eta$. This bounds $U(P, f, \alpha) - L(P,f,\alpha)$ by $$\begin{align*}
U(P, f, \alpha) - L(P,f,\alpha) &= \sum_{i=1}^n (\sup f(x) - \inf f(x))\Delta \alpha_i\\
&\le \eta \sum_{i=1}^n \Delta \alpha_i\\
&= \eta (\alpha(b) - \alpha(a))\\
&< \epsilon,
\end{align*}$$ which proves that $f\in \mathscr{R}(\alpha$) on $[a,b]$. 

**Thm** 6.9 
If $f$ is monotonic on $[a,b]$, and if $\alpha$ is continuous on $[a,b]$, then $f\in \mathscr{R}(\alpha)$. 
*Proof*: $\forall n\in \mathbb{N}$, it is possible to construct a partition $P_n$ in this way: Let $\alpha_i - \alpha_{i-1} = \frac{\alpha(b) - \alpha(a)}{n}$, then we can always find $x_i$ corresponding to each $\alpha_i$ (**Thm** 4.23). Citing that $f$ is monotonic, WLOG, assume it is monotonically increasing. We have $\sup f(x) = f(x_i)$ and $\inf f(x) = f(x_{i-1})$ for a $[x_{i-1}, x_i]$. 

Then, $$U(P_n,f,\alpha) - L(P_n,f,\alpha) = \sum_{i=1}^n (\sup f(x) - \inf f(x))\Delta \alpha_i = \sum_{i=1}^n (f(x_i) - f(x_{i-1}))\frac{\alpha(b) - \alpha(a)}{n}$$
What's the trick here is that the right hand side (the sum) converges to 0 as $n\to \infty$. In other words, $\forall \epsilon>0$, $\exists N\in \mathbb{N}$ s.t. $n>N$ implies $U(P_n,f,\alpha) - L(P_n,f,\alpha)<\epsilon$. This proves that $f\in \mathscr{R}(\alpha)$. 

**Thm** 6.10 
Suppose $f$ is bounded on $[a,b]$, $f$ has only finitely many points of discontinuity on $[a,b]$, and $\alpha$ is continuous at every point at which $f$ is discontinuous. Then $f\in \mathscr{R}(\alpha)$. 

**Thm** 6.11
Suppose $f\in \mathscr{R}(\alpha)$ on $[a,b]$, $m\le f\le M$, $\phi$ is continuous on $[m,M]$, and $h(x) = \phi(f(x))$ on $[a,b]$. Then $h\in \mathscr{R}(\alpha)$ on $[a,b]$.


## Properties of the Integral

**Thm** 6.12

**Thm** 6.13

**Def** 6.14

**Thm** 6.15

**Thm** 6.16

**Thm** 6.17

**Thm** 6.19 Change of Variable

## Integration and Differentiation

**Thm** 6.20

**Thm** 6.21 The Fundamental Theorem of Calculus

**Thm** 6.22 Integration by Parts

## Integration of Vector-Valued Functions

**Def** 6.23

**Thm** 6.24

**Thm** 6.25

## Rectifiable Curves

**Def** 6.26

**Thm** 6.27

## Exercises