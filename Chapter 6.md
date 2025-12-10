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
*Proof*: Fix an arbitrary $\epsilon >0$. Per **Thm** 6.8, suppose the points of discontinuity on $[a,b]$ are $x_1, \dots, x_n$, where $n$ is finite, then on each of $[a, x_1], [x_1, x_2], \dots, [x_{n-1}, x_n]$, $f$ is continuous and therefore, $f\in \mathscr{R}(\alpha)$. Therefore, we only need to discuss the parts where $f$ is not continuous. 

We can form small intervals around each of $x_n$, denoted as $[u_n, v_n]$. Since $\alpha$ is continuous, $\exists \delta>0$ s.t. we can control $|v_n - u_n| < \delta$ for all $n$ to force $|\alpha(v_n) - \alpha(u_n)|<\epsilon$. 

In designing the partition $\mathcal{P}$ here, we take the following consideration: Let $$\mathcal{P} = \{t_0, \dots, t_n\}$$We make each partition small, but we do not intend to chop up the small intervals $[u_n, v_n]$; i.e., if $x_{i-1}$ is not one of the $u_j$, then $\Delta x_i< \delta$, and each $u_j, v_j\in \mathcal{P}$ but no point in $(u_j, v_j)$ is in $\mathcal{P}$. For every $[t_{i-1}, t_i]$, thus, if $t_{i-1} \ne u_j$ for all $j$, $M_i - m_i < \epsilon$; if $t_{i-1} = u_j$ for some $j$, $M_i -m_i \le 2M$ because $f$ is bounded. This follows, $$U(\mathcal{P}, f, \alpha) - L(\mathcal{P},f, \alpha)< [\alpha(b)-\alpha(a)]\epsilon + 2M\epsilon$$
With $\epsilon$ arbitrary, this follows $f\in \mathscr{R}(\alpha)$. 

**Thm** 6.11
Suppose $f\in \mathscr{R}(\alpha)$ on $[a,b]$, $m\le f\le M$, $\phi$ is continuous on $[m,M]$, and $h(x) = \phi(f(x))$ on $[a,b]$. Then $h\in \mathscr{R}(\alpha)$ on $[a,b]$.


## Properties of the Integral

**Thm** 6.12 Basic properties
(a) If $f_1\in \mathscr{R}(\alpha)$ and $f_2\in \mathscr{R}(\alpha)$ on $[a,b]$, then $$f_1 + f_2 \in \mathscr{R}(\alpha),$$ $cf\in \mathscr{R}(\alpha)$ for every constant $f$, and $$\int_a^b (f_1 + f_2)\, d\alpha = \int_a^b f_1\,d\alpha + \int_a^b f_2\, d\alpha$$ $$\int_a^b cf\,d\alpha = c\int_a^b f\, d\alpha$$
(b) If $f_1(x)\le f_2(x)$ on $[a,b]$, then $$\int_a^b f_1\,d\alpha \le \int_a^b f_2\, d\alpha$$
(c) If $f\in \mathscr{R}(\alpha)$ on $[a,b]$ and if $a<c<b$, then $f\in \mathscr{R}(\alpha)$ on $[a,c]$ and on $[c,b]$, and $$\int_a^c f\,d\alpha + \int_c^b f\, d\alpha = \int_a^b f\, d\alpha$$
(d) If $f\in \mathscr{R}(\alpha)$ on $[a,b]$ and if $|f(x)|\le M$ on $[a,b]$, then $$\left\lvert \int_a^b f\,d\alpha \right\rvert \le M[\alpha(b) - \alpha(a)]$$
(e) If $f\in \mathscr{R}(\alpha_1)$ and $f\in \mathscr{R}(\alpha_2)$, then $f\in \mathscr{R}(\alpha_1 + \alpha_2)$ and $$\int_a^b f\, d(\alpha_1 + \alpha_2) = \int_a^b f\, d\alpha_1 + \int_a^b f\, d\alpha_2;$$ if $f\in \mathscr{R}(\alpha)$ and $c$ is a positive constant, then $f\in \mathscr{R}(c\alpha)$ and $$\int_a^b f\, d(c\alpha) = c\int_a^b f\, d\alpha$$
**Thm** 6.13
If $f\in \mathscr{R}(\alpha)$ and $g\in \mathscr{R}(\alpha)$ on $[a,b]$, then 
(a) $fg \in \mathscr{R}(\alpha)$;
(b) $|f| \in \mathscr{R}(\alpha)$ and $$\left\lvert \int_a^b f\,d\alpha \right\rvert \le \int_a^b |f| \,d\alpha $$
*The proof of (a) and $|f|\in \mathscr{R}(\alpha)$, see* **Thm** *6.11*. 
*Proof* of the inequality in (b): Choose $c\in \pm 1$. We are manually constructing the absolute value, so $c\int f\,d\alpha \ge 0$. Then, $$\left\lvert \int f\, d\alpha \right \rvert = c\int f\, d\alpha = \int cf\,d\alpha \le \int |f|\, d\alpha,$$ following from $cf\le |f|$. 

