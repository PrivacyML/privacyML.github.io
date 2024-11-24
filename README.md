privacy.github.io | ML Privacy &amp; Privacy Eval | A Tutorial at NeurIPS 2024 | Vancouver, British Columbia, Canada
## Meaningful Privacy-Preserving Machine Learning and How To Evaluate AI Privacy
In the world of large model development, model details and training data are increasingly closed down, pushing privacy to the forefront of machine learning – how do we protect privacy of the data used to train the model, permitting more widespread data sharing collaborations? How will individuals trust these technologies with their data? How do we verify that the integration of individual’s data is both useful to the rest of the participating federation, and, more importantly - safe for the data owner? How do the regulations integrate into this complex infrastructure?

These open questions require a multitude of considerations between the incentives of model development,the  data owning parties, and the overseeing agencies. Many cryptographic solutions target these incentives problems, but  are they covering all essential components of trustworthy data sharing? Are they practical, or likely to be practical soon?

In this tutorial, we attempt to answer questions regarding specific capabilities of privacy technologies in three parts: 1. overarching incentive issues with respect to data and evaluations, 2. Where cryptographic and optimisation solutions can help; for evaluations, we delve deep into secure computation and machine unlearning. 3. Cultural, societal, and research agendas relating to practically implementing these technologies.

We hope that, by identifying the boundaries of the use of privacy technologies, and providing a technical and structured framework for reasoning over these issues, we could empower the general audience to integrate these principles (and practical solutions) into their existing research. Those already interested in applying the technology can gain a deeper, hands-on understanding of implementation useful for modeling and developing incentive-compatible solutions for their own work.

# Why Tutorial
We observe that the ML community cannot sufficiently access privacy tech. People interested in safe ML topics such as model alignment often do not have a clear understanding of cryptography-based techniques when applied to ML.

On the other hand, cryptographers want to apply their knowledge, especially with practical security management, to machine learning systems. Yet they face the problem of a completely different mindset from machine learning researchers who currently drive the development of these systems.

These communities do not engage with each other, partly because they do not have a shared common ground. This tutorial can bridge the gap between cryptography and effective decentralized ML training and evaluation.

Through our work on evaluations of privacy technology for machine learning, we found that disparate communities in ML training, large model R&D, safety and policy urgently want to have an overview on the state of privacy and evaluations that suit their purpose, especially as generative AI technologies become important. However, there is no single technology that fits all use cases, and without in-depth knowledge of both machine learning and cryptography, it can be very difficult to initiate research in this impactful and fast-moving field. We hope that clarifying the technologies for this purpose will help towards effective scientific coordination.

# Speakers
Mimee Xu (​mimee@nyu.edu​)​: ​Mimee Xu is a 6th year PhD student at NYU’s Courant Institute, working under Prof. Leon Bottou on the intersection of Privacy and Security of ML. During her PhD, she interned at Facebook AI Research and Bytedance Machine Learning. Previously, she worked as a Research Engineer at Baidu SVAIL, UnifyID, and before that, she worked on security and stability on the Google Chrome team. She organized the ML for Systems workshop for 5 years.

Fazl Barez (fazl@robots.ox.ac.uk) is a Research Fellow at Torr Vision Group (TVG), University of Oxford, where he works on topics related to AI safety. Additionally, Fazl also holds affiliations with Kruger AI Safety Lab (KASL), the Centre for the Study of Existential Risk at University of Cambridge and Future of Life Institute.  Previously, Fazl  worked as Technology and Security Policy Fellow at RAND, on Interpretability at Amazon and The DataLab, safe recommender systems at Huawei, and on building a finance tool for budget management for economic scenario forecasting at Natwest Group. Fazl holds a PhD in Artificial Intelligence Safety and has previously organized a workshop at ICML (Mechnatic Interpretability) and a workshop at EACL (Inverse Scaling)

Dmitrii Usynin (dmitrii.usynin16@imperial.ac.uk) is a ML Researcher at Microsoft Research and a final year PhD student in a Joint Academy of Doctoral Studies (JADS) at Imperial College London and TU Munich. His research interests lie on the intersection of collaborative machine learning (CML) and trustworthy artificial intelligence (TAI). In particular, he is  interested in topics such as privacy-preserving machine learning (PPML), attacks on CML, adversarial robustness, federated learning and memorisation in ML. Previously Dmitrii has co-organized a workshop and a tutorial on decentralized and privacy-preserving ML at MICCAI. Outside of his PhD, Dmitrii is an Investment Partner at CreatorFund, leading early-stage deep tech investment in Europe. Previously he was also a privacy researcher at OpenMined, working on federated learning and differential privacy in healthcare.

# Panelists (TBD)
We would like to have a diverse set of perspectives represented through our panel, covering topics related to privacy evaluations.

Some potential questions for NeurIPS audience
* What is the state of each of the technologies (Homomorphic encryption for machine learning, secure-mpc or on-device training, private evaluations.) now?
* What do you say to the claim that “privacy is dead”, or “we don’t need privacy”?
* What are the limitations that you think are solvable in the near term?

## A. Feder Cooper
Dr. Cooper is a Postdoctoral Researcher at Microsoft Research, an Affiliate Researcher at Stanford HAI, and a future Assistant Professor, Yale CS. Cooper researched topics on reliable measurement and evaluation of machine learning systems and is a co-founder of the [GenLaw Center](https://genlaw.org/).

# Tentative Outline
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
* Controlling existent GPU footprint
* Mass production of hardware to support TEE
* Cheaper inference infrastructure
* Policy interventions

**Tractable technical problems for NeurIPS Community**

* Software infrastructure maturity
* Optimisation research towards exact unlearning
* Measurement science
* Industry-compatible unlearning standards
* More leakage detection research \- the theoretic limits.
