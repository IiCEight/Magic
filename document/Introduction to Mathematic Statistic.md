# Introduction to Mathematic Statistic

## Chapter 1 Probability and Distributions

#### 1.1.2 Set Function

Many of the functions used in calculus and in this book are functions that map real numbers into real numbers. We are concerned also with functions that **map sets into real numbers**. Such functions are naturally called functions of a set or, more simply, **set functions**. Next we give some examples of set functions and evaluate them for certain simple sets.

## Chapter 2 Multivariate Distribution

#### 2.1.1 Random Vector

Given **a random experiment** with a sample space $C$, consider  two random variable $X_1$ and $X_2$, which assign to each element  $c$ of $C$ **one** and only one ordered variables $X_1(c)=x_1, X_2(c)=x_2$. Then we say that $(X_1, X_2)$ is a **random vector**. The space of $(X_1, X_2)$ is the set of ordered pairs $D=\{(x_1, x_2)|x_1 = X_1(c), x_2 = X_2(c), c \in C\}$.


### 2.3 Conditional Distributions and Expectations

In this section, we discuss **conditional distributions**, i.e., **the distribution of one of the random variables when the other has assumed a specific value.**

Suppose $p_{X_1, X_2}(x_1,x_2)$ is joint pmf, and $p_{X_1}(x_1), p_{X_2}(x_2)$ are the marginal pmf of $X_1$ and $X_2$
So the conditional probability
$$
P\{X_2=x_2 | X_1=x_1\}=\frac {P\{X_2=x_2, X_1=x_1\}}{P\{ X_1=x_1\}}=\frac{p_{X_1, X_2}(x_1,x_2)}{p_{X_1}(x_1)}

$$
for all $x_2$ in the support $S_{X_2}$ of $X_2$. Define this function as 
$$
p_{X_2,X_2}(x_2|x_1)=\frac{p_{X_2, X_1}(x_1,x_2)}{p_{X_1}(x_1)}, \ \ x_2 \in S_{X_2}
$$
It's a pmf, so we call it **conditional pmf**  of the discrete type of random variable $X_2$, given that the discrete type of random variable $X_1 = x_1$.

That means for every $X_1, p(x_1) > 0$, there has a conditional pmf of $X_2$.

Continuous type is similar.



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


## Chapter 5 Consistency and Limiting Distributions

### 5.1 Convergence in Probability

#### Definition 5.1.1 

Let $\{X_n\}$ be a sequence of random variables and let $X$ be a random variable defined on a sample space. We say that $X_1$ converges in probability to $X$ if, for all $\epsilon >0$
$$
\lim_{n\rightarrow \infty}P[|X_n - X|\ge \epsilon] =0
$$
or equivalently
$$
\lim_{n\rightarrow \infty}P[|X_n - X|< \epsilon] =1
$$
If so, we write
$$
X_n \xrightarrow{P}X
$$

#### Weak Law of Large Numbers

Let $\{X_n\}$ be a sequence of i.i.d random variables having common mean $\mu$ and variance $\sigma^2 < \infty$.
$$
\bar{X}_n\xrightarrow{P}\mu.
$$

Proof:
The variance of $\bar{X}_n$ is $\frac {\sigma^2}{n}$ , so by Chebyshev’s inequality,
$$

P[|\bar X_n-\mu|\ge \epsilon] \le\frac{\sigma^2}{n\epsilon^2}
$$

#### Theorem 5.1.2 Property

Suppose $X_n \xrightarrow{P}X$ and $Y_n \xrightarrow{P}Y$ . Then $X_n+Y_n \xrightarrow{P}X+Y$ , $X_nY_n \xrightarrow{P}XY$.


Suppose $X_n \xrightarrow{P}X$. Then $aX_n \xrightarrow{P}aX$ .

Suppose $X_n \xrightarrow{P}a$ and the real function $g$ is  continuous at $a$. Then $g(X_n) \xrightarrow{P}g(a)$. And if $X_n \xrightarrow{P}X$ and $g$ is a continuous function, then $g(X_n) \xrightarrow{P}g(X)$.


#### Consistency
Let $X$ be a random variable with cdf $F(x, \theta)$,$\theta \in \Omega$. Let $X_1,...,X_n$ be a sample from the distribution of $X$ and let $T_n$ denote a statistic. We say $T_n$ is a consistent estimator of $\theta$ if
$$
T_n \xrightarrow{P} \theta
$$

#### Convergence in Distribution

Let $\{X_n\}$ be a sequence of random variables. Let $F_{X_n}$ and $F_X$ be, respectively, the cdfs of $X_n$ and $X$. Let $C(F_X)$ denote the set of all points where $F_X$ is continuous. We say that $X_n$ **converges in distribution** to $X$ if
$$
\lim_{n\rightarrow \infty}F_{X_n}(x)=F_X,\text{for all}\ x\in C(F_{X})
$$
We denote this convergence by
$$
X_n \xrightarrow{D}X
$$
This material on convergence in probability and in distribution comes under what statisticians and probabilists refer to as **asymptotic theory**. Often, we say that the distribution of $X$ is the **asymptotic distribution** or the **limiting distribution** of the sequence $\{X_n\}$.


If $X_n$ converges to $X$ in probability, then $X_n$ converges to $X$ in distribution.



## Chapter 6 Maximum Likelihood Methods

### 6.1 Maximum Likelihood Estimation

**Likelihood function**
$$
L(\theta;\boldsymbol{x})=\prod_{i = 1}^nf(x_i;\theta)
$$

#### Regularity Conditions
(R0) The cdfs are distinct;
(R1) The pdfs have common support for all $\theta$
(R2) The **true** value point $\theta_0$ is an interior point in $\Omega$


#### Theorem 6.1.1

Assume that $\theta_0$ is the true parameter and that $E_{\theta_0}[f(X_i;\theta)/f(X_i;\theta_0)]$ exist. Under assumptions (R0) and (R1),
$$
\lim_{n\rightarrow\infty}P_{\theta_0}[L(\theta_0,X) >L(\theta,X)]=1,\text{for all }\theta \ne \theta_0
$$



## Chapter 11 Bayesian Statistics

#### Prior and Posterior Distributions
