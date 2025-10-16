Numerical Sequences and Series

**Def** 3.1 Converge, diverge
A sequence $\{p_n\}$ in a metric space $X$ is said to *converge* if there is a point $p\in X$ with the following property: $\forall \epsilon>0, \exists N\in \mathbb{N}$ s.t. $n\ge N$ implies $d(p_n,p)< \epsilon$. We write $p_n\rightarrow p$ or $\lim_{n\rightarrow \infty} p_n = p$. 
$\{p_n\}$ is said to *diverge* if it does not converge.

**Thm** 3.2
Let $\{p_n\}$ be a sequence in a metric space $X$. 
(a) $\{p_n\}$ converges to $p\in X$ if and only if every neighborhood of $p$ contains $p_n$ for all but finitely many $n$. 
(b) If $p\in X$, $p'\in X$, and if $\{p_n\}$ converges to $p$ and to $p'$, then $p'=p$. (uniqueness)
(c) If $\{p_n\}$ converges then it is bounded.
(d) If $E\subset X$ and $p\in E'$, then $\exists \{p_n\}\subset E$ s.t. $p_n\rightarrow p$.

*Proof*: 
(a) For a convergent sequence $\{p_n\}$, by **Def** 3.1, $\forall \epsilon>0$, $\exists N\in \mathbb{N}$ s.t. $d(p_n,p)<\epsilon$ for all $n\ge N$. Then, all of $p_N, p_{N+1}, \dots$ are inside $B_\epsilon(p)$. Only the first $N-1$ points (finitely many points) are not.

In the other direction, if for all but finitely many $n$ ($\exists N\in\mathbb{N}, n\ge N$), $p_n\in B_\epsilon(p)$, we can say $n\ge N$ implies $d(p_n,p)<\epsilon$. (QED)

(b) Fix an arbitrary $\epsilon>0$, then $\exists N, N'\in \mathbb{N}$ s.t. $$n\ge N\Rightarrow p_n\in B_{\epsilon/2}(p)$$ and $$n\ge N'\Rightarrow p_n\in B_{\epsilon/2}(p')$$ then $$d(p,p')\le d(p,p_n) + d(p_n, p')<\epsilon$$ We can choose $\epsilon$ to be as small as we want, so $d(p,p')=0$. (QED)

(c) *Take the $r$ as the max of $\epsilon$ and $d(p_i,p)$ for the first $N-1$ terms, formal proof omitted.*

(d) *Construct $\{p_n\}$ by choosing a point in the neighborhood with radius $1/n$. 

**Thm** 3.3 Suppose $\{s_n\}$, $\{t_n\}$ are complex sequences, and $\lim_{n\rightarrow \infty} s_n = s$, $\lim_{n\rightarrow \infty} t_n = t$. Then
(a) $\lim (s_n+t_n) = s+t$.
(b) $\lim cs_n = cs$ and $\lim (c+s_n) = c+s, \forall c\in \mathbb{C}$.
(c) $\lim s_nt_n = st$.
(d) $\lim \frac{1}{s_n} = \frac{1}{s}$, provided $s_n\ne 0$ $ ($n=1,2,3,\dots), and $s\ne 0$.
*Proof*: (a-b) omitted.
(c) $\forall \epsilon>0$, $\exists N_1, N_2>0$: $$n\ge N_1\Rightarrow \lvert s_n - s\rvert <\sqrt{\epsilon}$$ $$n\ge N_2\Rightarrow \lvert t_n - t\rvert <\sqrt{\epsilon}$$ With $n\ge \max\{N_1, N_2\}$, $$\begin{align*} \lvert s_nt_n - st \rvert &= \lvert(s_n-s)(t_n-t)\\ &+s(t_n-t)\\ &+t(s_n-s)\rvert\\ &\le \lvert (s_n-s)(t_n-t) \rvert \\ &<\epsilon\end{align*}$$ (QED)

