---
type: Reference
resource: "Google Cloud Skills Boost — Generative AI Leader (ILT), Module 3: Gen AI - Navigate the Landscape"
author: Google Cloud
fidelity: transcription
retrieved: 2026-09-02T18:55:15Z
---

# Module 03: Gen AI — Navigate the Landscape

Transcribed from the official slide deck (242 slides). Progressive-reveal
build slides (the same slide shown multiple times as bullets are added one at
a time) are collapsed to their final, complete state. The recurring
"Proprietary + Confidential" footer is omitted throughout.

## Module objectives

1. Describe the layers of the gen AI landscape.
2. Identify entry points in the gen AI landscape to address business needs
   and innovation.
3. Describe components of the Google Cloud gen AI portfolio.
4. Explain how Google Cloud's AI-optimized resources support gen AI
   development.
5. Describe business factors to consider for specific applications.

## Agenda

1. The gen AI landscape
2. Gen AI applications and agents
3. Gen AI platform, models, and infrastructure
4. Gen AI project resources and management

## Section 1: The gen AI landscape

### Building blocks of generative AI

Five layers, top to bottom: Gen AI applications → Agents → Platform → Models
→ Infrastructure.

- **Gen AI applications**: the user-facing part of generative AI (frontend).
  Allows users to interact with and leverage AI capabilities. Examples: the
  Gemini app, Google Workspace with Gemini, Gemini Notebook.
- **Agents**: a piece of software that learns how to best achieve a goal
  based on inputs and tools available to it. Focuses on autonomous action.
  Examples: customer agents, code agents, data agents.
- **Platform**: provides tools and services for agents and models to
  interact. Offers APIs, data management capabilities, and model deployment
  tools.
- **Models**: the brain of the agent. A complex algorithm trained on vast
  amounts of data; generates new content, translates languages, answers
  questions. Examples: LLMs, image recognition models, recommendation
  systems.
- **Infrastructure**: provides the core computing resources needed for
  generative AI — the hardware and software needed to store and run AI
  models and training data.

### Activity: Layers of gen AI

Match a statement to a layer:
1. Tools to label training data, experiment with architectures, deploy a
   finalized model → **Platform**.
2. A website that generates an image instantly from a text description →
   **Application**.
3. Increasing processing power / specialized processors and high-speed data
   connections to train a large model → **Infrastructure**.
4. A system trained on millions of lines of code that suggests the next
   line → **Model**.
5. Monitoring social media, identifying negative sentiment, drafting a
   response automatically → **Agent**.

### Key takeaways

- Generative AI relies on interconnected layers, from infrastructure to gen
  AI applications.
- Understanding these layers empowers informed decisions and business
  innovation.

## Section 2: Gen AI applications and agents

### What can agents do?

A gen AI agent is an application that tries to achieve a goal by observing
the world and acting upon it using the tools it has at its disposal.

### Capabilities of agents

- **Understand and respond to natural language** — more intuitive
  interfaces that can understand complex requests.
- **Automate complex tasks** — handle multi-step processes within an
  application.
- **Personalization** — learn user preferences and tailor the application
  experience.

### Multi-agent systems in gen AI-powered applications

- **Travel booking app**: one agent finds the best flights/hotels; another
  suggests activities/attractions; the application provides the browsing and
  reservation interface.
- **Customer support app**: an agent answers common questions,
  troubleshoots, and escalates complex issues to humans; the application
  provides the chat interface and integrates with support systems.
- **Personalized learning app**: an agent assesses a student's knowledge,
  recommends materials, and generates personalized exercises; the
  application structures lessons and tracks progress.

### How agents work

Two categories:

- **Conversational agents** — flow: you provide input (type/speak) → agent
  understands → agent calls a tool → agent generates a response → agent
  delivers the response. Examples: answering questions, chatting casually,
  accessing information.
