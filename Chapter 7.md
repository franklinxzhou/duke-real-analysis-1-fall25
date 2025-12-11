Sequences and Series of Functions

$\Longrightarrow$ Read Rudin "Discussion of Main Problem"
## Uniform Convergence
**Def** 7.7 Uniform Convergence 
We say that a sequence of functions $\{f_n\}$, $n=1,2,3,\dots$, *converges uniformly* on $E$ to a function $f$ if for every $\epsilon>0$ there is an integer $N$ s.t. $n\ge N$ implies $$|f_n(x) - f(x)|\le \epsilon$$ for all $x\in E$. 

**Thm** 7.8 Cauchy criterion (I like to call it as "uniformly Cauchy")
The sequence of functions $\{f_n\}$, defined on $E$, converges uniformly on $E$ if and only if $\forall \epsilon>0$, $\exists N\in \mathbb{N}$ s.t. $m\ge N, n\ge N, x\in E$ implies $$|f_n(x) - f_m(x)|\le \epsilon$$
*Proof*: Suppose that $\{f_n\}$ converges uniformly on $E$ to $f$. Then, fix an arbitrary $\epsilon>0$, we have $N\in \mathbb{N}$ s.t. if $m\ge N, n\ge N$, $$|f_n(x) - f(x)|\le \frac{\epsilon}{2}$$ $$|f_m(x) - f(x)|\le \frac{\epsilon}{2}$$
Using $\Delta$-inequality, $$|f_n(x) - f_m(x)|\le |f_n(x) - f(x)| + |f_m(x) - f(x)| \le \epsilon$$
Fix $\epsilon>0$. Suppose, $\exists N\in\mathbb{N}$ s.t. $|f_n(x) - f_m(x)|\le \epsilon$ if $n,m\ge N$, then $\forall x_0\in E$, the numerical sequence $\{f_n(x_0)\}$ is Cauchy. On complete set $E\subset \mathbb{R}$, $\{f_n(x_0)\}$ converges. Such limit depends on $x_0$ we choose and is therefore a function of $x_0$. We define the function $f(x)$ by this pointwise limit: $$f(x) = \lim_{n \to \infty} f_n(x)$$
Now, let's look at that Cauchy inequality again. Fix a specific $n \ge N$ and a specific $x \in E$. Consider the inequality as a condition on the index $m$: $$|f_n(x) - f_m(x)| \le \epsilon \quad \text{for all } m \ge N$$Now, keep $n$ and $x$ fixed, and let $m \to \infty$. Note the following facts: The term $f_n(x)$ is constant (relative to $m$); the term $f_m(x)$ converges to $f(x)$; the function $g(y) = |f_n(x) - y|$ is continuous. Therefore, by the continuity of the absolute value, we can take the limit of the inequality: $$\lim_{m \to \infty} |f_n(x) - f_m(x)| \le \epsilon$$$$|f_n(x) - \lim_{m \to \infty} f_m(x)| \le \epsilon$$$$|f_n(x) - f(x)| \le \epsilon$$
This statement satisfies the definition of uniform convergence. 
*Remark*: The original Rudin proof is vaguely worded. This one makes it more rigorous - it emphasizes that the limit is pointwise. 

**Thm** 7.9 
Suppose $$\lim_{n\to \infty} f_n(x) = f(x), \qquad x\in E$$
Put $$M_n = \sup_{x\in E}|f_n(x) - f(x)|.$$
Then $f_n\to f$ uniformly on $E$ if and only if $M_n\to 0$ as $n\to \infty$. 

**Thm** 7.10 Weierstrass M-Test
Suppose $\{f_n\}$ is a sequence of functions on $E$ and $|f_n(x)|\le M_n$, $\forall x\in E$. If $\displaystyle\sum_{n=1}^\infty M_n<\infty$ then $\displaystyle\sum_{n=1}^\infty f_n$ converges. 
*Proof*: If $\sum M_n$ converges, then $\{\sum M_n\}$ is Cauchy. Fix an arbitrary $\epsilon>0$, then $\exists N\in \mathbb{N}$, $m,n \ge N$ implies $$\sum_{i=1}^m M_i - \sum_{i=1}^n M_i\le \epsilon$$
Note that $$\sum_{i=1}^m f_i(x) - \sum_{i=1}^nf_i(x) = \sum_{i=n}^m f_i(x)$$ $$\sum_{i=1}^m M_i - \sum_{i=1}^n M_i = \sum_{i=n}^m M_i,$$
$$\left\lvert \sum_{i=n}^m f_i(x)\right\rvert \le\sum_{i=n}^m M_i\le \epsilon$$
Therefore, we can see $$\left \lvert \sum_{i=1}^m f_i(x) - \sum_{i=1}^nf_i(x) \right\rvert\le \epsilon,$$ which shows, by **Thm** 7.8, that $\sum f_n$ converges uniformly. 

