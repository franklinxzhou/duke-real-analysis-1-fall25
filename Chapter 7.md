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
## Uniform Convergence and Integration

## Uniform Convergence and Differentiation

## Equicontinuous Families of Functions

## The Stone-Weierstrass Theorem