(d) Choose $M\in \mathbb{N}$ s.t. $$n\ge M\Rightarrow \lvert s_n-s\rvert<\frac{1}{2}\lvert s\rvert$$ $$\begin{align*}
|s| &= |s-s_n+s_n|\\
&\le |s-s_n| + |s_n|\\
&<\frac{1}{2}|s|+|s_n|
\end{align*}$$ Therefore, $|s_n|>\frac{1}{2}|s|$. $\forall \epsilon>0$, $\exists N>M$ s.t. $$n\ge N\Rightarrow |s_n-s|<\frac{1}{2}|s|^2\epsilon$$ $$\Rightarrow \left\lvert \frac{1}{s_n} - \frac{1}{s} \right\rvert = \left\lvert \frac{s_n-s}{s_ns} \right\rvert <\frac{2}{|s|^2}|s_n-s|<\epsilon$$ (QED)

**Thm** 3.4
(a) Suppose $\mathbf{x}_n\in \mathbb{R}^k$ ($n=1,2,3,\dots$) and $$\mathbf{x}_n = (\alpha_{1,n}, \dots, \alpha_{k,n}).$$ Then $\{\mathbf{x}_n\}$ converges to $\mathbf{x} = (\alpha_1,\dots, \alpha_k) if and only if $$\lim_{n\rightarrow \infty}\alpha_{j,n} = \alpha_j \quad (1\le j \le k)$$
(b) Suppose $\{\mathbf{x}_n\}$, $\{\mathbf{y}_n\}$ are sequences in $\mathbb{R}^k$, $\{\beta_n\}$ is a sequence of real numbers, and $\mathbf{x}_n\rightarrow\mathbf{x}$, $\mathbf{y}_n\rightarrow\mathbf{y}$, $\beta_n\rightarrow \beta$. Then $$\lim_{n\rightarrow\infty} (\mathbf{x}_n+\mathbf{y}_n) = \mathbf{x}+\mathbf{y}, \quad \lim_{n\rightarrow\infty} \mathbf{x}_n\cdot\mathbf{y}_n = \mathbf{x}\cdot\mathbf{y}, \quad \lim_{n\rightarrow\infty} \beta_n \mathbf{x}_n = \beta\mathbf{x}$$
## Subsequences

**Def** 3.5 Subsequence, subsequential limit

**Thm** 3.6
(a) If $\{p_n\}$ is a sequence in a compact metric space $X$, then some subsequence $\{p_n\}$ converges to a point of $X$.
(b) Every bounded sequence in $\mathbb{R}^k$ contains a convergent subsequence.
*Proof*:
(a) If the range of $\{p_n\}$ is finite then use pigeonhole principle: $\exists \{n_i\}$ with $n_1<n_2<\dots$, s.t. $$p_{n_1} = p_{n_2} = \dots = p.$$
If the range of $\{p_n\}$ = $E$ is infinite, apply **Thm** 2.37, $\exists p\in X$ that is a limit point of $E$. Construct $\{n_i\}$ in this way: Firstly choose $n_1$ s.t. $p_{n_1}\in B_1(p)$. Then, choose $n_2, \dots, n_{i}$ s.t. $p_{n_i}\in B_{1/i}(p)$. This subsequence $\{p_{n_i}\}$ converges to $p$. (QED)
(b) The bounded sequence in $\mathbb{R}^k$ is contained in $\overline{B}_r(0)$, $r>0$, which is compact. Then we can apply (a).

**Thm** 3.7
The subsequential limits of sequence $\{p_n\}$ in a metric space $X$ form a closed subset of $X$. 
*Proof*: Let $E^\star$ be the set of all subsequential limits of $\{p_n\}$ and let $q\in (E^\star)'$. We want $q\in E^\star$. Choose $n_1$ s.t. $p_{n_1}\ne q$. Let $\delta = d(q, p_{n_1})$, choose $\{n_i\}$ individually s.t. $\exists x\in E^\star$ with $d(x,q)<2^{-i}\delta$. Since $x\in E^\star, \exists n_i>n_{i-1}$ s.t. $d(x,p_{n_i})< 2^{-i}\delta$. Thus, $d(q, p_{n_i})\le d(x,q) + d(x, p_{n_i})< 2^{-(i-1)}\delta$. Thus, $\{p_{n_i}\}$ converges to $q$, which follows that $q\in E^\star$.

## Cauchy Sequences