- **Workflow agents** — flow: you provide input (define a task/trigger a
  process) → agent understands → agent calls a tool → agent generates a
  result/output → agent delivers the result/output. Examples: ecommerce
  order fulfillment, customer onboarding, automated research, security log
  parsing.

### Agent use cases

- **Customer service agents** — answer questions, resolve issues, provide
  personalized recommendations.
- **Employee productivity agents** — help workers find information, manage
  tasks, automate workflows.
- **Creative agents** — generate new ideas, create content, translate
  languages.
- **Code agents** — assist developers writing, reviewing, debugging, and
  generating code.
- **Data agents** — analyze large datasets, identify trends, extract
  insights.
- **Security agents** — automate security tasks.

### Gen AI agents: beyond just models

The reasoning loop often utilizes advanced prompt engineering frameworks to
guide its decision-making process.

- Frameworks include: simple rule-based calculations, complex thought
  chains, machine learning algorithms, probabilistic reasoning techniques.
- Named examples: **ReAct** (reasoning + acting) prompting, **Chain-of-
  thought (CoT)** prompting.

### Quiz (Lesson 02)

1. Primary purpose of a gen AI agent → to achieve a specific goal by
   observing its environment, reasoning, and acting upon it using available
   tools.
2. Relationship between gen AI agents and gen AI-powered applications →
   agents are intelligent components that function within a larger gen
   AI-powered application, which provides the UI and overall goals.
3. Best agent category for guiding new customers through account setup,
   tutorials, FAQs ("customer onboarding") → **workflow agent**.
4. Two key elements that distinguish AI agents from standalone LLMs and let
   them tackle complex, multi-step problems → **a reasoning loop and the
   ability to use tools**.

### Key takeaways

- Agents enhance applications by adding intelligence and automation.
- Applications provide the framework and purpose for agents.
- Gen AI agents, with reasoning and tools, solve complex problems beyond
  standalone models.

## Section 3: Gen AI platform, models, and infrastructure

### The platform layer

The platform layer provides the foundation for building and scaling AI
initiatives.

**Agent Platform** streamlines the entire ML workflow by providing:
infrastructure, pre-trained models, and tools to build, deploy, and manage.

Key features and benefits: open and flexible, powerful infrastructure,
pre-trained models, comprehensive tooling, customization, easy integration.

**Agent Platform MLOps tools** — help orchestrate end-to-end ML workflows,
perform feature engineering, run experiments, manage/iterate models, track
ML metadata, monitor/evaluate model quality, and automate/standardize the ML
project lifecycle. Named tools:

- **Agent Platform Feature Store** — share, serve, and reuse ML features to
  maintain consistency and efficiency.
- **Agent Platform Model Registry** — manage model versions, track changes,
  organize models throughout their lifecycle.
- **Agent Platform Model Evaluation** — evaluate and compare model
  performance.
- **Workflow orchestration** — automates ML workflows using Agent Platform
  Pipelines.
- **Model Monitoring on Agent Platform** — monitors models for performance
  degradation, detects input skew/drift, triggers updates or retraining.

### Quiz (platform tools)

1. Track experiments, manage model versions, keep a record of changes →
   **Model Registry**.
2. Deployed model's performance is declining; need to identify cause and
   retrain → **Model Monitoring**.
3. Automate the entire ML pipeline, data preprocessing to deployment →
   **Workflow orchestrations**.

### The models layer

At the heart of every AI/ML system lies the model — sophisticated
mathematical structures trained on massive amounts of data.

**Agent Platform: a model hub** — two paths:
1. **Use models with Model Garden** — discover, customize, deploy existing
   models; select from 160+ models; customize within Agent Platform; some
   pre-trained models usable out-of-the-box.
2. **Build models with Agent Platform** — go fully custom (create/train at
   scale) or use **Agent Platform AutoML** to create/train models.

Model Garden examples:
- First-party foundation models: **Gemini, Nano Banana, Veo, Chirp**.
- First-party pre-trained APIs: Speech-to-Text, Natural Language Processing,
  Translation, Vision.
