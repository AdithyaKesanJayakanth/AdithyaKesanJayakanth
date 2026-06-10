## Adithya Kesan Jayakanth

I build simulations of physical systems, and then try to find out where they are wrong.

Grade 12 in Chennai. Most of what I work on sits at the point where aerospace physics
stops being analytical and has to be computed — trajectory, heat transfer, fluid flow —
plus the optimisation and tooling that makes computing it bearable.

---

**[PLE-SBS](https://github.com/AdithyaKesanJayakanth/PLE-SBS)** · *one wire, a switch yard and a bay for every pod*

In the hours before a crewed launch, the crew and close-out technicians work 40–115 m above
a fully fuelled rocket. NASA's way down is the slidewire: baskets riding steel ropes under
gravity to a landing area hundreds of metres away. Every existing system gives each basket
its own wire and brakes it at the end of that wire, and each was engineered for one pad.

PLE-SBS is a method for sizing a slidewire at any launch pad. Its model reproduces the
Shuttle baskets' top speed without tuning (24.0 m/s predicted, about 24.6 m/s reported) and
shows that passive magnetic braking only works when the span is about 100 m + 4 × the crew
access height.

**My special add-on to the existing egress system: one wire, a switch yard and a bay for
every pod.** The braking moves off the wire. At the bottom, self-indexing points send each
pod into its own braked bay beside the bunker, so every pod shares one wire and leaves about
8 s after the one ahead. One wire clears 24 people almost as fast as six separate wires in a
design headwind, a pod whose brake has failed still stops at 1.4 g, and nothing needs power.

The repository has the paper, the simulator, and the CAD parts and test protocol for a
tabletop scale model. Try the simulator or read the paper at
[adithyakesan.com/ple_sbs](https://adithyakesan.com/ple_sbs/).

*Mentor and guide: Mrs. Abitha Peter, my Class 12 physics teacher.*

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

*Mentor and guide: Mrs. Abitha Peter, my Class 12 physics teacher.*

---

**[SIMC 2026](https://github.com/AdithyaKesanJayakanth/SIMC2026)** · *how many drinks are in the table?*

The Endeavour challenge at the Singapore International Mathematics Challenge: a 1,000 × 3,401
table of infrared spectra from an unknown number of fermented drinks, with errors planted in
it. Clean it, then work out how many distinct samples were actually measured.

PCA showed the data is strongly low-dimensional — an eight-dimensional signal inside
3,401 dimensions (λ₁/λ₂ ≈ 3.5). Clustering the vials two mathematically equivalent ways,
through the covariance matrix and through the Gram matrix, gave identical answers: 25
groups. The last one was hiding in what we had removed — 36 vials we first discarded as
anomalous turned out to be a real, concentrated drink. Putting them back gives 26 unique
samples, about 37 repeat measurements each; keeping the cleaning step reversible is the
only reason the count came out right.

A team of three, with K. Vishnu Kumar and Adithya Anand. The repository has the full
working across the four days of the event — the notebook, the Markov-chain and
power-method/SVD proofs, the report, and the defense deck.

**[SIMC Foundations](https://github.com/AdithyaKesanJayakanth/SIMC-Foundations)** · the linear
algebra from zero, in five days, that got me to the point of being able to attempt it.

---

Also, mostly unpublished: a real-time dashboard daemon I actually use every day, an
implementation of the Stanford generative-agents architecture, a chord-transcription
tool, and rather too many small daemons.

Previously Design Lead on a STEM Racing team — OpenFOAM, FEA, and a Python race
simulator that predicted our run time to within a few milliseconds.

[adithyakesan.com](https://adithyakesan.com)