**Def** 6.14 Unit Step Function
The *unit step function* $I$ is defined by $$I(x) = \begin{cases}
0 & x\le 0\\
1 & x>0
\end{cases}$$

**Thm** 6.15
If $a<s<b$, $f$ is bounded on $[a,b]$, $f$ is continuous at $s$, and $\alpha(x) = I(x-s)$, then $$\int_a^b f\,d\alpha = f(s)$$
*Proof*: Consider a partition $P = \{x_0, x_1, x_2, x_3\}$, where $x_0 = a, x_1 = s, s<x_2<b, x_3 = b$. Then, on $[x_0,x_1]$, $\alpha(x_1) - \alpha(x_0) = 0$; on $[x_1, x_2]$, $\alpha(x_2) - \alpha(x_1) = 1$; on $[x_2, x_3]$, $\alpha(x_3) - \alpha(x_2) = 0$. This follows $$U(P,f,\alpha) = M_2 \qquad \text{and} \qquad L(P,f,\alpha) = m_2,$$ where both $M_2, m_2$ converges to $f(s)$ as $x_2\to s$, so the value of the integral is $f(s)$.

**Thm** 6.16
Suppose $c_n\ge 0$ for $1,2,3,\dots$, $\sum c_n$ converges, $\{s_n\}$ is a sequence of distinct points in $(a,b)$, and $$\alpha(x) = \sum_{n=1}^\infty c_n I(x-s_n)$$
Let $f$ be continuous on $[a,b]$, then $$\int_a^b f\,d\alpha = \sum_{n=1}^\infty c_n f(s_n)$$
*Proof*: Notice that since $I(x-s_n)\le 1$ for all $x$,
$$\alpha(x) = \sum_{n=1}^\infty c_nI(x-s_n)\le \sum_{n=1}^\infty c_n,$$ which converges. Then $\alpha(x)$ converges. Fix an arbitrary $\epsilon>0$, then $\exists N\in \mathbb{N}$ s.t. $n>N$ implies $$\sum_{n=1}^\infty c_n - \sum_{n=1}^N c_n = \sum_{N+1}^\infty c_n<\epsilon.$$
Here, we let $$\alpha_1(x) = \sum_{n=1}^N c_nI(x-s_n),$$ and $$\alpha_2(x) = \sum_{N+1}^\infty c_n I(x-s_n).$$
This follows $$\int_a^b f\, d\alpha = \int_a^b f\, d\alpha_1 + \int_a^b f\,d\alpha_2.$$ Notice that $$\int_a^b f\,d\alpha_1 = \sum_{n=1}^N c_n \int_a^b f\,d I(x-s_n) = \sum_{n=1}^N c_nf(s_n),$$ then, notice that $\alpha_2(b) - \alpha_1(a)<\epsilon$, denoting $M$ as the supremum of $f$ on $[a,b]$, 
$$\left\lvert \int_a^b f\,d\alpha  - \sum_{n=1}^N c_nf(s_n)\right\rvert = \left\lvert \int_a^b f\,d\alpha_2\right\rvert \le M\epsilon$$

The right hand side shrinks to 0 as $N\to \infty$. This proves that $$\left\lvert \int_a^b f\,d\alpha - \sum_{n=1}^\infty c_nf(s_n)\right\rvert = 0$$