- Open models: **Gemma 2, CodeGemma, PaliGemma, Llama 3.1/3.2, Mistral
  AI/AI21, TII models**.
- Third-party models: **Anthropic's Claude** model family.

**Agent Platform AutoML** supported objectives by data type:
| Data type | Supported objectives |
|---|---|
| Image data | Classification, object detection |
| Video data | Action recognition, classification, object tracking |
| Tabular data | Classification or regression, forecasting |

Standard workflow for model creation/tuning: gather data → prepare data →
train model → deploy and predict → manage model.

### Quiz (model choice)

1. Need a translation model for a global ecommerce platform, readily
   available/high-performing, moderate budget → **Model Garden**.
2. Experienced AI researcher building a cutting-edge protein-folding model,
   needs complete control over architecture/training → **Agent
   Platform — build your own custom model**.

### Activity: agent versus model (creative-writing assistant)

- Which layer generates grammatically correct text? → **Model layer**.
- Which layer identifies and applies appropriate guidelines based on
  content type? → **Agent layer**.

### The infrastructure layer

The infrastructure layer is the foundation upon which any AI system is
built — the combination of hardware and software that provides the
resources to train, deploy, and scale AI models.

Key components:
- **High-performance computing**
  - **GPUs and TPUs** — the workhorses of AI, excel at parallel processing.
    GPUs: general-purpose parallel processing power. TPUs: custom-designed,
    optimized for AI tasks.
  - **Hypercomputers** — supercomputers built by connecting many individual
    nodes together; provide the massive scale needed to train/run gen AI
    models.
- **High-performance storage**
  - **Large-scale storage systems** — Google Cloud's storage is optimized
    for AI workloads: high throughput, scalability, ability to create dense
    compute clusters for faster training/inference.
  - **Fast storage access** — fast read/write speeds to keep up with
    training demands.
- **Networking** — fast, efficient communication is essential to coordinate
  processors; Google's global fiber network provides high-bandwidth,
  low-latency connectivity.

### Gen AI landscape: travel chatbot example

Maps the 5-layer model to a concrete system:
- Applications layer: website/chatbot.
- Agents layer: conversational agent (front door), planning agent (flight
  search), booking agent (booking tool).
- Platform layer: e.g. Agent Platform.
- Models layer: e.g. Gemini Pro.
- Infrastructure layer: underlying compute/storage/networking.

### Quiz (infrastructure)

1. Development stages where you must consider infrastructure requirements
   if not on a platform that handles it for you (select all) → model
   refinement, model monitoring, model deployment, data collection, model
   training (**all of the listed stages**).
2. What are GPUs and TPUs in AI infrastructure? → **specialized processors
   designed for parallel processing in AI tasks**.
3. Why is high-performance storage important for gen AI? → **to store and
   efficiently access the massive datasets used in AI training**.

### Edge computing

Edge computing runs AI on devices or servers closer to the data source or
point of need.

Benefits of going local/edge:
- Ensures real-time responsiveness.
- Increases data privacy.
- Reduces reliance on internet connectivity.
- **Lite Runtime (LiteRT)** helps ML models work efficiently on edge devices
  and mobile phones.
- **Gemini Nano** is an example of an AI model designed for edge.

**Gemini Nano** benefits: privacy (data stays on-device), speed (fast
responses, no round trip to the cloud), offline access (works without
internet).

Gemini Nano devices:
- **Pixel phones** — powers Call Notes (summarizes phone conversations) and
  Pixel Recorder (summarizes voice recordings).
- **Android** — available to developers via the AI Edge SDK to build AI
  experiences into apps.

**Edge deployment: Agent Platform tools**:
- Convert models — convert to **LiteRT** for optimal edge performance.
- Package and deploy — package models and dependencies into containers for
  edge hardware.
- Manage and monitor — manage edge deployments, track performance, gather
  insights to improve models over time.

### Activity: edge or cloud?

