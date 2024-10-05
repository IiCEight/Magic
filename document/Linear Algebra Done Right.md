# Linear Algebra Done Right

## Chapter 1 Vector Space

### 1A $R^n$ and $C^n$

**Complex arithmetic is a field**

$a,b,c,z \in C$ complex set.

1.commutaivity
$$
a+b = b+ a, ab =ba
$$
2.associativity
$$
(a+b)+c = a + (b + c),(ab)c=a(bc)
$$
3.identities
$$
z+0 =z,z\cdot1 =z
$$
4.additive inverse
$$
\forall a\in C, \exist !b\in C, s.t. \ a+ b = 0
$$
5.multiplicative inverse
$$
\forall a \ne 0, \exist!b \in C, s.t. ab =0
$$
6.distributive property
$$
c(a + b) = ca + cb
$$




### 1B Definition of Vector Space

The motivation for the definition of a vector space comes from properties of **addition** and **scalar multiplication** in $F^𝑛$:  Addition is commutative, associative, and has an identity. Every element has an additive inverse. Scalar multiplication is associative. Scalar multiplication by 1 acts as expected.



**It's not the same as field but similar to that.**



#### definition: vector space

A **vector space** is a set $V$ along with an addition on $V$ and a scalar multiplicationon $V$ such that the following properties hold.

$u,v,w\in F^n,a,b\in F$

1.commutativity
$$
u+v= v+ u
$$
2.associativity
$$
(u+v)+w=u+(v+w),(ab)v=a(bv)
$$
3.additive identity

4.additive inverse

5.multiplicative identity

6.distributive properties
$$
a(u+v) = au+av
$$

### 1C subspace

A subset $U$ of $V$ is a subspace of $V$ if and only if $U$ satisfies the following three conditions.

1.additive identity
$$
0\in U
$$
2.closed under addition

3.closed under scalar multiplication



#### definition: sum of subspaces

$$
V_1+...+V_m = \{v_1+...+v_m\ | \ v_1 \in V_1, ...,v_m \in V_m \}
$$

suppose $V_1, ..., V_m$ are subspaces of $V$. Then $V_1 +...+V_m$ is the smallest subspace of $V$ containing $V_1, ..., V_m$.



#### definition: direct sum $\oplus$

The sum $V_1, ..., V_m$ is called a direct sum if each element of $$V_1 +...+V_m$$ can be written in **only one way** as a sum $v_1 + ⋯ + v_m$, where each $v_k \in V_k$.



#### condition for a direct sum

Suppose $V_1, ..., V_m$ are subspaces of $V$. Then $V_1 +...+V_m$ is a direct sum if and only if the only way to write $0$ as a sum $v_1 + ⋯ + v_m$, where each $v_k \in V_k$, is by taking each $v_k$ equal to 0.



#### direct sum of two subspaces

Suppose $U$ and $W$ are subspaces of $V$. Then
$$
U+W \  is \ a \ direct \ sum \Lrarr U \cap W = \{0\} 
$$


## Chapter 2 Finite-Dimensional Vector Spaces

### 2A Span and Linear Independence



**span is the smallest containing subspace**



### 2B Bases

#### every subspace of $V$ is part of a direct sum equal to $V$

Suppose $V$ is finite-dimensional and $U$ is a subspace of $V$. Then there is a subspace $W$ of $V$ such that $V = W \oplus V$



### 2C Dimension

#### dimension of a sum

If $V_1$ and $V_2$ are subspaces of a finite-dimensional vector space, then
$$
\dim(V_1 + V_2) = \dim(V_1) + \dim(V_2) - \dim(V_1\cap V_2)
$$
For $S$ a finite set, let $\#S$ denote the number of elements of $S$. The table below compares finite sets with finite-dimensional vector spaces, showing the analogy between $\#𝑆$ (for sets) and dim $V$ (for vector spaces), as well as the analogy between unions of subsets (in the context of sets) and sums of subspaces (in the context of vector spaces).



## Chapter 3 Linear Maps

### 3A Vector Space of Linear Maps

A **linear map** from $V$ to $W$ is a function $T: V \rarr W$ with the following properties.

$u, v \in F^n, \lambda \in F$

1.additvity
$$
T(u + v) = T(u) + T(v)
$$
2.homogeneity
$$
T(\lambda v)= \lambda T(v)
$$
**Note that for linear maps we often use the notation $Tv$ as well as the usual function notation $T(v)$**



The set of linear maps from $V$ to $W$ is denoted by $\mathcal L(V, W)$.

The set of linear maps from $V$ to $V$ is denoted by $\mathcal L(V) = \mathcal L(V, V)$.



#### linear map lemma

