---
type: Reference
title: "Generative AI Leader — Module 4 slide deck"
description: Transcription of the official Google Cloud Skills Boost slide deck for Module 4 of the Generative AI Leader (ILT) certification course.
tags: [source, google-cloud, generative-ai, certification]
resource: "Google Cloud Skills Boost — Generative AI Leader (ILT), Module 4: Gen AI Apps - Transform Your Work"
author: Google Cloud
fidelity: transcription
retrieved: 2026-09-02T18:55:15Z
generated: { by: claude-code/sonnet-5, at: 2026-09-02T18:55:15Z }
status: stable
---

<!--
Transcribed from a pdftotext -layout dump of the official PDF export. Slide
page-break markers and the repeated "Proprietary + Confidential" footer are
stripped; content order and wording otherwise follow the deck.
-->

# Module 4: Gen AI apps — Transform your work

Learning path position: 04 of 05 (Beyond the chatbot → Unlock foundational
concepts → Navigate the landscape → **Gen AI apps: Transform your work** →
Gen AI agents: Transform your organization).

## Module objectives

1. Explain prompt engineering techniques for better results.
2. Develop automated workflows with gen AI templates and tools.
3. Describe core functionality and business value of Google Workspace with
   Gemini.
4. Describe core functionality and business value of Gemini for Google Cloud.

Agenda: 01 Prompting techniques, 02 Gen AI for productivity, 03 Gemini for
Google Cloud.

## 01 Prompting techniques

### One-, zero-, and few-shot prompting

- **Zero-shot prompting**: asking a foundation model to complete a task with
  no examples.
- **One-shot prompting**: showing the foundation model one example, then
  allowing it to learn and apply that knowledge.
- **Few-shot prompting**: providing the foundation model with multiple
  examples to learn from.

Online clothing store example (Cymbal Retail):
- Zero-shot — input: "What is Cymbal Retail's returns policy?" Output: the
  LLM answers from general knowledge, with no company-specific training.
- One-shot — input: a single example of a customer inquiry (shipping times)
  paired with an ideal response, then a new query. Output follows the
  example's pattern.
- Few-shot — input: several example inquiry/response pairs (shipping,
  returns), then a new query. Output follows the examples' pattern more
  reliably than one-shot.

Demo/discussion prompt used: zero-shot ("Write a helpful and empathetic
response to a customer complaining about a delayed shipment") vs. few-shot
(two worked examples of empathetic delay responses, then a new delayed-order
case).

### Role prompting

- A technique used to guide the behavior of LLMs by assigning them a
  specific role or persona.
- Enables you to influence the style, tone, and focus of responses.
- Example 1 — prompt: "You are a customer service agent for a
  telecommunications company with ten years of experience. A customer is
  inquiring about their latest bill, which is higher than expected." Output:
  helpful, patient tone; explains possible reasons; offers solutions;
  states policy clearly.
- Example 2 — prompt: "You are a marketing copywriter for a new line of
  athletic wear. Write a product description for a pair of running shoes
  emphasizing their comfort and performance-enhancing features." Output:
  persuasive, audience-targeted copy, sometimes narrative/emotional framing.
- "Try it" template: "You are a [persona]. Please write a [fill in the
  blank]."

### Prompt chaining

- Like having a conversation with the AI where each response builds upon
  the previous one, leading to a more sophisticated and refined outcome.
- In Gemini: continue chats without repeating history; use the same thread;
  name and pin chats for easy access.
