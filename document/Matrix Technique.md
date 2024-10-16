# Matrix Technique

### 1 The column vector of two matrix multiplication

$$
A = (a_1, ...,a_n), a_i \in R^m,A \in R^{m\times n}\\
B= (b_1, ...,b_s), b_i \in R^n,B \in R^{n\times s}
$$

$(AB)_{,i}$ represent the $i$ column of $AB$, and $(AB)_{i,}$ represent the $i$ row of $AB$
$$
AB =A(b_1, ...,b_s) = (Ab_1, Ab_2,...,Ab_s) 
$$
So, we have
$$
(AB)_{,i} = Ab_i
$$


### 2 Quadric form related

$$
H = (h_1, ...,h_n), h_i \in R^m,H \in R^{m\times n}\\
L  \in R^{m \times m} 
$$

By 1, we have
$$
h_i^TLh_i =H^T_{i,}LH_{,i}= H^T_{i,}(LH)_{,i}\\
$$
And RHS represent the $i$ row of $H^T$ times the $i$ column of $LH$ which is $(H^TLH)_{ii}$, so
$$
h_i^TLh_i = (H^TLH)_{ii}
$$
Finally we can see that
$$
\sum_{i=1}^nh_i^TLh_i=tr(H^TLH)
$$


Futhermore, 
$$
H^TLH = 
\begin{pmatrix}
h_1^TLh_1&h_1^TLh_2&...&h_1^TLh_n \\
h_2^TLh_1&h_2^TLh_2&...&h_2^TLh_n\\
&...&...\\
h_n^TLh_1&h_n^TLh_2&...&h_n^TLh_n
\end{pmatrix}
$$