**Thm** 6.17
Assume $\alpha$ increases monotonically and $\alpha'\in \mathscr{R}$ on $[a,b]$. Let $f$ be a bounded real function on $[a,b]$.
Then $f\in \mathscr{R}(\alpha)$ if and only if $f\alpha' \in \mathscr{R}$. In that case, $$\int_a^b f\,d\alpha = \int_a^b f(x)\alpha'(x) \, dx$$
*Proof*: Since $f\in \mathscr{R}(\alpha)$, $\exists P = \{x_0, \dots, x_n\}$ s.t. $U(P, \alpha') - L(P, \alpha')<\epsilon$. By the mean value theorem, $\exists t_i\in[x_{i-1}, x_i]$ s.t. $$\Delta \alpha_i = \alpha(x_i) - \alpha(x_{i-1}) = \alpha'(t_i)\Delta x_i$$
For an arbitrary $s_i\in [x_{i-1}, x_i]$, $$\sum_{i=1}^n |\alpha'(s_i) - \alpha'(t_i)|\Delta x_i \le U(P,\alpha') - L(P, \alpha') < \epsilon$$
Notice that, if we put $M = \sup |f(x)|$, then $$\sum_{i=1}^n f(s_i)\Delta \alpha_i = \sum_{i=1}^n f(s_i) \alpha'(t_i)\Delta x_i$$
Since we want to compare $U(P,f,\alpha)$ and $U(P, f\alpha')$, notice that $$U(P,f,\alpha) = \sum_{i=1}^n f(s_i)\Delta \alpha_i,$$ $$U(P,f\alpha')=\sum_{i=1}^n (f\alpha')(s_i)\Delta x_i,$$ $$\begin{align*}
|U(P,f,\alpha) - U(P,f\alpha')| &= \left| \sum_{i=1}^n f(s_i)\Delta \alpha_i - \sum_{i=1}^n (f\alpha')(s_i)\Delta x_i\right|\\
&= \left|\sum_{i=1}^n f(s_i) \alpha'(t_i)\Delta x_i - \sum_{i=1}^n f(s_i) \alpha'(s_i)\Delta x_i\right|\\
&= \left|\sum_{i=1}^n f(s_i) (\alpha'(t_i) - \alpha'(s_i))\Delta x_i\right|\\
&= \sum_{i=1}^n |f(s_i)| \cdot |\alpha'(t_i) - \alpha'(s_i)|\Delta x_i\\
&\le M|\alpha'(t_i) - \alpha'(s_i)|\Delta x_i\\
&< M\epsilon
\end{align*}$$
This follows that $$\int_a^b f\, d\alpha = \int_a^b f(x)\alpha'(x)\,dx$$

**Thm** 6.19 Change of Variable
Suppose $\varphi$ is a strictly increasing continuous function that maps an interval $[A,B]$ onto $[a,b]$. Suppose $\alpha$ is monotonically increasing on $[a,b]$ and $f\in \mathscr{R}(\alpha)$ on $[a,b]$. Define $\beta$ and $g$ on $[A,B]$ by $$\beta(y) = \alpha(\varphi(y)),\qquad g(y) = f(\varphi(y)).$$
Then $g\in \mathscr{R}(\beta)$ and $$\int_A^B g\, d\beta = \int_a^b f\, d\alpha$$
*Proof*: To each partition $\mathcal{P} = \{x_0, \dots, x_n\}$ of $[a,b]$, a partition $\mathcal{Q} = \{y_0, \dots, y_n\}$ of $[A,B]$ with $x_i = \varphi(y_i)$. $\varphi$ is bijective and monotonic so all partitions of $[a,b]$ and $[A,B]$ are related in this way. 

We claim $$\mathcal{U}(\mathcal{P}, g, \beta) = \mathcal{U}(\mathcal{Q}, f, \alpha)$$ and $$\mathcal{L}(\mathcal{P}, g, \beta) = \mathcal{L}(\mathcal{Q}, f, \alpha)$$
Since $f\in \mathscr{R}(\alpha)$, $\mathcal{P}$ can be chosen so $\mathcal{U}(\mathcal{P}, f, \alpha)$ and $\mathcal{L}(\mathcal{P}, f, \alpha)$ are close to $\int f\, d\alpha$. This follows that the corresponding $\mathcal{Q}$ ensures that $\mathcal{U}(\mathcal{Q},g, \beta)$ is close to $\mathcal{L}(\mathcal{Q},g,\beta)$. Therefore, $g\in R(\beta)$ and the identity of integral holds. 
## Integration and Differentiation

**Thm** 6.20
Let $f\in \mathscr{R}$ on $[a,b]$. For $a\le x\le b$, put $$F(x) = \int_a^x f(t)\,dt$$Then $F$ is continuous on $[a,b]$; furthermore, if $f$ is continuous at a point $x_0$ of $[a,b]$, then $F$ is differentiable at $x_0$, and $$F'(x_0) = f(x_0)$$
*Remark*: This theorem is saying that *the derivative of an integral is the original function under appropriate assumptions*. 
*Proof*: Since $f\in \mathscr{R}$, $f$ is bounded. Suppose $|f(t)| \le M$, $\forall a\le t\le b$. For all $x,y\in [a,b]$, $$|F(y) - F(x)| = \left|\int_x^y f(t)\,dt\right| \le M(y-x)$$
For given $\epsilon>0$, we see that $|F(y) - F(x)|<\epsilon$ if $|y-x|<\epsilon/M$. This proves the continuity of $F$. 

Suppose $f$ is continuous at $x_0$. $\forall \epsilon>0$, $\exists \delta>0$ s.t. $$|f(t) - f(x_0)|<\epsilon$$ if $|t-x_0|<\delta$. Let $s,t\in B_\delta(x_0)$, $$\begin{align*}
\left|\frac{F(t) - F(s)}{t-s} - f(x_0)\right| &= \left| \frac{1}{t-s}\int_s^t f(u)\,du - f(x_0)\right|\\
&= \left| \frac{1}{t-s}\int_s^t f(u)\,du - \frac{1}{t-s} \int_s^t f(x_0)\,du\right|\\
&= \left| \frac{1}{t-s}\int_s^t (f(u) - f(x_0))\,du\right|\\
&\le \frac{1}{t-s}\int_s^t |f(u) - f(x_0)|\,du\\
&< \frac{1}{t-s}\cdot (t-s)\epsilon\\
&= \epsilon
\end{align*}$$
It proves that $F'(x_0) = f(x_0)$.

**Thm** 6.21 The Fundamental Theorem of Calculus
If $f\in \mathscr{R}$ on $[a,b]$ and if there is a differentiable function $F$ on $[a,b]$ such that $F'=f$, then $$\int_a^b f(x)\,dx  = F(b) - F(a)$$
*Proof*: Fix an arbitrary $\epsilon>0$. Find a good partition $P = \{x_0, \dots, x_n\}$ s.t. $$U(P,f) - L(P,f)<\epsilon$$
$\forall i = 1, \dots, n$, $\exists t_i\in [x_{i-1}, x_i]$ s.t. $F(x_i) - F(x_{i-1}) = f(t_i)\Delta x_i$. This follows $$\sum_{i=1}^n f(t_i)\Delta x_i = F(b)-F(a)$$
Following $$\left\lvert \sum_{i=1}^n f(t_i)\Delta x_i - \int_a^b f\,d\alpha\right\rvert<\epsilon,$$ we have $$\left\lvert F(b) - F(a) - \int_a^b f\,d\alpha\right\rvert<\epsilon$$

**Thm** 6.22 Integration by Parts
Suppose $F$ and $G$ are differentiable functions on $[a,b]$, $F' = f\in \mathscr{R}$, and $G'=g\in \mathscr{R}$. Then $$\int_a^b F(x)g(x)\,dx = F(b)G(b) - F(a)G(a) - \int_a^b f(x)G(x)\,dx$$
*Remark*: Use **Thm** 6.21, the Fundamental Theorem of Calculus, and it's done.
## Integration of Vector-Valued Functions

**Def** 6.23
Let $f_1, \dots, f_k$ be real functions on $[a,b]$, and let $\mathbf{f} = (f_1, \dots, f_k)$ be the corresponding mapping of $[a,b]$ into $\mathbb{R}^k$. If $\alpha$ increases monotonically on $[a,b]$, to say that $\mathbf{f}\in \mathscr{R}(\alpha)$ means that $f_j = \mathscr{R}(\alpha)$ for $j =1, \dots, k$. If this is the case, we define $$\int_a^b \mathbf{f}\,d\alpha = \left(\int_a^b f_1\, d\alpha, \dots, \int_a^b f_k \, d\alpha\right)$$

**Thm** 6.24 The Fundamental Theorem of Calculus, vector-valued
If $\mathbf{f}$ and $\mathbf{F}$ map $[a,b]$ into $\mathbb{R}^k$, if $\mathbf{f}\in \mathscr{R}$ on $[a,b]$, and if $\mathbf{F}' = \mathbf{f}$, then $$\int_a^b \mathbf{f}(t)\, dt = \mathbf{F}(b) - \mathbf{F}(a)$$

**Thm** 6.25
If $\mathbf{f} maps $[a,b]$ into $\mathbb{R}^k$ and if $\mathbf{f}\in \mathscr{R}(\alpha)$ for some monotonically increasing function $\alpha$ on $[a,b]$, then $|\mathbf{f}|\in \mathscr{R}(\alpha)$ and $$\left\lvert \int_a^b \mathbf{f}\,d\alpha \right\rvert \le \int_a^b |\mathbf{f}| \,d\alpha $$
## Rectifiable Curves

**Def** 6.26 Curve; arc; closed curve; rectifiable curve
A continuous map $\gamma: [a,b]\rightarrow \mathbb{R}^k$ is a *curve*. If it is injective, it is an *arc*. If $\gamma(a)=\gamma(b)$ it is a *closed curve*. 

To each partition $\mathcal{P} = \{x_0, \dots, x_n\}$ of $[a,b]$, $$\Lambda(\mathcal{P},\gamma) = \sum_{i=1}^n|\gamma(x_i) - \gamma(x_{i-1})|$$ 
As the partition is refined, this approaches the length of the curve. So we define $$\Lambda(\gamma) = \sup_\mathcal{P}\Lambda(\mathcal{P}, \gamma)$$ If $\Lambda(\gamma) < \infty$ we say $\gamma$ is *rectifiable*. 

If we assume $\gamma$ has continuous derivative, this depends only on $\gamma([a,b])$, not $\gamma$. 

**Thm** 6.27
If $\gamma'$ is continuous on $[a,b]$, then $\gamma$ is rectifiable, and $$\Lambda(\gamma) = \int_a^b |\gamma'(t)|\,dt$$

## Exercises