uppose $v_1, ..., v_n$ is a basis of $V$ and $w_1,... , w_n \in W$. Then there exists a **unique** linear map $T: V \rarr W$ such that
$$
Tv_k = w_k, k = 1, ...,n
$$

####  addition and scalar multiplication on $\mathcal L(V, W)$

Suppose $S, T \in \mathcal L(V, W)$ and $\lambda \in F$. The sum $S + T$ and the product $\lambda𝑇$ are the linear maps from $V$ to $W$ defined by
$$
(S + T)(v) = Sv + Tv,(\lambda T)(v) = \lambda(Tv)
$$


#### $\mathcal L(V, W)$ is a vector space

With the operations of addition and scalar multiplication as defined above, $\mathcal L(V, W)$ is a vector space.





#### product of linear maps

Usually it makes no sense to multiply together two elements of a vector space,but for some pairs of linear maps a useful product exists, as in the next definition.

If $T \in \mathcal L(U, V)$ and $S \in \mathcal L(V, W)$, then the **product** $ST \in \mathcal L(U, W)$ is defined by
$$
(ST)(u) = S(Tu), u \in U
$$
Thus $ST$ is just the usual composition $S \circ T$ of two functions.



#### algebraic properties of products of linear maps

1.associativity
$$
(T_1T_2)T_3= T_1(T_2T_3) 
$$
2.identity
$$
TI = IT =T
$$
3.distributive properties
$$
(S_1+ S_2)T = S_1T + S_2T,S(T_1+T_2) = ST_1 + ST_2
$$
Multiplication of linear maps is **not** commutative.



#### linear maps take $0$ to $0$

Suppose $T$ is a linear map from $V$ to $W$. Then $T(0) = 0$.



### 3B Null Spaces and Ranges

For $T \in \mathcal L(V, W)$, the null space of $V$, denoted by $null\ T$, is the subset of $V$ consisting of those vectors that $T$ maps to $0$:
$$
null \ T = \{v\in V | Tv = 0\}
$$


#### The null space is a subspace



#### $T \in \mathcal L(V, W)$ is injective if and only if $null\ T = \{0\}$.



#### The range is a subspace

If $T \in \mathcal L(V, W)$, then range $T$ is a subspace of $W$.



#### Fundamental Theorem of Linear Maps

Suppose $V$ is finite-dimensional and $T \in \mathcal L(V, W)$. Then range $T$ is finitedimensional and
$$
\dim V = \dim null \ T + \dim range \ T
$$


### 3C Matrices

####  matrix of a linear map

suppose $T \in \mathcal L(V, W)$ and $v_1, ..., v_n$ is a basis of $V$ and $w_1, ..., w_m$ is a basis of $W$. The matrix of $T$ with respect to these bases is the m-by-n matrix $\mathcal M(𝑇)$ whose entries $𝐴_{j, k}$ are defined by
$$
Tv_k = A_{1, k}w_1+ ...+A_{m,k}w_m
$$


### 3D Invertibility and Isomorphisms

#### inverse is unique



#### A linear map is invertible if and only if it is injective and surjective.



#### definition: isomorphism, isomorphic

An isomorphism is an **invertible linear map**.

Two vector spaces are called isomorphic if there is an isomorphism from one vector space onto the other one.



#### dimension shows whether vector spaces are isomorphic

Two finite-dimensional vector spaces over $F$ are isomorphic if and only if they have the same dimension.



#### $\mathcal L(V, W)$ and $F^{m, n}$ are isomorphic

suppose $v_1, ..., v_n$ is a basis of $V$ and $w_1, ..., w_n$ is a basis of $W$. Then $\mathcal M$ is an isomorphism between $\mathcal L(V, W)$ and $F^{m, n}$.



#### definition: matrix of a vector

uppose $v \in V$ and $v_1, ..., v_n$ is a basis of $V$. The matrix of $v$ with respect to this basis is the n-by-1 matrix
$$
\mathcal M(v) = 
\begin{pmatrix}
b_1\\
b_2\\
...\\
b_n\\
\end{pmatrix}
$$
where $b_1, ..., b_n$ are scalars such that 
$$
v = b_1v_1 + ...+ b_nv_n
$$
It transform a vector to the $n\times 1$ matrix. So vector can be handle as matrix.



**Example:**

The matrix of a vector $x \in F^n$ with respect to the standard basis is obtained by writing the coordinates of $x$ as the entries in an n-by-1 matrix.In other words. if $x = (x_1, ...,x_n)\in F^n$
$$
\mathcal M (x) =
\begin{pmatrix}
x_1\\
x_2\\
...\\
x_n\\
\end{pmatrix}
$$


#### linear maps act like matrix multiplication

proof see page 89