**Def** 3.8 Cauchy sequence
A sequence $\{p_n\}$ in a metric space $X$ is said to be a *Cauchy sequence* if $\forall \epsilon>0, \exists N\in \mathbb{N}$ s.t. $d(p_n, p_m)<\epsilon$ with $n,m\ge N$.

**Def** 3.9 Diameter
Let $E$ be a nonempty subset of a metric space $X$, and let $S$ be the set of all real numbers of the form $d(p,q)$, with $p\in E, q\in E$. $$\operatorname{diam} E = \sup S.$$If $\{p_n\}$ is a sequence in $X$ and if $E_N$ consists of points $p_N, p_{N+1}, \dots$, then $\{p_n\}$ is a Cauchy sequence if only if $$\lim_{N\rightarrow \infty}\operatorname{diam} E_N = 0.$$
**Thm** 3.10
(a) If $\overline{E}$ is the closure of a set $E$ in a metric space $X$, then $$\operatorname{diam} \overline{E} = \operatorname{diam} E.$$
(b) If $K_n$ is a sequence of compact sets in $X$ s.t. $K_n\supset K_{n+1}$ ($n=1,2,3,\dots$)and if $$\lim_{n\rightarrow \infty}\operatorname{diam}K_n=0,$$ then $\bigcap_{n=1}^\infty K_n$ consists of exactly one point.
*Proof*:
(a) With $E\subset \overline{E}$, $\operatorname{diam} E \le \operatorname{diam} \overline{E}$. 

For a fixed $\epsilon>0$, choose $p,q \in \overline{E}$ and $p',q'\in E$ s.t. $$d(p,p')<\epsilon, \quad d(q,q')<\epsilon.$$ By triangle inequality, $$d(p,q)\le d(p,p') + d(p',q') + d(q',q) < 2\epsilon + d(p',q') \le 2\epsilon + \operatorname{diam} E.$$ The supremum of the left hand side is less than or equal to the right hand side, an upper bound of $d(p,q)$, then $$\operatorname{diam} \overline{E}\le 2\epsilon + \operatorname{diam} E,$$ which follows that $$\operatorname{diam} \overline{E} = \operatorname{diam} E.$$
(b) By **Thm** 2.36, $K = \bigcap_{n=1}^\infty K_n$ is nonempty. Assume, BWOC, that it contains more than 1 point. Then, $\operatorname{diam} K>0$. Notice that $K\subset K_n$, so $\operatorname{diam} K_n \ge \operatorname{diam} K$. This negates $\operatorname{diam} K_n\rightarrow 0$. $\Rightarrow \Leftarrow$

**Thm** 3.11 
(a) In any metric space $X$, every convergent sequence is a Cauchy sequence.
(b) If $X$ is a compact metric space and if $\{p_n\}$ is a Cauchy sequence in $X$, then $\{p_n\}$ converges to some point of $X$.
(c) In $\mathbb{R}^k$, every Cauchy sequence converges.
*Proof*:
(a) If $\{p_n\}\rightarrow p$, $\forall \epsilon>0$, $\exists N\in \mathbb{N}$ s.t. $$n\ge N\Rightarrow d(p_n, p)<\epsilon/2$$ Then, $\forall n,m\ge N$, $$d(p_n, p_m)\le d(p_n,p) + d(p,p_m)<\epsilon$$ (QED)

(b) **Thm** 3.10 states that with $\{p_n\}$ being Cauchy (i.e., $\lim \operatorname{diam}\overline{E}_N = 0$), then $\bigcap_{N=1}^\infty \overline{E}_N$ only contains one point. Let $\bigcap_{N=1}^\infty \overline{E}_N = \{p\}$. Considering the definition of Cauchy sequence, $\forall \epsilon>0$, $\exists N_0\in \mathbb{N}$ s.t. $\operatorname{diam} \overline{E}_N<\epsilon$ if $N>N_0$. Since $p\in \overline{E}_N$, $\forall q\in E_N$, $d(p,q)<\epsilon$. Therefore $p = \lim_{N\rightarrow \infty}p_N$. (QED)

(c) Notice that for some $N$, $\operatorname{diam} E_N<1$. Then, the range of $\{x_n\}$ is the union of $E_N$ and a finite set $\{x_n\} - E_N$, so $\{x_n\}$ is bounded. It is hence contained in a compact set and we can apply (b). (QED)