- Medical device analyzing patient data in real-time during surgery →
  **edge** (real-time analysis is critical; cloud latency is unacceptable).
- Customer service chatbot handling millions of daily inquiries → **cloud**
  (needs scalable, robust infrastructure).
- Smart-city traffic pattern analysis/optimization → **cloud** (needs a
  centralized system with cloud-scale capacity).

### Key takeaways

- Agent Platform streamlines machine learning, offering tools and MLOps to
  simplify AI development and deployment.
- AI systems rely on models. Agent Platform provides model options,
  enabling AI innovation.
- Google Cloud's infrastructure powers AI; leaders must understand it for
  efficient, scalable deployment and resource management.
- Edge AI enables real-time responsiveness; Google's tools and Agent
  Platform support building/deploying models at the edge.

## Section 4: Gen AI project resources and management

### Gen AI project resources: people, cost, and time

Framing questions: scale (individual/team/company/millions of customers);
how custom (fine-tuning or brand-new model); how/where/when will users
interact with the solution; how much time, how many people, and what's the
budget.

### Roles and responsibilities

- **Business leaders** — interact with pre-built gen AI solutions to
  enhance daily operations and improve customer experiences. Example:
  Google Workspace with Gemini. → maps to the **Gen AI applications** layer.
- **Developers** — build and deploy custom AI agents and integrate AI
  capabilities into existing applications. Examples: AI Applications, AI
  code generation, AI-driven data processing, pre-trained APIs, Agent
  Platform. → maps to the **Agents** layer.
- **AI practitioners** — customize, deploy, and optimize generative AI
  models. Examples: Agent Platform, scaling AI workloads, integrating
  models with BigQuery, implementing responsible AI measures. → maps to the
  **Platform / Models / Infrastructure** layers.

### Cost

Three primary paid activities: training the model, deploying the model to
an endpoint, using the model to make predictions (compute time, storage for
training data, and model outputs).

**Pricing models for using models**:
- **Usage-based** — pay for the amount used (tokens or characters
  processed).
- **Subscription-based** — recurring fee for access; usage limits or
  feature tiers.
- **Licensing fees** — one-time or recurring fees for commercial use or
  embedding in products.
- **Free tiers** — free access with limited usage, for experimentation or
  non-commercial purposes.

**Pricing metrics**: tokens (a piece of text, like a word or part of a
word), characters (charge per character processed), requests (charge per
request regardless of complexity/volume), compute time (processing time
factors into cost, especially for resource-intensive tasks).

