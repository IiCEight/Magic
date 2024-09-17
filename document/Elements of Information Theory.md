# Elements of Information Theory

## Chapter 2 Entropy,  Relative Entropy and Mutual Information

### 2.1 Entropy

#### Definition

The **entropy** $H (X)$ of a discrete random variable $X$ is defined by
$$
H(X) = -\sum_{x}p(x \in \mathcal X)\log p(x)
$$
The log is to the base 2 and entropy is expressed in **bits**. We will use the convention that $0 log 0 = 0$. Adding terms of zerop robability does not change the entropy.

If the base of the logarithm is $b$, we denote the entropy as $H_b(X)$.

 If the base of the logarithm is $e$, the entropy is measured in **nats**.

 Note that entropy is a **functional(泛函)** of the distribution of $X$.



### 2.2 JOINT ENTROPY AND CONDITIONAL ENTROPY

#### joint entropy

The **joint entropy** $H (X, Y )$ of a pair of discrete random variables $(X, Y)$ with a joint distribution $p(x, y)$ is defined as
$$
H(X,Y) = -\sum_{x \in \mathcal X}\sum_{y \in \mathcal Y}p(x, y)\log p(x,y)
$$


#### conditional entropy

If $(X, Y ) \sim p(x, y)$, the **conditional entropy** **H (Y|X)** is defined as
$$
H (Y|X) = \sum_{x \in \mathcal X}p(x)H (Y|X = x) = \\
-\sum_{x \in \mathcal X}p(x)\sum_{y \in \mathcal Y}p(y|x)\log p(y|x) =\\
-\sum_{x \in \mathcal X}\sum_{y \in \mathcal Y}p(x, y)\log p(y | x) =\\
 -E\log p(Y|X)
$$


#### Theorem 2.2.1 (Chain rule)

$$
H (X, Y ) = H (X) + H (Y|X)
$$

Note that $H (Y|X) = H (X|Y )$.



### 2.3 RELATIVE ENTROPY AND MUTUAL INFORMATION

#### relative entropy or Kullback–Leibler distance

The **relative entropy** or **Kullback–Leibler distance** between two probability mass functions p(x) and q(x) is defined as
$$
D(p \parallel q) = \sum_{x \in \mathcal X} p(x) \log \frac{p(x)}{q(x)} =\\
E_p\log \frac{p(x)}{q(x)}
$$

#### mutual information

$$
I(X;Y) = \sum_{x,y}p(x,y)\frac{p(x,y)}{p(x)p(y)}=\\
D(p(x,y)||p(x)p(y))=\\
H(X)-H(Y|X)
$$



#### Theorem 2.6.2 (Jensen's inequality) 

If $f$ is a convex function and $X$ is a random variable,
$$
Ef(X)\geq f(EX).
$$



#### Theorem 2.6.3 (Information inequality)

$$
D(p||q) \ge 0
$$





#### Theorem 2.6.4

$\mathcal{X}$ is the range of $X$. $|\mathcal X|$ is the number of elements in the range of $X$.
$$
H(X) \le \log|\mathcal{X}|
$$

#### Theorem 2.6.5 Conditioning reduces entropy

$$
H(X|Y) \le H(X)
$$

Note that is true only on the average. Specifically,  $H(X|Y = y)$ may be greater than or less than or equal to $H(X)$.



#### Theorem 2.6.6 

$$
H(X_1, X_2, ..., X_n) \le \sum_iH(X_i)
$$

with equality if and only if the $X_i$ are independent.



#### Theorem 2.7.2 (Convexity of relative entropy)

$D(p||q)$ is convex.



#### Theorem 2.7.3 (Convavity of entropy)

$H(p)$ is a concave function of $p$.



#### Conditional independence

For random variables $X, Y,Z$, $X$ is independent of conditioning on $Y$ if 
$$
p(x,y,z) = p(x,y)p(y,z)
$$
more intuitionistic, if $p(z) > 0$, then it's equivalent to 
$$
p(x,y|z)=p(x|z)p(y|z)
$$

$$

$$