**Def** 3.12 Complete
A metric space in which every Cauchy sequence converges is said to be *complete*.

**Def** 3.13 Monotonic
A sequence $\{s_n\}$ of real numbers is said to be 
(a) *monotonically increasing* if $s_n\le s_{n+1}$ ($n = 1,2,3,\dots$).
(b) *monotonically decreasing* if $s_n\ge s_{n+1}$ ($n = 1,2,3,\dots$).

**Thm** 3.14
Suppose $\{s_n\}$ is monotonic. Then it converges if and only if it is bounded.
*Proof*: (Conv. $\Rightarrow$ Bounded) **Thm** 3.2(c)
(Bounded $\Rightarrow$ Conv.) Suppose $\{s_n\}$ is bounded, and let $s$ be its least upper bound (the existence is guaranteed because $\mathbb{R}$ has the least-upper-bound property). Then, $\forall \epsilon>0$, $\exists N\in \mathbb{N}$ s.t. $s_N>s-\epsilon$. Then, notice that $\forall n\ge N$, $s_n \ge s_N$, so $d(s_n, s)<d(s_N,s)<\epsilon$. This proves the convergence. (QED)

## Upper and Lower Limits

**Def** 3.5
Let $\{s_n\}$ be a sequence of real numbers with the following property: $\forall M\in \mathbb{R}$, $\exists N\in \mathbb{N}$ s.t. $n\ge N$ implies $s_n\ge M$. We then write $s_n\rightarrow +\infty$.
$\forall M\in \mathbb{R}$, $\exists N\in \mathbb{N}$ s.t. $n\ge N$ implies $s_n\le M$. We then write $s_n\rightarrow -\infty$.

**Def** 3.16 limsup and liminf
Let $\{s_n\}$ be a sequence of real numbers. Let $E$ be the set of numbers $x$ s.t. $s_{n_k}\rightarrow x$ for some subsequence $\{s_{n_k}\}$. This set $E$ contains all subsequential limits plus possibly $\pm \infty$. Let $$s^\star = \sup E,$$ $$s_\star = \inf E.$$ Then, $s^\star$ is the *upper limit* of $\{s_n\}$, $$\limsup_{n\rightarrow \infty}s_n = s^\star$$ $s_\star$ is the *lower limit* of $\{s_n\}$, $$\liminf_{n\rightarrow \infty}s_n = s_\star$$

**Thm** 3.17 
Let $\{s_n\}$ be a sequence of real numbers. Then $s^\star$ has the following two properties:
(a) $s^\star\in E$.
(b) If $x>s^\star$, there is an integer $N$ s.t. $n\ge N$ implies $s_n<x$.
Moreover, $s^\star$ is the only number with properties (a) and (b).

*Remarks*: Traditionally, I prefer to write this theorem in this way: $\limsup x_n = L$ if:
(a) $\forall \epsilon>0, \exists n_0, \forall n>n_0, x_n<L+\epsilon$
(b) $\forall \epsilon>0, \forall n_0, \exists n>n_0, x_n>L-\epsilon$ 
Property (a) states that $L$ is an ultimate upper bound; property (b) states that there are infinitely many terms getting close to $L$.

Similarly, $\liminf x_n = L$ if:
(a) $\forall \epsilon>0, \exists n_0, \forall n>n_0, x_n>L-\epsilon$
(b) $\forall \epsilon>0, \forall n_0, \exists n>n_0, x_n<L+\epsilon$
Property (a) states that $L$ is an ultimate lower bound; property (b) states that there are infinitely many terms getting close to $L$. 

*Proof* of the Thm:
(a) When $s^\star = \infty$, $E$ is not bounded above, so $\{s_n\}$ is not bounded above and there is a subsequence $\{s_{n_k}\}$ s.t. $s_{n_k}\rightarrow \infty$.

When $s^\star = -\infty$, then $E$ contains only $-\infty$ and there is no subsequential limit. Hence, $\forall m\in \mathbb{R}$, $s_n>m$ for at least finitely many $n$. 

When $s^\star<\infty$, then $E$ is bounded above and at least one subsequential limit exists, **Thm** 3.7 says that $E$ is closed. Then, **Thm** 2.28 suggests that $s^\star = \sup E \in E$. (QED)

