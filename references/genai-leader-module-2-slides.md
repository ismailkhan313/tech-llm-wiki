---
type: Reference
resource: "Google Cloud Skills Boost — Generative AI Leader (ILT), Module 2: Gen AI - Unlock Foundational Concepts"
author: Google Cloud
fidelity: transcription
retrieved: 2026-09-02T18:55:15Z
---

# Module 2: Gen AI — Unlock Foundational Concepts

Transcription of the official slide deck (164 slides), footers and layout
artifacts stripped, quiz question/answer slides merged.

## Module objectives

1. Define core gen AI concepts.
2. Explain how data types are used in gen AI for business impact.
3. Explain the role of foundation models in gen AI.
4. Describe Google Cloud's strategies for handling LLM limitations.
5. Describe the challenges for responsible and secure AI development and
   deployment.

## Agenda

1. Core gen AI concepts
2. Foundation models
3. Building AI securely and responsibly

## 1. Core gen AI concepts

### Defining AI, ML, and gen AI

- **AI**: building or creating machines to do tasks that normally require
  human intelligence.
- **ML**: a subset of AI where machines learn from data to perform specific
  tasks. Different data creates different models.
- **Gen AI**: a subset of machine learning that focuses on creating new
  content.

### The importance of data in ML

- We try to get machines to recognize patterns and make predictions based on
  data.
- Data is information, and it can come in many forms.
- A machine learning model needs the right kind of data to learn effectively.
- ML models analyze the data they've been given, identify patterns, and then
  calculate the likelihood of different outcomes when presented with new
  information — data quality and accessibility are crucial for accurate
  predictions.

### Data quality (5 factors)

- **Accuracy** — if the data is inaccurate, the model will learn incorrect
  patterns and make faulty predictions.
- **Completeness** — refers to the size of a dataset and representation
  within it; the model needs enough data to make an accurate prediction.
- **Representative** — data needs to be representative and inclusive,
  otherwise it can lead to skewed samples and biased outcomes.
- **Consistency** — inconsistent data formats or labeling can confuse the
  model and hinder its ability to learn effectively.
- **Relevance** — data must be relevant to the task the AI is designed to
  perform.

### Data accessibility (3 factors)

- **Availability** — if the necessary data isn't available, the AI model
  can't be trained.
- **Cost** — the cost of acquiring high-quality data can be a significant
  barrier to AI development.
- **Format** — data needs to be in a format the AI model can understand and
  process.

### Data types

- **Structured data** — organized; easy to search for and find the
  information you need. Example: customer ID, customer name, delivery
  address, purchase date, order cost.
- **Unstructured data** — lacks a predefined structure; messy and complex,
  can't be easily organized. Example: product image, feedback (1-5 star
  scale is actually structured — free-form text feedback and email content
  are the unstructured examples given).

### Quiz — data

- Q: Numerous factual errors (wrong dates, mislabeled details) in training
  data compromise which quality factor? **A: Accuracy.**
- Q: Key nuance about large datasets and data accessibility? **A: While
  often beneficial, large volume isn't the only data aspect influencing
  performance.**

### Types of learning

- **Supervised learning** — trained on labeled data (tags like name, type,
  number that assign meaning). Labels enable the algorithm to learn
  relationships and make accurate predictions on new, unseen inputs.
- **Unsupervised learning** — trained on unlabeled data with no inherent
  "correct answer." The model finds natural groupings in raw data —
  exploratory analysis to uncover underlying structure.
- **Reinforcement learning** — the model learns through interaction and
  feedback (rewards/penalties), learning which actions lead to the best
  outcomes. Useful when you can't provide explicit instructions or labeled
  data.

### ML approaches on Google Cloud — examples

- **Predictive maintenance** with Agent Platform (supervised) — trains on
  sensor data to predict machine failure, enabling proactive maintenance.
- **Anomaly detection** with BigQuery ML (unsupervised) — analyzes
  historical transaction data to flag transactions that deviate from the
  norm.
- **Product recommendations** with Agent Platform (reinforcement) — learns
  to maximize user engagement and sales by refining recommendations.

### Scenario feedback (activity)

- Video game AI that learns from rewards/penalties through trial and error
  → **reinforcement learning** (learns via interaction with environment,
  maximizes cumulative reward).
- Email spam classifier trained on manually labeled emails →
  **supervised learning** (labeled dataset, learns input→output mapping).
- Discovering underlying topics in a document collection (topic modeling)
  → **unsupervised learning** (no predefined labels, model discovers
  structure on its own).

### Key stages of making data accessible for AI (ML lifecycle)

1. **Gather your data** — determine what data you need based on the desired
   outcome. Google Cloud tools: Pub/Sub (real-time streaming), Cloud Storage
   (unstructured), Cloud SQL and Spanner (structured).
2. **Prepare your data** — clean and transform raw data into a usable
   format (formatting, labeling). Google Cloud tools: BigQuery (analysis),
   BigQuery universal catalog (data governance).
