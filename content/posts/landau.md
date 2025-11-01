+++
date = '2025-10-26T21:00:43+01:00'
draft = false
title = "Landau and the dictatorship of the representation invariants"
+++

*Strip away degrees of freedom, align with symmetry and achieve the dictatorship of the representation invariants.*

I was attempting to recreate this paper by hand ... 

![Landua page](/images/first-page.png)
(courtesy: Collected Papers of Landau)

... and I remembered a recent article https://arxiv.org/pdf/2503.04778 on the specific method of Landau, and just was curious to test their hypothesis. 

**The paper "ON THE THEORY OF THE SPECTRA OF DIATOMIC MOLECULES" was written right after matrix mechanics. Spectroscopy of diatomic molecules had a well developed empirical band theory but needed a proper foundation in QM.**

Now, is this paper the first sign of his geometric reductionism? 


#### Step 1 - Transforming the H in order to reduce the problem to 1D


Letting capital letters denote the nuclei and small letters the electrons, we are given: 

$$
\vec{r} = r - \frac{M_1R_1 + M_2 R_2}{M_1+M_2} \tag{1}
$$
$$
R = R_2 - R_1 \tag{2}
$$
$$
C =  \frac{m \sum r + M_1R_1 + M_2 R_2}{ \sum m +M_1+M_2} \tag{3}
$$

And instead of having $\frac{M_1R_1 + M_2 R_2}{M_1+M_2}$, let's introduce 
$$
R_N = \frac{M_1R_1 + M_2 R_2}{M_1+M_2} \tag{4}
$$ 
which is the center of mass frame of the nuclei. The expression $\vec{r} = r - R_N$ is then the electron position measured from the nuclear COM. I would prefer if he denoted it with $\vec{r}_i$ and $r_i$, indicating that we take the position of each electron and subtract the distance from the nucleus. And especially strange since we have the summation sign for the mass but not for the radius vectors. 

To grasp equation (1) further, imagine a diatomic molecule consisisting of flourine. Each flourine atom has 9 electrons which means that $F_2$ has 18 total electrons to think about. Then the transformation $\vec{r}_i = r_i - R_N$ has to be done for every electron, i.e., we get 18 relative coordinates. What this does is to change the reference frame from the lab frame to the nuclei's center of mass frame for every electron.


Once we get the transformed variables we want to transform the Hamiltonian. What should be our first step? Well I like to start with the momenta. Generally $\hat{p} = -i \hbar \nabla$ where $\nabla = (\frac{\partial}{\partial x}, \frac{\partial}{\partial y},\frac{\partial}{\partial z})$. So we need to express $\nabla_{R_1}$, $\nabla_{R_2}$ and $\nabla_{r}$ in $C, R$ and $\vec{r_i}$. 


We start by rewriting $R_1$ and $R_2$ in terms of the new variables. For $R_1$ we plug $R_2 = R+R_1$ into eq. 4: 

$$
R_N =  \frac{ M_1R_1 + M_2(R+R_1)}{+M_1+M_2} =  \frac{R_1(M_1+M_2)+M_2R}{M_1+M_2} 
$$

$$
= R_1 + \frac{M_2}{M_1+M_2}R \leftrightarrow R_1 = R_N - \frac{M_2}{M_1+M_2}R
$$


Similarly for $R_2$ we do the same procedure but with $R_1 = R_2-R$ into eq. 4
$$
R_N =  \frac{ M_1(R_2-R) + M_2 R_2}{+M_1+M_2} =  \frac{R_2(M_1+M_2)-M_1R}{M_1+M_2} 
$$

$$
= R_2 - \frac{M_1}{M_1+M_2}R \leftrightarrow R_2 = R_N + \frac{M_1}{M_1+M_2}R
$$


And for the electron lab frame vector we have $r = \vec{r} + R_N$ from eq. (1).

The multivariable chain rule for a fucntion $f(x(q))$: $\frac{\partial f}{\partial q_i} = \sum_j \frac{\partial x_j}{\partial q_i} \frac{\partial f}{\partial x_j} $

Let's compute $\nabla_{R_1}$: 
$$
\nabla_{R_1} = \frac{\partial R_N}{\partial R_1} \cdot \nabla_{R_N} + \frac{\partial R}{\partial R_1} \cdot \nabla_R
$$
$$
= \frac{M_1}{M_1+M_2} \nabla_{R_N} - \nabla_R
$$


and $\nabla_{R_2}$: 
$$
\nabla_{R_2} = \frac{\partial R_N}{\partial R_2} \cdot \nabla_{R_N} + \frac{\partial R}{\partial R_2} \cdot \nabla_R
$$
$$
= \frac{M_2}{M_1+M_2} \cdot \nabla_{R_N} + \nabla_{R}
$$

and for $\nabla_{r} = \nabla_{\vec{r}_i}$.


Now let us finish the job by replacing $R_N$ with $C$ and $\vec{r}$

From eq. (3) 
$$
C = \frac{m \sum (\vec{r}+R_N) + (M_1+M_2)R_N}{\sum m + M_1+M_2} 
$$
$$
 = \frac{m \sum \vec{r} + (M_1+M_2+nm)R_N}{\sum m + M_1+M_2} \leftrightarrow R_N = \frac{C(\sum m + M_1+M_2) - m \sum \vec{r}}{M_1+M_2+nm}
$$
$$
\leftrightarrow R_N = C - \frac{m}{M_1+M_2+nm} \sum \vec{r}
$$

$\nabla_{R_N} = \frac{\partial C}{\partial R_n} \cdot \nabla_C + \frac{\partial \vec{r}}{\partial R_n} \cdot \nabla_{\vec{r}_i}$

$$
= \nabla_C - \nabla_{\vec{r}_i}
$$


So 
$$
\frac{M_1}{M_1+M_2}(\nabla_C - \nabla_{\vec{r}_i}) - \nabla_R
$$

$$
\frac{M_2}{M_1+M_2}(\nabla_C - \nabla_{\vec{r}_i}) + \nabla_R
$$

Now watch what happens, we have separated the motion in to COM and rel coordinates, and now Landau just says be gone with it, i.e., throw away the motion of COM. This is a literal reduction of phase space. But it is also standard practice now and reduction of phase space is something that always has been there ever since Jacobi. Hence I don't see anything distinctive about this. 



#### Step 2 - Go to spherical coordinates to use motion in a centrally symmetric field
Landau says "polar" here which is interesting. 

Now, why express the Hamiltonian in $p_R, p_\theta$ and $p_\varphi$? Because in the language of Heisenberg-Born-Jordan, coordinates and momenta are the fundamental objects
with commutators $[q,p] = i \hbar$. Think about it, if he would have kept the Laplacian standard, it would have looked like something Schrodinger-esque, and we are too early in history for that. Once in this lovely p-notation we can derive selection rules from angular momentum algebra. 

#### Step 3 - Going back to Descartes 
![Landua page](/images/transform.png)


This was super confusing first. Why do all of this endless algebra just to transform back to cartesian coordinates? 

*Because spectroscopy does not only care about $M^2$ but for projection on axes like M_z and how they change under Zeeman/Stark effects. Those are usually written in lab frames.*

... 