(b) Assume BWOC that $\exists x>s^\star$ s.t. $s_n\ge x$ for infinitely many $n$. Then, $\exists y\in E$ s.t. $y\ge x>s^\star$. $\Rightarrow\Leftarrow$ (QED)

**Example** 3.18
For a real-valued sequence $\{s_n\}$, $\lim_{n\rightarrow \infty}s_n = s$ if and only if $$\limsup_{n\rightarrow \infty} s_n = \liminf_{n\rightarrow \infty}s_n = s$$

**Thm** 3.19
If $s_n\le t_n$ for $n\ge N$, where $N$ is fixed, then $$\liminf_{n\rightarrow \infty}s_n\le \liminf_{n\rightarrow\infty} t_n,$$ $$\limsup_{n\rightarrow\infty} s_n\le \limsup_{n\rightarrow\infty} t_n.$$
## Some Special Sequences

**Thm** 3.20
(a) If $p>0$, then $$\lim_{n\rightarrow\infty}\frac{1}{n^p} = 0.$$
(b) If $p>0$, then $$\sqrt[n]{p} = 1$$
(c) $\lim\sqrt[n]{n} = 1$
(d) If $p > 0$ and $\alpha$ is real, then $$\lim_{n\rightarrow \infty}\frac{n^\alpha}{(1+p)^n} = 0$$
(e) If $|x|<1$, then $$\lim_{n\rightarrow \infty}x^n=0$$
## Series

**Def** 3.21 Series 

**Thm** 3.22 Restated *Cauchy criterion* (See **Thm** 3.11)
$\sum a_n$ converges if and only if for every $\epsilon >0 $ there is an integer $N$ s.t. $$\left\lvert \sum_{k=n}^m a_k\right\rvert\le \epsilon$$ if $m\ge n\ge N$.

**Thm** 3.23 
If $\sum a_n$ converges, then $\lim a_n = 0$.

**Thm** 3.24 (See **Thm** 3.14)
A series of nonnegative terms converges if and only if its partial sums form a bounded sequence.

**Thm** 3.25 
(a) If $|a_n|\le c_n$ for $n\ge N_0$, where $N_0$ is some fixed integer, and if $\sum c_n$ converges, then $\sum a_n$ converges.
(b) If $a_n\ge d_n\ge 0$ for $n\ge N_0$, and if $\sum d_n$ diverges, then $\sum a_n$ diverges.
*Proof*: 
(a) $$\left \lvert \sum_{k=n}^m a_k \right \rvert \le \sum_{k=n}^m |a_k| \le \sum_{k=n}^m c_k \le \epsilon$$
(b) Assume BWOC $\sum a_n$ converges. Then apply (a), so does $\sum d_n$. $\Rightarrow\Leftarrow$

## Series of Nonnegative Terms

**Thm** 3.26
If $0\le x < 1$, then $$\sum_{n=0}^\infty x^n = \frac{1}{1-x}.$$ If $x\ge 1$, the series diverges.
*Proof*:
$$\sum_{n=0}^\infty x^n = \sum_{n=0}^\infty\frac{1-x^{n+1}}{1-x} = \frac{1}{1-x}$$
Let $d_n = 1$, then $a_n = x^n$. When $x\ge 1$, $a_n\ge d_n$, so we can apply **Thm** 3.25(b). (QED)

**Thm** 3.27
Suppose $a_1\ge a_2\ge a_3 \ge \dots \ge 0$. Then the series $\sum_{n=1}^\infty a_n$ converges if and only if the series $$\sum_{k=1}^\infty 2^ka_{2^k} = a_1 + 2a_2 + 4a_4 + \dots$$ converges.

**Thm** 3.28 
$\sum\frac{1}{n^p}$ converges if $p>1$ and diverges if $p\le 1$. 
*Remark*: Notice that $$\sum_{k=0}^\infty 2^k\cdot \frac{1}{2^{kp}} = \sum_{k=0}^\infty 2^{(1-p)k}$$
**Thm** 3.29
If $p>1$, $$\sum_{n=2}^\infty \frac{1}{n(\log n)^p}$$ converges; if $p\le 1$, the series diverges.
*Remark*: We can still play the trick of **Thm** 3.27, $$\sum_{n=2}^\infty \frac{1}{n(\log n)^p} = \sum_{k=2}^\infty 2^k\frac{1}{2^k(k\log2)^p} =  \frac{1}{(\log 2)^p}\sum_{k=2}^\infty \frac{1}{k^p}$$ and then apply **Thm** 3.28.