### Important !!!

The result above can be used to think of every linear map (from a finite-dimensional vector space to another finite-dimensional vector space) as a matrix multiplication map after suitable relabeling via the isomorphisms given by $\mathcal M$.

Specifically, if $T \in \mathcal L(V, W)$ and we identify $v \in V$ with $\mathcal M(v) \in F^{n,1}$, then the result above says that we can identify $Tv$ with $\mathcal M(𝑇)\mathcal M(𝑣)$.

Because the result above allows us to think (via isomorphisms) of each linear map as multiplication on $F^{n,1}$ by some matrix $A$, keep in mind that the specific matrix $A$ depends not only on the linear map but also on the choice of bases. 



One of the themes of many of the most important results in later chapters will be **the choice of a basis** that makes the matrix $A$ **as simple as possible**.

**sometimes thinking of linear maps as matrices (or thinking of matrices as linearmaps) gives important insights that we will find useful.**



#### dimension of range $T$ equals column rank of $\mathcal M(T)$



### 3E Products and Quotients of Vector Spaces

#### product of vector spaces

Cartesian product.



#### product of vector spaces is a vector space





#### a sum is a direct sum if and only if dimensions add up

subspace $V_1, V_2, ..., V_m \sube V$. $V_1+ ...+V_m$ is a direct sum if and only if
$$
\dim (V_1 + ...+V_m) = \dim V_1+...+\dim V_m
$$


#### notation: $v +U$

suppose $v \in V$ and $U \sube V$. Then $v + U$ is the subset of $V$ defined by 
$$
v + U = \{v + u| u \in U\}
$$


#### definition: translate

For $v \in V$ and $U$ a subset of $V$, the set $v + U$ is said to be a translate of $U$



####  definition: quotient space

Suppose $U$ is a subspace of $V$. Then the quotient space $V/U$ is the set of all translates of $U$. Thus
$$
V/U = \{v + U | v \in V\}
$$

#### two translates of a subspace are equal or disjoint

Suppose $U$ is a subspace of $V$ and $v, w \in V$. Then
$$
v - w  \in U \Lrarr v + U = w+ U \Lrarr(v+U) \cap(w +U) \ne \empty
$$


#### addition and scalar multiplication on $V/U$

Suppose $U$ is a subspace of $V$. Then addition and scalar multiplication are defined on $V/U$ by
$$
(v+ U) + (w + U) = (v + w) + U \\
\lambda(v + U) = \lambda v + U
$$


#### quotient space is a vector space

**The element of quotient space is a set.**



#### definition: quotient map

Suppose $U$ is a subspace of $V$. The **quotient map** $\pi: V \rarr V/U$ is the **linear map** defined by
$$
\pi(v) = v + U \ \ (v \in V)
$$




#### dimension of quotient space

$$
\dim V/U = \dim V - \dim U
$$



Use the fundamental theorem of linear map. ($\pi$ is a linear map.)



####  notation: $\tilde T$

$T \in \mathcal L(V, W)$. Define $\tilde T :  V /(null \ T) \rarr W$ by
$$
\tilde T(v + null \ T) = Tv
$$
 It is a **linear map**.



#### null space and range of $\tilde T$

$T \in \mathcal L(V, W)$.

(a) $\tilde T \circ \pi = T$, where $\pi$ is  the quotient map of $V$ onto $V / (null \ T)$.

(b) $\tilde T$ is injective.

(c) range $\tilde T$  = range $T$

(d) $V/ (null \ T$) and range $T$ are isomorphic vector space.





(b) Proof : $\tilde T(v + null \ T) = Tv = 0$, so $v \in null \ T$, then $null \ \tilde T = \{0 + null \ T\}$.It means it is injective.

(d) Proof:  (b) says $\tilde T$ is injective and (c) says $\tilde T$ is surjective. So  $\tilde T$ is the isomorphic map from $V / null \ T$ onto range $T$ which complete the proof. 



### 3F Duality

Skipped.



## Chapter 4 Polynomials



#### each zero of a polynomial corresponds to a degree-one factor

Suppose $m$ is a positive integer and $p\in\mathcal{P}({F})$ is a polynomial of degree $m.$ Suppose $\lambda\in{F}.$ Then $p(\lambda)=0$ if and only if there exists a polynomial $q\in\mathcal{P}({F})$ of degree $m-1$ such that
$$
p(z)=(z-\lambda)q(z)
$$
for every $z\in{F}.$



#### degree $m$ implies at most $m$ zeros

Suppose $m$ is a positive integer and $p\in \mathcal{P}(F)$ is a polynomial of degree $m$.

Then $p$ has at most $m$ zeros in $F$.



#### fundamental theorem of algebra, first version

