**Week 1-2:**

I wanted to do a comparison of synthetic controls of a large-scale intervention (which I would do) and prior RCTs on the same intervention, to see if they align.

I spent a lot of time searching for good quality public data, but found it tricky. There was a lot of general data available for education, healthcare, climate etc. But the tricky requirement here was that I needed
- An RCT done on the intervention
- A subsequent implementation of the exact policy tested
- Monitoring and evaluation of the specific variables that the RCT studied

Point 3 in particular was difficult, because without this the comparison of Synthetic Controls to the RCT may not be useful.

**Weeks 3-4:**

I spent a ton of time getting data on education in India and malaria initiatives in Sub-Sahara.

The India education stats were in particular super exciting. In Econometrics+Causality there is all this buzz recently about RCT-driven policy interventions. 2019 Nobel Laureates (called the "randomistas") pioneered this movement in development policy and are personal heros.

They established distributing LLIN-bednets for malaria prevention was one of the most cost-effective interventions (in terms of Quality-Adjusted Life Years added per $ spent). They also established an educational intervention called Teaching At the Right Level (TARL).

RCTs in Northern Indian states were very promising and they rolled it out. I unfortunately hit snags with the data:
- Turns out the RCTs used a TARL policy that was materially different from the scaled-up version
- The RCTs measured improvements in specific skills like numeracy and reading through curated tests
- While government data proved excellent (they even had district level tags for female toilet availability!) they don't have subject level performance, just aggregated dropout rates, pass-fail etc.

This would be my back-up if I find no other dataset.

**Weeks 5-7:**

I became very interested in the Nordic Gender Paradox. This is a phenomenon in Nordic countries where, one would imagine that ranking higher on several measures of gender equality, we would see more female CEOs and STEM graduates. However, the gap actually widens compared to other countries. This is a somewhat controversial claim.

I have stored photos of all my notes in the link below.

This is the causal model I drew up for this [this project](https://docs.google.com/document/d/1Udi3FI0cPqxdA-J4_iLGWMnFxIEDUSvThgdx1kZblyo/edit?usp=sharing) on the first page (LionMail access). How much of this disparity is via Intrinsic vs. Extrinsic pathways?

One way I can think of testing this is to run a Synthetic Control study using macroeconomic data from Sweden, Norway and Finland. If a tax break for household services in SWE affects female participation in the workforce (NOR, FIN: donor pool), then we can assume that extrinsic factors indeed affect participation.

I found some datasets that would help, here.

**Week 8:**

Decided to switch to Dynamic Treatment Regimes (DTRs): which are multi-stage interventions where each time-step's optimal intervention depends on all past interventions and covariates. This allows us to model an environment that shifts with each intervention.

DTRs are notoriously hard to optimise. I am currently reading the literature. It appears that if the model is fully known, we have offline planning methods to get optimal treatments.

The problem is learning this on-line.

**Week 9-11:**

Trying to frame this as a Bandit problem seems tricky. I could regard the whole action-vector as one single action (decided at the start) and optimize for that, but it doesn't do justice to the "dynamic" angle of the problem. I could also make each step truly dependent on the past. But this gets intractable very quickly. Nathan Kallus has some super cool work on DTR Bandits, but it only handles 2-step interventions. Maybe I can try to generalize this once I understand the math.

Separately, I also tried to [code up some simulations](src/invariant-learning/utils/) for invariant learning. I think this would be really cool to just test out with a simple linear case, to see if dimensionality reduction retrieves the latents. But this is a separate workstream I should probably pursue in the summer.

**Week 12+:**

I think I figured out how to decompose the final outcome in terms of preceding variables, such that we are still able to look at all previous values when deciding an intervention.

Update: it's worked on an experiment!

Update: it's worked on another experiment!

I'm still trying to prove the theoretical guarantee, though. It's turning out to be quite tricky. In the standard EXP3 proof, we use actual losses per round, which is an unbiased estimator (after importance weighting). There's no reason to believe an estimated loss serves this function. Maybe I can try to also use actual values of covariates in each round in the decomposition. But this is going to be terribly noisy (maybe I can experiment with this approach later on).

I hope to eventually submit this to AISTAT 2023!!
