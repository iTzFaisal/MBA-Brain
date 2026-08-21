# Chapter 11: Artificial Intelligence, Robotics, and Quantum Computing Technology

## Core Idea
AI is the theory and development of computer systems that perform tasks normally requiring human intelligence, but most current systems are narrow, data-dependent tools. Use AI to augment decisions and discover patterns, not only automate labor. Combine it with robotics carefully, and treat quantum computing as a promising but immature capability requiring different assumptions about computation and risk.

## Frameworks Introduced
- **Three stages of Artificial Intelligence Development**: Use to distinguish current capability from future claims.
  - **Artificial narrow intelligence (ANI)** performs narrow, predefined tasks and describes most current applications. **Artificial general intelligence (AGI)** would match human capabilities. **Artificial super intelligence (ASI)** would exceed human capabilities. Do not plan as if AGI or ASI were current technology.
- **Four types of artificial intelligence machines**: Use to classify how an application uses experience and models its environment.
  - **Reactive machines** use fixed rules; **limited memory machines** combine rules with recent events; **theory of mind machines** would model other agents and emotions; **self-awareness machines** would model themselves. The last two remain future or hypothetical categories.
- **The Six Branches of Artificial Intelligence**: Use to select a capability: **machine learning**, **deep learning**, **natural language processing (NLP)**, **expert systems**, **fuzzy logic**, and **robotics**.
  - How: Match the branch to the work. ML finds patterns, DL uses neural networks, NLP handles human language, expert systems reason in a domain, fuzzy logic handles graded inputs, and robotics acts in the physical world.
- **Three approaches to machine learning**: Use according to the training signal.
  - **Supervised learning** trains from labeled answers; **unsupervised learning** discovers patterns without labels; **reinforcement learning** learns by trial and error from rewards and penalties.
- **Gartner Five-Stage AI Maturity Model**: Use to assess organizational readiness and set a realistic adoption path.
  - Move from **Awareness** to **Active** use cases, proofs of concept, and pilots; **Operational** production projects with experts and budgets; **Systematic** adoption across processes and the supply chain; and **Transformational** AI embedded throughout the business.
- **Quantum computing model**: Use to distinguish classical bits from quantum computation. Bits hold 0 or 1; qubits can represent values between 0 and 1 through **superposition**, and quantum systems also use **entanglement** and **interference**.

## Key Concepts
- **Turing Test**: A conversational test in which a judge cannot distinguish a computer from a human.
- **Machine learning (ML)**: Statistical algorithms trained on data to find patterns and produce a desired behavior.
- **Deep learning (DL)**: Machine learning using neural networks with an input layer, hidden layers, and an output layer.
- **Natural language processing (NLP)**: AI that understands or generates human language; NLU and NLG are its two basic components.
- **Expert system (ES)**: A domain-specific AI system composed of a knowledge base, inference engine, and user interface.
- **Fuzzy logic**: Reasoning that handles values between binary yes/no or true/false states.
- **Work automation**: Replacing human work with machines or computer technology.
- **Collaborative robots (cobots)**: Robots designed to work with people, often taking heavy, repetitive, or unsafe tasks.
- **Computer vision**: AI that uses cameras and deep learning to identify objects in images or video.
- **Decoherence**: Loss of a qubit's quantum state from noise, vibration, temperature, or electromagnetic effects.

## Mental Models
- **AI as a pattern engine**: Use AI when the organization has enough relevant data and a decision or prediction can be improved by finding patterns humans cannot process at scale.
- **Maturity before scale**: Move from a bounded proof of concept to a monitored production use case before making AI a systematic business capability.
- **Augment before replace**: Pair AI or robots with human judgment where explanation, empathy, safety, or accountability matters.
- **Quantum is a different substrate**: Think of qubits as a future way to solve certain microscopic, optimization, or simulation problems, not as a faster replacement for every classical computer.

## Anti-patterns
- **Using a black box in a regulated decision**: HSBC's case shows that finding a pattern is insufficient when bankers must explain why it indicates fraud.
- **Training on biased or contaminated data**: The COMPAS case and Microsoft's chatbot show that ordinary development choices or hostile interactions can produce discriminatory or harmful outputs.
- **Automating without a workforce plan**: Repetitive jobs may disappear, so retraining and role redesign are part of adoption, not optional public relations.
- **Treating an AI demo as production readiness**: Skills, data infrastructure, measurable benefits, privacy, security, and oversight remain necessary.
- **Investing in quantum hardware before a use case**: Current machines are error-prone, have low fault tolerance, and lose coherence quickly.

## Worked Example
**HSBC anti-money-laundering (AML).** Traditional rules could miss a suspicious account change buried in huge transaction volumes. Ayasdi first used feature engineering to identify useful variables, then machine-learning algorithms searched HSBC data for patterns and clusters. Ayasdi, HSBC IT specialists, and modeling experts reviewed and validated the results so the patterns could be explained rather than treated as an opaque prediction. The AML application found new fraud patterns and reduced false positives by 20%. The operational lesson is to combine data preparation, model discovery, expert validation, and explainability.

## Key Takeaways
1. Most business AI is ANI: narrow, useful, and dependent on data quality.
2. Choose ML training mode and AI branch from the task, labels, risk, and required explanation.
3. Use the maturity model to sequence awareness, pilots, production, systematic adoption, and transformation.
4. AI can augment prediction, sentiment analysis, content management, and human decisions beyond simple automation.
5. Robotics adds physical action; AI adds perception, learning, communication, or decisions.
6. Treat privacy, civil rights, bias, job transition, and explainability as design requirements.

## Connects To
- **Chapter 6**: Predictive analytics, big data, data mining, and visualization supply AI inputs and evaluation.
- **Chapter 8**: Recommendation engines, personalization, chatbots, computer vision, and mobile commerce use AI.
- **Chapter 10**: AI advances always-on supply chains, CRM, content management, and enterprise knowledge management.
- **Chapter 12**: AI, robotics, and quantum computing are strategic technology trends requiring deliberate scanning.
- **Chapter 14**: Automation, surveillance, bias, privacy, and civil-rights impacts require ethical governance.
- **Chapter 13**: PMTQ and project methods govern AI implementation and change.
