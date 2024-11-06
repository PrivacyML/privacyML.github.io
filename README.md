# ML Privacy & Privacy Eval Tutorial at NeurIPS 2024
**Location:** Vancouver, British Columbia, Canada  
**Date:** December 2024  
**Website:** [privacy.github.io](https://privacy.github.io)  

## **Meaningful Privacy-Preserving Machine Learning and How To Evaluate AI Privacy**

In large-scale model development, as model details and training data become more restricted, privacy has risen to the forefront of machine learning challenges. How do we safeguard the privacy of data used for model training, enabling broader data-sharing collaborations? How can individuals trust that their data is securely integrated into these models? How do we ensure that the inclusion of data is both beneficial to federated systems and safe for data owners? Moreover, how do regulatory frameworks adapt to support this intricate infrastructure?

These critical questions require balancing the interests of model developers, data custodians, and regulatory bodies. While cryptographic solutions target some of these privacy issues, are they adequately addressing all aspects of trustworthy data sharing? Are they practical for today’s needs?

### Tutorial Overview
This tutorial addresses essential questions around privacy technologies in three main parts:
1. **Incentive Issues**: Exploration of data and evaluation incentives.
2. **Technical Solutions**: Overview of cryptographic and optimization-based solutions, with a focus on secure computation and machine unlearning.
3. **Implementation Considerations**: Discussion of societal, cultural, and research aspects for effective deployment.

Through this structured framework, attendees will gain insights into applying privacy-preserving principles and practical solutions to their research, with a hands-on understanding for those interested in integrating privacy-enhanced, incentive-compatible methods into machine learning workflows.

### Tutorial Motivation
The ML community faces limited access to practical privacy technology. Those interested in safe ML, including model alignment, may lack a clear understanding of cryptography-based techniques relevant to ML applications. Conversely, cryptographers often seek to apply their knowledge within ML systems but encounter a knowledge gap due to different disciplinary perspectives.

Our tutorial aims to bridge this gap, enhancing collaboration between cryptography and ML communities. As generative AI technologies grow, an understanding of privacy evaluations and their applications is essential. By clarifying the state of these technologies, we aim to foster effective scientific coordination and enable impactful research.

## Speakers
- **Mimee Xu** (mimee@nyu.edu): 6th-year PhD student at NYU’s Courant Institute, with research at the intersection of privacy and security in ML, including experience with Facebook AI Research, Bytedance, and Baidu.
- **Fazl Barez** (fazl@robots.ox.ac.uk): Research Fellow at University of Oxford, focusing on AI safety with affiliations at Kruger AI Safety Lab and Cambridge’s Centre for the Study of Existential Risk.
- **Dmitrii Usynin** (dmitrii.usynin16@imperial.ac.uk): ML Researcher at Microsoft Research and PhD candidate at Imperial College London, specializing in privacy-preserving ML, federated learning, and adversarial robustness.

### Panelists
- **Feder Cooper**: Postdoctoral Researcher at Microsoft Research, Affiliate at Stanford HAI, and incoming Assistant Professor at Yale CS. Feder’s research focuses on reliable measurement and evaluation of ML systems.

## Tentative Outline

### Incentive Issues in ML Evaluations
- **Data Bottlenecks**: Costly training data, model secrecy, and lack of privacy oversight.
- **Evaluation Set Risks**: Public evaluation sets risk leakage.
- **Testing Leakage**: Detecting leakage from model outputs is statistically challenging, often relying on proxies for memorization estimates.

### Solution Part 1: Privacy-Enhanced ML
- **On-Device/On-Premise Solutions**: Differential privacy, distributed privacy, and cryptographic methods (with demos).
  - Homomorphic Encryption (SEAL demo)
  - Secure Multiparty Computation (CrypTen demo)
  - Secure Hardware (Trusted Execution Environment demo)
- **Challenges**: Current limitations include trade-offs between learning and memorization, usability issues, and precision constraints for large models.

### Solution Part 2: Privacy Evaluations
- **Machine Unlearning**: Inspired by the GDPR's “Right To Be Forgotten.”
  - Methods include Mechanistic Interpretation, Retrieval, and Alignment.
  - Issues: Degradation of models, data-centric proofs of unlearning, and fragility of interpretability-based approaches.

### What Are We Waiting For? A Tractable Agenda
1. **Human Factors**: Cultural barriers, coding practices, and community silos.
2. **Commercial Incentives**: Trade-offs between development goals and privacy requirements.
3. **Scientific and Environmental Constraints**: Publication culture in ML, environmental considerations, and the need for policy interventions.

### Key Challenges for NeurIPS Community
- **Software Infrastructure Maturity**: Development of optimized, industry-compatible standards.
- **Unlearning Optimization**: Research on exact unlearning methodologies.
- **Improved Leakage Detection**: Expansion of theoretical boundaries for leakage detection.

---

For more details, visit the official website or reach out to the organizing speakers.
