---
type: Reference
resource: "Google Cloud Skills Boost — Generative AI Leader (ILT), Module 5: Gen AI Agents - Transform Your Organization, and Course Summary"
author: Google Cloud
fidelity: transcription
retrieved: 2026-09-02T18:55:15Z
---

# Module 05 — Gen AI agents: Transform your organization

Module objectives:
1. Define gen AI agent components and how they work together.
2. Explain how to combine components of gen AI agents to build powerful solutions.
3. Describe how to create gen AI agents and solutions using Google Cloud's gen AI products.
4. Explain how to effectively lead organizational transformation with gen AI.

Agenda: 01 Today's agents · 02 Building agents · 03 Enhancing the customer experience with agents

## 01 Today's agents

### A brief history of agents

**Deterministic (traditional)**
- Based on predefined paths and actions.
- Workflow-based and event-driven.
- Offers a high degree of control and predictability.
- The same input will always provide the same output.
- Includes: Reasoning loop + tools (no foundation model!)

**Generative**
- Allows for much more natural and flexible conversations.
- Might give different answers to the same input.
- Includes: Reasoning loop + tools + foundation model.
- RAG enables integration from external sources.
- Hybrid agents (combine both).

### Components of a generative AI agent

- **Foundation model** — the underlying LLM that powers the agent. Select a model with training data relevant to the agent's intended use case.
- **Tools** — allow the agent to observe the world and act upon it (enable interaction). Examples: extensions that connect to APIs, functions that act as mock API calls, and data stores.
- **Reasoning loop** — the core of the agent, responsible for making decisions and taking actions. An iterative process where the agent considers its goal, the available tools, and the information it has gathered. Frameworks guide the reasoning process.

**Key takeaway:** Generative AI agents evolved from inflexible deterministic types by adding natural language understanding. They use foundation models, tools for interaction, and a reasoning loop.

## 02 Building agents

### Using models — sampling parameters and settings

- **Token count** — tokens are groups of characters (1 token ≈ 4 characters). Models have limits on how many tokens they can handle at once.
- **Temperature** — controls the "creativity" of the model by adjusting randomness of word choices during text generation. Influences diversity/unpredictability of output.
- **Top K** — lets the model randomly return a word from the top K most probable words.
- **Top P (nucleus sampling)** — the cumulative probability of the most likely tokens considered during text generation.
- **Safety settings** — filter out potentially harmful or inappropriate content from the model's output.
- **Output length** — determines the maximum length of the generated text.

By experimenting with these parameters, you can significantly influence the AI model's behavior. Accessing/changing model settings varies by model source and access method, often done via APIs.

### Google gen AI tools

- **Google AI Studio** — web-based tool for developers, students, researchers to try Gemini models and start building with the Gemini Developer API. Designed for ease of use/accessibility. Simpler interface, usage limits, better suited for prototyping with a standard Google account.
- **Agent Studio** — Google Cloud console tool for rapidly prototyping/testing generative AI models. Respects Google Cloud policies (governance/security). Developers can test models with prompt samples, design/save prompts, tune foundation models. Part of Agent Platform — a comprehensive platform for professionals to build, train, deploy ML models at scale. Enterprise-grade security, flexible quotas, incurs service charges. Easy integration with other tools; grounding for better accuracy.

Demo referenced: aistudio.google.com — "Parameter playground."

### Adding prompt engineering to your reasoning loops

**The reasoning loop:**
- Iterative process — agent continuously evaluates progress and determines the next best action.
- Internal reasoning — agent uses its underlying LM to think through the steps needed to complete a task.
- Decision making — based on internal reasoning, agent decides the next course of action (choosing tools, determining inputs).
- Reasoning frameworks — reasoning loop utilizes prompt engineering frameworks/techniques to guide reasoning and planning.

**Chain-of-thought (CoT)**
- A technique where you guide an LLM through a problem-solving process by providing examples with intermediate reasoning steps.
- Instead of just prompting and expecting an answer, you guide it through the reasoning process; the intermediate steps are the "chain of thought."
- Ways to implement CoT:
  - *Self-consistency* — encouraging the LLM to generate multiple solutions and choose the most consistent one.
  - *Active-prompting* — allowing the LLM to ask clarifying questions or request additional information.
  - *Multimodal CoT* — combining text with other data forms (images, videos) to enhance reasoning.
- Why CoT is important: improved reasoning (solve complex problems requiring logical thinking), better accuracy (breaking problems into smaller steps), enhanced explainability (easier to see how the LLM arrived at an answer, builds trust).
- CoT in action: complex reasoning tasks, explanation generation, multi-step planning.

