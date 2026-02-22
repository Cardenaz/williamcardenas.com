+++
date = '2026-02-22T13:57:14+01:00'
draft = false
title = 'Visualizing PES and nano sandwiches'
+++


### PES


PES is one of few times we read off SP directly. 


A metal substrate, often Au, with chiral molecules adsorbed i.e. attached to the surface.

Light (UV/X photons) hits the sample and frees electrons like: 

![Landua page](/images/test.png)

the runaway electrons enter some analyzer then gets accelerated and scattered off a gold-foil to a Mott-detector with a left/right counter giving us a readout of SP. [Attach drawing soon]

### 2-Terminal transport
Now let's simplify the two terminal transport experiment. 

Metal -> Molecule -> Metal. 

Connect a voltage source and an ammeter. Set +V to the left side and let electrons flow. Suppose you measure the current $I(M)$ where M is the magnetization current. 
See sketch: 

![Landua page](/images/twoterminal.png)

Then flip M, and measure I(-M). If you observe $I(M) \neq I(-M)$ then the device is magnetization dependent, which is an important signal. 

Can you visualize how the current flows? The L-electrode has let's say a higher chemical potential, which means we have more filled electronic states than on the right. So they TUNNEL through the molecule and enter parking spots on the right. 

In the R-electrode (ferromagnet) there are more spin-up states than down (at the Fermi-level). 

How to flip the magnetization experimentally? Apply external B-field. Assuming it is strong enough to overcome the internal magnetization of the material. If the molecule favors spin-up such that electrons exiting it has a preference, and the FM also has M-up, then transmission is higher and current larger. If we flip M then fewer parking slots are available hence lower transmission and smaller current. At least experiments report this. But it violates symmetry expectation someone yells! Welp, maybe the molecule isn't reading the same textbook as you. And it would help a lot if molecules wrote books on molecules in the same way birds write books on  ornithology. 

But of course, just because something depends on magnetization it does not mean that the transmitted current is SP. Altough I am wondering if we could probe the current with a quantum dot spin and get a read out.