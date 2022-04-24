**14 Apr:**

I was only just directed by a classmate to the part in the course description detailing that we need to maintain this repository. Sincere apologies for starting my commits late, I will back-date my project history through the semester.

**Week 1:**

I wanted to do a comparison of synthetic controls of a large-scale intervention (which I would do) and prior RCTs on the same intervention, to see if they align.

I spent a lot of time searching for good quality public data, but found it tricky. There was a lot of general data available for education, healthcare, climate etc. But the tricky requirement here was that I needed
- An RCT done on the intervention
- A subsequent implementation of the exact policy tested
- Monitoring and evaluation of the specific variables that the RCT studied

Point 3 in particular was difficult, because without this the comparison of Synthetic Controls to the RCT may not be useful.

**Weeks 2-3:**

I spent a ton of time getting data on education in India and malaria initiatives in Sub-Sahara.

The India education stats were in particular super exciting. In Econometrics+Causality there is all this buzz recently about RCT-driven policy interventions. 2019 Nobel Laureates (called the "randomistas") pioneered this movement in development policy and are personal heros.

They established distributing LLIN-bednets for malaria prevention was one of the most cost-effective interventions (in terms of Quality-Adjusted Life Years added per $ spent). They also established an educational intervention called Teaching At the Right Level (TARL).

RCTs in Northern Indian states were very promising and they rolled it out. I unfortunately hit snags with the data:
- Turns out the RCTs used a TARL policy that was materially different from the scaled-up version
- The RCTs measured improvements in specific skills like numeracy and reading through curated tests
- While government data proved excellent (they even had district level tags for female toilet availability!) they don't have subject level performance, just aggregated dropout rates, pass-fail etc.

This would be my back-up if I find no other dataset.

**Weeks 4-5:**

I became very interested in the Nordic Gender Paradox. This is a phenomenon in Nordic countries where, one would imagine that ranking higher on several measures of gender equality, we would see more female CEOs and STEM graduates. However, the gap actually widens compared to other countries. This is a somewhat controversial claim, and I have stored photos of all my notes in the link below.

The main crux of investigation is the causal model in [this document's](https://docs.google.com/document/d/1Udi3FI0cPqxdA-J4_iLGWMnFxIEDUSvThgdx1kZblyo/edit?usp=sharing) first page (LionMail access). How much of this disparity is via Intrinsic vs. Extrinsic pathways?

One way I can think of testing this is to run a Synthetic Control study using macroeconomic data from Sweden, Norway and Finland. If a tax break for household services in SWE affects female participation in the workforce (NOR, FIN: donor pool), then we can assume that extrinsic factors indeed affect participation.

