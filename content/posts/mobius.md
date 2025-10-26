+++
date = '2025-10-26T20:19:32+01:00'
draft = true
title = 'Mobius Transformations in HM'
+++




# Mobiustransforms in Hamiltonian Mechanics


Suddenly at a lecture where we were mapping a periodic system in phase space to something easier with HJ, I wondered if we equivalently could do it with a tool from complex analysis. 

Phase space is equipped with a symplectic 2-form $\omega = dq \wedge dp$ which has to be preserved if we want a valid canonical transformation. So the question naturally arises, under what conditions do Mobius transforms preserve this symplectic structure if at all? 

Typically we know that MT preserves angles, not area. If we let $z = q + ip$, then $\omega = idz \wedge d \overline{z}$, where $f^{*} \omega = \omega$. 

### Why MT inversion fails in flat symplectic geometry. 

Take the simplest example, a dimensionless harmonic oscillator $H(q,p) = q^2 + p^2$, and let $z=q+ip$. Attempt the transform of $w = \frac{1}{z} \implies H = \frac{1}{\mid w \mid ^"}$. Now, circular orbits $\mid z \mid$ are mapped to circles/lines on the $w$-plane. 

What happens to the $2$-form? $dw = -\frac{1}{z^2} dz$ and $d \overline{w} = - \frac{1}{\overline{z}^2} d\overline{z}$. 


$$
i dw \wedge d \overline{w} ? \frac{1}{\mid z \mid^4}i dz \wedge d \overline{z}
$$
We have rescaled this by a factor of $\frac{1}{\mid z \mid^4}$ so the Jacobi determinant is not 1 hence not canonical. 

Result: MT are not canonical in "flat" phase space, but if we give it a hyperbolic symplectic structure of the Poincare disk the SU(1,1) MT is canonical. 