### The Number $e$

**Def** 3.30 $e$
$$e = \sum_{n=0}^\infty \frac{1}{n!}$$

*Remark*: Binomial Theorem is used in the proof of the next theorem.
$$(x+y)^n = \sum_{k=0}^n \frac{n!}{k!(n-k)!}x^{n-k}y^k$$

**Thm** 3.31 
$$\lim_{n\rightarrow \infty}\left(1+\frac{1}{n}\right)^n = e$$

### The Root and Ratio Tests
**Thm** 3.33 Root Test
Given $\sum a_n$, put $\alpha = \limsup_{n\rightarrow \infty} \sqrt[n]{|a_n|}$. Then
(a) If $\alpha <1$, $\sum a_n$ converges;
(b) If $\alpha >1$, $\sum a_n$ diverges;
(c) If $\alpha = 1$, the test gives no information.

**Thm** 3.34 Ratio Test 
The series $\sum a_n$
(a) converges if $$\limsup_{n\rightarrow \infty} \left\lvert \frac{a_{n+1}}{a_n} \right\rvert<1$$
(b) diverges if $$\limsup_{n\rightarrow \infty} \left\lvert \frac{a_{n+1}}{a_n} \right\rvert\ge1$$ for all $n\ge n_0$, where $n_0\in \mathbb{N}$.