## Uniform Convergence and Continuity
**Thm** 7.11
Suppose $f_n\to f$ uniformly on a set $E$ in a metric space. Let $x$ be a limit point of $E$, and suppose that $$\lim_{t\to x} f_n(t) = A_n, \qquad n=1,2,3,\dots$$
Then $\{A_n\}$ converges, and $$\lim_{t\to x}f(t) = \lim_{n\to\infty} A_n.$$
*Remark*: The conclusion is stating that the limits are commutable: $$\lim_{t\to x}\lim_{n\to \infty}f_n(t) = \lim_{n\to \infty}\lim_{t\to x} f_n(t)$$
*Proof*: Fix an arbitrary $\epsilon>0$. Since $f_n\to f$ uniformly, we apply the **Thm** 7.8 (Cauchy Criterion), and $\{f_n(t)\}$ is a Cauchy sequence piecewise $\forall t\in E$. This means $\exists N\in \mathbb{N}$ s.t. $n\ge N$, $m\ge N$, $t\in E$ imply $$|f_n(t) - f_m(t)|\le \epsilon.$$
If we take $t\to x$, $$\lim_{t\to x}|f_n(t) - f_m(t)| = |A_n - A_m|\le \epsilon$$
This implies that $\{A_n\}$ is a Cauchy sequence, which, on the complete set $E$, converges to some $A$. For the fixed $\epsilon$, we can find $N\in \mathbb{N}$ s.t. $n\ge N$ implies $|f(t) - f_n(t)| \le \epsilon/3$ and $|A_n-A|\le \epsilon/3. We can also limit $t$ within $B_\delta(x)$ s.t. $|f(t) - A_n|\le \epsilon/3$. Using the $\Delta$-inequality, $$|f(t) - A| \le |f(t) - f_n(t)| + |f_n(t) - A_n| + |A_n - A|\le \epsilon$$
Since $\epsilon$ is arbitrary, this follows $$\lim_{t\to x}f(t) = \lim_{n\to\infty} A_n.$$
**Thm** 7.12 
If $\{f_n\}$ is a sequence of continuous functions on $E$, and if $f_n\to f$ uniformly on $E$, then $f$ is continuous on $E$. 
*Proof*: Fix $\epsilon>0$. Then, since $f_n\to f$ uniformly, $\exists N\in \mathbb{N}$, $n\ge N$ implies $$|f_n(t) - f(t)| \le \frac{\epsilon}{3},$$ $$|f_n(x) - f(x)|\le\frac{\epsilon}{3};$$$\exists \delta>0$, $d(t,x)<\delta$ implies $$|f_n(t) - f_n(x)|<\frac{\epsilon}{3}.$$
As a result, this $\delta$ can ensure that $d(t,x)<\delta$ implies $$|f(x) - f(t)|\le |f(x) - f_n(x)| + |f_n(x) - f_n(t)| + |f_n(t) - f(t)| < \epsilon,$$ which proves the continuity of $f$.

**Thm** 7.13
Suppose $K$ is compact, and 
(a) $\{f_n\}$ is a sequence of continuous functions on $K$,
(b) $\{f_n\}$ converges pointwise to a continuous function $f$ on $K$,
(c) $f_n(x)\ge f_{n+1}(x)$ for all $x\in K$, $n=1,2,3,\dots$. 
Then $f_n\to f$ uniformly on $K$. 
*Proof*: Fix $\epsilon>0$. Let $g_n = f_n - f$, so 
(a) $\{g_n\}$ is a sequence of continuous functions on $K$,
(b) $g_n(x)\to 0$ pointwise, 
(c) $g_n(x)\ge g_{n+1}(x)$ for all $x\in K$, $n = 1,2,3,\dots$.

