## Adithya Kesan Jayakanth

I build simulations of physical systems, and then try to find out where they are wrong.

Grade 12 in Chennai. Most of what I work on sits at the point where aerospace physics
stops being analytical and has to be computed — trajectory, heat transfer, fluid flow —
plus the optimisation and tooling that makes computing it bearable.

---

**[PLE-SBS-Capstone](https://github.com/AdithyaKesanJayakanth/PLE-SBS-Capstone)** · *one wire, a switch yard and a bay for every pod*

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

The repository has the paper, the poster, the simulator, and a print-only 1:50 scale model
of the wire and the switch yard: its part files, assembly guide and fit checks. Try the
simulator or read the paper at [adithyakesan.com/ple_sbs](https://adithyakesan.com/ple_sbs/).

*Mentor and guide: Mrs. Abhitha Peter, my Class 12 physics teacher.*

---

**[AETHER-Capstone](https://github.com/AdithyaKesanJayakanth/AETHER-Capstone)** · *which capsule shape slows you down without burning you up?*

A re-entry capsule needs drag to slow down, and the blunt face that makes the drag is where
the gas is hottest. AETHER asks how three shape parameters of an Apollo-like capsule — nose
radius, shoulder radius, cone angle — move its drag coefficient and the peak heat flux on
the heat shield, at one fixed condition: the Apollo wind-tunnel test NASA published in 1966,
so there was real data to be judged against.

Twenty shapes, laminar Navier–Stokes in SU2 on structured meshes drawn from one parameter
table, a three-level mesh study, two NASA benchmarks, and a selection rule written before
any result. Drag follows the nose and shoulder radius; the cone angle does nothing (0.4 %);
the heating peak lives at the shoulder; and a nose radius of one diameter gives 5 % less
peak heating for under 2 % of drag, four times the margin measured by refinement.

The part I did not plan: the solver converged to a wrong answer. A carbuncle — a numerical
shock mode with the stagnation pressure 12 % above the pitot limit — passed every
convergence monitor. The fix was in the mesh, not the settings, and the abandoned mesh
family stays in the repository as a cross-check. Report, poster, a two-minute video, and
every solver case with its logs are in the repository.

---

**[SIMC 2026](https://github.com/AdithyaKesanJayakanth/SIMC2026)** · *how many drinks are in the table?*

The Endeavour Challenge at SIMC 2.0, the Singapore International Mathematical and
Computational Challenge, where our team won **Second Prize (Distinction)**: a 1,000 × 3,401
table of infrared spectra from an unknown number of food samples, with errors planted in it.
Clean it, then work out how many distinct samples were actually measured.

PCA showed the data is strongly low-dimensional — an eight-dimensional signal inside
3,401 dimensions (λ₁/λ₂ ≈ 3.5). Using PCA, we narrowed 1,000 samples with 3,401
dimensions to 25 samples. Clustering the vials two mathematically equivalent ways, through
the covariance matrix and through the Gram matrix, gave identical answers.

I led a team of three, with K. Vishnu Kumar and Adithya Anand. The repository has the full
working from the three-day contest — the notebook, the Markov-chain and
power-method/SVD proofs, the report, and the defense deck.

**[SIMC Foundations](https://github.com/AdithyaKesanJayakanth/SIMC-Foundations)** · the linear
algebra from zero, in five days, that got me to the point of being able to attempt it.

---

Also, mostly unpublished: a real-time dashboard daemon I actually use every day, an
implementation of the Stanford generative-agents architecture, a chord-transcription
tool, and rather too many small daemons.

Previously Engineering and Simulation Lead on a STEM Racing (F1 in Schools) team, which won
the Research & Development Award at the Open National Finals — OpenFOAM, FEA, and a Python
race simulator that predicted a race time of 0.892–0.895 s.

[adithyakesan.com](https://adithyakesan.com)