3. **Train your model** — the process of creating your ML model using data.
   Google tools: Agent Platform (managed training environment).
4. **Deploy and predict** — make a trained model available for use.
   Google tools: Agent Platform.
5. **Manage your model** — manage and maintain models over time: versioning,
   performance tracking, drift monitoring, data management (Agent Platform
   Feature Store), storage (Model Garden), automation (Agent Platform
   Pipelines).

### Identity and Access Management (IAM)

- Create and manage user accounts.
- Assign roles to users.
- Grant and revoke permissions to resources.
- Audit user activity.
- Monitor your security position.

### Quiz — lesson 1

- Q: How does consistency impact AI model training? **A: Inconsistent
  formats and labeling can confuse the model and hinder learning.**
- Q: What is a model in ML? **A: A complex mathematical structure that
  processes inputs to generate outputs.**
- Q: Primary way agents learn in reinforcement learning? **A: By interacting
  with their environment and receiving feedback.**

### Key takeaways — Lesson 1

- AI is the broad field, ML is a method/approach within AI, gen AI is an
  application of AI that creates new content.
- Data quality and accessibility are crucial for AI; understand data types
  (structured/unstructured) and quality dimensions.
- Supervised, unsupervised, or reinforcement learning train ML models based
  on task and data.
- The ML lifecycle has several key stages supported by Google Cloud tools
  like Agent Platform.

## 2. Foundation models

### Deep learning

- **Machine learning** — a broad field encompassing many techniques to
  teach computers to learn; one of these techniques is **deep learning
  (DL)**.
- **Deep learning** — a specific way of teaching computers to learn from
  data using artificial neural networks. Neural networks leverage labeled
  and unlabeled data (semi-supervised learning).
- Generative AI uses the power of deep learning — particularly neural
  networks — to create new content spanning text, images, audio, and beyond.

### Foundation models

- Use deep learning; trained on massive datasets, allowing them to learn
  complex patterns and perform a variety of tasks across different domains.
- Develop a broad understanding of the world, capturing intricate patterns
  and relationships within the data they consume.

### Types of foundation models

- **Large language models (LLMs)** — understand and generate human
  language; translate, write content, answer questions.
- **Diffusion models** — generate high-quality images, audio, and video
  through iterative refining of data and patterns.

### Quiz — terminology

- Q: Subset of AI that enables machines to learn from data without explicit
  programming? **A: Machine learning.**
- Q: Broad field of computer science for machines performing
  human-intelligence tasks? **A: Artificial intelligence.**
- Q: Specialized subset of ML using multi-layer neural networks for complex
  patterns? **A: Deep learning.**

### Factors when choosing a model for your use case

- **Modality** — the type of data the model can process and generate (text,
  images, video, audio).
- **Context window** — the amount of information a model can consider at
  one time when generating a response.
- **Security** — paramount, especially with sensitive data; consider model
  security features and industry standards.
- **Availability and reliability** — crucial for production applications;
  consider uptime guarantees, redundancy, disaster recovery.
- **Cost** — consider pricing model and cost effectiveness; match the model
  to the task.
- **Performance** — accuracy, speed, efficiency; evaluate on relevant
  benchmarks and datasets.
- **Fine-tuning and customization** — for specialized use cases, consider
  models that offer fine-tuning capabilities.
- **Ease of integration** — integration into existing systems/workflows;
  well-documented APIs and SDKs.

### Google Cloud's gen AI models

- **Gemini** — multimodal understanding, advanced conversational AI, content
  creation, and question answering.
- **Gemma** — user-friendly, customizable, for local deployments and
  specialized AI applications.
- **Nano Banana** — generates high-quality images from textual descriptions.
- **Veo** — generates video content based on text descriptions or still
  images.

### Foundation model limitations

- **Data dependency** — performance is heavily data-dependent; biases or
  incompleteness in data seep into outputs.
- **Knowledge cut-off** — the last date the model was trained on new
  information.
- **Bias** — an LLM learns from large amounts of data, which may contain
  biases; subtle biases can be magnified in outputs.
- **Fairness** — interpreted differently by different people; fairness
  assessments have inherent limitations, typically focusing on specific
  categories of bias and potentially overlooking others.
- **Hallucinations** — models sometimes produce outputs that aren't
  accurate or based on real information; fix by grounding the AI to
  specific, reliable data.
- **Edge cases** — rare/atypical scenarios can expose a model's weaknesses,
  leading to errors, misinterpretations, unexpected results.

### Techniques to overcome limitations

- **Prompt engineering** — crafting precise prompts to guide the model
  toward desired outputs.
- **Grounding** — using specific data (e.g. company documents) to provide
  accurate, relevant, enterprise-specific responses, increasing
  trustworthiness.
- **Retrieval-Augmented Generation (RAG)** — a grounding method using search
  to find relevant info from a knowledge base, then feeding it to the LLM
  as context. Steps: (1) retrieve information based on meaning, (2) augment
  the prompt, (3) generate a response.
