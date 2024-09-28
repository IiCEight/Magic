# Introduction to Mathematic Statistic

## Chapter 1 Probability and Distributions

#### 1.1.2 Set Function

Many of the functions used in calculus and in this book are functions that map real numbers into real numbers. We are concerned also with functions that **map sets into real numbers**. Such functions are naturally called functions of a set or, more simply, **set functions**. Next we give some examples of set functions and evaluate them for certain simple sets.

## Chapter 2 Multivariate Distribution

#### 2.1.1 Random Vector

Given **a random experiment** with a sample space $C$, consider  two random variable $X_1$ and $X_2$, which assign to each element  $c$ of $C$ **one** and only one ordered variables $X_1(c)=x_1, X_2(c)=x_2$. Then we say that $(X_1, X_2)$ is a **random vector**. The space of $(X_1, X_2)$ is the set of ordered pairs $D=\{(x_1, x_2)|x_1 = X_1(c), x_2 = X_2(c), c \in C\}$.

#### 2.6.1 Multivariate Variance-Covariance Matrix

Let $\mathbf{X} = (X_1, X_2, ..., X_n)^T$ be an n-dimensional random vector.

We define $E[\mathbf{X}] = (E[X_1], E[X_2], ..., E[X_n])^T$.




Now suppose $\mathbf{W}$ is an $n \times m$ matrix of random variable. Note that we can always string out the matrix into an mn × 1 random vector. Hence, we define the expectation of a random matrix
$$
E[\mathbf {W}] =[E[W_{i, j}]]
$$

$[A_{ij}]$ means a matrix in which the entry at row $i$ and column $j$ is $A_{ij}$.

The **mean** of $\mathbf{X}$ is $\boldsymbol{\mu} = E[\mathbf {X}]$ and we define its **variance-covariance matrix** as
$$
Cov(\mathbf{X}) = Cov(E[(\mathbf{X} -\boldsymbol{\mu})(\mathbf{X} -\boldsymbol{\mu})^T]) =[\sigma_{ij}]
$$

#### properties
$$
\begin{align}
& E[A_1W_1+A_2W_2]=A_1E[W_1]+A_2E[W_2] \\
&E[AWB]=AE[W]B\\
& Cov(\mathbf{X})=E[\mathbf{X}\mathbf{X}^T]-\boldsymbol{\mu}\boldsymbol{\mu}^T\\
&cov(\mathbf{X})= \mathbf{A}E[\mathbf{X}]\mathbf{A}^T
\end{align}
$$


All variance-covariance matrices are **positive semi-definite** matrices; that is, $\mathbf{a}^T Cov(\mathbf{X})\mathbf{a} ≥ 0$, for all vectors $\mathbf{a} \in R^n$.
To see this let $\mathbf{X}$ be a random vector and let $\mathbf{a}$ be any $n \times 1$ vector of constants. And $Y = \mathbf{a}^T\mathbf{X}$ is a one dimension random variable. So
$$
0\le Var(Y) = Var(\mathbf{a}^T\mathbf{X})=Cov(\mathbf{a}^T\mathbf{X})= \mathbf{a}^T\mathbf{X}\mathbf{a}
$$

#### 2.8 Linear Combinations of Random variables

Let $(X_1,...,X_n)$ denote a random vector. In this section, we consider linear combinations of these variables, writing them , generally, as
$$
T = \sum_{i = 1}^n a_iX_i
$$
Suppose
$$
W = \sum_{i = 1}^m b_iY_i
$$
then
$$
Cov(T, W) = \sum_{i = 1}^n\sum_{j = 1}^m a_ib_jCov(X_i, Y_j)
$$
$$
Var(T) = Cov(T,T)=\sum_{i=  1}^na_i^2Var(X_i) +2\sum_{i \le j}a_ia_jCov(X_i, X_j)
$$

If $X_1, ...,X_n$ are independent, then
$$
Var(T)=\sum_{i=  1}^na_i^2Var(X_i)
$$
#### 2.8.1 Random Sample
If the random variables $X_1, X_2,...,X_n$ are independent and identically distributed, i.e. each $X_i$ has the same distribution, then we say that these random variables constitute a **random sample** of size n from that common distribution. We abbreviate independent and identically distributed by **iid**.


## Chapter 4 Some Elementary Statistical Inferences

### Confidence Intervals

#### 4.2.1 (Confidence Interval)

Let $X_1,...,X_n$ be a sample on a random varibale $X$, where $X$ has pdf $f(x; \theta),\theta \in \Omega$. Let $0 < \alpha < 1$ be specified. Let $L=L(X_1, ...,X_n)$ and $U = U(X_1, ..., X_n)$ be two statistics. We say that the interval $(L, U)$ is a $(1 -\alpha)100\%$ **confidence interval** for $\theta$ if 
$$
1-\alpha = P_{\theta}[\theta \in (L, U)]
$$
That is, the probability that the interval includes $\theta$ is $1-\alpha$, whch is called the **confidence coeffcient** or the **confidence level** of the interval.

A measure of efficiency based on a confidence interval is its expected length.


### 4.4 Order Statistics


### 4.5 Introduction to Hypothesis Testing

Suppose our interest centers on a random variable $X$ that has density function $f(x; \theta)$, where $\theta \in \Omega$. Suppose we think, due to theory or a preliminary experiment, that $\theta \in \omega_0$ or $\theta ∈ \omega_1$, where $\omega_0$
 and $\omega_1$ are disjoint subset of $\Omega$. We label these hypothese as
 $$
 H_0: \theta \in \omega_0 \ \ v.s. \ H_1:\theta \in \omega_1
 $$
 Denote the space of the sample by $D$; that is, $D = \space\{(X_1, ...,X_n)\}$. A **test** of $H_0$ is based on a subset $C$ of $D$. This set $C$ is called the **critical region** and its corresponding decision rule (test) is

Reject $H_0$ if $(X_1,...,X_n) \in C$
remain $H_0$ if $(X_1,...,X_n) \in C^{c}$

#### critical region

We say a critical region $C$ is of size $\alpha$ if
$$
\alpha = max_{\theta \in \omega_0} P_{\theta}[(X_1, ..., x_n)\in C]
$$
Roughly speaking, when $H_0$ is ture, the maximum probability we reject $H_0$ is $\alpha$.

Over all critical regions of size $\alpha$, we want to consider critical regions that havelower probabilities of Type II error. That is, for $\theta \in \omega_1$, we maximize the probability of acceptance of $H_1$ which means we minimize probability of Type II error.
$$
1 − P_{\theta}[\text{Type II Error}] = P_{\theta}[(X_1,...,X_n) \in C].
$$
The probability on the right side of this equation is called the **power** of the test at $\theta$.

We define the **power function** of a critical region to be
$$
\gamma C (\theta) = P_{\theta}[(X_1,...,X_n) \in C];  \ \ \ \theta \in \omega_1.

$$

Hence, given two critical regions $C_1$ and $C_2$, which are both of size $\alpha$, $C_1$ is better than $C_2$ if $\gamma C_1 (\theta) \ge \gamma C_2 (\theta)$ for all $\theta \in \omega_1$.