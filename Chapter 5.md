Differentiation
## The Derivative of a Real Function
**Def** 5.1 Derivative of a real function
Let $f$ be defined (and real-valued) on $[a,b]$. For any $x\in [a,b]$ form the quotient $$\phi(t) = \frac{f(t) - f(x)}{t-x} \qquad (a<t<b, t\ne x)$$ and define $$f'(x) = \lim_{t\rightarrow x}\phi(t),$$ provided this limit exists. We call $f'$ the *derivative* of $f$. If $f'$ is defined at a point $x$, we say that $f$ *differentiable* at $x$. 

**Thm** 5.2 Differentiable $\Rightarrow$ Continuous
Let $f$ be defined on $[a,b]$. If $f$ is differentiable at a point $x\in [a,b]$, then $f$ is continuous at $x$. 

*Remark*: Rudin proves this theorem elegantly by showing $t\to x$ implies $f(t) - f(x)\to 0$, which is equivalent with the traditional $\epsilon-\delta$ way. 

**Thm** 5.3 
Suppose $f$ and $g$ are defined on $[a,b]$ and are differentiable at a point $x\in [a,b]$. Then $f+g$, $fg$, and $f/g$ are differentiable at $x$, and 
(a) $(f+g)'(x) = f'(x) + g'(x)$
(b) $(fg)'(x) = f'(x)g(x) + f(x)g'(x)$
(c) $\displaystyle\left(\frac{f}{g}\right)'(x) = \frac{g(x)f'(x)-g'(x)f(x)}{g^2(x)}$
*Proof* of (b), (c):
Let $h = fg$. Then, 
$$\begin{align*}
h(t) - h(x) &= f(t)g(t) - f(x)g(x)\\
&= f(t)g(t) - f(t)g(x) + f(t)g(x) - f(x)g(x)\\
&= f(t)(g(t) - g(x)) + g(x)(f(t) - f(x))
\end{align*}$$
$$\lim_{t\to x}\frac{h(t) - h(x)}{t-x} = f(x)\lim_{t\to x}\frac{g(t) - g(x)}{t-x} + g(x)\lim_{t\to x}\frac{f(t) - f(x)}{t-x}$$ $$h'(x) = f(x)g'(x) + f'(x)g(x)$$
Let $h = f/g$. Then, 
$$\begin{align*}
h(t) - h(x) &= \frac{f(t)}{g(t)} - \frac{f(x)}{g(x)}\\
&= \frac{1}{g(t)g(x)}[f(t)g(x) - f(x)g(t)]\\
&= \frac{1}{g(t)g(x)}[f(t)g(x) - f(x)g(x) + f(x)g(x) - f(x)g(t)]\\
&= \frac{1}{g(t)g(x)}[g(x)(f(t) - f(x)) - f(x)(g(t) - g(x))]
\end{align*}$$
$$\lim_{t\to x} \frac{h(t)-h(x)}{t-x} = \lim_{t\to x}\frac{1}{g(t)g(x)}\left[g(x)\frac{f(t) - f(x)}{t-x} - f(x)\frac{g(t) - g(x)}{t-x}\right]$$ $$h'(x) = \frac{f'(x)g(x) - f(x)g'(x)}{g^2(x)}$$
**Thm** 5.5
Suppose $f$ is continuous on $[a,b]$, $f'(x)$ exists at some point $x\in [a,b]$, $g$ is defined on an interval $I$ which contains the range of $f$, and $g$ is differentiable at the point $f(x)$. If $$h(t) = g(f(t))$$ then $h$ is differentiable at $x$, and $$h'(x) = g'(f(x))f'(x)$$
*Proof*: Let $t\in [a,b]$, $s = f(t)$, $y = f(x)$. We introduce the error terms $u(t)\to 0$ as $t\to x$, $v(s)\to 0$ as $s\to y$. Then, $$f(t) - f(x) = (t-x)(f'(t)+u(t))$$ $$g(s) - g(y) = (s-y)(g'(y)+v(s))$$
Then, $$\begin{align*}
h(t) - h(x) &= g(f(t)) - g(f(x))\\
&= (f(t) - f(x))(g'(y)+v(s))\\
&= (t-x)(f'(x)+u(t))(g'(y)+v(s))
\end{align*}$$
Thus, as $t\to x$,
$$\lim_{t\to s}\frac{h(t) - h(x)}{t-x} = \lim_{t\to s}(f'(x)+u(t))(g'(f(x))+v(s)) = f'(x)g'(f(x))$$

## Mean Value Theorems
**Def** 5.7 Local maximum; local minimum (*defined likewise*)
Let $f$ be a real function defined on a metric space $X$. We say that $f$ has a *local maximum* at a point $p\in X$ if $\exists \delta>0$ s.t. $f(q)\le f(p)$, $\forall q\in B_\delta(p)$. 

**Thm** 5.8
Let $f$ be defined on $[a,b]$; if $f$ has a local maximum at a point $x\in (a,b)$, and if $f'(x)$ exists, then $f'(x) = 0$. 
*Proof*: Fix $\delta>0$, $a<x-\delta < x < x+\delta <b$ s.t. $f(x) = \max\{f(y)\mid y\in B_\delta(x)\}$. For $x-\delta<t<x$, $$\frac{f(t) - f(x)}{t-x}\ge 0 \Rightarrow \lim_{t\to x}\frac{f(t) - f(x)}{t-x}\ge 0 \Rightarrow f'(x) \ge 0$$
For $x<t<x+\delta$, $$\frac{f(t) - f(x)}{t-x}\le 0 \Rightarrow \lim_{t\to x}\frac{f(t) - f(x)}{t-x}\le 0 \Rightarrow f'(x) \le 0$$
Therefore, $f'(x) =0$. (QED)

**Thm** 5.9 Precursor of MVT; Cauchy's MVT
If $f$ and $g$ are continuous real functions on $[a,b]$ which are differentiable in $(a,b)$, then there is a point $x\in (a,b)$ at which $$[f(b) - f(a)]g'(x) = [g(b)-g(a)]f'(x)$$
*Proof*: Let $h(x) = [f(b) - f(a)]g(x) - [g(b)-g(a)]f(x)$. Notice that $h(a) = [f(b) - f(a)]g(a) - [g(b)-g(a)]f(a) = f(b)g(a) - g(b)f(a)$ and $h(b) = f(b)g(a) - g(b)f(a)$. This means $h(a) = h(b)$. 

Notice that $f$ and $g$ are differentiable in $(a,b)$, then $$h'(x) = [f(b) - f(a)]g'(x) - [g(b)-g(a)]f'(x)$$
We want $\exists x\in (a,b)$ s.t. $h'(x) =0$. If $h(x)$ remains a constant throughout $(a,b)$, then the proof is done. If $\exists x\in (a,b)$ s.t. $h(x)> h(a)$, then with Extreme Value Theorem, $h$ reaches its global max and min somewhere in $[a,b]$. Since $h$ is nonconstant on $[a,b]$, it is impossible that $h$ attains its global extreme values at both end points. This follows that either $$h(c) = \max_{x\in[a,b]}h(x)\qquad \text{or}\qquad h(c) = \min_{x\in[a,b]}h(x)$$ for some $c\in (a,b)$. These global extreme values are automatically local extreme values, so at such $c$, $h'(c) = 0$. 

Since we have proven that $\exists x\in(a,b)$ s.t. $h'(x) = 0$, at such point, $[f(b) - f(a)]g'(x) = [g(b)-g(a)]f'(x)$. 

**Thm** 5.10 Mean Value Theorem
If $f$ is a continuous real function on $[a,b]$ which is differentiable in $(a,b)$, then there is a point $x\in (a,b)$ at which $$f(b) - f(a) = (b-a)f'(x)$$ 
*Remark*: MVT is a special case of Cauchy's MVT when $g(x) = x$. This follows the theorem connecting the signs of the derivative and the monotonicity of functions:

**Thm** 5.11
Suppose $f$ is differentiable in $(a,b)$, 
(a) If $f'(x)\ge 0$ for all $x\in (a,b)$, then $f$ is monotonically increasing.
(b) If $f'(x) = 0$ for all $x\in (a,b)$, then $f$ is constant.
(c) If $f'(x) \le 0$ for all $x\in (a,b)$, then $f$ is monotonically decreasing.

## The Intermediate Values of Derivatives

**Thm** 5.12 Darboux's Theorem
Suppose $f$ is a real differentiable function on $[a,b]$ and suppose $f'(a)<\lambda<f'(b)$. Then, there is a point $x\in (a,b)$ s.t. $f'(x) = \lambda$. 
*Proof*: We construct a new auxiliary function $g(x)$; notice, $g'(x) = f'(x) - \lambda$, so $g'(x) = 0$ when $f'(x) = \lambda$. On this compact interval $[a, b]$, since $g$ is continuous, $g$ must attain its minimum for some $x\in [a, b]$. Since we are given that $f'(a)<\lambda < f'(b)$, at $a$, $g'(a) = f'(a) - \lambda < 0$, so $\exists t_1\in (a,b)$ around $a$, s.t. $g(t_1)>g(a)$; at $b$, $g'(b) = f'(b) - \lambda>0$, so $\exists t_2\in (a,b)$ around $b$, s.t. $g(t_2)<g(b)$. Therefore, this minimum can be attained at neither $a$ or $b$. Then, $\exists x\in (a,b)$, $g$ attains its minimum. At this $x$, $g'(x) = 0$, which follows $f'(x) = \lambda$. 
## L'Hospital's Rule

**Thm** 5.13 L'Hospital's Rule
Suppose $f$ and $g$ are real and differentiable in $(a,b)$, and $g'(x) \ne 0$ for all $x\in (a,b)$, where $-\infty \le a<b \le +\infty$. Suppose $$\frac{f'(x)}{g'(x)}\to A \text{ as }x\to a.$$ If (1) $$f(x)\to 0\text{ and }g(x)\to 0 \text{ as }x\to a,$$ or if (2) $$g(x)\to +\infty\text{ and }x\to a,$$ then $$\frac{f(x)}{g(x)}\to A\text{ as }x\to a.$$
*Remark*: The proof is long and confusing, and in the lecture only condition (1) is proven. Here is the game plan:
1. Use the Cauchy's Mean Value Theorem to turn $f/g$ to $f'/g'$.
2. Use the 0/0 limit fact to kill off extra terms.
3. Trap the result between an upper bound, $q$, and a lower bound, $p$. 

*Proof* for Condition (1): Assume that $A$ is finite. Choose $q\in \mathbb{R}$ s.t. $A<q$, and $r\in \mathbb{R}$ s.t. $A<r<q$.  Then, $\exists c\in (a,b)$ s.t. if $a<x<c$, then $\frac{f'}{g'}<r$. 

Let $y\in (x,c)$. By Cauchy's mean value theorem, as $a<x<y<c$, $\exists t\in (x,y)$, $$[f(x) - f(y)]g'(t) = [g(x) - g(y)]f'(t)$$ $$\frac{f(x) - f(y)}{g(x) - g(y)} = \frac{f'(t)}{g'(t)} < r$$
Since $f(x) \to 0$, $g(x)\to 0$ as $x\to a$, $$\lim_{x\to a}\frac{f(x) - f(y)}{g(x) - g(y)} = \frac{-f(y)}{-g(y)} = \frac{f(y)}{g(y)}\le r <q$$
On the other hand, $\forall p< A$, $\exists c_2$ s.t. $\frac{f'(x)}{g'(x)}>p$ for $a<x<c_2$. Then, using Cauchy's MVT again, for $a<x<y<c_2$, $t\in (x,y)$, $$\frac{f(x) - f(y)}{g(x) - g(y)} = \frac{f'(t)}{g'(t)} >p $$
As $x\to a$, $$\frac{f(y)}{g(y)}\ge p$$
Since $p$, $r$ are arbitrarily close to $A$, $$\frac{f(y)}{g(y)}\to A$$ as $y\to a$. 

*Proof* for Condition (2): Fix an arbitrary $\epsilon>0$, since $$\frac{f'(x)}{g'(x)}\to A$$ as $x\to a$. $\exists y\in (a,b)$ s.t. $\forall t\in (a,y)$, $$\left\lvert \frac{f'(t)}{g'(t)} - A\right\rvert<\frac{\epsilon}{2}$$
This bounds $f'/g'$ as $$A - \frac{\epsilon}{2} < \frac{f'(t)}{g'(t)} < A + \frac{\epsilon}{2}$$
By Cauchy's mean value theorem, $\exists \zeta\in (x,y)$ s.t. $$\frac{f(x) - f(y)}{g(x) - g(y)} = \frac{f'(\zeta)}{g'(\zeta)}$$
Since $\zeta\in (x,y)$, $a<x$, $\zeta\in (a,y)$. Then, $$A - \frac{\epsilon}{2} < \frac{f(x) - f(y)}{g(x) - g(y)} < A + \frac{\epsilon}{2}$$
As a reminder, we investigate the limit of $f/g$, so $$\frac{f(x)}{g(x)} = \frac{f(x) - f(y)}{g(x) - g(y)}\left(1-\frac{g(y)}{g(x)}\right) + \frac{f(y)}{g(x)}$$
Take the limit as $x\to a$, $$\lim_{x\to a} \frac{f(x)}{g(x)} = \lim_{x\to a}\frac{f(x) - f(y)}{g(x) - g(y)} = A$$
## Derivatives of Higher Orders

**Def** 5.14 

## Taylor's Theorem

**Thm** 5.15 Taylor Theorem
Suppose $f:[a,b]\rightarrow \mathbb{R}$, $n>0$, $f^{(n-1)}$ is continuous on $[a,b]$. Let $a\le \alpha< \beta \le b$ and define $$P(t) = \sum_{k=0}^{n-1}\frac{f^{(k)}(\alpha)}{k!}(t-\alpha)^k$$ Exists $x\in (\alpha, \beta)$ s.t. $$f(\beta) = P(\beta) + \frac{f^{(n)}(x)}{n!}(\beta - \alpha)^n$$
*Proof*: Fix $M\in \mathbb{R}$ s.t. $$f(\beta) = P(\beta) + M(\beta - \alpha)^n$$
Put $g(t) = f(t) - P(t) - M(t-\alpha)^n$, $$g^{(n)}(t) = f^{(n)}(t) = n!M$$
It is sufficient to show that $\exists x\in (\alpha, \beta)$, $g^{(n)}(x) = 0$. 

Notice that $$P^{(k)}(\alpha) = f^{(k)}(\alpha) \qquad \text{for }k=0, \dots, n-1, $$ which follows $$g(\alpha) = g^{(1)}(\alpha) = \cdots = g^{(n-1)}(\alpha) = 0.$$ Also notice by our way of constructing $g$, $g(\beta) = 0$. This follows that $\exists x_1\in (\alpha, \beta)$, g'(x_1) = 0, which follows that $\exists x_2\in (\alpha, x_1)$, $g^{(2)}(x_2) = 0$. Recursively, $\exists x_n\in (\alpha, x_{n-1})$, $g^{(n)}(x_n) = 0$. 
## Differentiation of Vector-valued Functions

For $f: [a,b]\rightarrow \mathbb{R}^n$, we say $f$ is differentiable at $x\in[a,b]$ if $$\lim_{t\rightarrow x}\frac{f(t) - f(x)}{t-x}$$ exists. $f = (f_1, \dots, f_k)$ is differentiable at $x$ $\Leftrightarrow$ all $f_i$ 's are differentiable at $x$. 

The first example shows that MVT does not generate to vector-valued functions.

**Example** MVT fails for vector-valued functions
Suppose $f(x) = e^{ix} = \cos x+i\sin x$. Notice that $f(2\pi) - f(0) = 1-1 = 0$, but as $f'(x) = ie^{ix}$ so that $|f'(x)| = 1$. $\not\exists x\in (0,2\pi)$ s.t. $f'(x) = 0$. 

The second example shows that L'Hospital's rule does not generate to vector-valued functions.

**Example** L'Hospital's rule fails for vector-valued functions
Suppose $f(x) = x, g(x) = x+x^2e^{i/x^2}$, $x\in (0,1)$, since $|\exp(it)| = 1$ for all $t$, $$\lim_{x\to 0}\frac{f(x)}{g(x)} = 1$$
On the contrary, $$g'(x) = 1+\left(2x - \frac{2i}{x}\right)e^{i/x^2}, x\in (0,1)$$$$\Rightarrow |g'(x)|\ge \left|2x-\frac{2i}{x}\right| - 1\ge \frac{2}{x} - 1$$$$\Rightarrow\left\lvert \frac{f'(x)}{g'(x)}\right\rvert = \frac{1}{|g'(x)|}<\frac{x}{2-x}$$$$\Rightarrow \lim_{x\rightarrow }\frac{f'(x)}{g'(x)} = 0$$

**Thm** 5.19 Weaker MVT but can generalize to vector-valued functions
Suppose $\mathbf{f}$ is a continuous mapping of $[a,b]$ into $\mathbb{R}^k$ and $\mathbf{f}$ is differentiable in $(a,b)$. Then there exists $x\in (a,b)$ s.t. $$|\mathbf{f}(b) - \mathbf{f}(a)|\le (b-a)|\mathbf{f}'(x)|$$
*Proof*: Put $z = f(a) - f(b)$. and define $\varphi(t) = z\cdot f(t)$. $\varphi$ is a real valued continuous function on $[a,b]$ which is diff on $(a,b)$. MVT $\Rightarrow \varphi(b) - \varphi(a) = (b-a)\varphi'(x)$ for some $x\in (a,b)$.  $\Rightarrow \varphi(b) - \varphi(a) = (b-a)z\cdot f'(x)$. 

Notice $\varphi(a) - \varphi(b) = z\cdot f(b) - z\cdot f(a) = z\cdot z = |z|^2$. Use Schwartz Inequality, 
$$\begin{align*}|z|^2 &= (b-a)|z\cdot f'(x)| \\ &\le (b-a)|z||f'(x)|\\ \Rightarrow |z|&\le (b-a)|f'(x)|\end{align*}$$
## Exercises