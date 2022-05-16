# Applied-Causality
Applied Causality project, Spring 2022

CausalEXP3: An Efficient Causal Algorithm for Adversarial Bandits

Abstract-
Adversarial bandits are important in safety-critical or risk-averse settings where rewards distributions might change with great detriment to the learner. Recent variants of common algorithms, like the LinEXP3 variant of the standard EXP3, explore how to improve regret guarantees in settings with assumptions like linear realizability. We introduce a novel algorithm CausalEXP3 that leverages knowledge of the underlying structural causal model to demonstrably reduce the cumulative regret incurred during on-line learning. We apply this experimentally in the context of Dynamic Treatment Regimes (DTR). First, we test it on a Lung Cancer DTR, involving heavy confounding between variables. Second, we test it on a Drug-Offences Intervention DTR under adversarial reward shift conditions. In both experiments, we demonstrate it outperforms the same EXP3 algorithm that does not exploit structural causal knowledge. 

The code for this expriment is in 2 notebooks in the src/final project folder:

- Experiment 1: Cancer_DTR.ipynb
- Experiment 2: DrugRehab_DTR.ipynb
