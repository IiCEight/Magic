# A First Course in Probability

## Chapter 2 Axioms of Probability 

### 2.2 Sample Space and Events

Consider an experiment whose outcome is not predictable with certainty. However, although the outcome of the experiment will not be known in advance, let us suppose that the set of all possible outcomes is known. This set of all possible outcomes of an experiment is known as the **sample space** of the experiment and is denoted by *$S$*.



Any subset $E$ of the sample space is known as an **event**. 



### 2.3 Axioms of Probability 

Consider an experiment whose sample space is $S$. For each event $E$ of the sample space $S$ we assume that a number $P(E)$ is defined and satisfies the following three axioms:

#### Axiom 1

$$
0 \le P(E) \le 1
$$

#### Axiom 2

$$
P(S) = 1
$$

#### Axiom 3

For any sequence of mutually exclusive events $E_1,E_2,...($that is, events for which $E_iE_j=\emptyset$ when $i\neq j)$,
$$
P(\bigcup_{i = 1}^\infin E_i) = \sum_{i = 1}^{\infin}E_i
$$


We refer to $P(E)$ as the **probability** of the event $E$ .



### 2.6 Probability as a Continuous Set Function

A sequence of events $\{E_n,n\geq1\}$ is said to be an **increasing sequence** if
$$
E_1\subset E_2\subset\cdotp\cdotp\cdotp\subset E_n\subset E_{n+1}\subset\cdotp\cdotp\cdotp 
$$
whereas it is said to be a **decreasing sequence** if
$$
E_1\supset E_2\supset\cdots\supset E_n\supset E_{n+1}\supset\cdots 
$$

#### Proposition 6.1

If $\{E_n,n\geq1\}$ is either an increasing or a decreasing sequence of events, then
$$
\lim_{n\to\infty}P(E_n)=P(\lim_{n\to\infty}E_n)
$$


## Chapter 3 Conditional Probability and Independence 

#### Definition

The odds of an event $A$ are defined by 
$$
\frac{P(A)}{P(A^{c})} = \frac{P(A)}{1-P(A)} 
$$


## Chapter 4 Random Variables 

### 4.2 Discrete Random Variables 

#### probability mass function

For a discrete random variable $X$, we define the **probability mass function** $p(a)$ of $X$ by
$$
p(a) = P(X = a)
$$


### 4.4 Expectation of a Function of a Random Variable

If $X$ is a discrete random variable that takes on one of the values $x_i,i\geq1$, with respective probabilities $p(x_i)$, then, for any real-valued function $g$,
$$
E[g(X)]=\sum_i g(x_i)p(x_i)
$$

### 4.9 Expected Value of Sums of Random Variables 

Now, if $X$ and $Y$ are both random variables, then so is their sum $Z$. 
$$
Z(s) = X(s) + Y(s), \ \ s\in S
$$


For random variables $X_1,X_2,...,X_n$,
$$
E[\sum_i X_i] = \sum_i E[X_i]
$$


## Chapter 6 Jointly Distributed Random Variables 

### 6.4 Conditional Distributions: Discrete Case 

Hence, if $X$ and $Y$ are discrete random variables, it is natural to define the conditional probability mass function of $X$ given that $Y = y$ by
$$
p_{x | Y}(x|y) = \frac{p(x, y)}{p_Y(y)}
$$

### 6.5 Conditional Distributions: Continuous Case 

If $X$ and $Y$ have a joint probability density function $f(x,y)$, then the conditional probability density function of $X$ given that $Y = y$ is defined, for all values of $y$ such that $f_Y(y) >0$ by
$$
f_{X|Y}(x|y) = \frac{f(x, y)}{f_{Y}(y)}
$$


## Chapter 7 Properties of Expectation 

If $X$ and $Y$ have a joint probability mass function $p(x,y)$, then
$$
E[g(X,Y)]=\sum_y\sum_xg(x,y)\:p(x,y)
$$
If $X$ and $Y$ have a joint probability density function $f(x,y)$, then
$$
E[g(X,Y)]=\int_{-\infty}^{\infty}\int_{-\infty}^{\infty}g(x,y)f(x,y)\:dx\:dy
$$


### 7.4 Covariance, Variance of Sums, and Correlations 

If $X$ and $Y$ are independent, then, for **any functions** $h$ and $g$,
$$
E[g(X)h(Y)]=E[g(X)]E[h(Y)]
$$


### 7.5 Conditional Expectation 

It is therefore natural to define, in this case, the conditional expectation of $X$ given
that $Y=y$, for all values of $y$ such that $p_Y(y)>0$,by
$$
E[X|Y=y]=\sum_{x}\:xP\{X=x\:|\:Y=y\}\\
=\sum_{x}xp_{X|Y}(x|y)
$$
It is natural, in this case, to define the conditional expectation of $X$, given that $Y=y$, by
$$
E[X|Y=y]=\int_{-\infty}^\infty xf_{X|Y}(x|y)\:dx
$$

$$
E[g(X)|Y=y]=\begin{cases}\sum_xg(x)\:p_{X|Y}(x|y)&\text{in the discrete case}\\\\\int_{-\infty}^\infty g(x)\:f_{X|Y}(x|y)\:dx&\text{in the continuous case}\end{cases}
$$



#### Computing expectations by conditioning 

**Note: $E[X | Y = y]$ is just a real number.**

Let us denote by $E[X | Y]$ that **function of the random variable $Y$** whose value at $Y = y$

is $E[X | Y= y]$. So we can think that
$$
f = E[X | Y]\\
f(y) = E[X | Y = y], \ \ y \in Y\\
$$


**And furthermore, $X | Y = y$ is also a random variable.**

**Since E[X | Y] is a real function and domain is sample space, So E[X | Y] is also a  random variable**



#### The conditional expectation formula

So we can compute expectation of random variable $E[X|Y]$, 
$$
E[E[X|Y]] = E[X]
$$
Amazing! It's $E[X]$.

If $Y$ is a discrete random variable, then 
$$
E[E[X|Y]] = E[X] =\sum_yE[X|Y=y]P\{Y=y\}
$$
whereas if $Y$ is continuous with density $f_Y(y)$,then Equation (5.1) states
$$
E[E[X|Y]] =E[X]=\int_{-\infty}^\infty E[X|Y=y]f_Y(y)\:dy
$$
**In facts, $E[X|Y]$ is a function of $Y$, so we can say**
$$
g(Y) = E[X|Y]
$$
so
$$
E[E[X|Y]] = E[g(Y)] = \sum_yg(y)p(y) =\sum_yE[X|Y=y]P\{Y=y\}
$$


One way to understand  is to interpret it as follows: To calculate $E[X]$, we may take a **weighted average** of the conditional expected value of $X$ given that $Y = y$, **each of the terms $E[X | Y = y]$ being weighted by the probability $p(Y = y)$ of the event on which it is conditioned**. 

This is an **extremely useful result** that often enables us to compute expectations easily by first conditioning on some appropriate random variable. 



#### Conditional variance 

**See page 550**



## Chapter 8 Limit Theorems 

 