Every nonconstant polynomial with complex coefficients has a zero in $C$.



#### fundamental theorem of algebra, second version

If $p\in\mathcal{P}({C})$ is a nonconstant polynomial, then $p$ has a unique factorization(except for the order of the factors) of the form
$$
p(z)=c(z-\lambda_1)\cdots(z-\lambda_m),
$$
where $c,\lambda_1,...,\lambda_m\in{C}.$



#### factorizationofa polynomial over R

Suppose $p\in\mathcal{P}({R})$ is a nonconstant polynomial. Then $p$ has a **unique** factorization (except for the order of the factors) of the form
$$
p(x)=c(x-\lambda_1)\cdots(x-\lambda_m)(x^2+b_1x+c_1)\cdots(x^2+b_Mx+c_M),
$$
where $c,\lambda_1,...,\lambda_m,b_1,...,b_M,c_1,...,c_M\in{R}$, with $b_k^2<4c_k$ for each $k.$



## Chapter 5 Eigenvalues and Eigenvectors

### 5A Invariant Subspaces

#### definition: operator

A linear map from a vector space to itself is called an **operator(算子)**.



####  definition: invariant subspace

Suppose $T \in \mathcal L(V)$. A subspace $U$ of $V$ is called **invariant** under $T$ if $Tu \in U$ for every $u \in U$.





#### definition: eigenvalue

Suppose $T \in \mathcal L(V)$. A number $\lambda \in F$ is called an eigenvalue of $T$ if there exists $v \in V$ such that $v \ne 0$ and $Tv = \lambda  v$.

#### definition: eigenvector



### 5B The Minimal Polynomial

#### existence of eigenvalues

Every operator on a finite-dimensional nonzero complex vector space has an eigenvalue.



### 5C Upper-Triangular Matrices

#### conditions for upper-triangular matrix

Suppose $T \in \mathcal L(V)$ and $v_1, ..., v_n$ is a basis of $V$. Then the following are equivalent.

(a) The matrix of $T$ with respect to $v_1, ..., v_n$ is upper triangular.

(b) span($v_1, ..., v_n$) is invariant under $T$ for each $k = 1, ..., n$.

(c) $Tv_k \in span(v_1, ..., v_n)$ for $k = 1, ..., n$.



#### equation satisfied by operator with upper-triangular matrix

Suppose $T \in \mathcal L(V)$ and $V$ has a basis with respect to which $T$ has an uppertriangular matrix with diagonal entries $\lambda_1, ...,\lambda _n$. Then
$$
(T- \lambda_1I)...(T - \lambda_nI) =0
$$
Right hand side $0$ is a $n \times n$ matrix.



#### determination of eigenvalues from upper-triangular matrix

Suppose $T \in \mathcal L(V)$ has an upper-triangular matrix with respect to some basis of $V$. Then the eigenvalues of 𝑇 are precisely the entries on the diagonal of that upper-triangular matrix.



### 5D Diagonalizable Operators

#### diagonalizable

An operator on $V$ is called **diagonalizable** if the operator has a diagonal matrix with respect to some basis of $V$.



#### definition: eigenspace

Suppose $T \in \mathcal L(V)$ and $\lambda \in F$. The eigenspace of $T$ corresponding to $\lambda$ is the subspace $E(\lambda, T)$ of $V$ defined by
$$
E(\lambda, T) = null(T - \lambda I) = \{v \in V|Tv = \lambda v\}
$$
Hence $E(\lambda,  T)$ is the set of all eigenvectors of $T$ corresponding to $\lambda$, along with the $0$ vector.



#### sum of eigenspaces is a direct sum

Suppose $T \in \mathcal L(V)$ and $\lambda_1, ...,\lambda_m$ are distinct eigenvalues of $T$. Then
$$
E(\lambda_1, T)+ ... +E(\lambda_m, T)
$$
is a direct sum. Furthermore,  if $V$ is finite-dimensional, then
$$
\dim E(\lambda_1, T)+...+\dim E(\lambda_m, T) \le V
$$


#### Conditions for Diagonalizability

Suppose $V$ is finite-dimensional and $T \in \mathcal L(V)$. Let $\lambda_1, ...,\lambda_m$ denote the distinct eigenvalues of $T$. Then the following are equivalent.

(a) $T$ is diagonalizable.

(b) $V$ has a basis consisting of eigenvectors of $T$.

(c) $V = E(\lambda_1, T)\oplus ... \oplus E(\lambda_m, T)$

(d) $\dim V = \dim E(\lambda_1, T) + ...+ \dim(\lambda_m, T)$



#### Gershgorin disks

