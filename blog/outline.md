---
layout: page
title: "Outline"
permalink: /outline/
---

| Section                          | Start | End  |
|----------------------------------|-------|------|
| Introduction: PrivacyML Overview | 2:30  | 2:45 |
| Confidential Computation         | 2:45  | 3:20 |
| Tea Break                        | 3:20  | 3:30 |
| Empirical Evaluations            | 3:30  | 3:40 |
| Evaluating Differential Privacy  | 3:45  | 4:00 |
| Evaluating Machine Unlearning    | 4:00  | 4:15 |
| Demo + Panel                     | 4:25  | 5:00 |

**Incentive Issues in ML Evaluations: An Epistemological Crisis.**

* Data bottleneck: costly training data, secret models, and lacking privacy oversight.
* Private training set, public eval sets: evaluation sets risks leakage.
* Leakage may be commonplace with large models.
  * Testing for leakage through only model outputs is non-trivial statistically. Tests rely on finding proxies to make memorization estimates.
  * Often a rough estimate, or a lower bound.

**Solution, Part 1: Privacy-enhanced ML**: a mathematical run down, demos, why & where they don’t work (yet)

* On-device/on-premise (video)
* Differential privacy and distributed privacy (software demo)
* Cryptography-aided solutions
  * Homomorphic encryption
    * Auditing of training data  (SEAL tutorial/demo)
  * Secure Multiparty Computation
    * Appraisal of training data  (CrypTen tutorial/demo)
    * Evaluating transformers on secret held-out sets (demo)
  * Secure hardware (Potential [TTE](https://learn.microsoft.com/en-us/azure/confidential-computing/trusted-execution-environment) demo)
* Some evaluations are practical, and should be private. Why not now?
  1. Methods That Degrade Models Are Not Competitive

		i. Learning-memorization trade-off & what it means for differential privacy**.**

2. Cryptography-aided Solutions Have Usability Issues

   i. Model training today requires researchers in the loop, so switching entirely to ”private mode” where all details are hidden hinders utility.

   ii. private machine learning technologies are not mature for computations that need high precision and scale, thus limiting their prospect for supporting the large models in the current markets.

**Solution, Part 2: Privacy Evaluations**: a journey through machine unlearning methods’ evaluations.

* Model Editing and Machine Unlearning
  * Loosely inspired by GDPR “Right To be Forgotten”
  * Difference between training data forgetting and
* Unlearning Through Mechanistic Interpretation (paper)
* Unlearning Through Retrieval and Alignment (paper)
* Some methods are promising, and can be implemented without much overhead. Why not now?
1. Degradation of models is undesirable to industry
2. Only data-centric proofs of unlearning satisfies privacy constraints
   1. Fundamental trade-off of concept composition and unlearning
   2. How is duplicate data treated mathematically matters
3. Interpretability-inspired unlearning is brittle (paper)
   1. Unlearning often can be relearned
   2. Features found through interpretability are often fragile

**What Are We Waiting For? A Tractable Agenda.**
**Human factors**
Cultural: machine learning and cryptography are silo-ed communities

* Shifting tool sharing, coding practices, publishing norms.

Commercial Incentives: development vs. privacy and safety

* Increased optimism of capability hurts evaluations
* Alignment?

Scientific: Machine learning conference publishing culture can encourage poor measurement design

* ML science does not necessarily incorporate industrial constraints
* Data-intensive training hurts held-outness

**Environmental**
Controlling existent GPU footprint
Mass production of hardware to support TEE
Cheaper inference infrastructure
Policy interventions

**Tractable technical problems for NeurIPS Community**

* Software infrastructure maturity
* Optimisation research towards exact unlearning
* Measurement science
* Industry-compatible unlearning standards
* More leakage detection research \- the theoretic limits.
