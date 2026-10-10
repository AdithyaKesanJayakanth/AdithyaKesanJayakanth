## Adithya Kesan Jayakanth

I build simulations of physical systems, and then try to find out where they are wrong.

Grade 12 in Chennai. Most of what I work on sits at the point where aerospace physics
stops being analytical and has to be computed — trajectory, heat transfer, fluid flow —
plus the optimisation and tooling that makes computing it bearable.

---

**[AETHER](https://github.com/AdithyaKesanJayakanth/aether)** · *when cooler is not safer*

A re-entry vehicle is normally designed against peak heat flux, the worst instant of
heating on its outer surface. But heat shields do not fail at the surface — they fail at
the bondline, where the shield meets the structure, and the bondline responds to the
integral rather than the peak.

Those two quantities are not optimised by the same trajectory. AETHER measures the gap:
a verified atmosphere / 3-DOF trajectory / stagnation-heating / transient-conduction
chain in Python, with the conduction solver checked against an analytical solution to
0.002% before it was used for anything.

Over the domain tested so far, the two metrics are perfectly anti-ordered — a 38%
reduction in peak heat flux produced a 114 K *hotter* bondline. OpenFOAM CFD is next.

The repository keeps its negative results, including two of my own bugs and the
boundary condition that diverged on the first run.

---

**[SIMC Foundations](https://github.com/AdithyaKesanJayakanth/SIMC-Foundations)** · linear algebra
from zero, in five days, for the Singapore International Mathematics Challenge. The
competition task was PCA and clustering on 1,000 infrared spectra; this is the working
that got me to the point of being able to attempt it.

---

Also, mostly unpublished: a real-time dashboard daemon I actually use every day, an
implementation of the Stanford generative-agents architecture, a chord-transcription
tool, and rather too many small daemons.

Previously Design Lead on a STEM Racing team — OpenFOAM, FEA, and a Python race
simulator that predicted our run time to within a few milliseconds.

[adithyakesan.com](https://adithyakesan.com)