**ReAct (Reason and Act)**
- A prompting framework that allows the LLM to reason and take action on a user query, with or without in-context examples. Lets the LLM interact with the real world and gather information.
- "Thought-action-observation" loop: **Think** (LLM generates a thought about the problem) → **Act** (LLM decides what action to take and specifies the input) → **Observe** (LLM receives feedback from the action) → **Respond** (LLM generates a response) — repeats/iterates as needed.
- Why ReAct is important: dynamic problem solving (LLMs tackle complex tasks requiring interaction with external resources and adapting to new info), reduced hallucination (grounding reduces risk of incorrect/nonsensical info), increased trustworthiness (reasoning process and external interactions are visible/transparent).
- ReAct in action: question answering, fact verification, decision making.
- **CoT vs ReAct**: CoT focuses on internal reasoning, while ReAct enables external interaction. The two techniques can be combined for deeper reasoning and dynamic action.

Activity scenarios (ReAct vs CoT): "find a restaurant near current location" → ReAct (needs external info); "summarize an article" → CoT (understanding/distilling); "brainstorm product ideas" → CoT (creative ideation); "search for research papers on a topic" → ReAct (needs external/academic database interaction).

### Adding tooling

**Types of agent tools:**
- **Extensions (APIs)** — sets of rules governing how software interacts. Standardize agent interaction with external APIs, simplifying access to services/data despite varying API designs.
- **Functions** — specialized, reusable actions within an agent's toolbox. The reasoning system selects the appropriate function for the task.
- **Data stores** — give agents access to real-time, historical, and knowledge-based information, ensuring accurate/relevant responses.
- **Plugins** — add new skills and integrations, extending an agent's capabilities by connecting it to services/specialized tools or enabling interaction with other platforms.

**How the reasoning loop works with tools** (4-step cycle):
1. Reasoning (tool selection) — agent analyzes the task and determines which tools are needed.
2. Acting (tool execution) — agent executes the selected tool.
3. Observation — agent receives the output from the tool.
4. Iteration (dynamic iteration) — agent reasons about the next steps.

Example — scheduling a garden consultation: agent needs a time slot → uses scheduling plugin to check availability + accesses customer DB → plugin returns available slots → agent presents slots to client.

**Google's tooling — key Google Cloud tools for agents:**
- Cloud Storage — highly scalable/durable object storage service.
- Databases (Cloud SQL, Spanner, Firestore) — store/retrieve data the agent needs; manage user data or track its own progress.
- Cloud Run functions — serverless functions acting as specialized tools for your agent; easily triggered, scale automatically.
- Cloud Run — serverless platform for deploying/running stateless containers; ideal for custom tools with specific dependencies/more control.
- Agent Platform — create models or agents that are themselves called as tooling by other agents.

**Google's tooling — pre-built AI APIs:**
- Speech-to-Text API — converts speech into text; transcribes meetings, calls, video content.
- Text-to-Speech API — converts text into natural-sounding speech; voice UIs, personalized communication.
- Translation API — translates text, documents, websites, audio/video files.
- Document Translation API — translates formatted documents while keeping original layout.
- Document AI API — extracts data from various document formats; automates data capture/document processing; summarizes documents.
- Cloud Vision API — understands image content; image tagging, content moderation, visual search.
- Cloud Video Intelligence API — analyzes video content, extracts meaningful info; content recommendation, video search, media analysis.
- Natural Language API — derives insights from unstructured text; sentiment, content classification, entity extraction.
- Google Cloud also offers a vast API Library linked to other Google products (Google Maps, Workspace, YouTube, Google Photos, etc.).

Activity example — meeting location planner: Document AI API (extract addresses from uploaded doc) → Google Maps Geocoding API (convert addresses to lat/long, calculate distances/travel times) → Location analysis via custom logic in a Cloud Run function (determine suggested location).

Quiz recap: Extensions = connect to external services via APIs; Functions = define specific actions/tasks; Data stores = provide access to information; Plugins = add new skills/integrations.

### Building applications from your agents

**Integrating APIs into applications (2 steps):**
1. Generate an API key or set up authentication for secure access — obtain credentials for your application to securely access/communicate with the Gemini API.
2. Start making API calls from your application code — API calls send prompts and parameters to the Gemini model and receive generated text in response.

