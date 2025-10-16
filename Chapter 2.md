Basic Topology

## Finite, Countable, and Uncountable Sets
**Def** 2.1 Function/mapping, domain, values, range
$$f:A\rightarrow B$$
$f$ is said to be a *function*, or a *mapping* from $A$ to $B$. The set $A$ is called the *domain* of $f$, the elements $f(x)$ are called the *values* of $f$, and the set of all values is called the *range* of $f$. 

**Def** 2.2 (Part 1) image, inverse image
$$f:A\rightarrow B$$
If $E\subset A$, $f(E)$ is defined to be the set of all elements $f(x)$, for $x\in E$. Then, $f(E)$ is the *image* of $E$ under $f$. 

If $E\subset B$, $f^{-1}(E)$ denotes the set of all $x\in A$ s.t. $f(x)\in E$. Then, $f^{-1}(E)$ is the *inverse image* of $E$ under $f$.

**Def** 2.2 (Part 2) Onto/surjective, one-to-one/injective (I am more comfortable using the terms "surjective" and "injective")
If $f(A) = B$, we say that $f$ maps $A$ *onto* $B$ (i.e., $f$ is a *surjective* mapping). In other words, if $f$ is surjective, $\forall y\in B$, $\exists x\in A$ s.t. $f(x) = y$. 
If, for each $y\in B$, $f^{-1}(y)$ consists of at most one element of $A$, then $f$ is said to be a *one-to-one* mapping of $A$ into $B$ (i.e., $f$ is a *injective* mapping). In other words, if $f$ is injective, whenever $x_1\neq x_2$, $x_1\in A$, $x_2\in A$, $f(x_1)\neq f(x_2)$.

**Def** 2.3 1-1 correspondence/bijective, cardinal number
If there exists a mapping that is both surjective and injective, then we say that $A$ and $B$ can be put in *1-1 correspondence* (i.e., $f$ is bijective). We say that $A$ and $B$ have the same *cardinal number* or $A\sim B$. Notice that this relation is:
Reflexive: $A\sim A$.
Symmetric: If $A\sim B$, then $B\sim A$. 
Transitive: If $A\sim B$ and $B\sim C$, then $A\sim C$. 

Note: Any relation with these three properties is called an *equivalence relation*.

