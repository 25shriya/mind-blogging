## An Introduction to Classical Groups

#### Shriya Meenakshisundaram



This article introduces some classical matrix groups and proves Suslin's normality theorem, which relates a normal subgroup of the Elementary Linear Group to the familiar General Linear Group, both defined over an arbitrary commutative ring $R$.

We recall definitions of the following groups.

$ \textit{General Linear Group}$ over a commutative ring $R$, $GL_{n}(R)$, is the group (under matrix multiplication) of all invertible $n \times n$ matrices that have entries from a commutative ring $R$. Note that $\forall \, A \, \in \, GL_{n}(R), \, \text{det}(A) \, \in \, R^*$. (all non zero elements of $R$)

$\textit{Elementary Linear Group}$ over a commutative ring $R$, $E_{n}(R)$, is the group (under matrix multiplication) of all $n \times n$ matrices generated by $E_{ij}(a) \, = \, I_n \, + \, e_{ij}(a)$ , where $a \, \in \, R$  and $1 \, \leq \, i, \, j \, \leq \, n$.

Note that every element of $E_{n}(R)$ can be written as $E_{ij}(r)$ for some $r \, \in \, R$ and $1 \, \leq \, i, j \, \leq \, n$. Each of these matrices are invertible as they can be obtained by performing elementary row operations on $I_{n}$. It follows that $E_{n}(R)$ is a subgroup of $GL_{n}(R)$.

We define the $\textit{matrix commutator}$ of matrices $A, \, B \, \in \, GL_{n}(R)$ as follows: $[A,B] \, = \, ABA^{-1}B^{-1}$.

Some interesting properties of elements of $E_{n}(R)$ under the matrix commutator are:

1. $[E_{ij}(a), E_{jk}(b)] \, = \, E_{ik}(ab)$.
2. $[E_{ij}(a), E_{kl}(b)] \, = \, I_{n}$.

The above two properties can be checked by simple matrix manipulation.

We now define an important normal subgroup of the Elementary Linear Group.

Consider an ideal $J$ of a commutative ring $R$. The group $E_{n}(R, J)$, generated by elements of the form $E_{ij}(x)$ for all $x \, \in \, J$, is a normal subgroup of $E_{n}(R)$. A quick proof would be to show that every element $A E_{ij}(x) A^{-1}$ lies in $E_{n}(R,J)$, for all $x \, \in \, J$ and $A \, \in \, E_{n}(R)$.  

Suslin's normality theorem proves that for any ideal $J$ of $R$, $E_{n}(R,J)$ is a normal subgroup of $GL_{n}(R)$. In particular, $E_{n}(R)$ is a normal subgroup of $GL_{n}(R)$.

Here's a sequence of lemmas (accompanied by a summary of the proof) that lead to Suslin's normality theorem. In all statements below, $R$ can be taken as any commutative ring and $J$ its ideal.

1. Here's a theorem that takes two arbitrary matrices $\alpha \, \in \, M_{n \times m}(J)$ and $\beta \, \in \, M_{m \times n}(R)$. We claim that $I_{n} \, + \, \alpha\beta$ is invertible $\iff$ $I_{m} \, + \, \beta\alpha$ is invertible. To prove forward implication, we assume $I_n \, + \, \alpha\beta$ is invertible with inverse matrix $\gamma$. A bit of algebra shows that $I_{m} \, - \, \beta\gamma\alpha$ is the inverse of $I_m \, + \, \beta\alpha$, thus concluding the proof. The backward implication follows from a similar argument on $I_m \, + \, \beta\alpha$.

2. Taking this forward, assuming $I_{m} \, + \, \beta\alpha \, \in \, GL_{m}(R)$, we have  $I_n \, + \, \alpha\beta \, \in GL_n(R)$. Subsequently, we obtain the matrix $\begin{bmatrix}   I_n + \alpha\beta  & 0 \\   0 & (I_m + \beta\alpha)^{-1} \end{bmatrix}$ as a product of conjugates of elements of $E_{n}(R,J)$, implying that the above matrix lies in $E_{n+m}(R,J)$ as the latter is a normal subgroup of $E_{n}(R)$.

3. Now, we narrow down the argument to the case when $m = 1$ and when $\beta\alpha = 0$. In such a case we can prove that $I_n + \alpha\beta \, \in \, E_{n+1}(R,J)$ (under suspension[^1]), as an extension of the argument from the above theorem by plugging in the value of $m$ and $\beta\alpha$. In a special case of this theorem, when $\alpha$ has at least one zero coordinate, we prove that $I_{n} + \alpha\beta \, \in \, E_{n+1}(R,J)$, by taking $\alpha = \begin{bmatrix} \alpha' \\ 0 \end{bmatrix}$,  $\beta = \begin{bmatrix} \beta' && b \end{bmatrix}$ for some vectors $\alpha', \beta'$ with entries in $J$ and $R$ respectively and an arbitrary element $b \in R$. We substitute these values in $I_{n} + \alpha\beta$ to obtain $I_{n} + \alpha\beta \, \in \, E_{n}(R,J)$.

4. To conclude, we now prove the statement of Suslin's normality theorem. Since $E_{n}(R,J)$ is a normal subgroup of $E_n(R)$, the former is generated by elements of the form $A (I_n + e_{ij}(a)) A^{-1}$, for $a \in J, \, i \neq j$ and $A \in E_n(R)$. We now have to prove that all conjugates of the form $B (I_n + e_{ij}(a)) B^{-1}$, for $a \in J, \, i \neq j$ and $B \in GL_n(R)$ lie in $E_n(R,J)$ to prove normality. 

   For this proof, we fix such a matrix $B$. Let $\alpha$ be the $i^{th}$ column of $B$ and $\beta$ be the $j^{th}$ row of $B^{-1}$.  Since $i \neq j$, $\beta\alpha = 0$ and hence, $\beta(a\alpha) = 0$. We apply part 3 to prove that $I_{n} + (a\alpha)\beta \, \in \, E_{n}(R,J)$. Now, note that, $I_{n} + (a\alpha)\beta \, = \, I_{n} + a(Be_{ij}(1_{R})B^{-1}) \, = \, I_{n} + Be_{ij}(a)B^{-1} \, \in \, E_n(R,J)$.

This normality theorem proof can be [extended](https://arxiv.org/abs/2211.01416) to $\textit{Elementary Symplectic Group }(ESp_{2n}(R))$ and $\textit{Elementary Orthogonal Group }(EO_{n}(R))$ as well.



This work has been taken from a part of my study of classical groups under [Dr Pratyusha Chattopadhyay](https://www.bits-pilani.ac.in/hyderabad/pratyusha-chattopadhyay/) as a part of my undergraduate coursework.







[^1]: What is [under suspension?](https://en.wikipedia.org/wiki/Suspension_(topology))






