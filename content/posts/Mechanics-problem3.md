+++
date = '2025-11-17T22:45:47+01:00'
draft = true
title = 'Landau - Mechanics Vol 1 - Problem 3'
+++

Since I got this problem wrong I thought it would be necessary to write about it for my own sake. 

*"A simple pendulum of mass $m$ whose point of support moves uniformly on a vertical circle with constant frequency $\gamma$. Find the Lagrangian for the system when placed in a uniform gravitational field (acceleration g)."*

![Landua](/images/problem.png)


First of all, what is meant by "vertical circle"? A "vertical circle" is a circle that lies in the plane, where the motion is perpendicular to the ground. Contrast this with a horizontal circle, where instead the motion would be parallell to the ground. 

We want to express the co-ordinates of the mass on the spring. 

$$
x = a \cos{(\gamma t)} + l \sin{\phi}
$$
$$
y = -a \sin{(\gamma t)} + l \cos{\phi}
$$

Why is $\gamma*t$ an angle? Because $\gamma$ has units $rad/s$. 

We could move straight in to computing the velocities but let me stop you for a moment. Why is $a \cos{(\gamma t)} -a \sin{(\gamma t)}$ a circle with radius $a$? Since $\mid a \cos{(\gamma t)} -a \sin{(\gamma t)} \mid = \sqrt{a^2 \cos^2{(\gamma t)} +a^2\sin^2{(\gamma t)}} = a$. Ok, we get that this is a circle with radius a centered at the origin in the xy-plane. 


$$
\dot{x} = -a \gamma \sin{(\gamma t)} + l \dot{\phi} \cos{\phi}
$$
$$
\dot{y} = -a \gamma \cos{(\gamma t)} + l \dot{\phi} \sin{\phi}
$$


$$
\implies \dot{x}^2 = a^2 \gamma^2 \sin{\gamma t}^2 -2a \gamma l \dot{\phi} \sin{\gamma t} \cos{\phi} + l^2 \dot{\phi}^2 \cos^2{\phi}
$$
$$
\implies \dot{y}^2 = a^2 \gamma^2 \cos{\gamma t}^2 -2a \gamma l \dot{\phi} \sin{\phi} \cos{\gamma t} + l^2 \dot{\phi}^2 \sin^2{\phi}
$$

$$
\dot{x}^2 + \dot{y}^2 = a^2\gamma^2 -2a\gamma l\dot{\phi}(\sin \gamma t \cos \phi + \sin \phi \cos \gamma t) + l^2 \dot{\phi}^2
$$

The potential can be written as 
$$
U = -(mg a \sin(\gamma t) + mg l \cos \phi)
$$

The Lagrangian becomes: 

$$
L = \frac{1}{2} m(a^2\gamma^2 -2a\gamma l\dot{\phi}(\sin \gamma t \cos \phi + \sin \phi \cos \gamma t) + l^2 \dot{\phi}^2) - (mg a\sin(\gamma t) + mg l \cos \phi)
$$

Getting rid of terms ony depending on time, and using trig identity: 

$$
L = \frac{1}{2} m l^2 \dot{\phi}^2 - 2am\gamma l\dot{\phi}\sin{(\gamma t + \phi)} +  mg l \cos \phi
$$