Demo referenced: [Google Cloud's pricing calculator](https://cloud.google.com/products/calculator?hl=en).
Additional resource referenced: "Cost of building and deploying AI models
in Agent Platform."

**Factors affecting cost**:
- Model size and complexity — larger, more capable models generally cost
  more.
- Context window — a larger context window can increase costs.
- Features — specialized features can have separate pricing.
- Deployment — may have compute-based costs.

### Time

- The more custom your solution is, the more time and resources it takes to
  build.
- Evaluate project timelines against needs and requirements.

### Gen AI solution needs

- **Scale**
  - Small scale — select pre-built tools; leverage existing gen
    AI-powered applications.
  - Large scale — select for scalability and security; consider
    infrastructure costs, data storage, latency challenges.
- **Customization** — start with existing models; identify unique needs
  (what sets the project apart — specialized knowledge, complex tasks,
  unique UX?); consider data specificity (fine-tune with domain-specific
  datasets for specialized domains); consider task complexity (simple vs.
  intricate — impacts model choice and training approach).
- **User interaction**
  - UI — integrate AI seamlessly into existing workflows; dedicated
    interface or embedded within current applications.
  - UX — aim for a user-friendly experience; decide if conversational,
    informative, or task-oriented; consider level of guidance/feedback
    users need.
- **Privacy**
  - Data security — measures to protect data during processing/storage:
    encryption, access controls, secure data centers.
  - Compliance — specific regulations to adhere to.
- **Other considerations**
  - Latency — acceptable response time limits; real-time vs. some delay.
  - Connectivity — will the solution always have internet access? consider
    offline functionality.
  - Accuracy — acceptable error tolerances, defined explicitly.
  - Explainability — do you need to understand the AI's reasoning?
    transparency is key in certain domains.

### Quiz (roles, cost)

1. Key factor when determining how custom a gen AI solution needs to be →
   whether grounding/fine-tuning is sufficient or a brand-new model is
   required.
2. Primary responsibility of AI practitioners → customizing, deploying, and
   optimizing generative AI models while ensuring responsible AI practices.
3. Primary cost associated with building gen AI solutions → **model
   training**.

### Decision-making and maintenance

**Making decisions**:
- Comparison of companies/models — evaluate model capabilities, compare
  pricing structures, factor in additional costs, read the fine print.
- Key resources for comparison — provider websites, research papers and
  benchmarks, community forums and discussions.

**Maintenance** — questions: how will the project be maintained? resources
in place to maintain over time? specific maintenance needs?

Key maintenance considerations:
- Model monitoring and retraining — continuously monitor performance,
  retrain periodically.
- Data updates — plan regular updates to keep the model fresh/relevant.
- Software updates and bug fixes — stay informed about updates, implement
  them properly.
- Hardware and infrastructure — server maintenance, security updates,
  capacity planning.
- Security and compliance — regularly review/update security measures,
  ensure ongoing compliance with data privacy regulations.

### Activity: best solution

- Need realistic images from text for a marketing campaign; some coding
  skill, short on time → **use a pre-trained API like Nano Banana to
  generate images quickly**.
- Chatbot for personalized movie recommendations; basic AI understanding,
  no coding experience → **use AI Applications to create a conversational
  agent**.

### Quiz (roles/efficiency)

1. Who is responsible for building/deploying custom AI agents and
   integrating AI into applications? → **Developers**.
2. Marketing team needs product descriptions quickly for an ecommerce sale
   → most efficient: **use a gen AI powered application like Google
   Workspace with Gemini to draft the descriptions**.

### Key takeaways

- Generative AI success requires strategic resource allocation, cost
  awareness, and realistic timelines based on solution complexity.
- Plan for AI's future — adapt, update, and optimize to ensure continued
  value and avoid costly errors.

## Module 03 wrap-up quiz

1. Key elements distinguishing AI agents from standalone AI models →
   **reasoning loop and tools**.
2. Primary advantage of edge computing for AI applications → **real-time
   responsiveness and reduced latency**.
3. Important step when making decisions about gen AI solutions →
   **comparing different companies and models**.

## Additional resources (as listed in the deck)

- Lesson 03: example models and specs.
- Lesson 03: Lite Runtime (LiteRT) overview.
- Cost of building and deploying AI models in Agent Platform.

## Appendix: extra quiz questions (Lesson 02 / Lesson 04)

**Layers of the gen AI landscape**:
1. A data science team training a model on a massive image dataset needs
   powerful hardware/software resources for the compute-intensive training
   process → which layer? → **Infrastructure**.
2. A game developer wants NPCs that hold dynamic conversations, react to
   player actions, adapt behavior, and have unique personalities — which
   layer is most crucial for defining their behaviors/capabilities? →
   **Agents**.
3. A travel agency's AI agent gathers preferences, searches
   flights/hotels/activities, builds itineraries, books, and provides
   ongoing support — how do the agents and applications layers work
   together? → **the agents layer defines the AI's capabilities (searching,
   booking, recommending), while the applications layer provides the
   user-facing tool (website/app) to interact with the agent**.
4. A news organization's agent learns user interests, filters/prioritizes
   articles, summarizes, recommends, and adapts to feedback — how does the
   agents layer contribute? → **the agents layer defines the specific tasks
   the AI performs (filtering, summarizing, recommending)**.

**Cost**:
1. Which factor can increase the cost of using a model? → **a larger
   context window**.