**Def** 2.4 Finite, infinite, countable, uncountable, at most countable
(Rudin's definitions are based on equivalence, which is not so intuitive, but it turns out that after making sense of them, they are precise and clear.)
For any positive integer $n$, let $J_n$ be the set whose elements are the integers $1,2,\dots, n$; let $J$ be the set consisting of all positive integers. For any set $A$, we say:
(a) $A$ is *finite* if $A\sim J_n$ for some $n$ (the empty set is also considered to be finite). 
(b) $A$ is *infinite* if $A$ is not finite.
(c) $A$ is *countable* if $A\sim J$. 
Remark: $J = \mathbb{N}$, so this definition is equivalent to, more intuitively, "$A$ is countable if it has a bijection from $\mathbb{N}$".
(d) $A$ is *uncountable* if $A$ is neither finite nor countable.
(e) $A$ is *at most countable* if $A$ is finite or countable. 

Note: A set $A$ can be finite, infinitely countable, and uncountable. The former two cases are collectively called at most countable. 

**Def** 2.7 Sequence
A *sequence* is a function $f$ defined on $\mathbb{N}$. If $f(n) = x_n$, for $n\in \mathbb{N}$, it is customary to denote the sequence $f$ by the symbol $\{x_n\}$. The values of $f$ (i.e., the elements of $\{x_n\}$) are called the *terms* of the sequence. If $A$ is a set and if $x_n\in A, \forall n\in \mathbb{N}$, then $\{x_n\}$ is called a *sequence in* $A$, or a *sequence of elements of* $A$. 

**Thm** 2.8 Every infinite subset of a countable set $A$ is countable. 
*Proof*: Let $E\subset A$, where $E$ is infinite. Then, arrange $A$ so that it can be written as a sequence $\{x_n\}$ of distinct elements. Now, find the smallest $n_1\in \mathbb{N}$ such that $x_{n_1}\in E$. Having chosen $x_{n_1}, \dots, x_{n_k}$, find the smallest $n_{k+1}\in \mathbb{N}$ such that $x_{n_{k+1}}\in E$. Then, we have constructed inductively a sequence $\{n_k\}$. Then, we have obtained a bijection between $\mathbb{N}$ and $E$, so $E$ is countable. (QED)

**Def** 2.9 Union, intersection

2.10-2.11 Omitted

**Thm** 2.12 Let $\{E_n\}$, $n=1,2,3,\dots$, be a sequence of countable sets, and put $$S = \bigcup_{n=1}^\infty E_n.$$ Then $S$ is countable.
*Proof*: Arrange $E_n$ in a sequence $\{x_{nk}\}$ where elements of $E_n$ fills the $n$th row. Then, the elements can be arranged in the following sequence $$x_{11}; x_{21}, x_{12}; x_{31}, x_{22}, x_{13}; \dots$$ As the aforesaid list contains non-unique elements, we can have $T\subseteq \mathbb{N}$ such that there is a bijection between $S$ and $T$. Then, we have proved that $S$ is at most countable. With it being infinite, it is countable. (QED)

**Thm** 2.13 Let $A$ be a countable set, and let $B_n$ be the set of all $n$-tuples $(a_1, \dots, a_n)$, where $a_k\in A$ $(k = 1,\dots,n)$, and the elements $a_1, \dots, a_n$ need not be distinct. Then $B_n$ is countable.
*Proof*: When $n=1$, $B_1 = A$ is countable.

Assume that $B_n$ is countable, then all elements in $B_{n+1}$ is in the form of $(\mathbf{b}_n, a_{n+1})$, where $\mathbf{b}_n\in B_n$, $a_{n+1}\in A$. Then, notice that for each of $\mathbf{b}_n\in B_n$, the set of all $(\mathbf{b}_n, a_{n+1})$, denoted as $B_{\mathbf{b}_n}$, has a bijection from $A$. Then the set $B_{\mathbf{b}_n}$ is countable. 
Then, $$B_{n+1} = \bigcup_{\mathbf{b}_n\in B_n}B_{\mathbf{b}_n}$$ is countable because $B_n$ is countable.

As a conclusion, $B_n$ is countable. (QED)

**Cor** $\mathbb{Q}$ is countable. 
*Proof roadmap*: Use the **Thm** 2.13 with $n=2$. Every $q\in \mathbb{Q}$ can be written as a 2-tuple $(p,q)$. 

**Thm** 2.14 Let $A$ be the set of all sequences whose elements are the digits 0 and 1. This set $A$ is uncountable. 
*Proof*: Assume, BWOC, that this set is actually countable. Then, we are able to list the elements in the set of all sequences whose elements are the digits 0 and 1. 

Let $b_{nk}\in \{0,1\}$, where $n, k\in \mathbb{N}$. Then, 
$$\begin{align*}
s_1 &= (b_{11}, b_{12}, b_{13}, \dots)\\
s_2 &= (b_{21}, b_{22}, b_{23}, \dots)\\
s_3 &= (b_{31}, b_{32}, b_{33}, \dots)\\
&\vdots
\end{align*}$$ Notice that we have exhausted all possible $s_k$, based on the assumption. Let us construct a new sequence $t$ in this way: For all $b_{nn}$, if $b_{nn} = 1$ then $t_n = 0$, vice versa. Then, this $t$ has elements either 0 or 1, but it differs from all elements in $A$ by one digit. Therefore, $t\notin A$. $\Rightarrow \Leftarrow$ (QED)

*As a remark*, the sequence in $A$ can be viewed as the digits of a number written in binary. Therefore, there is a bijection between $A$ and $[0,1]$. This theorem proves that $[0,1]$ is uncountable, and for $\mathbb{R}\supset [0,1]$, $\mathbb{R}$ is of course uncountable.

## Metric Spaces

**Def** 2.15 Metric space, distance function/metric
A set $X$, whose elements we shall call *points*, is a *metric space* if there is a $d: X\times X\rightarrow \mathbb{R}_{\ge 0}$ mapping the combination of any two points $p,q\in X$ to some nonnegative real number $d(p,q)$, called the *distance* from $p$ to $q$, such that
(a) $d(p,q)>0$ if $p\neq q$; $d(p,p)=0$.
(b) $d(p,q) = d(q,p)$.
(c) $d(p,q)\le d(p,r) + d(r,q)$, $\forall r\in X$.

Any function with these three properties is a *distance function*, or a *metric*.

(Segment, interval, "half-open interval" are Rudin's language to describe open interval, closed interval, and intervals not open and not closed, like $[a,b)$, respectively.)

**Def** 2.17 Convex
We call a set $E\subset \mathbb{R}^k$ convex if $$\lambda \mathbf{x}+(1-\lambda) \mathbf{y}\in E$$ whenever $\mathbf{x}\in E, \mathbf{y}\in E$, and $0<\lambda<1$.

THE FOLLOWING DEFINITIONS ARE VERY IMPORTANT IN TOPOLOGY
**Def** 2.18 Let $X$ be a metric space. All points and sets mentioned below are understood to be elements and subsets of $X$.
*Note: In Rudin's understanding, a neighborhood is an open ball. However, while it does not cause an issue here, a neighborhood can take ANY shape.*
(a) (neighborhood, radius) A *neighborhood* of p is a set $B_r(p)$ consisting of all $q$ s.t. $d(p,q)<r$, for some $r>0$. The number $r$ is called the *radius* of $B_r(p)$. 
(b) (limit point) A point $p$ is a *limit point* of the set $E$ if every neighborhood of $p$ contains a point $q\neq p$ s.t. $q\in E$.
(c) (isolated point) If $p\in E$ and $p$ is not a limit point of $E$, then $p$ is called an *isolated point* of $E$.
(d) (closed) $E$ is *closed* if every limit point of $E$ is a point of $E$. 
(e) (interior point) A point $p$ is an *interior point* of $E$ if there is a neighborhood $N$ of $p$ such that $N\subset E$.
(f) (open) $E$ is *open* if every point of $E$ is an interior point of $E$.
(g) (complement) The *complement* of $E$ in $X$ (denoted by $X-E$) is the set of all points $p\in X$ s.t. $p\notin E$.
(h) (perfect) $E$ is *perfect* if $E$ is closed and if every point of $E$ is a limit point of $E$. 
(i) (bounded) $E$ is *bounded* if there is a real number $M$ and a point $q\in X$ s.t. $d(p,q)<M$ for all $p\in E$. 
(j) (dense) $E$ is *dense* in $X$ if every point of $X$ is a limit point of $E$, or a point of $E$ (or both).

**Thm** 2.19 Every neighborhood is an open set.
*Proof*: Choose an arbitrary $p\in B_r(x)$, then $d(x,p)<r$. There exists an $\epsilon > 0$ s.t. $d(x,p) \le r - \epsilon < r$. Then, around $p$, there is a neighborhood $B_\epsilon(p)$. Choose an arbitrary point $q\in B_\epsilon (p)$. Then, $d(p,q)<\epsilon$. $$d(x,q)\le d(x,p)+d(p,q) <r-\epsilon + \epsilon = r$$ With $d(x,q)<r$, $q\in B_r(x)$. Then, $B_\epsilon(p)\subset B_r(x)$. Thus, every point in $B_r(x)$ is an interior point, so $B_r(x)$ is open. (QED)

**Thm** 2.20 If $p$ is a limit point of a set $E$, then every neighborhood of $p$ contains infinitely many points of $E$. 
*Proof*: Assume, BWOC, that $\exists B_r(p)$, where $r>0$, only contains $k$ points of $E$. Call the set of such points $$P = \{p_1, \dots, p_k\}.$$ Then, find $p' = \operatorname{argmin}_{p_i\in P} d(p, p_i)$. Then, let $\delta = d(p,p')$, and use $\delta$ as the radius to find a neighborhood around $p$. Then, because $p$ is a limit point of $E$, $\exists q\in B_\delta(p)$ and $q\neq p, q\in E$. Notice that with $\delta < r$, $B_\delta(p)\subset B_r(p)$. Then, there is a $(k+1)$-th element in $P$. $\Rightarrow\Leftarrow$

Therefore, every neighborhood of $p$ contains infinitely many points of $E$. (QED)

**Cor** A finite point set has no limit points.

*Remarks* on **Example** 2.21: For (b), it is a perfect set because (i) it is closed; and (ii) every neighborhoods of all of its elements contain some points in it, making every element inside it a limit point.

**Thm** 2.22 
Let $\{E_\alpha\}$ be a (finite or infinite) collection of sets $E_\alpha$. Then $$\left(\bigcup_\alpha E_\alpha\right)^c = \bigcap_\alpha (E_\alpha^c).$$
*Proof roadmap*: Let $x\in \left(\bigcup_\alpha E_\alpha\right)^c\Rightarrow x\notin \bigcup_\alpha E_\alpha \Rightarrow \forall \alpha, x\notin E_\alpha \Rightarrow \forall \alpha, x\in E_\alpha^c \Rightarrow x\in\bigcap_\alpha (E_\alpha)^c$. Therefore, $\left(\bigcup_\alpha E_\alpha\right)^c \subseteq \bigcap_\alpha (E_\alpha^c)$.

Let $x\in \bigcap_\alpha (E_\alpha^c)\Rightarrow \forall \alpha, x\in E_\alpha^c \Rightarrow \forall \alpha, x\notin E_\alpha \Rightarrow x\notin \bigcup_\alpha E_\alpha \Rightarrow x\in (\bigcup_\alpha E_\alpha)^c$. Therefore, $\left(\bigcup_\alpha E_\alpha\right)^c \supseteq \bigcap_\alpha (E_\alpha^c)$.

Then, $\left(\bigcup_\alpha E_\alpha\right)^c = \bigcap_\alpha (E_\alpha^c)$. (QED)

**Thm** 2.23
A set $E$ is open iff its complement is closed.
*Proof*: For "if a set $E$ is open, then its complement is closed", we prove the contrapositive. Suppose its complement is not closed, i.e., it does not have all its limit points. Suppose that for $E^c$, $x$ is a limit point but $x\notin $E^c$. Then, $x\in E$. By the definition of a limit point, all its neighborhoods must contain some points in $E^c$, i.e., $\forall r>0, B_r(x)\cap E^c\neq \varnothing$. Then, $B_r(x)$ is not contained by $E$. Therefore, $E$ is not open.

For "if the complement of $E$ is closed, then it is open", we continue to prove the contrapositive. Suppose that $E$ is not open. Then, $\exists x\in E$, $\not\exists r>0$ s.t. $B_r(x)\subset E$. Then, $\forall r>0, B_r(x)\cap E^c\neq \varnothing$. In other words, for all neighborhoods of $x$, it contains some points in $E^c$. This is the very definition of a limit point of $E^c$. Since a limit point of $E^c$ is in $E$, $E^c$ cannot contain all its limit points, i.e., $E^c$ is not closed.

(QED)

**Thm** 2.24 
(a) For any collection $\{G_\alpha\}$ of open sets, $\bigcup_\alpha G_\alpha$ is open. 
(b) For any collection $\{F_\alpha\}$ of closed sets, $\bigcap_\alpha F_\alpha$ is closed.
(c) For any finite collection $G_1, \dots, G_n$ of open sets, $\bigcap_{i=1}^n G_i$ is open.
(d) For any finite collection $F_1, \dots, F_n$ of closed sets, $\bigcup_{i=1}^n F_i$ is closed. 

*Proof*: 
(a) $\forall x\in \bigcup_\alpha G_\alpha$, $\exists \alpha$ s.t. $x\in G_\alpha$. Since $G_\alpha$ is open, $\exists r>0$ s.t. $B_r(x)\subset G_\alpha \subset \bigcup_\alpha G_\alpha$. Therefore, $\bigcup_\alpha G_\alpha$ is open. (QED)
(b) Apply **Thm** 2.23, if $\forall \alpha, F_\alpha$ are closed sets, $F_\alpha^c$ are open sets. Apply (a), for the collection $\{F_\alpha^c\}$ of open sets, $\bigcup_\alpha F_\alpha^c$ is open. Notice that $\bigcap_\alpha F_\alpha = (\bigcup_\alpha F_\alpha^c)^c$, then $\bigcap_\alpha F_\alpha$ is closed.
(c) Choose a $x\in \bigcap_{i=1}^n G_i$. Then, $x\in G_1, \dots, x\in G_n$. Since $G_i, i = 1, \dots, n$ are all open sets, $\exists r_i>0$ s.t. $B_{r_i}(x)\subset G_i$. Now, choose $r = \min_{i = 1,\dots,n} r_i$. Then, $\forall i$, $B_{r}(x)\subset G_i$.  One step further, $B_r(x)\subset \bigcap_{i=1}^m G_i$. This proves that $\bigcap_{i=1}^n G_i$ is open.
(d) Use the complement set trick as in Part (b).

Why in Part (c) (and hence in Part (d)), we require *finite* collection? Without this condition, it is impossible to find a minimum for all $r_i$. One counterexample, as in **Example** 2.25, is $$G_n = \left(-\frac{1}{n}, \frac{1}{n}\right).$$
**Def** 2.26 Closure
If $X$ is a metric space, if $E\subset X$, and if $E'$ denotes *the set of all limit points* of $E$ in $X$, then the *closure* of $E$ is the set $$\overline{E} = E\cup E'.$$
**Thm** 2.27 
If $X$ is a metric space and $E\subset X$, then
(a) $\overline{E}$ is closed.
(b) $E = \overline{E}$ if and only if $E$ is closed.
(c) $\overline{E}\subset F$ for every closed set $F\subset X$ s.t. $E\subset F$. 

*Proof*: (a) Take an arbitrary point $p\in \overline{E}'$. Then, $\forall \epsilon>0$, $\exists q\in \overline{E}$ s.t. $q\in B_\epsilon(p)$. There are two cases, $q\in E$ or $q\in E'$. In the former case, we can conclude that $p$ is a limit point of $E$. In the latter case, notice that $B_\epsilon(p)$ is open, then $\exists \delta>0$, s.t. $B_\delta(q)\subset B_\epsilon(p)$. In $B_\delta(q)$, since $q\in E'$, $\exists q'\in E$ s.t. $q'\in B_\delta (q)$. This follows that $q'\in B_\epsilon(p)$. Then, $p$ is a limit point of $E$. Recall that $\forall p\in E', p\in \overline{E}$. Then, $\overline{E}'\subset \overline{E}$. This proves that $\overline{E}$ is closed. (QED)

*Remark*: Rudin uses the method of proving that the complement is open. It doesn't make sense to me though.

(b) Suppose $E$ is closed, $E$ contains all its limit points. Then, $E'\subset E$. Therefore, $E\cup E'=E$. Then, $\overline{E} = E\cup E' = E$.

Suppose $E=\overline{E}$. Then, $E = E\cup E'$. Thus, $E'\subset E$. This is the definition of closedness. Then, $E$ is closed. (QED)

(c) If $F$ is closed, then $F'\subset F$. Notice that if $E\subset F$, $E'\subset F'$. Then, $E'\subset F$. Since $E\subset F$, $\overline{E} = E\cup E' \subset F$. (QED)

**Thm** 2.28
Let $E$ be a nonempty set of real numbers which is bounded above. Let $y = \sup E$. Then $y\in \overline{E}$. Hence $y\in E$ if $E$ is closed.
*Proof*: Suppose that $y=\sup E$. Hence, $\forall \gamma <y$, $\gamma$ is not an upper bound of $E$. Thus, $\exists x\in (\gamma, y)$, s.t. $x\in E$. Therefore, $\forall r = y - \gamma >0$, $\exists x\in E, x\in B_r(y)$. Then, $y\in E'$. Since $\overline{E} = E\cup E'$, $y\in \overline{E}$. When $E$ is closed, apply **Thm** 2.27(b), $y\in \overline{E} = E$. (QED)

**Remark** 2.29 Open relative to
Suppose $E\subset Y\subset X$, where $X$ is a metric space. We say that $E$ is *open relative to* $Y$ if to each $p\in E$ there is associated an $r>0$ s.t. $q\in E$ whenever $d(p,q)<r$ and $q\in Y$. 

**Thm** 2.30
Suppose $Y\subset X$. A subset $E$ of $Y$ is open relative to $Y$ if and only if $E = Y\cap G$ for some open subset $G$ of $X$. 
*Proof*: Suppose $E$ is open relative to $Y$. By definition, $\forall p\in E, \exists r_p>0$ s.t. $q\in E$ if $d(p,q)<r_p$, $q\in Y$. For this particular $p$, the collection of $q\in X$ s.t. $d(p,q)<r_p$ is denoted as $V_p$. Let $G = \bigcup_{p\in E}V_p$, then $G$ is also an open set. 

For an arbitrary $q\in E$, we have $q\in V_p\subset G$. Also, as $E\subset Y$, $q\in Y$. Then, $q\in G\cap Y$. Thus, $E\subset G\cap Y$. By the definition of $V_p$, $V_p\cap Y\subset E$. Hence, $G\cap Y = (\bigcup V_p)\cap Y \subset E$. As a conclusion, $E = Y\cap G$. 

*Remark*: Rudin did not prove the other way.

Suppose $E = Y\cap G$ for some open $G$. Choose an arbitrary $p\in E$. Thus, $p\in Y$ and $p\in G$. With $G$ open, $\exists r'>0$, s.t. $\forall x\in X$, $d(p,x)<r$, then $x\in G$.  For an arbitrary $q\in Y$ with $d(p,q)<r$, according to the previous step, $q\in G$. Then, $q\in G\cap Y$. Recall $E = G\cap Y$, $q\in E$. 

Then, $\forall p\in E$, $\exists r>0$ s.t. $q\in Y$ with $d(p,q)<r$ implies $q\in E$. 

## Compact Sets

**Def** 2.31 Open cover
By an *open cover* of a set $E$ in a metric space $X$ we mean a collection $\{G_\alpha\}$ of open subsets of $X$ such that $E\subset \bigcup_\alpha G_\alpha$.

**Def** 2.32 Compact
A subset $K$ of a metric space $X$ is said to be *compact* if every open cover of $K$ contains a finite subcover.

**Thm** 2.33 
Suppose $K\subset Y\subset X$. Then $K$ is compact relative to $X$ if and only if $K$ is compact relative to $Y$.

*Remark*: This theorem implies that unlike the property of being open (which depends on the space in which $K$ is embedded), the property of being compact is not dependent on any embedding space.

**Thm** 2.34
Compact subsets of metric spaces are closed.

*Proof*: Suppose the compact set $E\subset X$. For $X-E$, choose an arbitrary $p\in X-E$. Then, choose an arbitrary $q\in E$. Let $$r_q < \frac{d(p,q)}{2}.$$ Notice that $E$ is compact. It only takes finitely many $V_i = B_{r_{q_i}}(q_i)$ to cover the entire $E$. That is $$E = V_1 \cup \dots \cup V_n.$$ For each of $V_1$ to $V_n$, we can construct $U_1, \dots, U_n$, $U_i = B_{r_{q_i}}(p_i)$. $U_i$ is disjoint from the corresponding $V_i$, and the finite intersection of such $U_i$ is also open, so we have constructed an open neighborhood $(U_1\cap \dots \cap U_n)\cap E = \varnothing$. This follows that $$U_1\cap \dots \cap U_n\subset X-E,$$ so $X-E$ is open. Thus, $E$ is closed. (QED)

**Thm** 2.35
Closed subsets of compact sets are compact.
*Proof*: Suppose $E\subset K\subset X$, where $K$ is a compact set, and $E$ is closed. Let $\{V_\alpha\}$ be an open cover of $E$. Notice that $\{K-E\}$ is an open cover of $K-E$. Then, $\{V_\alpha\}\cup\{K-E\}$ is an open cover of $K$. Apply the compactness of $K$, there is a finite subcover of $\{V_\alpha\}\cup\{K-E\}$ that still covers $K$. We remove $K-E$ from this finite subcover, resulting a finite subcollection of $\{V_\alpha\}$ covering $E$. Hence, $E$ is compact. (QED)

**Thm** 2.36 
If $\{K_\alpha\}$ is a collection of compact subsets of a metric space $X$ s.t. the intersection of every finite subcollection of $\{K_\alpha\}$ is nonempty, then $\bigcap K_\alpha$ is nonempty. 
*Proof*: Assume, BWOC, $\bigcap K_\alpha = \varnothing$. Hence, $\exists K\in \{K_\alpha\}$ s.t. it is disjoint from all other elements in $K_\alpha$. Then, let $G_\alpha = X - K_\alpha$, then $$K\subset \bigcup_\alpha G_\alpha.$$ Apply **Thm** 2.34, all of $K_\alpha$ are closed. Hence, all of $G_\alpha$ are open. Then, $\bigcup_\alpha G_\alpha$ is an open cover of $K$. Recall that $K$ is compact, so $\exists \bigcup_{i=1}^n G_i$ a finite cover of $K$. Then, $$K\cap \bigcap_{i=1}^n K_i=\varnothing.$$
Recall that the intersection of every finite subcollection of $\{K_\alpha\}$ is nonempty. $\Rightarrow\Leftarrow$ (QED)

**Cor** If $\{K_n\}$ is a sequence of nonempty compact sets s.t. $K_n\supset K_{n+1}$ ($n=1,2,3,\dots$), then $\bigcap_{n=1}^\infty K_n$ is not empty.

**Thm** 2.37
If $E$ is an infinite subset of a compact set $K$, then $E$ has a limit point in $K$. 
*Proof*: Assume, BWOC, that there does not exist a limit point in $E$. Since $K$ is compact, for every open cover $\{V_\alpha\}$, $\exists V_1, \dots, V_n\in \{V_\alpha\}$, $\{V_i\}_{i=1}^n$ alone is a finite subcover of $K$. $$E\subset K \subset \bigcup_{i=1}^n V_i.$$ Choose $\{V_\alpha\}$ in a way that each $V_\alpha$ can contain at most one point in $E$. Thus, no finite subcollection of such $V_\alpha$ can cover $E$. $\Rightarrow\Leftarrow$ (QED)

**Thm** 2.38
If $\{I_n\}$ is a sequence of intervals in $\mathbb{R}$, s.t. $I_n\supset I_{n+1}$ ($n=1,2,3,\dots$), then $\cap_{n=1}^\infty I_n$ is not empty.
*Remark*: By saying "interval", Rudin means "closed interval". This theorem appears before Heine-Borel, so we need to prove from scratch. 
*Proof*: We firstly show that each of $I_n$ is compact. Take an arbitrary open cover of $I_n = [a,b]$, denoted as $\mathcal{C}$. Then, let $$S = \{x\in [a,b]\mid [a,x]\text{ can be covered by a finite subcollection of }\mathcal{C}\}$$ This set is bounded above by $b$, and is not empty because $x\in S$ (the set of a single point must be able to have a finite subcover). Recall that $\mathbb{R}$ has the least-upper-bound property, so $$\alpha = \sup S$$ exists. Notice that if $\alpha < b$, we are always able to find an open set containing $\alpha$ but extending the coverage to some $x\in (\alpha, b)$. Therefore, $\alpha = b$. Thus, the entire $I_n$ can be covered by a finite subcollection of $\mathcal{C}$. 

After proving this, notice that with $I_n\supset I_{n+1}$ inductively defined, every finite subcollection of $\{I_n\}$ is nonempty. As a result, we can apply **Thm** 2.36 and conclude that $\bigcap_{n=1}^\infty I_n$ is not empty. (QED)

**Thm** 2.40
Every $k$-cell is compact.
*Proof*: Take 1-cells (closed intervals) as the base case, which is completed in the proof of **Thm** 2.38. 

Then, assume that $k$-cells are compact. Consider $k+1$-cells. $$I = J\times [a,b],$$ where $J$ is a $k$-cell, which is assumed to be compact. Let $\mathcal{C}$ be an arbitrary open cover of $I$.

Notice that, if we choose a slice, $\forall \mathbf{x}\in J$, $\{\mathbf{x}\}\times [a,b]$ is a compact set because it is a copy of a closed interval. For this slice, $\mathcal{C}$ is still an open cover. Since this slice is compact, there exists a finite subcover $U_\mathbf{x}$. 

We can find an open neighborhood around $\mathbf{x}$, denoted as $N_\mathbf{x}$, such that $N_\mathbf{x} \times [a,b]$ is contained in $U_\mathbf{x}$. Then, $\{N_\mathbf{x}\mid \mathbf{x}\in J\}$ is an open cover of $J$. Thus, there exists a subcover $\{N_{\mathbf{x}_n}\mid \mathbf{x}_n\in J\}$ of $J$. Then, $\{N_{\mathbf{x}_n}\times [a,b]\mid \mathbf{x}_n\in J\}$ is a finite collection of tubes that covers $I$, each of which is covered by a $U_{\mathbf{x}_n}$. We have found the finite subcover of $\mathcal{C}$. Therefore, $k$-cell is compact. (QED)

**Thm** 2.39 
Let $k$ be a positive integer. If $\{I_n\}$ is a sequence of $k$-cells s.t. $I_n\supset I_{n+1}$ ($n=1,2,3,\dots), then $\bigcap_{n=1}^\infty I_n$ is not empty.
*Remark*: I do not get it why Rudin put this above **Thm** 2.40. This theorem is a direct result of **Thm** 2.40 and **Thm** 2.36. Formal proof omitted.

**Thm** 2.41 HEINE-BOREL THEOREM
If a set $E$ in $\mathbb{R}^k$ has one of the following three properties, then it has the other two:
(a) $E$ is closed and bounded.
(b) $E$ is compact.
(c) Every infinite subset of $E$ has a limit point in $E$.
*Proof*: (a)$\Rightarrow$(b)
Suppose $E$ is bounded, it is a subset of a $k$-cell $F$: $$F = \{x\in \mathbb{R}^k\mid \lvert x_j\rvert \le m \text{ for }j = 1,2,\dots,k\},$$ which has been proven to be compact in **Thm** 2.40. Since $E$ is also closed, according to **Thm** 2.35, a closed subset of a compact set is still compact. Thus, $E$ is compact. 

(b)$\Rightarrow$(c) See **Thm** 2.37
(c)$\Rightarrow$(a) Assume, BWOC, that $E$ is not closed. Then, $\exists p\notin E$ but $p$ is a limit point. Construct a sequence $\{p_n\}$ in $E$: Take one point $p_n$ from each of the neighborhood $B_{1/n}(p), n\in \mathbb{N}$. Hence, this infinite sequence converges to $p$, and is an infinite subset of $E$. Then, it has a limit point in $E$. The only limit point, by the way we choose points in $\{p_n\}$, must be $p$. We have $p\in E$. $\Rightarrow\Leftarrow$

Assume, BWOC, that $E$ is not bounded. We construct a sequence $\{s_n\}$ in this way: Firstly, starting from $s_1\in E$. Then, choose $s_2\in E$ s.t. $d(s_1,s_2)>1$. Then, choose $s_3\in E$ s.t. $d(s_1,s_3)>1$, $d(s_2,s_3)>1$. Repeat this way so that $\forall i,j\in \mathbb{N}$, $d(i,j)>1$. Then, we have constructed a infinite subset $\{s_n\}$ of $E$. It has a limit point $p\in E$. By definition of a limit point, in each neighborhood around $p$, $\exists$ infinitely many points of $\{s_n\}$. Therefore, consider $B_{1/2}(p)$, $\exists s_m, s_n\in B_{1/2}(p)$, where $m\neq n$ and $m,n\in \mathbb{N}$. Thus, $d(s_m, p)<1/2, d(p,s_n)<1/2$. Notice that by triangle inequality, $$d(s_m,s_n)\le d(s_m,p) + d(p, s_n)<1$$ This contradicts with $d(i,j)>1$. $\Rightarrow\Leftarrow$

Therefore, $E$ is closed and bounded. 

(QED)

**Thm** 2.42 Weierstrass Theorem
Every bounded infinite subset of $\mathbb{R}^k$ has a limit point in $\mathbb{R}^k$. 
*Proof*: Let $E$ be an infinite subset of $\mathbb{R}^k$. Then, as it is bounded, it is a subset of a $k$-cell. A $k$-cell is compact, so $E$ has a limit point in the $k$-cell (and consequently, in $\mathbb{R}^k$). (QED)

*Remark*: Here is the conclusion of the *Compactness* section. Here is the logic flow of theorems and conclusions in this part: 
**Part 1** Foundation
- **Def** 2.31 & 2.32 - Definition of compactness with the idea of open cover
- **Def** 2.33 - Compactness is independent of any embedding space
- **Thm** 2.34 - Compact $\Rightarrow$ Closed
- **Thm** 2.35 - Closed subsets of compact sets are compact
**Part 2** Alternative Characterizations
- **Thm** 2.36 - (Compact $\Rightarrow$ Finite Intersection Property) If every finite intersection of compact subsets is nonempty, then the intersection of all compact subsets in nonempty
- **Thm** 2.37 - (Compact $\Rightarrow$ Limit Point Property) An infinite subset $E$ of a compact set $K$ must have a limit point in $K$
**Part 3** Building Blocks in $\mathbb{R}^k$
- **Thm** 2.38 - Closed intervals are compact
- **Thm** 2.40 - $k$-cells are compact
**Part 4** The Synthesis and Main Results
- **Thm** 2.41 - The Heine-Borel Theorem, TFAE:
	- Closed and bounded
	- Compact
	- With the Limit Point Property
- **Thm** 2.42 - The Weierstrass Theorem: Every bounded infinite subset of $\mathbb{R}^k$ has a limit point in $\mathbb{R}^k$.

## Perfect Sets
**Thm** 2.43 
Let $P$ be a nonempty perfect set in $\mathbb{R}^k$. Then $P$ is uncountable.

**Cor** Every interval $[a,b]$ ($a<b$) is uncountable. In particular, the set of all real numbers is uncountable. 

*Remark*: Professor Marius Junge, at University of Illinois, has the following way to prove that $\mathbb{R}$ or any closed interval $[a,b]$ is uncountable.

**Lemma** 1 The power set of natural numbers, $2^\mathbb{N}$, is uncountable. 
Assume, BWOC, that it is countable. $\exists \phi: \mathbb{N}\rightarrow 2^\mathbb{N}$, which is bijective. Define a subset of $\mathbb{N}$ as $$B = \{n\in\mathbb{N}\mid n\notin \phi(n)\}.$$ Then we discuss an arbitrary $n\in \mathbb{N}$, s.t. $\phi(n) = B$: If $n\in B$, then $n\notin \phi(n)$, then $n\notin B$. If $n\notin B$, then $n\in \phi(n)$, then $n\in B$. $\Rightarrow \Leftarrow$

**Lemma** 2 $[0,1]$ is uncountable. 
Let $\psi: 2^\mathbb{N}\rightarrow [0,1]$. 

*As a side note, if we have $f: A\rightarrow B$, knowing $A$ uncountable & proving $B$ uncountable, we need $f$ to be injective; knowing $B$ uncountable & proving $A$ uncountable, we need $f$ to be surjective. Bijective is a stronger condition that works for both cases.
Knowing $A$ countable & proving $B$ countable, we need $f$ to be surjective; knowing $B$ countable & proving $A$ countable, we need $f$ to be injective. 

| Given Information    | Function Property | Conclusion About Other Set |
| -------------------- | ----------------- | -------------------------- |
| **A** is uncountable | Injective         | **B** is uncountable       |
| **B** is uncountable | Surjective        | **A** is uncountable       |
| **A** is countable   | Surjective        | **B** is countable         |
| **B** is countable   | Injective         | **A** is countable         |
Let us construct an injective function: $$\psi(A) = \sum_{k\in A}3^{-k}, A\in 2^\mathbb{N}$$ Notice that $$\sum_{k\in A} 3^{-k}\le\sum_{k=1}^\infty 3^{-k} = \frac{1}{2},$$ so this function is well-defined.

 To prove that $\psi$ is injective, consider $A, B\in 2^\mathbb{N}, A\neq B$. Denote the smallest number that is exclusively in $A$ but not in $B$ is $m_0$. Denote the sum over all numbers before $m_0$ be $\alpha$, then $$\psi(A) = \alpha + 3^{-m_0}+\sum_{\substack{j\in A\\j>m_0}}3^{-j}$$ $$\psi(B) = \alpha + 0+\sum_{\substack{j\in B\\j>m_0}}3^{-j}$$ Also notice that $$\sum_{\substack{j\in B\\j>m_0}}3^{-j} - \sum_{\substack{j\in A\\j>m_0}}3^{-j}\le \sum_{\substack{j\in B\\j>m_0}}3^{-j}\le \sum_{j=m_0+1}^\infty 3^{-j} = 3^{-(m_0+1)}\left(\frac{1}{1-\frac{1}{3}}\right) = \frac{1}{2}\cdot 3^{-m_0},$$ which says $$\psi(B)\le \alpha + \frac{1}{2}\cdot 3^{-m_0}+\sum_{\substack{j\in A\\j>m_0}}3^{-j}< \psi(A).$$ In this equality, $A$ and $B$ can swap their places. Thus, $\psi(B)\neq \psi(A)$. 
As we have proven the injectivity of $\psi$, as $2^\mathbb{N}$ is uncountable, $[0,1]$ is uncountable. 

From this point, we can find a bijection $f: [0,1]\rightarrow [a,b]$, $$f(x) = a + (b - a)x$$
We can also find an injective function $g: [0,1]\rightarrow \mathbb{R}$, $$g(x) = x$$
Therefore, we have proven that the arbitrary closed interval $[a,b]$ and $\mathbb{R}$ are uncountable. 

**Def** 2.44 The Cantor set

## Connected Sets

**Def** 2.45 Separated, connected
Two subsets $A$ and $B$ of a metric space $X$ are said to be *separated* if both $A\cap\overline{B}$ and $\overline{A}\cap B$ are empty, i.e., if no point of $A$ lies in the closure of $B$ and no point of $B$ lies in the closure of $A$.
A set $E\subset X$ is said to be *connected* if $E$ is not a union of two nonempty separated sets. 

**Thm** 2.47 
A subset $E$ of the real line $\mathbb{R}$ is *connected* if and only if it has the following property: If $x\in E$, $y\in E$, and $x<z<y$, then $z\in E$.

*Proof*: (Connected $\Rightarrow$ Property)
Assume, BWOC, that $\exists z\in \mathbb{R}$, s.t. $x<z<y$ but $z\notin E$. Then, $E\subset (x,y) - \{z\}$. If this is the only point missing in the interval $(x,y)$, then $E = (x,z)\cup(z,y)$ where $(x,z)$ and $(z,y)$ are separated and nonempty. Then, $E$ is not connected.

(Property $\Rightarrow$ Connected)
Assume, BWOC, that $E$ is not connected. Then, $E = A\cup B$ where $A\cap \overline{B} = \varnothing$ and $\overline{A}\cap B = \varnothing$. As both $A$ and $B$ are nonempty, choose $x$ and $y$ strategically s.t. $x\in A$ and $y\in B$. WLOG, assume $x<y$. 

Let $A_0 = A\cap(x,y)$, $B_0 = B\cap(x,y)$. Since $(x,y)\in E$, $E\cap(x,y) = A_0\cup B_0$. Then, let $z = \sup A_0$. This supremum is well-defined because $\mathbb{R}$ has the least-upper-bound property. 

If $z\in A_0$, then by the definition of supremum, any $z+\epsilon$ for all $\epsilon>0$ is an upper bound of $A_0$. Then $(z,z+\epsilon)\cap A_0 = \varnothing$. Thus, $(z,z+\epsilon)\subset B_0$. This means any neighborhood around $z$ contains some elements in $B_0$. Thus, $z\in B_0'\Rightarrow z\in \overline{B}_0$. $z\in A_0\cup \overline{B}_0\neq \varnothing$. Thus, $E$ is connected. $\Rightarrow\Leftarrow$

If $z\in B_0$, then by the definition of the supremum, any $z-\epsilon$ for all $\epsilon>0$ is not an upper bound of $A_0$. Then, $(z-\epsilon, z)\cap A_0\neq \varnothing$. Thus, any neighborhood around $z$ contains some elements in $A_0$. Thus, $z\in A_0'\Rightarrow z\in \overline{A}_0$. $z\in \overline{A}_0\cup B_0\neq \varnothing$. $\Rightarrow\Leftarrow$

(QED)

## Exercises
### Question 1
This question seems so trivial, but there is a post on [Stack Overflow](https://math.stackexchange.com/questions/631042/direct-proof-of-empty-set-being-subset-of-every-set) with a state-of-the-art proof I really like: $$\forall B\subseteq A, A-B\subseteq A\Rightarrow \text{Since }A\subseteq A, A - A = \varnothing \subseteq A.$$
### Question 2
We construct, for all $N\in \mathbb{N}$, $$\mathcal{P}_N = \{p\in \mathbb{R}[z]\mid p(z) = a_0z^n + a_1z^{n-1} + \dots + a_{n-1}z + a_n, n+ \lvert a_0 \rvert + \dots + \lvert a_n \rvert = N\},$$ which is finite as there are only finitely many equations with $$n+ \lvert a_0 \rvert + \dots + \lvert a_n \rvert = N.$$
We further construct $$\mathcal{A}_N = \{z\in \mathbb{C}\mid p(z) = 0, p\in \mathcal{P}_N\}.$$ What can we say about this one? Since the root of a particular equation $p(z) = 0$ is finite, the number of roots of a finite collection of equations $p(z) = 0$ is also finite. Then, we know that the set of all algebraic numbers is $$\mathcal{A} = \bigcup_{N\in\mathbb{N}}\mathcal{A}_N,$$
which is countable because a countable union of finite sets is countable. (QED)

### Question 3
Assume, BWOC, there does not exist any real number that is not algebraic. Thus, all real numbers are algebraic. Then, $\mathbb{R}\subseteq \mathcal{A}$. Notice that the subset of a countable set must be countable, and as $\mathcal{A}$ is countable, $\mathbb{R}$ must also be countable. 

We have proven in a couple of ways that $\mathbb{R}$ is not countable. $\Rightarrow\Leftarrow$ (QED)

### Question 4
*No*. Assume, BWOC, that the set of all irrational real numbers, denoted as $\mathbb{P}$, is countable. Notice that the countable union of countable sets is still countable. We have proven that $\mathbb{Q}$ is countable. Then, $$\mathbb{R} = \mathbb{Q}\cup \mathbb{P}$$ is countable. We have proven in a couple of ways that $\mathbb{R}$ is not countable. $\Rightarrow\Leftarrow$ (QED)

### Question 5
$$A = \bigcup_{i=0}^2 \{i+\frac{1}{n}\mid n\in \mathbb{N}\}$$

### Question 6
Fix some $p\in (E')'$. Then, fix an arbitrary $\epsilon/2>0$, $\exists $q\in E'$ s.t. $d(p,q)<\epsilon/2$. Notice that $q$ is a limit point of $E$, so $\exists r\in E$ s.t. $d(q,r)<\epsilon/2$. By triangle inequality, $$d(p,r)\le d(p,q) + d(q,r) < \epsilon,$$ so $p\in E'$. Thus, $(E')'\subseteq E'$. This proves that $E'$ is closed.

Recall $\overline{E} = E\cup E'$. Thus, $\overline{E}' = (E\cup E')'$. As a matter of fact, $(E\cup E')' = E'\cup (E')'$. As we have previously proven, $(E')'\subseteq E'$. Therefore, $E'\cup (E')' = E'$. This proves that $\overline{E}' = E'$. 

*The proof below is what I initially think to address the question "Do $E$ and $E'$ always have the same limit points?"*
If $a\in \overline{E}'$ , then $\forall \epsilon>0$, $\exists b\in \overline{E}$ s.t. $d(a,b)< \epsilon$. Recall $\overline{E} = E\cup E'$. If $b\in E$, then $a\in E'$. If $b\in E'$, then $a\in (E')'$. Since $(E')'\subseteq E'$, $a\in E'$. Therefore, $$\overline{E}'\subseteq E'.$$

If $a\in E'$, then $\forall \epsilon >0$, $\exists b\in E$ s.t. $d(a,b)<\epsilon$. Then, since $E\subseteq \overline{E}$, this $b\in \overline{E}$. This makes $a\in \overline{E}'$. Therefore, $$E'\subseteq \overline{E}'.$$
These two follow that $E' = \overline{E}'$. Hence, $E$ and $E'$ always have the same limit points.

**What is wrong?** 
1. This proof, by stating "$a\in (E')'$", falsely assumes that $(E')'\neq \varnothing$. When $E$ only has finitely many limit points, $E'$ is a discrete set, and $(E')' = \varnothing$.    
2. The logic leap here "If $b\in E$, then $a\in E'$. If $b\in E'$, then $a\in (E')'$" is invalid. We require that in *every* neighborhood, if $\exists b\in E$, then $a\in E'$; if $\exists b\in E'$, then $a\in (E')'$. 

*Remark*: The discussion of $E$ and $\overline{E}$ bypasses the assumption that $(E')'\neq \varnothing$. 

### Question 7
(a) We want to show that $$B_n\cup B'_n = \underbrace{\overline{B}_n = \bigcup_{i=1}^n \overline{A}_i}_{\text{objective}} = \left(\bigcup_{i=1}^n A_i\right)\cup\left(\bigcup_{i=1}^n A'_i\right) = B_n\cup\left(\bigcup_{i=1}^n A'_i\right),$$ so we want to show that $$B'_n = \bigcup_{i=1}^n A'_i.$$
Suppose $p\in B'_n$. Then, assume, BWOC, that $p\notin \bigcup_{i=1}^n A'_i$. This requires that $p\notin A'_i$ for all $i=1,2,\dots, n$. In other words, for all such $A_i$, there exists some neighborhood around p that contains no points of $A_i$. In other words,
* For $i = 1$, $\exists \epsilon_1>0$ s.t. $B_{\epsilon_1}(p)\cap A_1 \subseteq \{p\}$. 
* For $i = 2$, $\exists \epsilon_2>0$ s.t. $B_{\epsilon_2}(p)\cap A_2 \subseteq \{p\}$. 
  $\vdots$
* For $i = n$, $\exists \epsilon_n>0$ s.t. $B_{\epsilon_n}(p)\cap A_n \subseteq \{p\}$. 

**Since $n$ is finite**, we can always find a minimum $$\epsilon = \min\{\epsilon_1, \dots, \epsilon_n\}$$ s.t. $\forall i = 1,2,\dots, n$, $B_\epsilon(p)\cap A_i\subseteq \{p\}$. This is to say, $$\bigcup_{i=1}^{n}(B_\epsilon(p)\cap A_i) = \{p\}$$ $$B_\epsilon(p)\cap\bigcup_{i=1}^{n}A_i = \{p\}$$  $$B_\epsilon(p)\cap B_n = \{p\},$$ so $p\notin B'_n$. $\Rightarrow\Leftarrow$

Hence, $B'_n\subseteq \bigcup_{i=1}^nA'_i$.

In the other direction, assume $p\in \bigcup_{i=1}^nA'_i$. Then, for at least one of $A'_i$, $p\in A'_i$. Denote this set with $i=m$. Then, $\forall \epsilon >0$, $\exists q\in A_m$, s.t. $q\neq p$, $q\in B_\epsilon(p)$. Notice that $A_m\subseteq B_n$. Then, $\forall \epsilon >0$, $\exists q\in B_n$, s.t. $q\neq p$, $q\in B_\epsilon(p)$. This proves that $p'\in B_n$, which follows that $\bigcup_{i=1}^n A'_i\subseteq B'_n$.

Therefore, $B'_n = \bigcup_{i=1}^nA'_i$. It follows that $\overline{B}_n = \bigcup_{i=1}^n\overline{A}_i$, for $n\in \mathbb{N}$. (QED)

(b) Notice that only the proof in (a) after "in the other direction" is valid when $n$ goes to infinity. Then, $$\overline{B}\supset \bigcup_{i=1}^\infty \overline{A}_i.$$ (QED)

### Question 8
**For open set $E\subset \mathbb{R}^2$**:
**Yes**, by definition of an open set, $\forall x\in E$, $\exists \epsilon>0$ s.t. $B_\epsilon(x)\subset E$. We want, for any $r>0$, $B_r(x)$ contains some point $y\in E$ s.t. $y\neq x$.

Here, let $0\neq\delta = \min\{\epsilon, r\}$. Let $x = (x_0, y_0)$, and $t = (x_0 + \frac{\delta}{3}, y_0)$. Then, $d(x,t) = \frac{\delta}{3}<\epsilon$, so $t\in B_\epsilon(x)\subset E$. $d(x,t) = \frac{\delta}{3}<r$, so $t\in B_r(x)$. Therefore, any neighborhood around $x$ with an arbitrary radius $r$ contains a point $t\neq x$.

**For closed set $E\subset \mathbb{R}^2$**:
**No**, because any finite set can be a counterexample. $\{(0,0), (1,1)\}$ has no limit point. 

### Question 9
(a) Fix an arbitrary $x\in E^\circ$. Then, since $x$ is an interior point, $\exists r>0$ s.t. $B_r(x)\subset E$. We want $B_r(x)\subset E^\circ$. Choose an arbitrary $y\in B_r(x)$, i.e., $d(x,y)<r$. Let $0<\delta < r - d(x,y)$, then we can fit $B_\delta (y)$ inside $B_r(x)$. Hence, $B_\delta(y)\subset B_r(x)\subset E$. Thus, $y\in E^\circ$. Recall that $y$ is arbitrary, $B_r(x)\subset E^{\circ}$. This proves that $E^\circ$ is open. (QED)

(b) Suppose $E$ is open, then $\forall x\in E$, $\exists r>0$, $B_r(x)\subset E$. Thus, such $x\in E^\circ$. Therefore, $E\subseteq E^\circ$. For all $y\in E^\circ$, to make sure that some neighborhood around $y$ is contained by $E$, $y\in E$. Thus, $E^\circ\subseteq E$. Therefore, $E^\circ = E$.

Suppose $E^\circ = E$. This is the definition of the openness of $E$. (QED)

(c) $\forall x\in G$, since $G$ is open, $\forall r>0$, $B_r(x)\subset G \subset E$. Thus, $x\in E^\circ$. This proves that $G\subset E^\circ$. (QED)

(d) We want $X-E^\circ = \overline{X-E}$.

Find an arbitrary $x\in X - E^\circ$. Thus, $x\notin E^\circ$. Thus, $\forall x>0$, the neighborhood $B_r(x)$ is not a subset of $E$. There are two cases: In the first case, $x\notin E\Rightarrow x\in X-E\subset \overline{X-E}$. In the second case, $x\in E$. Also, $\forall r>0$, $B_r(x)$ contains at least one point in $X-E$. This makes $x$ a limit point of $X-E$ and therefore, $x\in \overline{X-E}$. Then, $X-E^\circ\subseteq \overline{X-E}$.

Find an arbitrary $x\in \overline{X-E}$. Then, there are two cases: In the first case, $x\in X-E$. Then, $x\notin E\Rightarrow X\notin E^\circ \Rightarrow x\in X-E^\circ$. In the second case, $x\notin X-E$ but $x\in \overline{X-E}$. Thus, $\forall r>0$, $B_r(x)\cap (X-E)\neq \varnothing$. Hence, $\not\exists r>0$, $B_r(x)\subset E$. This makes $x\notin E^\circ\Rightarrow x\in X-E^\circ$. Then, $\overline{X-E}\subseteq X-E^\circ$.

Therefore, $X-E^\circ = \overline{X-E}$. (QED)

(e) *No*. Take $E = (0,1)\cup (1,2)$, then $\overline{E} = [0,2]$. $E^\circ \neq \operatorname{Int}(\overline{E})$.

(f) *No*. Take $E = \mathbb{Q}$, and $\overline{E} = \mathbb{Q}$. Then $E^\circ = \varnothing$, and $\overline{E}^\circ = \varnothing$.

### Question 10
Check for three conditions:
- $d(p,q) = 1 > 0$ if $p\neq q$. $d(p,p) = 0$.
- When $p=q$, $d(p,q) = 0$, $d(q,p) = 0$, so $d(p,q) = d(q,p)$. When $p\neq q$, $d(p,q) = 1$, $d(q,p)=1$, so $d(p,q) = d(q,p)$.
- Assessing if $p\ne q$, $q\ne r$, and $r\ne q$, we have the following table:

| $p \ne q$ | $p\ne r$ | $r\ne q$ |
|-----------|----------|----------|
| 0         | 0        | 0        |
| 1         | 1        | 0        |
| 1         | 0        | 1        |
| 1         | 1        | 1        |
The values in this table is not only the bull value of $p\ne q$, $p\ne r$, and $r\ne q$, but also the value of $d(p,q), d(p,r), d(r,q)$. Therefore, we can see $d(p,q)\le d(p,r) + d(r,q)$. (QED)

*Openness* and *Closedness*
A subset $\mathscr{O}$ is said to be open if $\forall x\in \mathscr{O}$, $\exists r>0$ s.t. $B_r(x)\in \mathscr{O}$. Thus, if we choose $0<r\le 1$, then $B_r(x)= \{x\}$. In this way, we can say that every subset of $X$ is open.

A subset $\mathscr{C}$ is said to be closed if $X-\mathscr{C}$ is open. Since every $X-\mathscr{C}$ is open, every $\mathscr{C}$ is closed.

*Compactness*
For an arbitrary set $K\subset X$. Then, consider the following open cover: $$\{\{x\}\subset X\mid x\in K\}.$$ Then, the condition to make a finite subcover for this open cover is that $K$ is finite. Therefore, a compact set in this metric space is a finite set.

### Question 11
Condition code:
1 = $d(p,q)>0$ if $p\ne q$; $d(p,p)=0$
2 = $d(p,q) = d(q,p)$
3 = Triangle inequality
- $d_1$: No, it fails 3
- $d_2$: Yes
- $d_3$: Yes
- $d_4$: No, it fails 1
- $d_5$: Yes
*Some tricks proving the triangle inequality* of $d_3$ and $d_5$
$d_3$: we can change variables, let $a = x^2$, $b=y^2$, and c = $r^2$, then to show $$|x^2 - y^2|\le |x^2 - r^2| + |r^2 - y^2|,$$ we only need to show $$|a - b|\le|a - c| + |c - b|,$$ which is true by triangle inequality.
$d_5$: Notice the increasing function $$f(t) = \frac{t}{1+t}$$ can be applied to $$a\le b+c,$$ where $a = |x-y|$, $b = |x-r$|, and $c = |r-y|$, so $$f(a)\le f(b)+f(c).$$

### Question 12
Assume, BWOC, that $K=\{0\}\cup\{1/n\mid n\in \mathbb{N}\}$ is not compact; i.e., it has an infinite open cover $\{V_\alpha\}$ that does not have a finite subcover. There must be some $V_0\in \{V_\alpha\}$ that contains 0. Since $1/n\rightarrow 0$, $\forall \epsilon>0$, $\exists N\in \mathbb{N}$ s.t. $n>N\Rightarrow 1/n<\epsilon$. Then, in $V_0$, there are infinitely many points from $K$. This left $N-1$ points for all other open sets in $\{V_\alpha\}$, so $\{V_\alpha\}$ has a finite subcover $V_0, V_1, \dots, V_{N-1}$, where $V_i = \{1/i\}$ for each $i = 1, \dots, N-1$. $\Rightarrow \Leftarrow$ (QED)

### Question 13
$$K = \{0\}\cup\left(\bigcup_{m=1}^\infty \left\{\frac{1}{m} + \frac{1}{n}\middle\vert n\in \mathbb{N}\right\}\right)$$

### Question 14
$$\{(1/n, 2)\mid n\in \mathbb{N}, n\ge 2\}$$

### Question 15
Counterexample for: 
	If $\{K_\alpha\}$ is a collection of closed subsets of a metric space $\mathbb{R}$ s.t. the intersection of every finite subcollection of $\{K_\alpha\}$ is nonempty, then $\bigcap K_\alpha$ is nonempty. 

For $$\{[n, \infty)\mid n\in \mathbb{N}\},$$ any finite intersection must contain all real numbers after the least $n$ of the collection, but $$\bigcap_{n\in\mathbb{N}} \{[n, \infty)\mid n\in \mathbb{N}\} = \varnothing.$$
Counterexample for: 
	If $\{K_\alpha\}$ is a collection of bounded subsets of a metric space $\mathbb{R}$ s.t. the intersection of every finite subcollection of $\{K_\alpha\}$ is nonempty, then $\bigcap K_\alpha$ is nonempty. 

$$\left\{\left(-\frac{1}{n}, 0\right)\cup \left(0,\frac{1}{n}\right)\mid n\in \mathbb{N}\right\}$$

### Question 16
*Proof Scratch*
To discuss if $E$ is closed, a convenient way is to discuss the openness of $\mathbb{Q} - E = \{p\in \mathbb{Q}\mid p^2\le 2 \text{ or }p^2\ge 3\} = \{p\in \mathbb{Q}\mid p^2\le 2\}\cup \{p\in \mathbb{Q}\mid p^2\ge 3\}$. We need to prove that either of the two set does not have a minimum/maximum. 

(To cut the proof short, I only prove that $\{p\in \mathbb{Q}\mid p^2\le 2\}$ does not have a maximum.) Let $L = \{p\in \mathbb{Q}\mid p^2\le 2\}$. Suppose $\exists q\in L$ s.t. $\forall r\in L$, $r\le q$. Construct a small number $h$ s.t. $$h<\frac{2-q^2}{2q+1},$$ which, from the formula, is in $\mathbb{Q}$. Then, $$2qh+h<2-q^2$$ Since we take very small $h$, $h>h^2$, $$2qh+h^2 < 2qh+h < 2-q^2$$Rearrange, $$q^2+2qh+h^2<2$$ $$(q+h)^2<2,$$ which proves that $q+h\in L$. $\Rightarrow\Leftarrow$

Therefore, near the boundaries of $\{p\in \mathbb{Q}\mid p^2\le 2\}$ or $\{p\in \mathbb{Q}\mid p^2\ge 3\}$, we can draw open balls completely contained in $\mathbb{Q} - E$. This proves that $\mathbb{Q} - E$ is open, so $E$ is closed.

$E$ is bounded because $E\in [-2,2]$, which is bounded.

$E$ is open in $\mathbb{Q}$ using a similar argument as we used above around the boundaries.

$E$ is not compact because Heine-Borel only applies to $\mathbb{R}^k$.

### Question 17

### Question 18

### Question 19
(a) Since $A$ and $B$ are all closed sets, $\overline{A} = A$ and $\overline{B} = B$. Thus, if $A\cap B = \varnothing$, $$A\cap\overline{B}=\varnothing$$ $$\overline{A}\cap B=\varnothing$$ so they are separated. (QED)

(b) Assume, BWOC, that they are not separated, i.e., $$A\cap \overline{B}\neq \varnothing$$ or $$\overline{A}\cap B \neq \varnothing$$ *Discuss the case of one of them is sufficient.* Suppose $x\in A\cap \overline{B}$, then either $x\in A\cap B$ or $x\in A\cap B'$. 

In the former case, $\Rightarrow\Leftarrow$ 

In the latter case, $\forall r>0$, $\exists y\in B$ s.t. $y\in B_r(x)$ and $x\ne y$. Also, since $x\in A$, and $A$ is open, $\exists r>0$ s.t. $B_r(x)\subset A$. Then, $y\in A$. Hence $y\in A\cap B\ne \varnothing$. $\Rightarrow\Leftarrow$

(QED)

(c) For $p\in X$, $$A = \{q\in X\mid d(p,q)<\delta\}$$ $$B = \{q\in X\mid d(p,q)>\delta\}$$ They are disjoint open sets. Apply (b), they are separated. (QED)

(d) Let $d(p,q) = d$. $\forall \delta \in (0,d)$, there is a point with $d(p,r) = \delta$, otherwise we can apply (c) and show that the connected $X$ is separable. Then, there is a bijection between $X$ and $[0,d]$. Since $[0,d]$ is uncountable, $X$ is uncountable. (QED)

### Question 20
Yes for closures but no for interiors. 

For closures, intuitively, adding points that are infinitesimally close does not creates new gaps or disconnections.

Counterexample for interiors: In $\mathbb{R}^2$, $$\{(x,y)\in \mathbb{R}^2\mid(x-2)^2+y^2 \le 4\}\cup\{(x,y)\in \mathbb{R}^2\mid(x+2)^2+y^2 \le 4\}$$ is connected, but its interior, $$\{(x,y)\in \mathbb{R}^2\mid(x-2)^2+y^2 < 4\}\cup\{(x,y)\in \mathbb{R}^2\mid(x+2)^2+y^2 < 4\},$$ a union of two disjoint open sets, is not connected.

### Question 21
(a) Assume, BWOC, that $A_0$ and $B_0$ are not separated. WLOG, $$A_0\cap \overline{B}_0\ne \varnothing.$$ Suppose $t\in A_0\cap \overline{B}_0$, then $t\in A_0\Rightarrow \mathbf{p}(t)\in A$. Also, $t\in \overline{B}_0$. If $t\in B_0$, $\mathbf{p}(t)\in B$ and $A\cap B\ne \varnothing$, $A$ and $B$ are not separated. If $t\notin B_0$, then $\forall r>0$, $\exists x\in B_0, \lvert t-x\rvert< r$. Notice $$\mathbf{p}(t) = (1-t)\mathbf{a} + t\mathbf{b}\in A$$ $$\mathbf{p}(x) = (1-x)\mathbf{a} + x\mathbf{b}\in B$$ $$\lvert \mathbf{p}(t) - \mathbf{p}(x) \rvert = \lvert t-x \rvert \lvert\mathbf{a} - \mathbf{b}\rvert,$$ where $\lvert \mathbf{a} - \mathbf{b} \rvert$ is fixed because we have fixed $\mathbf{a}$ and $\mathbf{b}$. Thus, $$\lvert \mathbf{p}(t) - \mathbf{p}(x) \rvert < r \lvert\mathbf{a} - \mathbf{b}\rvert.$$ Therefore, $\mathbf{p}(t)$ is a limit point of $B$. $$A\cap \overline{B}\ne \varnothing,$$ which proves that $A$ and $B$ are *not* separated. $\Rightarrow\Leftarrow$ (QED)

(b) Assume, BWOC, that $\forall t_0\in (0,1)$, $\mathbf{p}(t_0)\in A\cup B$. Then, $\mathbf{p}(t_0)\in A$ or $\mathbf{p}(t_0)\in B$. Therefore, $t_0\in A_0$ or $t_0\in B_0$. This means $t_0\in A_0\cup B_0$, so $(0,1)\subseteq A_0\cup B_0$. (Counting on $\mathbf{a}\in A$, $\mathbf{b}\in B$, $[0,1]\subseteq A_0\cup B_0$.) Then, let $A_0' = A_0\cap [0,1]$, $B_0' = B_0\cap[0,1]$, then $A_0'\cup B_0' = A_0\cup B_0\cap[0,1]$. We have $[0,1]\subseteq A_0'\cup B_0'$. Meanwhile, $A_0'\subseteq [0,1]$, $B_0'\subseteq [0,1]$, so $A_0'\cup B_0'\subseteq [0,1]$. Therefore, $[0,1]=A'_0\cup B'_0$. With $0\in A_0'$ and $1\in B_0'$, $A_0'$ and $B_0'$ must be separated, which follows that $[0,1]$ is separated (ridiculous!) $\Rightarrow\Leftarrow$ (QED)

(c) The logic behind Assumptions $\Rightarrow$ Conclusion in (b) is that if $X$, a subset of $\mathbb{R}^k$ is not connected, then $\exists t_0\in (0,1)$ s.t. $\mathbf{p}(t_0) \notin A\cup B$. This part asks that if $X$ is a convex subset of $\mathbb{R}^k$ (i.e, $\forall t\in (0,1)$, $\mathbf{p}(t_0)\in X$), then $X$ is connected. We can see that these two are contrapositive. (QED)

### Question 22
The countable, dense subset is $$\{\mathbf{x}\in \mathbb{R}^k\mid x_i\in \mathbb{Q}, i = 1, \dots, k\}$$ (QED)

### Question 23
Let $X$ be an arbitrary separable space.

For the collection of open subsets $\{V_\alpha\}$, for each $V_i$, as it is open, there is always some open ball $B_\epsilon(x)\subseteq V_i$, so if we can find such a countable set of open balls, then we can prove that there is a countable base.

Construct this set of open balls in the following way: Since $X$ is separable, let $D$ be a countable, dense subset of $X$. 
$$\mathscr{B} = \{B_r(d)\mid d\in D, r\in \mathbb{Q}_{>0}\}$$

With both $D$ and $\mathbb{Q}_{>0}$ countable, $\mathscr{B}$ is also a countable set. 

Now, choose an arbitrary $x\in X$ and $G$ that contains $x$. Notice that $G$ is open, by definition of an open set, so $\forall \epsilon>0$, $B_\epsilon(x)\subseteq G$. Then, we choose an open ball with a radius of $\epsilon/2$, since $D$ is dense in $X$, $\forall x\in X$, either $x\in D$ or $x$ is a limit point of $D$. In the former case, $x \in B_{\epsilon/2}(x)$ and $x\in D$, then $x\in D\cap B_{\epsilon/2}(x)$, so $D\cap B_{\epsilon/2}(x) \neq \varnothing$. In the latter case, every neighborhood around $x$ contains some point from $D$, so $D\cap B_{\epsilon/2}(x) \neq \varnothing$. 

Choose an arbitrary $d\in D\cap B_{\epsilon/2}(x)$. Notice that we can always find some $r\in \mathbb{Q}_{>0}$ such that $d(x,d)<r<\epsilon/2$. With this $r$ as the radius, draw another open ball around $d$. Then, $\forall t\in B_r(d)$, $d(d,t)<r<\epsilon/2$. By triangle inequality,
$$d(x,t) \leq d(d,t) + d(x,d) <\epsilon.$$

I have therefore proven that $B_r(d)\subseteq B_\epsilon(x)\subseteq V_i$, $i\in \alpha$. We have shown that $X$ admits a countable base. Hence, every separable space admits a countable base. (QED)

### Question 24
Following Rudin's hint, fix some $\delta>0$. Choose $x_1\in X$ and inductively choose $x_1, \dots, x_j$ such that $d(x_i, x_{i+1})\geq \delta$. I will show that this process must stop after $x_k$, $k<\infty$. Let the limit point be $x$, so in an open ball around $x$ with a radius of $\delta/2$, $\exists x_m\in B_{\delta/2}(x)$ and $x_m\neq x$. Choose a new radius $d(x,x_m)$ to draw a new open ball, $\exists x_n \in B_{d(x,x_m)}(x)$, $x_n\neq x_m\neq x$, $d(x,x_n)<d(x,x_m)<\frac{\delta}{2}$. By triangle inequality,
$$d(x_m,x_n) \leq d(x,x_n) + d(x,x_m) < \delta$$

If any two distinct $x_n, x_m$ have a distance less than $\delta$, this process stops. 

Here the way to construct a set of the centers of the corresponding neighborhoods. We take $\delta = 1/i$ each time to generate a finite set $C_i$ until any two distinct $x_{i,n}, x_{i,m}$ have a distance less than $1/i$. 
$$C = \bigcup_{i=1}^\infty C_i$$

As a union of countable sets, $C$ is countable. Then, I need to show that any $y\in X$ is either a point in $C$ or a limit point of $C$. If $y\in C$, the condition is met. If $y\notin C$, we fix an arbitrary $\epsilon>0$ and center an open ball $B_\epsilon(y)$ on $y$. Choose $N\in \mathbb{N}$ such that $1/N<\epsilon$. Consider the set $C_N$, notice that by our construction, for some $x_{N,i}\in C_N$, $d(y,x_{N,i})<1/N<\epsilon$. Then, $x_{N,i}\in C_N\subseteq C$ such that $x_{N,i}\in B_\epsilon(y)$. This shows that $y$ is a limit point of $C$. Therefore, $C$ is dense in $X$. 

As a conclusion, $C$ is both countable and dense in $X$. We can further conclude that $X$ is separable. (QED)

### Question 25

### Question 26
As a first step, I will show that every sequence in $X$ must have a convergent subsequence. Choose an arbitrary sequence $\{x_n\}$ on $X$. If there are finitely many distinct values in $\{x_n\}$, then there must be an infinite subsequence $\{x_{n_k}\}$ that share the same value. This constant subsequence converges to the constant value. If there are infinitely many distinct values in $\{x_n\}$, then this infinite subset $S=\{x_i\}_{i= 1}^\infty$ has a limit point $x$. Around this $x$, there are infinitely many points in $S$. We play the following trick:
1. In the open ball $B_1(x)$, there are infinitely many points in $S$. We choose $x_{n_1}$.
2. In the open ball $B_{1/2}(x)$, there are infinitely many points in $S$. We choose $x_{n_2}$, where $n_2$ is larger than $n_1$.
3. We repeat the iteration for $k$ times. In the open ball $B_{1/k}(x)$, there are infinitely many points in $S$. We choose $x_{n_k}$, where $n_k$ is larger than $n_{k-1}$.
4. This process may continue if needed.

It is important to note that $\forall \epsilon\in \mathbb{R}_{>0}$, $\exists K\in \mathbb{N}$ such that $1/K< \epsilon$. Then, $\forall k>K$, $d(x_{n_k}, x)<1/k < 1/K < \epsilon$. This proves that $\{x_{n_k}\}$ converges to $x$. 

As a sequence like $\{x_n\}$ exists in $X$, $\exists \{\mathscr{O}_i\}_{i=1}^{\infty}$, a countable open cover, covering all of $X$. This is because $X$ is separable (see Question 24), and it admits a countable base (see Question 23). Now, assume, BWOC, that we cannot find a finite subcover. In other words, regardless of how many sets we use to cover $X$, we must leave some elements behind.

1. $W_1 = \mathscr{O}_{1}$ cannot cover $X$, so $\exists y_1 \in X - W_1$.
2. $W_1 = \mathscr{O}_{1}\cup \mathscr{O}_{2}$ cannot cover $X$, so $\exists y_2 \in X - W_2$.
3. For every $W_m = \bigcup_{i=1}^m \mathscr{O}_i$, it cannot cover $X$, so $\exists y_m \in X-W_m$.

Notice that every infinite subset of $X$ has a limit point. Let the limit point for $\{y_n\}$ be $y$. $\exists N\in \mathbb{N}$ such that $y \in \mathscr{O}_N$ because $\{\mathscr{O}_i\}_{i=1}^{\infty}$ covers $\{y_n\}$. Notice that since $\mathscr{O}_N$, exists an open ball centered at $y$ is contained by $\mathscr{O}_N$. There exists sufficiently large $N'>N$ such that $y_{N'}$ is in this open ball. Then, $y_{N'} \in \mathscr{O}_N$. However, notice that $y_{N'}\in X - W_{N'}$. Thus, $y_{N'}\notin W_{N'}\supseteq \mathscr{O}_{N'}$. $\Rightarrow\Leftarrow$ (QED)

### Question 27
When we say a set is "at most countable", we mean that it is finite or countably infinite. Following Rudin's hint, we need to notice first that $\mathbb{R}^k$ is separable because it contains the dense countable set $\mathbb{Q}^k$. Then, the countable base $\{V_n\}$ exists. Choose those $V_n$ for which $E\cap V_n$ is finite or countably infinite. The union of such $V_n$ is denoted as $W$. 

We then discuss the relationship of $P$ and $X-W$. Suppose $p\in P$, by definition, $p$ is a condensation point of $E$. In the base $\{V_n\}$, for $P\subseteq \mathbb{R}^k$ and $p\in P$, $\exists V_\alpha$, $\alpha\in \mathbb{N}$, such that $p\in V_\alpha\subseteq P$. Such $V_\alpha$ is an open set containing $p$, so it is a neighborhood of $p$. Then, it contains uncountably many points of $E$. Therefore, $V_\alpha\not \subseteq W$. $V_\alpha \subseteq X - W$. Thus, $p\in X - W$, which proves that $P\subseteq X-W$. 

Suppose $x\in X - W$. Then, $x\notin W$. This implies that we cannot find a $V_\beta$ in the countable base $\{V_n\}$, $\beta\in \mathbb{N}$, $x\in V_\beta$, such that $E\cap V_\beta$ is finite or countably infinite. The only option is that this $E\cap V_\beta$ contains uncountably many points. In other words, $V_\beta$ contains uncountably many points of $E$. This means $x$ is a condensation point of $E$. By definition, $X-W\subseteq P$. 

From these two directions, we can conclude that $P = X-W$. By definition, $W$ contains those elements of $\{V_n\}$ which contain countably many points of $E$. The union of the sets each containing countably many points also contains countably many points of $E$. Then, at most countably many points of $E$ are not in $X-W = P$. Check that $P$ is perfect: As $W$ is the union of some open sets, it must be open, so $X-W$ must be closed. 

Moreover, we show that $\forall p\in P$, $p$ is a limit point of $P$. Notice that, as we have identified earlier, $\exists V_\alpha$ in $\{V_n\}$ such that $p\in V_\alpha$. Then, since $V_\alpha\not\subseteq W$, $E\cap V_\alpha$ is uncountable. Since $W$ is itself at most countable, $E\cap W$ is at most countable. Let $P_\alpha = \{x\mid x\in E\cap V_\alpha, x\notin E\cap W\}$, then $P_\alpha$ must be uncountable. In another way to express the nature of $P_\alpha$, $P_\alpha = E\cap V_\alpha\cap P$. An uncountable set must contain more than one element, so $\exists q\neq p$, $q\in E\cap V_\alpha\cap P$. Notice that the neighborhood $V_\alpha$ is arbitrary, so all neighborhood of $p$ must contain some $q\in P$, $q\neq p$. This proves that $\forall p\in P$, $p$ is a limit point of $P$. 

Therefore, $P$ is also perfect. (QED)

### Question 28
Denote this set as $F$ in a metric space $X$. Then, if it is at most countable, then
$$F = \varnothing \cup F$$

If it is not, according to Problem 2, the separable metric space $X$ has a countable base $\{V_n\}$ for it. Then, let $W$ be the union of those $V_n$ for which $F\cap V_n$ is countable. Then, $X-W$ is equal to the set of all condensation points of $F$, as we have proven in Problem 5. We have also proven that there are at most countably many points of $F$ not in $X-W$. Then, $W\cap F$ is at most countable.

Notice that we assume that $F$ is uncountable. Then, $F - W\cap F$ must be uncountable. In Problem 5, we have not had the chance to assess whether $E$ contains all its condensation points, but in this question, through the following Lemma we are able to conclude that $P\subseteq F$.
	For a set $F\subseteq X$, every condensation point for $F$ is a limit point of $F$.

*Proof* of the lemma: Let $p$ is a condensation point for . By definition, $\forall \mathscr{O}$ open and containing $p$, $\mathscr{O}\cap F$ is uncountable. Assume, by way of contradiction, that $p$ is not a limit point of . Then, we cannot find another point in $\mathscr{O}\cap F$. In other words, $\mathscr{O}\cap F$ only has one element. Then, it is countable. We have reached the contradiction. Therefore, for a set , every condensation point for $F$ is a limit point of $F$.

We can notice that $\forall p\in P$, $p$ is a limit point of $F$. Since $F$ is closed, $p\in F$. This proves $P\subseteq F$. 

Notice that $P = X - W$. Then, $(X - W)\cap F = X - W$. Notice that $(X - W)\cap F = X\cap F - W \cap F = F - W\cap F$, so $F - W\cap F$ is the set of condensation points for $F$, which is perfect. 

Therefore, 
$$F = (F - W\cap F)\cup (W\cap F),$$
where $F - W\cap F$ is perfect and $W\cap F$ is at most countable. (QED)

### Question 29
*Proof Roadmap*: For all nonempty open set $U\subset\mathbb{R}$, 
1. Firstly, we construct the $I_x$ for each $x\in U$: $$a_x = \inf\{a\in \mathbb{R}\mid (a,x]\subset U\}$$ $$b_x = \sup\{b\in \mathbb{R}\mid [x,b)\subset U\}$$ $$I_x = (a_x, b_x)$$
2. Secondly, we can prove that (i) this $I_x$ is open set containing $x$; (ii) it is contained in $U$; (iii) If $x,y\in U$, $I_x$ and $I_y$ are either disjoint or identical. 
3. Thirdly, we can construct a bijection between $\mathcal{C}$, the collection of $I_x$, and $\mathbb{Q}$. As $\mathbb{Q}$ is countable, we finish the proof. 