Therefore, if we let $K_n = \{x\in K: g_n(x)\ge \epsilon\}$, then since $\{g_n(x)\in g_n(K): g_n(x)\ge \epsilon\}$ is closed, $K_n$ is closed. Since $g_n\ge g_{n+1}$, if $g_{n+1}(x)\ge \epsilon$ then $g_n(x)\ge \epsilon$. This shows that $K_n\supset K_{n+1}$. 

Since $g_n(x)\to 0$ pointwise, $\forall x\in K$, $\exists N\in \mathbb{N}$ s.t. $n\ge N$ implies $g_n(x)< \epsilon$. Therefore, $\forall x\in K$, $x\notin K_n$ for some $n$. This means $$\bigcap K_n = \varnothing,$$ which follows, by **Thm** 2.36, that $\exists N\in \mathbb{N}, K_N=\varnothing$. Notice that $\forall n\ge N$, $K_n = \varnothing$; i.e., $\forall n\ge N$, $g_n(x)<\epsilon$. This is the very exact definition of $g_n\to 0$ uniformly. 

**Def** 7.14 $\mathscr{C}(X)$, supremum norm
IF $X$ is a metric space, $\mathscr{C}(X)$ will denote the set of all complex-valued, continuous, bounded functions with domain $X$. We associate with $f\in \mathscr{C}(X)$ with its *supremum norm*, $$\lVert f\rVert = \sup_{x\in X}|f(x)|$$
We can define a metric between $f \in \mathscr{C}(X)$ and $g\in \mathscr{C}(X)$ to be $\lVert f-g \rVert$. 

**Thm** 7.15 
The above metric makes $\mathscr{C}(X)$ into a complete metric space. 
*Proof*: Let $\{f_n\}$ be a Cauchy sequence on $\mathscr{C}(X)$. Then, $\forall \epsilon>0$, $\exists N\in \mathbb{N}$ s.t. $n,m\ge N$ implies $\lVert f_n - f_m \rVert <\epsilon$. Use the Cauchy criterion, we know for some $f$ with domain $X$, $f_n\to f$ uniformly. With **Thm** 7.12, this $f$ must be continuous; since $\exists n\in \mathbb{N}$, $|f(x) - f_n(x)|<1$, so $f$ is bounded. Then, $f\in \mathscr{C}(X)$, and the proof is done.