**Thm** 3.37
For any sequence $\{c_n\}$ of positive numbers, $$\liminf_{n\rightarrow\infty}\frac{c_{n+1}}{c_n}\le \liminf_{n\rightarrow\infty}\sqrt[n]{c_n}$$ $$\limsup_{n\rightarrow\infty}\sqrt[n]{c_n} \le \limsup_{n\rightarrow\infty}\frac{c_{n+1}}{c_n}$$
*Proof*: Let $$\beta = \liminf_{n\rightarrow \infty}\frac{c_{n+1}}{c_n}$$ If $\beta = -\infty$, then trivial. If $\beta$ is finite, choose some $\beta'<\beta$. Then, there is some $N\in \mathbb{N}$ s.t. $n\ge N$ implies $$\frac{c_{n+1}}{c_n}\ge \beta'$$ Then, $\forall p>0$,
$$\frac{c_{N+k+1}}{c_{N+k}}\ge \beta' \quad (k = 0, 1, \dots, p-1)$$ We can see then $$c_{N+p}\ge \beta'^p c_N$$ or $$c_n\ge c_N\beta'^{-N}\cdot \beta'^n$$
$$\sqrt[n]{c_n}\ge \sqrt[n]{c_N\beta'^{-N}}\cdot \beta'$$ so that $$\limsup_{n\rightarrow \infty}\sqrt[n]{c_n} \ge \beta'$$ Recall that this is true $\forall \beta'<\beta$, $$\limsup_{n\rightarrow \infty}\sqrt[n]{c_n} \ge \beta$$ The proof of the other equation, see Rudin pp. 68-69.

## Power Series

**Def** 3.38 Power series
(*I know what a power series is*)

**Thm** 3.39 
Given the power series $\sum c_n z^n$, put $$\alpha = \limsup_{n\rightarrow \infty}\sqrt[n]{|c_n|}, \quad R = \frac{1}{\alpha}.$$ Then the series conv. if $|z|<R$ and div. if $|z|>R$.

*Proof is simple with Root Test*

## Summation by Parts

**Thm** 3.41 
Given two sequences $\{a_n\}$, $\{b_n\}$, put $$A_n = \sum_{k=0}^n a_k$$ if $n\ge 0$; put $A_{-1} = 0$. Then, if $0\le p \le q$, we have $$\sum_{n=p}^q a_nb_n = \sum_{n=p}^{q-1}A_n(b_n-b_{n+1})+A_qb_q - A_{p-1}b_p.$$ *This is a discrete analogue of integration by parts.*
*Proof*: 
$$\begin{align*}
\sum_{n=p}^q a_nb_n &= \sum_{n=p}^q(A_n - A_{n-1})b_n\\
&= \sum_{n=p}^q A_nb_n - \sum_{n=p-1}^{q-1}A_nb_{n+1}\\
&= \sum_{n=p}^{q-1}A_n(b_n-b_{n+1})+A_qb_q - A_{p-1}b_p
\end{align*}$$
(QED)

**Thm** 3.43 Alternating Series Test
Suppose
(a) $|c_1|\ge|c_2|\ge \dots$
(b) $c_{2n-1}\ge 0$, $c_{2n}\le 0$.
(c) $\lim c_n = 0$.
Then $\sum c_n$ converges.

*Remark*: $a_n = (-1)^{n+1}, b_n = |c_n|$.

**Thm** 3.44 
Suppose that the radius of convergence of $$\sum_{n=0}^\infty c_nz^n$$ is 1. and $$c_0\ge c_1 \ge \dots$$ $$\lim_{n\rightarrow \infty}c_n = 0$$ Then the series converges on $\{z\mid |z|\le 1\} -\{1\}$.
*Proof*: $a_n = z^n$, $b_n = c_n$. $$|A_n| = \left\lvert \sum_{m=0}^n z^m\right\rvert  = \left\lvert \frac{1-z^{n+1}}{1-z}\right\rvert\le \frac{2}{|1-z|}$$ Every point on $\{z\mid |z|\le 1\} -\{1\}$ can make $|A_n|$ bounded. (QED)


## Absolute Convergence

**Thm** 3.45
If $\sum a_n$ converges absolutely, then $\sum a_n$ converges.
*Remark*: Easy proof with $\Delta$-inequality.

## Addition and Multiplication of Series

**Thm** 3.47 Addition and Scalar Multiplication (OK)

**Def** 3.48 Cauchy product or convolution
Given $\sum a_n$ and $\sum b_n$, then let $$c_n = \sum_{k=0}^n a_k b_{n-k},$$ then $\sum c_n$ is a *Cauchy product* or *convolution* of $\sum a_n$ and $\sum b_n$.

**Thm** 3.50
If $A=\sum_{n=0}^\infty a_n$ converges absolutely and $B=\sum_{n=0}^\infty b_n$ and $c_n = \sum_{k=0}^\infty a_k b_{n-k}$, then $$AB=\sum_{n=0}^\infty c_n$$
*Proof*: Let $$A(x) = \sum_{n\le x}a_n, \quad B(x) = \sum_{n\le x}b_n, \quad C(x) = \sum_{n\le x}c_n, \quad \beta_n = -B(n) +B$$$$\begin{align*}
C(n)&= a_0b_0 + (a_0b_1 + a_1b_0) + \dots + (a_0b_n + a_1b_{n-1} + \dots + a_nb_0)\\
&= a_0 B(n) + a_1 B(n-1)+ \dots + a_nB(0)\\
&= a_0 (B-\beta_n) + \dots + a_n(B-\beta_0)\\
&= A(n)B - (a_0+\beta_n + \dots + a_n\beta_0)
\end{align*}$$
Put $\gamma_n = a_0+\beta_n + \dots + a_n\beta_0$. Since $A(n)B\rightarrow AB$, it is enough to show $\gamma_n \rightarrow 0$ to prove this theorem. Let $\epsilon>0$, since $\beta_n\rightarrow 0$, for all $n\ge N$, $$|\beta_n|\le \epsilon.$$ For $n\ge N$, $$\begin{align*}
|\gamma_n|&\le |\beta_0a_n + \beta_N a_{n-N}|\\
&+|\beta_{N+1}a_{n-N-1} + \beta_n a_{0}|\\
&\le \underbrace{|\beta_0a_n + \beta_N a_{n-N}|}_{\text{every term}\rightarrow 0}+ \epsilon \alpha\\
&\le \epsilon \alpha
\end{align*}$$
Therefore, $\limsup_{n\rightarrow \infty}|\gamma_n| \le \epsilon \alpha$. Now we have $\gamma_n\rightarrow 0$. (QED)