Suppose $T \in \mathcal L(V)$ and $v_1, ..., v_n$ is a basis of $V$. Let $A$ denote the matrix of $T$ with respect to this basis. A **Gershgorin disk** of $T$ with respect to the basis $v_1, ..., v_n$ is a set of the form
$$
\{z \in F | |z - A_{j,j}| \le \sum_{k = 1, k\ne j}^n |A_{j, k}| \}
$$
where $j \in \{1, ..., n\}$





#### Gershgorin disk theorem

Suppose $T \in \mathcal L(V)$ and $v_1, ..., v_n$ is a basis of $V$. Then each eigenvalue of $T$ is contained in some Gershgorin disk of $T$ with respect to the basis $v_1, ..., v_n$.





### 5E Commuting Operators

#### commute

Two operators $S$ and $T$ on the same vector space **commute** if $ST = TS$.

Two square matrices $A$ and $B$ of the same size **commute** if $AB = BA$.



**Commuting matrices are unusual.** For example, there are 214,358,881 pairs of 2-by-2 matrices all of whose entries are integers in the interval [−5, 5]. Only about 0.3% of these pairs of matrices commute.



#### commuting operators correspond to commuting matrices



#### eigenspace is invariant under commuting operator

Suppose $S,T \in \mathcal L(V)$  commute and $\lambda \in F$. Then $E(\lambda, S) $ invariant under under $T$







## Chapter 6 Inner Product Spaces

### 6A Inner Products and Norms

####  inner product

An inner product on $V$ is a function that takes each ordered pair $(u,v)$ of elements of $V$ to a number $\langle u,v\rangle\in F$ and has the following properties.

**positivity**

$\langle v,v\rangle\geq0$ for all $v\in V.$

**definiteness**

$\langle v,v\rangle=0$ if and only if $v=0.$

**additivity in first slot**

$\langle u+v,w\rangle=\langle u,w\rangle+\langle v,w\rangle$ for all $u,v,w\in V.$

**homogeneity in first slot**

$\langle\lambda u,v\rangle=\lambda\langle u,v\rangle$ for all $\lambda\in F$ and all $u,v\in V.$

**conjugate symmetry**
$\langle u,v\rangle=\overline{\langle v,u\rangle}$ for all $u,v\in V.$



####  inner product space

An **inner product space** is a vector space $V$ along with an inner product on $V$.



## NOTE:

For the rest of this chapter and the next chapter, $v$ and $w$ denote inner product spaces over $F$.



#### Norms

For $v\in V$,the norm of $v$,denoted by $\|v\|$, is defined by
$$
\|v\|=\sqrt{\langle v,v\rangle}
$$


#### orthogonal

Two vectors $u,v \in V$ are called **orthogonal** if $\langle u, v\rangle = 0$.



#### Pythagorean theorem

Suppose $u,v\in V.$ If $u$ and $v$ are orthogonal, then
$$
\|u+v\|^2=\|u\|^2+\|v\|^2
$$


#### an orthogonal decomposition

Suppose $u,v \in V$, with $v \ne 0$. Set $c = \frac {\langle u, v\rangle}{||v||^2}$, and $w = u -\frac {\langle u, v\rangle}{||v||^2} v$. Then
$$
u = cv + w,\langle w, v\rangle = 0
$$


#### Cauchy–Schwarz inequality

Suppose $u, v \in V$. Then
$$
|\langle u, v\rangle |\le||u||\  ||v||
$$
his inequality is an equality if and only if one of $u,v$ is a scalar multiple of the other.



####  triangle inequality

$$
||u + v||\le||u|| + ||v||
$$



####  parallelogram equality



### 6B Orthonormal Bases

#### orthonormal(标准正交)



Suppose $e_1,...,e_n$ is an orthonormal basis of $V$ and $u,v\in V.$ Then

(a) $v=\langle v,e_1\rangle e_1+\cdots+\langle v,e_n\rangle e_n;$

(b) $\|v\|^2=|\langle v,e_1\rangle|^2+\cdots+|\langle v,e_n\rangle|^2;$

(c) $\langle u, v\rangle = \langle u, e_1\rangle \overline {\langle v, e_1\rangle }+ \cdots + \langle u, e_n\rangle \overline {\langle v, e_n\rangle }.$



#### linear functional, dual space,

A **linear functional** on $V$ is a linear map from $V$ to $F$. The **dual space** of $V$, denoted by $V'$
, is the vector space of all linear functionals on $V$. In other words, $V' = \mathcal{L}(V,F)$.



#### Riesz representation theorem

Suppose $V$ is fnite-dimensional and $\varphi$ is a linear functional on $V.$ Then there is a unique vector $v\in V$ such that
$$
\varphi(u)=\langle u,v\rangle 
$$
for every $u\in V.$