- Process: (1) Set a goal — think of a multi-step task or complex question
  (e.g., business proposal, trip itinerary, multi-element marketing image).
  (2) Start the chain — an initial prompt that sets the stage (e.g., "I need
  to plan a 5-day business trip to Tokyo in August... Can you help me create
  a preliminary itinerary?"). (3) Build the chain — follow-up prompts that
  refine the output (e.g., "Can you suggest hotels near the conference
  center...", "Can you also add day trips to nearby cities?"). (4) Observe
  and analyze — note how each prompt builds on the previous one toward a
  more comprehensive, nuanced result.
- Worked scenario: marketing manager first prompt asks for anti-aging
  organic-skincare campaign ideas; Gemini returns social/influencer/content
  ideas; the follow-up narrows to a 3-month content calendar (blog topics,
  social posts, email themes) aligned to the same audience.

### Reusing prompts

- Reusable prompt templates by role:
  - Marketing manager: "Write a catchy social media post for [platform]
    promoting our new [product/service]. Highlight [key features/benefits]
    and include a call to action to [desired action]."
  - Content writer: "Write a [content type: blog post, article, script]
    about [topic]. The target audience is [audience description]. The tone
    should be [tone: informative, humorous, persuasive]. Include
    [keywords]."
  - Customer support: "Respond to this customer email: [paste email
    content]. Be empathetic and address their concerns about [issue]. Offer
    a solution that aligns with our [company policy]."
  - Software developer: "Write Python code to [task]. Use
    [libraries/frameworks] and follow [coding style guidelines]."

### Grounding

- Grounding refers to the ability of the AI model to connect its output to
  verifiable and specific sources of information.

### Retrieval-augmented generation (RAG)

- Two-step process: (1) retrieving relevant information — the AI model
  retrieves relevant information from a vast knowledge base; (2) generating
  output — the model uses this retrieved information to generate the final
  output.
- Model only (without RAG): Prompt → Model → Output.
- Model with RAG: Prompt → Query → Vector DBs → Model → Output.
- Benefits of RAG:
  - Improved accuracy and relevance — produces more accurate and
    informative outputs.
  - Improved explainability and transparency — shows the specific sources
    used to generate the output.
  - Extending LLM capabilities — only generates a response based on the
    additional context it was provided.

### Quiz (Lesson 1)

1. Which prompting technique relies entirely on the foundation model's
   pre-existing knowledge, without any provided examples? A. One-shot B.
   Zero-shot C. Few-shot D. Multi-shot.
2. Language-learning app AI tutor — which role-prompt would be most
   effective? A. "You are a language model built to help students learn a
   new language." B. "You are a helpful and encouraging tutor who provides
   constructive feedback on language learning exercises." C. "Provide
   personalized feedback to students practicing conversational skills." D.
   "You are a robot programmed to assess language proficiency."
3. What is the primary function of RAG in AI models? A. Enhance the model's
   ability to memorize vast amounts of information. B. Enable the model to
   access and utilize external knowledge sources for generating outputs. C.
   Restrict the model's output to a predefined set of responses. D. Replace
   human intervention in the model's output generation process.

(The PDF text export does not preserve which option is marked correct on
the "Answer" slide graphically — only the question repeats.)

### Key takeaways (Lesson 1)

- Effective prompting optimizes AI outputs for complex tasks.
- Use role prompting, prompt chaining, and clear, reusable prompts for
  efficient, effective AI interaction.
- RAG lets AI access external data, improving output reliability and
  insight beyond memorized information.

## 02 Gen AI for productivity

### Explore and reflect (framing questions)

- Is this gen AI use case repeatable?
- Is gen AI falling short because it lacks customization?

### Google Workspace

- A collection of cloud-based productivity and collaboration tools: Gmail,
  Calendar, Drive, Meet, Chat, Docs, Sheets, Slides, Forms, Keep, Voice,
  Sites, Tasks, Apps Script, Admin.

### Google Workspace with Gemini

- **Gemini side panel** — found on the side of many Workspace apps;
  summarize, analyze, and generate content using insights gathered from
  emails, documents, etc., without switching applications/tabs. Example:
  new employees use the Drive side panel to get up to speed on projects.
- Per-app value:
  - **Gmail** — write and refine emails more efficiently. Example: an HR
    rep uses Gemini to draft a company-wide benefits-announcement email.
  - **Google Docs** — streamlines content creation, refining, and
    proofreading in-document. Example: a marketing team member generates
    taglines and social posts for a shoe campaign.
  - **Google Slides** — generates photorealistic images to enhance
    presentations. Example: "create an image of a modern office building."
  - **Google Sheets** — generates formulas using AI. Example: ask Gemini to
    "create a formula to find cell C1 in range D:G and output the value in
    column G."
  - **Google Meet** — real-time transcription and translation for
    multilingual meetings; automates meeting summaries and action items.
    Example: translate a meeting into Spanish in real time; summarize key
    points and action items.

### Taking enterprise Workspace farther

- **Google Vids** — an online video creation and editing app. Generate a
  first draft of a video; share project updates, timelines, and key
  insights.
- **AppSheet** — a no-code app development tool. Create an app structure
  with tables, columns, and links; review and edit the app structure.
- Use case referenced: Understood.org.

### Gemini Advanced

- Strengths: coding, logical reasoning, following nuanced instructions,
  creative collaboration, adjustable retention settings.
- Positioned as an upgrade tier from the base Gemini app.

### Saved Info

- Adjust Saved Info settings if you want the gen AI tool to remember
  context but not everything in the whole conversation history. Example: a
  sales rep practicing different pitches wants feedback not influenced by
  earlier practice sessions or past-client details — they can let Gemini
  know their role (sales rep) via Saved Info without carrying full history.

### Gems

- "Think of Gems as your personalized AI assistants within Gemini."
- AI assistants that process information and reason over complex ideas
  within the context of a chosen task.
- Automate repetitive workflows and tasks.
- Gemini offers pre-made and custom Gems. Examples: creative writing,
  coding, marketing.
- How Gems work:
  - **Personalized responses** — tailored instructions increase relevance
    to specific needs.
  - **Streamlined workflows** — templates, prompts, or instructions save
    time on repetitive activities.
  - **Reset context** — set context, then have separate, focused chats with
    a Gem; each chat remains isolated, like distinct expert conversations.
- Prompting info you can provide to a custom Gem: how to act/what to do,
  role-prompting, documents and resources, clear specific instructions,
  examples, refined instructions, user interaction considerations.
- Creating custom Gems: (1) identify a Gem to use as a base — consider
  functionality, license, simplicity (optional but recommended) — then make
  a copy.

### Gemini Notebook (NotebookLM)

- A personalized AI research partner. References provided source material
  and can answer any question about it.
- Helps you learn and understand information better by acting as a virtual
  research assistant.
- "Grounds" itself in specific sources; creates summaries.
- Organizational use patterns: sales notebook (product info, competitor
  analysis, market research), marketing notebook (blog posts, reports,
  webinars), training/onboarding notebook (training manuals, presentations,
  videos), development notebook (specs, design docs, feedback reports —
  with viewer/full-notebook/chat-only access levels and a welcome note),
  teaching/learning notebook (strategy plan, education standards, lecture
  notes, course readings — with Studio outputs: study guide, briefing doc,
  FAQ, timeline), customer support notebook (help center articles, product
  docs, FAQs — used as a group knowledge base/help center).
- Configure Chat: conversation style (Default, Analyst, Guide, Custom) and
  response length (Default, Longer, Shorter).
- Studio feature: Audio Overview — a "Deep Dive conversation" with two
  hosts (English only), with an Interactive mode to join and ask questions.
- Considerations before creating a notebook:
  - **Purpose and topic** — define the main goal; notebooks function
    independently.
  - **Collaboration and access** — Viewer or Editor roles; sharing a
    notebook does not share the underlying source file; chat-only mode
    hides the sources.
  - **Sources handling and sync** — size and usage limits; must manually
    re-sync out-of-date sources; data is not used to train models.
- Source upload types: Google Docs, Google Slides, YouTube videos,
  websites, audio files, PDF files, text files. Notebook cannot delete or
  edit your original files — it extracts text from files, saving a local
  copy.
- Use cases: create training materials, research a new topic, learn by
  listening to audio, build a shared knowledge base for a team, prepare for
  a presentation, develop documentation, create project proposals and
  plans, quickly find answers to customer questions.
- Example: writing a research paper — upload relevant documents, then ask
  it to summarize key findings per source, identify connections/
  contradictions between perspectives, generate outlines/drafts, and answer
  specific questions.
- Benefits vs. Gemini/Gems:
  - **Hyper-focused knowledge** — focuses solely on the sources you
    provide.
  - **Interactive learning** — encourages active learning via questions,
    summaries, and quizzes.
  - **Source-based answers** — every answer/insight is directly grounded in
    your uploaded sources.
- Versions:
  - **Gemini Notebook Pro** — enhanced research, increased capacity,
    customization of response length/style, usage analytics.
  - **Gemini Notebook Enterprise** — enhanced version of Pro; compliance
    and administrative features; extra privacy/security features;
    information shared only with chosen collaborators; access managed with
    IAM.
- Summary: centralizing resources in a shared notebook lets a team ask
  questions and gain deeper shared understanding, generate collaborative
  summaries/reports, identify connections/contradictions across
  perspectives more easily, and stay current with the latest information.

### "Pick-a-product" matching activity (product distinctions)

- Allows you to create your own custom versions of Gemini → **Gems**.
- Lets you personalize an AI assistant for repeatable tasks or specific
  interaction styles → **Gems**.
- Acts as an AI research assistant grounded only in the documents/sources
  you provide, and does not use general web knowledge for its answers →
  **Gemini Notebook**.
- Helps you write, summarize, and brainstorm directly within Docs, Gmail,
  and Sheets; acts as a collaborative partner integrated into everyday
  productivity apps → **Google Workspace with Gemini**.
- Gives priority access to the latest experimental AI features/models from
  Google; excels at highly complex tasks like coding, logical reasoning,
  and creative collaboration → **Gemini Advanced**.

### Quiz (Lesson 2)

1. Which two statements are true? A. Grounding allows an AI model to
   connect its responses to specific sources of information. B. Gemini
   Notebook can access and use information from the entire internet. C. You
   can use Gemini Notebook to create quizzes based on your uploaded
   documents. D. Gemini Notebook is best suited for tasks like writing
   creative stories or poems. E. Grounding is a feature exclusive to Gemini
   Notebook.
2. Virtual team meeting in Google Meet, attendees struggling with language
   barriers — how can Gemini help? A. Automatically adjust each speaker's
   volume. B. Provide translated summaries in the meeting chat. C. Generate
   live translated captions with speaker identification. D. Automatically
   summarize the discussion for those who missed the meeting.
3. Freelance writer switching between content types/tones, wants
   consistency across formats — which Gemini feature best suits this? A.
   Gems B. Gemini saved info C. Gemini for Google Cloud D. Gemini Deep
   Research.
4. Product manager preparing for a launch meeting with market research,
   competitor analysis, and customer feedback in Drive — how can Gemini
   Notebook help? A. Automatically generate a presentation with slides and
   talking points. B. Predict questions the team will ask based on
   personalities and prepare answers. C. Summarize key findings, identify
   potential challenges, and provide talking points for discussion. D.
   Automatically send calendar invites with a suggested agenda.

(As above, the correct option isn't recoverable from the text layer alone.)

### Key takeaways (Lesson 2)

- Diverse capabilities of Google Workspace with Gemini can enhance
  productivity to drive impactful outcomes.
- Gemini Notebook analyzes your uploaded sources and provides accurate and
  traceable summaries and answers.

## 03 Gemini for Google Cloud

### Tool integration

- **Gemini Cloud Assist** — helps design, manage, and optimize applications
  on Google Cloud; provides personalized guidance and application
  lifecycle management assistance; analyzes your cloud environment,
  deployed resources, metrics, and logs.
- **Gemini in BigQuery** — makes data analysis easier and more accessible;
  helps write code, understand your data, and generate insights
  automatically.
- **Gemini Code Assist** — acts as an AI pair programmer; provides code
  suggestions, generates code blocks, and offers explanations; supports
  20+ popular programming languages, code editors, and developer
  platforms.
- **Gemini in Colab Enterprise** — brings AI assistance to your notebooks;
  helps write Python code by suggesting code segments; generates code
  based on your descriptions.
- **Gemini in Databases** — helps developers and database administrators
  manage databases more effectively; uses AI to simplify many aspects of
  using a database.
- **Gemini in Looker** — helps you analyze data and gain insights; helps
  you understand your data, create visualizations, and generate reports.
- **Gemini in Security** (Security Command Center) — helps security teams
  detect, contain, and stop threats from spreading; provides near-instant
  analysis of security findings and potential attack paths; summarizes
  prevalent tactics, techniques, and procedures used by threat actors.
- Enterprise security: Gemini for Google Cloud prompts and responses aren't
  used for training, and standard Google Cloud protections are applied.
- Use case referenced: "Gemini in action" (unnamed case study).

### Quiz (Lesson 3)

1. A team of developers wants to improve coding efficiency and
   collaboration — which Gemini for Google Cloud tool is most beneficial?
   A. Gemini Cloud Assist B. Gemini Code Assist C. Gemini in Databases D.
   Gemini in Security Command Center.

### Key takeaways (Lesson 3)

- Gemini in Google Cloud streamlines data and code, enhancing services for
  productivity and innovation across platforms.

## Module 4 wrap-up quiz

1. What is the main advantage of using role prompting? A. It allows the AI
   model to learn from a few examples. B. It improves the AI model's
   ability to understand complex questions. C. It influences the style,
   tone, and focus of the AI's responses by assigning it a specific
   persona. D. It enables complex tasks like planning a business trip
   itinerary.
2. A sales rep is using gemini.google.com to practice different sales
   pitches and wants feedback tailored to each pitch without interference
   from previous sessions — what's the most suitable approach? A. Use
   prompt chaining. B. Enable saved info. C. Use a Gem.

## Additional resources (as listed in the deck)

- Lesson 01: Google Workspace with Gemini.
- Lesson 02: Upgrade to Gemini Advanced; Get started with Gems in Gemini
  Apps; Semantic search; Vector databases; What is Gemini Notebook
  Enterprise?
- Lesson 03: Creating trust through transparency.
