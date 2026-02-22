+++
date = '2026-02-21T15:19:01+01:00'
draft = false
title = 'Amar Bose on problem solving'
+++


Last few days I have been listening to the late great Amar Bose on general problem solving. In one video he recounts Professor Chu's working relationship with General Dynamics. Chu would have engineers lined up outside his room for months in advance. They would only get 10 minutes with him but always came out of the room relieved. Clearly Amar wanted to figure out what went on in that room so he asked Chu. 

From the transcript: 

>  I decided I was going to make electromagnetics my field. He had come over, I guess, from Taiwan and was a student. And he made that decision, and he said after I made the decision, every problem that came to me in electromagnetics, either was assigned to me or was something that I looked at, I followed a strict discipline. I looked at the problem. I then divided the problem into the smaller problem. Looked at that problem and divided it into a smaller one yet, until I got to the smallest problem, the most elementary problem that I could make out of this seemingly complex problem. And then I decided I would understand that thoroughly, and that involved usually simple mathematics.


> And when I understood that simplest problem I could make very thoroughly, I went to the next level back. Went to the next level, to the next level, and finally to the original problem. And he said I did that with iron discipline. 

(Source: https://infinite.mit.edu/video/amar-g--bose--6-312-lecture-01/) 


Let's try to use this method, on some random problem. 


![Landua page](/images/angular-problem.png)

How can we make this simpler? Maybe the angular part of an atom ... how to make that simpler? What about the angular part of a single particle ... simpler? Ask yourself how to find the angular part of a free particle. 

Below is an *outline*, not a description of all details.

#### bottom layer (the socially isolated particle)
So you set up the Hamiltonian, $H = -\frac{\hbar}{2m} \nabla^2$, where 

$$
\nabla^2 =\frac{1}{r^2}\frac{\partial}{\partial r}(r^2 \frac{\partial}{\partial r})-\frac{\hat L^2}{\hbar^2 r^2}
$$

since $L^2 Y = \hbar^2 l(l+1)Y$ the angular part is the set of eigenfunctions of $L^2$ (spherical harmonics). 

#### next layer (particle with life circumstances)
What if we add a potential to the free particle problem? Well assuming the potential ony contains the radius vector to the particle, this won't affect the solutions to the angular part at all because the same symmetry persists. 

#### next layer (the last time Schrödinger slept well)
What if we now consider the simplest atom. Two body problem, let reduced mass be $\mu$. Hamiltonian becomes

$$
H = -\frac{\hbar}{2\mu} \nabla^2 - \frac{e^2}{4 \pi \epsilon_0} \frac{1}{|r_1-r_2|}
$$

And again same solution set as above, same symmetry.

#### next layer (the birth of approximation)
The next step ought to be some multielectron atom, simplest case is Helium. Which we can treat as two hydrogenic Hamiltonians but with some extra term accounting for the electron-electron interaction. 


$$
H = [-\frac{\hbar}{2m} \nabla^2 - \frac{2e^2}{4 \pi \epsilon_0} \frac{1}{r_1}] + [-\frac{\hbar}{2m} \nabla^2 - \frac{2e^2}{4 \pi \epsilon_0} \frac{1}{r_2}] + extra term
$$

The interaction is Coulomb so let $extraterm = \frac{1}{4 \pi \epsilon_0} \frac{e^2}{|\vec{r}_1-\vec{r}_2|}$. 

Supposing you ignore the extra term, and factorize total wave function $\psi_{tot} = \psi_{nlm} \psi_{n'l'm'}$, well then the angular part is clearly $Y_{l}^{m} Y_{l'}^{m'}$. If you then compute the energies for the ground state you will see that it will be off 30 eVs (ish) from the actual experimental one. This gives you now indication to why we need that extra term. 

The difference for the He compared to H is that the AM-operator $\hat{L} = \vec{r}_1 \times \vec{p}_1 + \vec{r}_2 \times \vec{p}_2$ where $[H, L^2] = 0$, and you are still looking at S.H.

#### next layer (the first time space matters)
Based on the earlier layers we realised that the solution set is eigenfunctions of $L^2$ and $L_z$, particulary SH, but this was only true due to spherical symmetry. With a diatomic molecule we don't have this.

Well what stays the same if we rotate this thing in space? Hmm it seems that the relative distance between atom 1 and 2 are the same. And likely the relative distance between each electron and the center of mass frame of the molecule is the same. Constructing an operator $\hat{K}$, then, should depend on both of these things s.t. $[H, \hat{K}] = 0$

$$
\hat{K} = \vec{r} \times \hat{p} + \sum_i (\vec{r}_i \times \hat{p}_i) 
$$

where we want to find functions f that satisfy $\hat{K^2} f = \lambda f$ and $\hat{K_z} f = \lambda f$. 

But, the only way to untangle it from here is to really really understand what happens in the previous case with the operators. 

The process is tedious but necessary. By going through each layer thoroughly, you literally will see the problem fall apart in your hands, just like Professor Chu.  