### 6C Orthogonal Complements and Minimization Problems

#### Orthogonal Complements

If $U$ is a subset of $V$, then the orthogonal complement of $U$, denoted by $U^\perp$, is the set of all vectors in $V$ that are orthogonal to every vector in $U{:}$
$$
U^\perp=\{v\in V:\langle u,v\rangle=0\text{ for every }u\in U\}
$$


#### properties of orthogonal complement

(a) If $U$ is a subset of $V$, then $U^\perp$ is a subspace of $V.$

(b) $\{0\}^\perp=V.$

(c) $V^\perp = \{ 0\} .$

(d) If $U$ is a subset of $V$, then $U|\cap U^\perp\subseteq\{0\}.$

(e) If $G$ and $H$ are subsets of $V$ and $G\subseteq H$, then $H^\perp\subseteq G^\perp.$



#### direct sum of a subspace and its orthogonal complement

Suppose $U$ is a finite-dimensional subspace of $V$. Then 
$$
V = U \oplus U^{\perp} \\
\dim U^{\perp}=\dim V - \dim U
$$


#### orthogonal complement of the orthogonal complement

Suppose $U$ is a finite-dimensional subspace of $V$. Then
$$
U = (U^{\perp})^{\perp}
$$


####  orthogonal projection

Suppose $U$ is a fınite-dimensional subspace of $V.$ The orthogonal projection of $V$ onto $U$ is the operator $P_u\in\mathcal{L}(V)$ defıned as follows: For each $v\in V$, write $v=u+w$, where $u\in U$ and $w\in U^\perp.$ Then let $P_Uv=u.$



**Orthogonal projection $P_{U}$ maps $v$ to the point which is the closest to $v$ in $U$.**



#### properties of orthogonal projection

Suppose $U$ is a fınite-dimensional subspace of $V.$ Then
(a) $P_U\in\mathcal{L}(V);$

(b) $P_Uu=u$ for every $u\in U;$

(c) $P_Uw=0$ for every $w\in U^\perp;$ 

(d) range $P_U=U;$ 

(e) null$P_U=U^\perp;$ 

(f) $v- P_Uv\in U^\perp$ for every $v\in V;$

(g) $P_U^2=P_U;$

(h) $\|P_Uv\|\leq\|v\|$ for every $v\in V;$

(i)  if $e_1, . . . , e_m$ is an orthonormal basis of $U$ and $v\in V$,then
$$
P_Uv=\langle v,e_1\rangle e_1+\cdots+\langle v,e_m\rangle e_m.
$$


### Minimization Problems

#### minimizing distance to a subspace

Suppose $U$ is a fınite-dimensional subspace of $V,v\in V$, and $u\in U.$ Then
$$
\|v-P_Uv\|\leq\|v-u\|.
$$
Furthermore, the inequality above is an equality if and only if $u=P_Uv.$



### Pseudoinverse

If $T$ is not invertible, then we can still try to do as well as possible with the equation above. For example, if the equation above has no solutions, then instead of solving the equation $Tv-w=0$, **we can try to fınd $v\in V$ such that $\|Tv-w\|$ is as small as possible.** As another example, if the equation above has infinitely many solutions $v\in V$, **then among all those solutions we can try to find one such that $\|v\|$ is as small as possible.**
The pseudoinverse will provide the tool to solve the equation above as well as possible, even when $T$ is not invertible. 



#### restriction ofalinear map to obtain a one-to-one and onto map(Amazing!)

Suppose $V$ is finite-dimensional and $T\in\mathcal{L}(V,W).$ Then $T|_{(\text{null}T)^\perp}$ is an injective map of (null $T)^\perp$ onto range $T.$



Now we can define the **pseudoinverse** $T^{\dagger}$ (T dagger) of a linear map $T$



#### pseudoinverse

Suppose that $V$ is fnite-dimensional and $T\in\mathcal{L}(V,W).$ The pseudoinverse$T^\dagger\in\mathcal{L}(W,V)$ of $T$ is the linear map from $W$ to $V$ defıned by
$$
T^\dagger w=(T|_{(\text{null T})^\perp})^{-1}P_{\text{range T}}w
$$
for each $w\in W.$



$T|_{U}$ means the domain of $T$ is $U$ but the map rule keeps the same $T|_{U}(u) = Tu$.

**Psudoinverse maps 0 to 0, and $w \ne 0$ to a unique point(It is a bijective) in $(null \ T)^{\perp}$** 



#### algebraic properties of the pseudoinverse

Suppose $V$ is fınite-dimensional and $T\in\mathcal{L}(V,W).$

(a) If $T$ is invertible, then $T^\dagger=T^{-1}.$