## Uniform Convergence and Integration
**Thm** 7.16
Let $\alpha$ be monotonically increasing on $[a,b]$. Suppose $f_n\in \mathscr{R}(\alpha)$ on $[a,b]$, for $n=1,2,3, \dots$, and suppose $f_n\to f$ uniformly on $[a,b]$. Then $f\in \mathscr{R}(\alpha)$ on $[a,b]$, and $$\int_a^b f\,d\alpha = \lim_{n\to \infty} \int_a^b f_n\,d\alpha$$
*Proof*: Suppose we have a $P = \{x_0, \dots, x_j\}$. Write $$U(P,f,\alpha) = \sum_{i=1}^j M_i \Delta \alpha_i,$$ $$L(P,f,\alpha) = \sum_{i=1}^j m_i \Delta \alpha_i,$$ then $$U(P,f,\alpha) - L(P,f,\alpha) = \sum_{i=1}^j (M_i - m_i)\Delta \alpha_i.$$
For a particular $n$, since $f_n\to f$ uniformly, we let $\epsilon_n = \sup |f_n(x) - f(x)|$, then $M_i\le \sup_{[x_{i-1},x_i]} f(x) +\epsilon_n$ because $\epsilon_n$ is the supremum taken over the entire $[a,b]$, $m_i \ge \inf_{[x_{i-1},x_i]} f(x) - \epsilon_n$. We get $$M_i - m_i \le \sup_{[x_{i-1},x_i]} f(x) - \inf_{[x_{i-1},x_i]}f(x) + 2\epsilon_n.$$
Then, $$U(P,f,\alpha) - L(P,f,\alpha) \le \sum_{i=1}^j\left(\sup_{[x_{i-1},x_i]} f(x) - \inf_{[x_{i-1},x_i]}f(x)\right)\Delta \alpha_i + 2\epsilon_n[\alpha(b) - \alpha(a)]$$
With $f_n\in \mathscr{R}(\alpha)$, the first term is arbitrarily small. With $\epsilon_n\to 0$ as $n\to \infty$, so is the second term with a sufficiently large $n$. These follow $f\in \mathscr{R}(\alpha)$. 
## Uniform Convergence and Differentiation
**Thm** 7.17
Suppose $\{f_n\}$ is a sequence of functions, differentiable on $[a,b]$ and such that $\{f_n(x_0)\}$ converges for some point $x_0$ on $[a,b]$. If $\{f'_n\}$ converges uniformly on $[a,b]$. If $\{f'_n\}$ converges uniformly on $[a,b]$, then $\{f_n\}$ converges uniformly on $[a,b]$, to a function $f$, and $$f'(x) = \lim_{n\to \infty} f'_n(x)$$
*Proof*: We need to show three things:
(a) $\{f_n\}$ converges uniformly on $[a,b]$. 
Fix an arbitrary $\epsilon>0$. Since for at least one $x_0$, $\{f_n(x_0)\}$ converges, the numerical sequence $\{f_n(x_0)\}$ is Cauchy. In other words, $\exists N\in \mathbb{N}$, $n,m\ge N$ implies $$|f_n(x_0) - f_m(x_0)|<\frac{\epsilon}{2}$$
Note also $\{f'_n\}$ uniformly converges. Using the Cauchy criterion, $$|f'_n(t) - f'_m(t)|<\frac{\epsilon}{2(b-a)}$$
It is possible to use a single $N$ for the two, because we can always take the maxmimum. Then, with the mean value theorem trick, for some $\zeta$ between $x$ and $t$, $$|(f_n(x) - f_m(x)) - (f_n(t) - f_m(t))| \le |x-t| |f'_n(\zeta) - f'_m(\zeta)|$$ $$|(f_n(x) - f_m(x)) - (f_n(t) - f_m(t))| \le \frac{|x-t|\epsilon}{2(b-a)}\le \frac{\epsilon}{2}$$
Let $t = x_0$, $$|f_n(x) - f_m(x)|\le |(f_n(x) - f_m(x)) - (f_n(t) - f_m(t))| + |f_n(x_0) - f_m(x_0)|\le \epsilon$$ $$|f_n(x) - f_m(x)|< \epsilon,$$ which follows that $\{f_n\}$ uniformly converges, using the Cauchy criterion. 

(b) $f'(x) = \lim_{n\to \infty}f'_n(x)$. 
Notice that this equation can be rewritten as $$\lim_{n\to\infty}\lim_{t\to x}\frac{f_n(t) - f_n(x)}{t-x} = \lim_{t\to x}\lim_{n\to\infty}\frac{f_n(t) - f_n(x)}{t-x}$$
Before we can draw this conclusion with **Thm** 7.11, we need to prove one last thing: Define $$\phi_n(t) = \frac{f_n(t) - f_n(x)}{t-x},$$ then $\phi_n(t)$ converges. Recall $$|(f_n(x) - f_m(x)) - (f_n(t) - f_m(t))| \le \frac{|x-t|\epsilon}{2(b-a)}\le \frac{\epsilon}{2},$$ then $$|\phi_n(t) - \phi_m(t)|\le \frac{\epsilon}{2(b-a)},$$ for $n\ge N, m\ge N$. Using Cauchy criterion, $\{\phi_n\}$ indeed uniformly converges. Then, we use **Thm** 7.11 (commuting limits) to show $f'(t) = \lim_{n\to \infty} f'_n(x)$. 


**Thm** 7.18
There exists a real continuous function on the real line which is nowhere differentiable.
*Remark*: There is an example $$f(x) = \sum_{n=0}^\infty \left(\frac{3}{4}\right)^n \varphi(4^nx)$$

## Equicontinuous Families of Functions
**Def** 7.19 Pointwise bounded; uniformly bounded
Let $f_n: E\rightarrow \mathbb{C}$. $\{f_n\}$ is *pointwise bounded* on $E$ if $\{f_n(x)\}$ is bounded $\forall x\in E$. $\Leftrightarrow$ $|f_n(x)|\le \phi(x)$ for some function $\phi: E\rightarrow \mathbb{R}$ and all $x\in E$. 

$\{f_n\}$ is *uniformly bounded* if $\exists M$ s.t. $|f_n(x)|\le M$, $\forall x\in E$. 

**Def** 7.22 Equicontinuous
A family $\mathscr{F}$ of complex functions $f$ defined on a set $E$ in a metric space $X$ is said to be *equicontinuous* on $E$ if $\forall \epsilon>0$, $\exists \delta>0$ s.t. $$|f(x) - f(y)|<\epsilon$$ whenever $d(x,y)<\delta$, $x\in E$, $y\in E$, and $f\in \mathscr{F}$. 

**Thm** 7.23 Cantor Diagonalization Process
If $\{f_n\}$ is a pointwise bounded sequence of complex functions on a countable set $E$, then $\{f_n\}$ has a subsequence $\{f_{n_k}\}$ s.t. $\{f_{n_k}(x)\}$ converges for every $x\in E$. 
*Proof*: We start from the master sequence $\{f_n\}$. Then, since $\{f_n\}$ is pointwise bounded (i.e., $\forall x_i\in E$, $\{f_n(x_i)\}$ is bounded), $\forall x_i\in E$, there is a subsequence of $\{f_n\}$ converging for $x_i$. Take the subsequence converging for $x_1$, we call it $\{f_{1,k}\}$. Then, we know that $\{f_{1,k}\}$ is pointwise bounded, there is a subsequence of $\{f_{1,k}\}$ converging for $x_2$, we call it $\{f_{2,k}\}$. Continuing this process, $$\begin{matrix} S_1: & f_{1,1} & f_{1,2} & f_{1,3} & f_{1,4} & \dots & (\text{Conv. at } x_1) \\ S_2: & f_{2,1} & f_{2,2} & f_{2,3} & f_{2,4} & \dots & (\text{Conv. at } x_1, x_2) \\ S_3: & f_{3,1} & f_{3,2} & f_{3,3} & f_{3,4} & \dots & (\text{Conv. at } x_1, x_2, x_3) \\ \vdots & \vdots & \vdots & \vdots & \vdots & & \end{matrix}$$
This process will go infinitely, since $E$ can have infinitely many elements. There is a trick: We take the subsequence $\{f_{1,1}, f_{2,2}, \dots\}$. It is a subsequence of $S_i$, for all $i$. Then, $\{f_{n,n}(x_i)\}$ converges as $n\to \infty$ for all $x_i\in E$. 

**Thm** 7.24 From uniform convergence to equicontinuity
If $K$ is a compact metric space, if $f_n\in \mathscr{C}(K)$ for $n=1,2,3,\dots$, and if $\{f_n\}$ converges uniformly on $K$, then $\{f_k\}$ is equicontinuous on $K$. 
*Proof*: Fix $\epsilon>0$. Since $\{f_n\}$ uniformly converges, $\exists f$ where $f_n\to f$ uniformly. With **Thm** 7.2, $f$ is continuous. Citing the fact that $K$ is compact, $f$ is uniformly continuous.

Then, $\exists N\in \mathbb{N}$, if $n>N$ and $d(x,y)<\delta$, from uniform convergence, $$|f_n(x) - f(x)| < \frac{\epsilon}{3}$$ $$|f(y) - f_n(y)|<\frac{\epsilon}{3}$$
From uniform continuity, $$|f(x)-f(y)|<\frac{\epsilon}{3}$$
With $\Delta$-inequality, $$|f_n(x) - f_n(y)|\le |f_n(x) - f(x)| + |f(x)-f(y)| + |f(y) - f_n(y)| < \epsilon,$$ so $\{f_n\}_{n=N+1}^\infty$ is equicontinuous on $K$. We still need to take care of the finite tail, where $n = 1, \dots, N$. They are uniformly continuous, so $\exists \delta_n$ s.t. if $d(x,y)<\delta_n$,  $$|f_n(x) - f_n(y)|<\epsilon.$$
We find the final threshold of $d(x,y)$ by taking the minimum of $\{\delta, \delta_1, \dots, \delta_N\}$. Then, we have proven that $\{f_n\}$ is equicontinuous. 

**Thm** 7.25 Arzelà-Ascoli Theorem
If $K$ is compact, if $f_n\in \mathscr{C}(K)$ for $n=1,2,3,\dots$, and if $\{f_n\}$ is pointwise bounded and equicontinuous on $K$, then 
(a) $\{f_n\}$ is uniformly bounded on $K$,
(b) $\{f_n\}$ contains a uniformly convergent subsequence. 
*Proof*: To prove (a), fix an arbitrary $\epsilon>0$. Then, $\exists \delta$ s.t. $d(x,y)<\delta$ implies $|f_n(x) - f_n(y)|<\epsilon$. Since $K$ is compact, it admits a finite open cover. Suppose this open cover is a collection of open balls with a radius of $\delta$ centered at $p_i$, $i = 1,\dots, j$, then $\forall x\in K$, $x\in B_\delta(p_i)$ for some $i$. 

For this specific $p_i$, $\exists M_i<\infty$ s.t. $f_n(p_i)<M_i$ for all $n$ because $\{f_n\}$ is pointwise bounded. Put $M = \max \{M_i\}$, then $|f_n(x)| < M+\epsilon$. This proves the uniform boundedness. 

For (b), $\exists E\subset K$ which is countable and dense in $K$ (See Exercise 25, Chapter 2). We have proven in **Thm** 7.23 that if $\{f_n\}$ is countable and pointwise bounded, then $\exists$ a subsequence $\{f_{n_k}(x)\}$ converging for every $x\in E$. This shows that $\{f_{n_k}\}$ piecewise converges on $K$. 

Recall to prove (a), we have constructed balls $\{B_\delta(p_i)\}$ that covers $K$. Since $\{f_{n_k}\}$ piecewise converges on $K$, forall $p_i$, we have $N\in \mathbb{N}$ s.t. if $r,s \ge N$, $$|f_{n_r}(p_i) - f_{n_s}(p_i)|<\frac{\epsilon}{3}$$

Notice that since we put an arbitrary $x\in K$ in one of the balls, $d(x,p_i)<\delta$. Equicontinuity gives $$|f_{n_r}(x) - f_{n_r}(p_i)|<\frac{\epsilon}{3}$$
$$|f_{n_s}(x) - f_{n_s}(p_i)|<\frac{\epsilon}{3}$$
Using $\Delta$-inequality, $$|f_{n_r} (x) - f_{n_s}(x)| \le |f_{n_r}(x) - f_{n_r}(p_i)| + |f_{n_r}(p_i) - f_{n_s}(p_i)| + |f_{n_s}(x) - f_{n_s}(p_i)| < \epsilon,$$ which proves that $\{f_{n_k}\}$ is a uniformly convergent subsequence. 

## The Stone-Weierstrass Theorem
**Thm** 7.26 The First Version: Weierstrass Approximation Theorem
If $f$ is a continuous complex function on $[a,b]$, there exists a sequence of polynomials $P_n$ s.t. $$\lim_{n\to \infty} P_n(x) = f(x)$$ uniformly on $[a,b]$. If $f$ is real, the $P_n$ may be taken real. 
*Proof*: In the first step, we standardize the integral. *Rudin briefly justified why it is okay to let $[a,b]=[0,1]$ WLOG.* Let $[a,b] = [0,1]$, $f(0) = 0$, $f(1) = 0$, $f(x) = [0,1]$. Also define $f(x) = 0, \forall x\notin [0,1]$ but $x\in \mathbb{R}$. 

Construct a "tube", $$Q_n(x) = c_n(1-x^2)^n,$$ where $c_n$ is chosen s.t. $$\int_{-1}^1 Q_n(x)\,dx = 1$$ Since $$\int_{-1}^1 (1-x^2)^n\,dx >\frac{1}{\sqrt{n}},$$ $c_n<\sqrt{n}$ and on $\delta\le |x| \le 1$, $$Q_n(x)\le \sqrt{n}(1-\delta^2)^n$$ This also follows that $Q_n(x)\to 0$ in $\delta\le |x|\le 1$. 

Put $$P_n(x) = \int_{-1}^1 f(x+t)Q_n(t)\,dt, \qquad 0\le |x|\le 1$$
Here is the change-of-variable trick: We aim to find the range of $t$ s.t. $x+t\in[0,1]$. This gives that $t\in [-x,1-x]$. $$P_n(x) = \int_{-x}^{1-x} f(x+t)Q_n(t)\,dt$$
Let $u = x+t$, then $t=u-x$ and $u=0$ when $t=-x$, $u=1$ when $t=1-x$. $$P_n(x) = \int_0^1f(u)Q_n(u-x)\,du$$
We keep using $t$, $$P_n(x) = \int_0^1 f(t)Q_n(t-x)\,dt$$
Since $f$ is continuous, given an $\epsilon>0$, $\exists \delta>0$, $|y-x|<\delta$ implies $$|f(y) - f(x)|<\frac{\epsilon}{2}$$
Since we are going to bound $|P_n(x) - f(x)|$, we notice the identity: $$f(x) = f(x)\int_{-1}^1 Q_n(t)\,dt = \int_{-1}^1 f(x)Q_n(t)\,dt$$
This follows $$|P_n(x) - f(x)| \le \int_{-1}^1 |f(x+t) - f(x)| Q_n(t)\,dt$$ Now, we can divide the range of $t$, $[-1,1]$ into two parts. For the first part, $|t|<\delta$ s.t. $f(x+t)$ is close to $f(x)$ due to continuity. $$\int_{-\delta}^\delta |f(x+t) - f(x)|Q_n(t)\,dt \le \frac{\epsilon}{2}\int_{-\delta}^{\delta} Q_n(t)\,dt \le \frac{\epsilon}{2}$$
For the second part, $\delta \le |t| \le 1$, we leverage the supremum of $|f(x)|$ over $[-1,1]$ to bound $|f(x+t) - f(t)|$. If $M = \sup |f(x)|$, $|f(x+t) - f(t)|\le 2M$. $$\int_{\delta\le |t|\le 1}|f(x+t)-f(x)|Q_n(t)\,dt \le 2M\left(\int_{-1}^{-\delta} Q_n(t)\,dt + \int_\delta^1 Q_n(t)\,dt\right)\le 4M\sqrt{n}(1-\delta^2)^n$$
As a result, $$|P_n(x) - f(x)|\le \frac{\epsilon}{2} + 4M\sqrt{n}(1-\delta^2)^n$$

**Def** 7.28 Algebra; uniformly closed; uniform closure
A family $\mathscr{A}$ of complex functions defined on a set $E$ is said to be an *algebra* if (i) $f+g \in \mathscr{A}$, (ii) $fg\in \mathscr{A}$, and (iii) $cf\in \mathscr{A}$ for all $f\in \mathscr{A}$, $g\in \mathscr{A}$ and for all complex constants $c$. 

If $\mathscr{A}$ has the property that $f\in \mathscr{A}$ whenever $f_n\in \mathscr{A}$ ($n\in \mathbb{N}$) and $f_n\to f$ uniformly on $E$, then $\mathscr{A}$ is said to be *uniformly closed*.

If $\mathscr{B}$ be the set of all functions which are limits of uniformly convergent sequences of members of $\mathscr{A}$. Then $\mathscr{B}$ is called the *uniform closure* of $\mathscr{A}$. 

**Thm** 7.29
Let $\mathscr{B}$ be the uniform closure of an algebra $\mathscr{A}$ of bounded functions. Then $\mathscr{B}$ is a uniformly closed algebra.

**Def** 7.30 Separate points; vanish at no point
Let $\mathscr{A}$ be a family of functions on a set $E$. Then $\mathscr{A}$ is said to *separate points* on $E$ if to every pair of distinct points $x_1, x_2\in E$ there corresponds a function $f\in \mathscr{A}$ s.t. $f(x_1)\ne f(x_2)$. 

If to each $x\in E$ there corresponds a function $g\in \mathscr{A}$ s.t. $g(x)\ne 0$, we say that $\mathscr{A}$ *vanishes at no point* of $E$. 

**Thm** 7.31
Suppose $\mathscr{A}$ is an algebra of functions on a set $E$, $\mathscr{A}$ separates points on $E$, and $\mathscr{A}$ vanishes at no point of $E$. Suppose $x_1, x_2$ are distinct points of $E$, and $c_1, c_2$ are constants (real if $\mathscr{A}$ is an algebra). Then $\mathscr{A}$ contains a function $f$ such that $f(x_1)=c_1$, $f(x_2)=c_2$. 

**Thm** 7.32 The Stone-Weierstrass Theorem
Let $\mathscr{A}$ be an algebra of real continuous functions on a compact set $K$. If $\mathscr{A}$ separates points on $K$ and if $\mathscr{A}$ vanishes at no point of $K$, then uniform closure $\mathscr{B}$ of $\mathscr{A}$ consists of all real continuous functions on $K$. 
*Proof*:
STEP 1: If $f\in \mathscr{B}$, then $|f| \in \mathscr{B}$. 
Let $\alpha = \sup |f(x)|$ over $K$ and fix an arbitrary $\epsilon>0$. Resulting from **Thm** 7.26 we can construct a polynomial $g(y) = \sum_{i=1}^n c_iy^i$, where $y = f(x)$, $c_1,\dots, c_n\in \mathbb{R}$, s.t. $$\left\lvert \sum_{i=1}^n c_i(f(x))^i - |f(x)|\right\rvert <\epsilon.$$
Since $\mathscr{B}$ is an algebra, $g\in \mathscr{B}$. Then, by $|g(x) - |f(x)||<\epsilon$, $g(x)\to |f(x)|$ uniformly. Since $\mathscr{B}$ is uniformly closed, $|f|\in \mathscr{B}$. 

STEP 2: If $f\in \mathscr{B}$ and $g\in \mathscr{B}$, then $\max(f,g) \in \mathscr{B}$ and $\min(f,g)\in \mathscr{B}$. 
*Remark*: $$\max (f,g) = \frac{f+g}{2} + \frac{|f-g|}{2}$$ $$\min(f,g) = \frac{f+g}{2} - \frac{|f-g|}{2}$$
STEP 3: Given a real function $f$, continuous on $K$, a point $x\in K$, and $\epsilon>0$, there exists a function $g_x\in \mathscr{B}$ s.t. $g_x(x) = f(x)$ and $$g_x(t)>f(t)-\epsilon$$
$\forall y\in K$, $\exists$ a local scanner $h_y\in \mathscr{B}$ s.t. $h_y(x) = h(x)$, $h_y(y) = h(y)$. Notice that $f$ is continuous, so denote the open set around $y$ as $J_y$, $\forall t\in J_y$, $$h_y(t)>f(t) - \epsilon$$
Since $K$ is compact, we can find a finite cover, centered at a finite set of points $y_1, \dots, y_n$. Let $g_x = \max (h_{y_1}, \dots, h_{y_n})$. Following Step 2, this step is done. 

STEP 4: Given a real function $f$, continuous on $K$, and $\epsilon>0$, $\exists$ a function $h\in \mathscr{R}$ s.t. $$|h(x) - f(x)|<\epsilon$$ for all $x\in K$. 

In Step 3's way, we can construct $g_x$ for each $x\in K$, with $g_x(x)=f(x)$ and $g_x(t)>f(t) - \epsilon$. Since $g_x, f$ are both continuous, $$g_x(t)<f(t)+\epsilon$$ in some open set containing $x$, denoted as $V_x$. Again, using compactness of $K$, $$K\subset \bigcup_{i=1}^m V_{x_i},$$ centered at $x_i$. Here, we define $$h(t) = \min(g_{x_1}, \dots, g_{x_m}).$$ With the conclusion of Step 2, $h(t)\in \mathscr{B}$. 

With the conclusion of Step 3, we have proven the "floor", $$h(t)>f(t) - \epsilon$$
By the construction here, we set a "ceiling" for $h$, $$h(t)<f(t)+\epsilon$$
This concludes $$|h(x) - f(x)|<\epsilon.$$ Since $\mathscr{B}$ is uniformed closed, this arbitrary $f\in \mathscr{B}$ and it is the end of the Stone-Weierstrass Theorem. 

**Thm** 7.33 
Suppose $\mathscr{A}$ is a self-adjoint algebra of complex continuous functions on a compact set $K$, $\mathscr{A}$ separates points on $K$, and $\mathscr{A}$ vanishes at no point of $K$. Then the uniform closure $\mathscr{B}$ of $\mathscr{A}$ consists of all complex continuous functions on $K$; i.e., $\mathscr{A} is dense in $\mathscr{C}(K)$. 

