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


Typically we have $R = \frac{M_1R_1 + M_2 R_2}{M_1+M_2}$, and let $r = r_2 - r_1$. And we may introduce $M = M_1 + M_2$ for less load on your crow. 



Generally $p = -i\hbar \nabla$, so $$


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