(b) $TT^\dagger=P_{\text{range}T}=$the orthogonal projection of $W$ onto range $T.$ 

(c) $T^\dagger T=P_{(\text{null }T)^\perp}=$the orthogonal projection of $V$ onto (null $T)^\perp.$



#### pseudoinverse provides best approximate solution or best solution

Suppose$V$ is finite-dimensional, $T\in\mathcal{L}(V,W)$, and $w\in W.$

(a) If $v\in V$,then
$$
\|T(T^\dagger w)-w\|\leq\|Tv-w\|,
$$
with equality if and only if $v\in T^\dagger w+$ null $T.$

(b) If $v\in T^\dagger w+$null $T$,then
$$
\|T^\dagger w\|\leq\|v\|,
$$
with equality if and only if $v=T^\dagger w.$



(a) means $v = T^\dagger w$ makes $Tv$ is the closest to $w$ of all $v \in V$

(b) means if there are many points that are closest to $w$ ($T^\dagger w + null \ T$), then $T^\dagger w$ has the smallest norm.



## Chapter 7 Operators on Inner Product Spaces

### 7A Self-Adjoint and Normal Operators

#### adjoint

Suppose $T\in\mathcal{L}(V,W).$ The **adjoint** of $T$ is the function $T^*:W\to V$ such that
$$
\langle Tv,w\rangle=\langle v,T^*w\rangle 
$$
for every $v\in V$ and every $w\in W.$



#### adjoint of a linear map is a linear map



#### properties of the adjoint

Suppose $T\in\mathcal{L}(V,W).$ Then

(a) $(S+T)^*=S^*+T^*$ for all $S\in\mathcal{L}(V,W);$

(b) $(\lambda T)^*=\overline{\lambda}T^*$ for all $\lambda\in\mathbf{F};$

(c) $( T^* ) ^* = T;$

(d)  $( ST) ^* = T^* S^*$ for all $S\in\mathcal{L}(W,U)$ (here $U$ is a finite-dimensional innerproduct space over $F$);

(e) $I^*=I$, where $I$ is the identity operator on $V;$

( f)  if $T$ is invertible, then $T^*$ is invertible and $(T^*)^{-1}=(T^{-1})^*.$



####  null space and range of $T^*$

Suppose $T\in\mathcal{L}(V,W)$. Then

(a) null $T^*=($range $T)^\perp;$

(b) range $T^*=$ (null $T)^\perp;$

(c) null $T=($range $T^*)^\perp;$

(d) range $T=($null $T^*)^\perp.$



#### conjugate transpose

The conjugate transpose of an m-by-n matrix $A$ is the n-by-m matrix $A^*$ obtained by interchanging the rows and columns and then taking the complex conjugate of each entry. In other words, if $j\in\{1,...,n\}$ and $k\in\{1,...,m\}$, then
$$
(A^*)_{j,k}=\overline{A_{k,j}}.
$$


matrix of $𝑇^∗$ equals conjugate transpose of matrix of $T$

Let $T\in\mathcal{L}(V,W).$ Suppose $e_1,...,e_n$ is an orthonormal basis of $V$ and $f_1,...,f_m$ is an orthonormal basis of $W.$ Then $\mathcal{M}(T^*,(f_1,...,f_m),(e_1,...,e_n))$ is the conjugate transpose of $\mathcal{M}(T,(e_1,...,e_n),(f_1,...,f_m)).$ In other words,
$$
\mathcal{M}(T^*)=\left(\mathcal{M}(T)\right)^*.
$$

#### self-adjoint

An operator $T\in\mathcal{L}(V)$ is called **self-adjoint** if $T = T^*$



#### eigenvalues of self-adjoint operators

Every eigenvalue of a self-adjoint operator is real.



#### normal

An operator on an inner product space is called **normal** if it commutes with its adjoint.

In other words, $T\in\mathcal{L}(V)$ is normal if $TT^* =T^*T$



Suppose $T\in\mathcal{L}(V).$ Then

$T$ is normal $\Longleftrightarrow\|Tv\|=\|T^*v\|$ for every $v\in V.$



#### orthogonal eigenvectors for normal operators

Suppose $T$ is normal. Then eigenvectors of $T$ corresponding to distinct eigenvalues are orthogonal.



### 7B Spectral Theorem

#### Real Spectral Theorem

Suppose $T\in\mathcal{L}(V)$ is self-adjoint and $b,c\in\mathbf{R}$ are such that $b^2<4c$. Then
$$
T^2+bT+cI
$$
is an invertible operator.





### 7C Positive Operators

An operator $T\in\mathcal{L}(V)$ is called positive if T is self-adjoint and
$$
\langle Tv,v\rangle\geq0
$$
for all $v\in V.$