- Using the API: enable API access via Agent Studio or Google AI Studio (follow each tool's directions).
- Using the API: leverage your agent within applications via **Cloud Run functions** (small pieces of code triggered by specific events; process events using your AI Studio API; no server management) or **Cloud Run** (run containerized applications; easy to deploy/scale; useful for complex apps needing specific software/config).
- Gemini API integrates into any application supporting HTTP requests — web, mobile, desktop, embedded systems.
- Low-code/no-code tooling: **Apps Script** — low-code platform, automates Google Workspace with JavaScript/built-in services, uses Gemini APIs to create gen AI add-ons for Workspace. **AppSheet** — no-code platform for building custom business apps; uses AppSheet + Gemini API for automation/intelligent features.

**Multi-agent applications:**
- Systems that use multiple agents, each specialized for a specific task.
- Agents can work independently or interact with each other.
- Improves efficiency, allows greater flexibility and scalability.
- An agent itself can be a tool within another agent.

**Key takeaways:**
- Generative AI learns patterns to create text; Agent Studio and Google AI Studio allow parameter adjustments for customized application integration.
- The reasoning loop processes information for AI agent decisions; prompt engineering enhances reasoning for improved interactions.
- Agent tooling enables AI to perform actions; equip AI agents with tools for complex tasks and intelligent interaction.
- Integrate generative AI via various tools; multi-agent systems enhance efficiency for diverse applications.

## 03 Enhancing the customer experience with agents

### Retrieval-augmented generation (RAG) and tooling

**How the model works with RAG (3 stages + iteration):**
1. **Retrieval** — the LLM, equipped with retrieval tools, identifies relevant info from external sources. Tools can include: data stores, vector databases, search engines, knowledge graphs.
2. **Augmentation** — retrieved information is incorporated ("augmented") into the prompt fed to the LLM; the augmented prompt contains the user's original query plus relevant retrieved context.
3. **Generation** — the LLM processes the augmented prompt and generates a response.
- Note: in some RAG systems the LLM iterates on the retrieval process, continuously improving response quality/relevance.

Example — "What were the main developments at the recent climate conference in Dubai?": query → LLM queries a vector database and search engine (retrieval) → combines query with retrieved info (augmentation) → generates a response summarizing developments, citing sources (generation) → may iterate with different search terms/other data sources.

**Data stores** in AI applications act as structured and unstructured knowledge bases the agent draws upon: websites, structured databases, unstructured data.

Quiz recap: Retrieval = fetching relevant documents from a knowledge base based on user query; Augmentation = adding context to the query from the knowledge base; Generation = creating the natural-language response.

### The power of search agents

**Agent Platform: search solutions**
- Document search — search across a large repository of unstructured documents stored in Google Cloud Storage.
- Media search — use with rich media libraries; understands and searches images, videos, audio files.
- Healthcare search — enables searching across healthcare data while supporting regulatory compliance.
- Search for commerce — focuses on building a search app for your retail catalog.

**Agent Platform: recommendations solutions**
- Media recommendations — tailored for consumer-focused media applications (audio/video streaming, digital publishing).
- Search for commerce — optimized for e-commerce, drives sales via personalized product recommendations.

**How Agent Search works:**
- Uses intelligent data connection and generative AI; acts as an agent, retrieving/recommending information from diverse data stores based on context.
- Key strength: grounds gen AI LLM responses with your first-party data, curated third-party data, and Google's knowledge graph (RAG approach).

**Agent Search: extra generative AI features**
- Search summaries — generates concise, tailored summaries of search results, saving user time.
- Answers and follow-ups — adds AI-generated answers to search results; users can ask questions in natural language.

Agent Search offers secure, scalable search with advanced analytics and easy API/SDK integration for enterprises of all sizes.

Use case referenced: enhancing the shopping experience with Agent Search.

### Customer engagement

**Gemini Enterprise for CX** — three components:
- Customer Experience agents — act as effective chatbots communicating with customers.
- Agent Assist — supports live human contact-center agents.
- Customer Experience Insights — gain insights into all communications with customers.

**Customer Experience agents — three types:**
1. Deterministic — follow explicitly defined rules and logic; requires low-to-medium code for all actions.
2. Generative — use LLMs for natural conversation; determine actions based on prompts with minimal-to-no code.
3. Hybrid — CX Agent Studio enables hybrid agents, combining deterministic control with generative AI flexibility for improved customer service.

Use case referenced: Cymbal Taxes' Agentic Tax Assistant.

**Agent Assist** — supports live agents with real-time AI help: generated responses, knowledge base suggestions, transcription, translation, summaries for faster/more accurate resolutions.

**Customer Experience Insights (CX Insights)** — analyzes customer interactions to boost efficiency and improve agent performance. Generative FAQ identifies common questions and response effectiveness, highlighting areas for improvement.

**Contact Center as a Service (CCaaS)** — simplifies complex contact centers with 24/7 omnichannel support, CRM integration, and infrastructure management. Handles multichannel communication, integrates with agent/insight tools, lets businesses focus on customer experience.

Product-matching recap (activity): Agent Search = delivers search over org data, specialized tuning for retail/media/healthcare; Agent Assist = guidance/suggestions to human contact-center agents during live calls, improves efficiency/consistency/first-call resolution; Recommendations = personalized product/content suggestions, increases engagement/discovery; CX Agent Studio = design/build/deploy AI-powered chatbots and voice bots, understands user intent and extracts key info.

### Gemini Enterprise app

Gemini Enterprise app creates AI-powered, customized agents that access and understand company data from any source, integrating into internal systems to act as personal work research assistants.

**Launch point for enterprise-ready agents:**
- Connect to Gemini Notebook Enterprise — employees upload information to analyze, get insights, listen to audio summaries of data.
- Connect to multimodal search agents — grounded in your data across multiple systems so employees can find relevant information within the company.
- Add generative AI assistants — grounded in enterprise data, can be prompted to take actions through connectors (tools).
- Add custom agents — through CX Agent Studio.

### Strategy: Planning ahead

**Plan for generative AI integration (6 steps):**
1. Establish a clear vision — align gen AI with strategy, secure leadership buy-in, appoint an adoption champion.
2. Prioritize high-impact use cases — align gen AI opportunities with business goals, considering feasibility and transformation potential.
3. Invest in capabilities — develop gen AI skills via training/recruitment, foster a learning/experimentation culture.
4. Drive organizational change — manage gen AI workflow shifts, encourage agile collaboration and knowledge sharing for scaling.
5. Measure and demonstrate value — track gen AI impact with data to continuously improve and demonstrate value.
6. Champion responsible AI — implement a robust responsible AI framework ensuring fairness, transparency, privacy, security.

**Plan for impact (3 steps):**
1. Define key metrics — identify metrics most relevant to your goals/business objectives.
2. Collect and analyze data — set up tracking mechanisms, conduct surveys, or analyze existing data to understand impact of gen AI initiatives.
3. Iterate and improve — use insights from data analysis to refine your gen AI strategy and optimize performance.

**Plan for change (5 practices):** regularly review and refine your strategy · stay informed · engage with the generative AI community · invest in training and development · attract and retain top talent.

**Key takeaways:**
- Data stores are key for reliable AI agents, managing knowledge for accurate/relevant responses using RAG.
- Integrating Agent Search empowers customers to find/understand information faster for better decisions and efficiency.
- Gemini Enterprise for Customer Experience offers powerful agents using generative AI and other tech for seamless customer experiences.
- Gemini Enterprise app is a central, secure platform for customized AI work assistants, enhancing productivity across business teams.

## Module 05 closing

Module objectives recap (same 4 as opening). Additional resources listed: comparison of Agent Studio and Google AI Studio, "Takeaway try it" activities (parameter playground, RAG in action, build your own agent), API Library, "Send text prompts to Gemini using Agent Studio," "Generate an API key," course study guide.

---

# Course summary (closing material, all 5 modules)

## Course objectives (recap)
1. Discover the business value and impact of Gen AI on your organization.
2. Define core gen AI concepts.
3. Identify the core layers of the gen AI landscape.
4. Explain how to combine components of gen AI agents to build powerful solutions.
5. Identify Google Cloud's gen AI implementation and scaling solutions.

## Module recap (titles + sub-topics as presented in closing deck)
- **Module 01 — Gen AI: Beyond the chatbot**: (1) Introduction to gen AI for businesses, (2) Introduction to gen AI foundations, (3) Gen AI strategy.
- **Module 02 — Gen AI: Unlock foundational concepts**: (1) Core gen AI concepts, (2) Foundation models, (3) Building AI securely and responsibly.
- **Module 03 — Gen AI: Navigate the landscape**: (1) The gen AI landscape, (2) Gen AI agents and applications, (3) Gen AI platform, model, and infrastructure, (4) Gen AI project resources and management.
- **Module 04 — Gen AI apps: Transform your work**: (1) Prompting techniques, (2) Gen AI for productivity, (3) Gemini for Google Cloud.
- **Module 05 — Gen AI agents: Transform your organization**: (1) Today's agents, (2) Building agents, (3) Enhancing the customer experience with agents.

## Generative AI Leader certification exam

> A Google Cloud Certified Generative AI Leader is a visionary professional with comprehensive business knowledge of how generative AI can transform businesses using Google Cloud's gen AI products and services. They understand Google's AI-first approach and can drive innovative and responsible AI adoption by identifying use cases, fostering collaboration across technical and non-technical teams, and leveraging Google Cloud's enterprise offerings.

- **Length:** 90 minutes.
- **Exam format:** 50–60 multiple choice questions.
- **More info:** cloud.google.com/learn/certification/generative-ai-leader

## What's next

**Prepare for the certification exam:**
- Use resources/information from cloud.google.com/learn/certification/generative-ai-leader
- Access the course study guide.
- Revisit the Generative AI Leader material from this ILT course, or the on-demand format: skills.google/paths/1951

**Continue your learning journey:**
- Explore more/go deeper with other learning paths and courses: skills.google
- Hands-on: Intermediate — Generative AI Labs with Gemini on Google Cloud: skills.google/paths/1872
- Improve productivity: Google Workspace with Gemini: skills.google/paths/249