- **Fine-tuning** — further training a pre-trained/foundation model on a
  new, task-specific dataset; helps models excel in specific areas, useful
  for specific tasks or output formats. Used when prompt engineering alone
  doesn't achieve the desired outcome.

### Humans in the loop (HITL)

- Use cases: content moderation, sensitive applications, high-risk decision
  making.
- Applied at: pre-generation review, post-generation review.

### Quiz — foundation models

- Q: Best foundation model type for photorealistic images from text? **A:
  Diffusion model.**
- Q: Primary role of HITL in ML? **A: To integrate human expertise into the
  ML process, especially for tasks requiring judgment or context.**
- Q: Techniques to overcome foundation model limitations? **A: Grounding,
  prompt engineering, fine-tuning, and humans in the loop (HITL).**

### Key takeaways — Lesson 2

- Deep learning powers foundation models, enabling generative AI to create
  new content.
- Consider all relevant factors when choosing a gen AI model. Google
  Cloud's Agent Platform offers Gemini, Gemma, Nano Banana, Veo.
- Foundation models have limitations like bias and hallucinations.
  Grounding, prompt engineering, fine-tuning, and HITL can address these.

## 3. Building AI securely and responsibly

### Secure AI principles applied to the ML lifecycle

1. **Gather your data** — secure data is the foundation of any robust AI
   system; must be protected at all times. Access, addition, and input to
   data must be controlled.
2. **Prepare your data** — special attention to confidential/sensitive data
   in training data: anonymization, validation, secure processing, logging
   and real-time monitoring.
3. **Train your model** — safeguard both training data and model parameters
   from unauthorized access or modification.
4. **Deploy and predict** — control access to the model; verify sources and
   check for vulnerabilities in pre-built models.
5. **Manage your model** — stay current on security best practices, make
   regular updates, monitor model performance/outputs for anomalies or
   tampering, review access permissions regularly.
- Also: guard against adversarial attacks; monitor AI outputs to prevent
  leaks and harmful content.

### Secure AI Framework (SAIF)

- Establishes security standards for building and deploying AI systems
  responsibly.
- Google Cloud enables secure development via secure-by-design
  infrastructure, encryption, IAM, Security Command Center, and monitoring
  tools.
- Google Threat Intelligence Group's global insights + Mandiant's frontline
  expertise move protection toward proactive, AI-driven operational
  readiness.

### Foundations of responsible AI

- **Transparency** — users need to understand how their information is
  used and how the AI system works.
- **Privacy** — protect via anonymizing/pseudonymizing data; safeguard
  against models inadvertently leaking sensitive training data.
- **Data quality, bias, and fairness** — ethical AI requires high-quality
  data and responsible use of data; AI inherits societal biases, causing
  unfair outcomes — fairness must be central to development.
- **Accountability and explainability** — fairness requires accountability;
  explainable AI makes AI decision-making transparent and understandable;
  understand how your application uses and interprets the AI's output.

### Legal implications

- Key legal areas: data privacy, non-discrimination, intellectual property,
  product liability.
- AI laws require responsible data handling, bias mitigation, transparency,
  and model compliance.
- The evolving legal landscape demands vigilance and counsel for
  trustworthy AI.

### Quiz — secure & responsible AI

- Q: Ethically sound AI loan-assessment system — select two. **A: Regularly
  audit the model's performance to identify and mitigate emerging biases;
  train on a diverse dataset representing different demographics/
  socioeconomic backgrounds.**
- Q: Primary goal of SAIF? **A: To establish security standards for
  building and deploying AI responsibly, addressing the unique challenges
  and threats in the AI landscape.**
- Q: Primary goal of ethical AI development? **A: To ensure AI systems are
  used responsibly and do not cause harm.**

### Key takeaways — Lesson 3

- AI offers significant benefits but introduces security risks; Google
  Cloud's SAIF and tools help build secure AI.
- Responsible AI development requires understanding potential issues and
  mitigating safety, security, and ethical implications throughout the AI
  lifecycle.

## Module wrap-up quiz

- Q: Key aspect of securing the model training phase? **A: Safeguarding
  training data and model parameters from unauthorized access.**
- Q: Consequence of inaccurate/incomplete training data? **A: It introduces
  biased outcomes and unfair results.**
- Q: When is fine-tuning particularly useful? **A: When prompt engineering
  alone doesn't achieve the desired outcome, and the model needs to be
  specialized for specific tasks/output formats using a new, task-specific
  dataset.**
- Q: Key legal responsibility for organizations developing/deploying AI?
  **A: Ensure adherence to data privacy laws, non-discrimination
  principles, and the specific licensing terms of AI models.**

## Additional resources (cited by the deck)

- Lesson 2: "Summary of techniques to overcome limitations of foundation
  and pre-trained models."
- Lesson 3: "Google's Secure AI Framework (SAIF)."