#### square root

An operator $R$ is called a square root of an operator $T$ if $R^2=T$.



### 7E Singular Value Decomposition

#### properites of $T^*T$

Suppose $T \in \mathcal{L}(V,W)$. Then

(a) $T^*T$ is a positive operator on $V$;

(b) $null \ T^*T=null \ T$

(c) $range \ T*T=range \ T^*$

(d) $\dim range\ T = \dim range\ T^*=\dim range \ T^*T$ 



#### singular values

Suppose $T\in\mathcal{L}(V,W).$ The singular values of $T$ are the nonnegative square roots of the eigehvalues of $T^*T$, listed in decreasing order, each included as many times as the dimension of the corresponding eigenspace of $T^*T.$



#### singular value decomposition

Suppose $T\in\mathcal{L}(V,W)$ and the positive singular values of $T$ are $s_1,...,s_m$ Then there exist orthonormal lists $e_1,...,e_m$ in $V$ and $f_1,...,f_m$ in $W$ such that
$$
Tv=s_1\langle v,e_1\rangle f_1+\cdots+s_m\langle v,e_{m}\rangle f_m
$$
for every $v\in V.$


$$
T*Te_i = s^2e_i, \ \ i=1,...,m \  \\ f_i = \frac{Te_i}{s_i}
$$

**(a) $e_i$ is an orthonormal basis of $(null \ T)^{\perp}$, and they are orthonormal eigenvecotors of $T*T$.**

**(b) $f_i$ is an orthonormal basis of $range \ T$, and $f_i = \frac{Te_i}{s_i}$**




#### singular value decomposition of adjoint and pseudoinverse

Suppose $T\in\mathcal{L}(V,W)$ and the positive singular values of $T$ are $s_1,...,s_m.$ Suppose $e_1,...,e_m$ and $f_1,...,f_m$ are orthonormal lists in $V$ and $W$ such that
$$
Tv=s_1\langle v,e_1\rangle f_1+\cdots+s_m\langle v,e_m\rangle f_m
$$
for every $v\in V.$ Then
$$
T^*w=s_1\langle w,f_1\rangle e_1+\cdots+s_m\langle w,f_m\rangle e_m
$$
and
$$
T^\dagger w=\frac{\langle w,f_1\rangle}{s_1}e_1+\cdots+\frac{\langle w,f_m\rangle}{s_m}e_m
$$
for every $w\in W.$

 

#### matrix version of SVD

Supposle $A$ is a $p$-by-$n$ matrix of rank $m\geq1.$ Then there exist a $p$-by-$m$ matrix $B$ with orthonormal columns, an $m$-by-$m$ diagonal matrix $D$ with positive numbers on the diagonal, and an $n$-by-$m$ matrix $C$ with orthonormal columns such that
$$
A=BDC^*.
$$

$B$ is a matrix whose colums are $f_1, ...,f_m$
$D$ is a matrix whose diagonal entries are $s_1,...,s_m$
$C$ is a matrix whose colums are $e_1,...,e_m$

equvialently,
$$
A = \sum_{i= 1}^ms_if_ie_i^T
$$

## Chapter 8 Operators on Complex Vector Spaces
### 8A Generalized Eigenvectors and Nilpotent Operators

### sequence of increasing null spaces

Suppose $T\in \mathcal L(V)$. Then
$$
\{0\}=\mathrm{null~}T^0\subseteq\mathrm{null~}T^1\subseteq\cdots\subseteq\mathrm{null~}T^k\subseteq\mathrm{null~}T^{k+1}\subseteq\cdots
$$


#### equality in the sequence of null spaces

Suppose $T\in \mathcal L(V)$ and =$m$ is a nonnegative integer such that
$$
\text{null T}^{m}=\text{null T}^{m+1}
$$
Then
$$
\text{null T}^{m}=\text{null T}^{m+1}=\text{null T}^{m+2}=\text{null T}^{m+3}=\cdots
$$

#### null spaces stop growing

Suppose $T\in \mathcal L(V)$. Then
$$
\text{null T}^{\dim V}=\text{null T}^{\dim V+1}=\text{null T}^{\dim V+2}=\cdots
$$

#### 8.4
Suppose $T\in \mathcal L(V)$. Then
$$
V=\text{null}\ T^{\dim V}\oplus\text{range} \ T^{\dim V}.
$$

#### generalized eigenvector

Suppose $T\in\mathcal{L}(V)$ and $\lambda$ is an eigenvalue of $T.$ A vector $v\in V$ is called a generalized eigenvector of $T$ corresponding to $\lambda$ if $v\neq0$ and
$$(T-\lambda I)^kv=0$$

for some positive integer $k$.