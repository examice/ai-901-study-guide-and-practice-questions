# AI-901 study guide and practice questions

Exam AI-901, Microsoft Azure AI Fundamentals, is for people at the start of a career in AI solution development who know basic Python and have used Azure. It tests AI concepts and responsible AI, and it asks you to build small apps and a single agent with Microsoft Foundry. Passing it earns the Microsoft Certified: Azure AI Fundamentals certification; AI-901 replaced AI-900 as the exam for that certification on June 30, 2026. This repository holds a study guide built on the official skills outline, a three week study plan, a cheat sheet, links to free Microsoft resources, and 15 original practice questions with explained answers.

> Unofficial study notes by [Examice](https://examice.com/exams/microsoft/ai-901?utm_source=github&utm_medium=social&utm_campaign=ai-901-study-guide-and-practice-questions&utm_content=link_1). Not affiliated with or endorsed by Microsoft. The practice questions are original, written for this guide, and not taken from the exam.

## Contents

- [Exam at a glance](#exam-at-a-glance)
- [What the exam covers](#what-the-exam-covers)
- [Study plan](#study-plan)
- [Cheat sheet](#cheat-sheet)
- [Free official resources](#free-official-resources)
- [Practice questions](#practice-questions)
- [Exam day tips](#exam-day-tips)
- [FAQ](#faq)
- [Contributing](#contributing)
- [License](#license)

## Exam at a glance

| Item | Official detail |
| --- | --- |
| Exam | AI-901: Microsoft Azure AI Fundamentals |
| Certification earned | Microsoft Certified: Azure AI Fundamentals |
| Level | Fundamentals |
| Expected background | Conceptual knowledge of AI solutions in Azure, Python syntax and programming techniques, and familiarity with Azure resources |
| Time to complete | 45 minutes, the exam time Microsoft sets for fundamentals exams; plan for 65 minutes of seat time |
| Passing score | 700 on a scaled range of 1–1,000 |
| Price | $99 in the United States; the price depends on the country or region where you take the exam |
| Languages | English, Arabic (Saudi Arabia), Chinese (Simplified), Chinese (Traditional), French, German, Indonesian (Indonesia), Italian, Japanese, Korean, Portuguese (Brazil), Russian, and Spanish |
| Skills outline | Version dated April 15, 2026 |
| Retirement date | None listed |
| Renewal | Not needed: fundamentals certifications don't expire |
| Retakes | Wait 24 hours after a first failed attempt, then 14 days between later attempts, with at most 5 attempts in 12 months |
| Replaces | AI-900, retired on June 30, 2026; the certification kept its name |

Sources: the [AI-901 exam page](https://learn.microsoft.com/en-us/credentials/certifications/exams/ai-901/), the [AI-901 study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/ai-901), the [Azure AI Fundamentals certification page](https://learn.microsoft.com/en-us/credentials/certifications/azure-ai-fundamentals/), the [AI-900 exam page](https://learn.microsoft.com/en-us/credentials/certifications/exams/ai-900/), [exam duration](https://learn.microsoft.com/en-us/credentials/support/exam-duration-exam-experience), [exam scoring](https://learn.microsoft.com/en-us/credentials/certifications/exam-scoring-reports), the [retake policy](https://learn.microsoft.com/en-us/credentials/support/retake-policy), [certification renewal](https://learn.microsoft.com/en-us/credentials/certifications/renew-your-microsoft-certification), and Microsoft's [June 2026 credentials roundup](https://techcommunity.microsoft.com/blog/skills-hub-blog/microsoft-credentials-roundup-june-2026/4528350), checked October 28, 2026. The price is the US figure on the exam page; pick your country there to see yours.

## What the exam covers

| Domain | Weight |
| --- | --- |
| [Identify AI concepts and capabilities](#identify-ai-concepts-and-capabilities-4045) | 40–45% |
| [Implement AI solutions by using Microsoft Foundry](#implement-ai-solutions-by-using-microsoft-foundry-5560) | 55–60% |

The weights come from the [study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/ai-901). It says most questions cover generally available features and that you should be familiar with REST APIs, SDKs, and CLIs. The short description on the exam card still lists machine learning on Azure, but that line is the old AI-900 text: the AI-901 skills outline has no machine learning section.

### Identify AI concepts and capabilities (40–45%)

- **Describe principles of responsible AI.** Know the six principles (fairness, reliability and safety, privacy and security, inclusiveness, transparency, and accountability) and what each one asks of a real solution. Docs: [What is responsible AI](https://learn.microsoft.com/en-us/azure/machine-learning/concept-responsible-ai), [Responsible AI unit](https://learn.microsoft.com/en-us/training/modules/get-started-ai-fundamentals/7-responsible-ai).
- **Identify AI model components and configurations.** Explain how a generative model works (tokens, embeddings, transformers, predicting the next token), choose a model by what it can do, and recognize deployment options and parameters such as temperature, top_p, and the token limit. Docs: [Large language models unit](https://learn.microsoft.com/en-us/training/modules/fundamentals-generative-ai/3-language-models), [Foundry Models overview](https://learn.microsoft.com/en-us/azure/foundry/concepts/foundry-models-overview), [Deployment types](https://learn.microsoft.com/en-us/azure/foundry/foundry-models/concepts/deployment-types), [Prompt engineering](https://learn.microsoft.com/en-us/azure/foundry/openai/concepts/prompt-engineering).
- **Identify AI workloads.** Match a scenario to generative and agentic AI, text analysis, speech, computer vision, or information extraction. Know the text techniques (key term extraction, entity detection, sentiment analysis, and summarization), speech recognition and synthesis, the vision tasks and image generation, and how information comes out of text, images, audio, and video. Docs: [Introduction to natural language processing concepts](https://learn.microsoft.com/en-us/training/modules/introduction-language/), [Introduction to AI speech concepts](https://learn.microsoft.com/en-us/training/modules/introduction-ai-speech/), [Introduction to computer vision concepts](https://learn.microsoft.com/en-us/training/modules/introduction-computer-vision/), [Introduction to information extraction concepts](https://learn.microsoft.com/en-us/training/modules/introduction-information-extraction/).

### Implement AI solutions by using Microsoft Foundry (55–60%)

- **Generative AI apps and agents.** Write system and user prompts, deploy a model and chat with it in the Foundry portal, build a small chat client with the Foundry SDK, create and test one agent in the portal, and write a small client app that calls the agent. Docs: [Foundry SDK quickstart](https://learn.microsoft.com/en-us/azure/foundry/quickstarts/get-started-code), [Create a prompt agent](https://learn.microsoft.com/en-us/azure/foundry/agents/quickstarts/prompt-agent), [Playgrounds](https://learn.microsoft.com/en-us/azure/foundry/concepts/concept-playgrounds), [System message design](https://learn.microsoft.com/en-us/azure/foundry/openai/concepts/advanced-prompt-engineering).
- **Text and speech.** Build a small app with text analysis, answer spoken prompts with a deployed multimodal model, and build a small app with Azure Speech in Foundry Tools. Docs: [Azure Language overview](https://learn.microsoft.com/en-us/azure/ai-services/language-service/overview), [Azure Speech overview](https://learn.microsoft.com/en-us/azure/ai-services/speech-service/overview), [Text to speech](https://learn.microsoft.com/en-us/azure/ai-services/speech-service/text-to-speech).
- **Computer vision and image generation.** Send images in prompts to a multimodal model, create new images with a generative model, and build a small app with vision features. Docs: [Images in chat prompts](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/gpt-with-vision), [Image generation](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/dall-e).
- **Information extraction.** Use Azure Content Understanding in Foundry Tools to pull information from documents and forms, images, audio, and video, and build a small app around it. Docs: [Content Understanding overview](https://learn.microsoft.com/en-us/azure/ai-services/content-understanding/overview), [Prebuilt analyzers](https://learn.microsoft.com/en-us/azure/ai-services/content-understanding/concepts/prebuilt-analyzers), [Audio analyzers](https://learn.microsoft.com/en-us/azure/ai-services/content-understanding/audio/overview).

## Study plan

The plan assumes about 5 hours a week for three weeks. The two learning paths behind the course AI-901T00 take about 9.5 hours by Microsoft's estimates (568 minutes). You need an Azure subscription for the exercises in the second path.

| Week | Focus | Tasks | Hours |
| --- | --- | --- | --- |
| 1 | AI concepts | Complete [AI concepts for developers and technology professionals](https://learn.microsoft.com/en-us/training/paths/ai-concepts/) (7 modules). Write one example scenario for each responsible AI principle and learn the terms in the cheat sheet. | 5 |
| 2 | Foundry basics | Do the first two modules of [Get started with AI applications and agents on Azure](https://learn.microsoft.com/en-us/training/paths/get-started-ai-apps-agents/). Create a Foundry resource and project, deploy a model, try the same prompt with different system messages and temperatures in the playground, call the deployment from Python with the Foundry SDK, and create one agent with file search. | 5 |
| 3 | Text, speech, vision, extraction, and review | Finish the path. Try PII detection in Azure Language, a text to speech voice with SSML, an image in a chat prompt, image generation, and a Content Understanding analyzer on a document and an audio file. Take the free practice assessment and work through [practice-questions.md](practice-questions.md). | 5 |

## Cheat sheet

### AI concepts and capabilities

**Responsible AI principles** ([What is responsible AI](https://learn.microsoft.com/en-us/azure/machine-learning/concept-responsible-ai), [Responsible AI unit](https://learn.microsoft.com/en-us/training/modules/get-started-ai-fundamentals/7-responsible-ai))

| Principle | What it asks | Example |
| --- | --- | --- |
| Fairness | Similar people get similar outcomes; reduce bias in data and testing | A loan model treats equally qualified applicants the same across groups |
| Reliability and safety | The system works as designed, handles unexpected conditions safely, and resists manipulation | Testing a triage assistant with unusual inputs before launch |
| Privacy and security | Personal and business data stays protected, and the model can't be used to reveal it | Redacting personal data from transcripts before storage |
| Inclusiveness | Nobody is shut out of the benefits | Captions and screen reader support in an AI app |
| Transparency | People understand how the system works, how it reaches decisions, and its limits | Telling an applicant which factors led to a decision |
| Accountability | The people and organizations behind the system answer for it, with governance and human control | A named team owns the system and a person signs off on its decisions |

**Generative AI terms**

| Term | Meaning | Source |
| --- | --- | --- |
| Token | The unit a model reads and writes: a word, part of a word, or punctuation | [LLM unit](https://learn.microsoft.com/en-us/training/modules/fundamentals-generative-ai/3-language-models) |
| Embedding | A vector of numbers that captures meaning; similar text produces nearby vectors | [Embeddings](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/embeddings) |
| Transformer | The model architecture that uses attention to relate tokens; the decoder predicts the next most probable token | [LLM unit](https://learn.microsoft.com/en-us/training/modules/fundamentals-generative-ai/3-language-models) |
| System message | Instructions that set the assistant's role, boundaries, tone, and output format | [System message design](https://learn.microsoft.com/en-us/azure/foundry/openai/concepts/advanced-prompt-engineering) |
| User message | The request the user sends on each turn | [System message design](https://learn.microsoft.com/en-us/azure/foundry/openai/concepts/advanced-prompt-engineering) |
| Temperature | 0 to 2; lower gives focused, repeatable output and higher gives more varied output | [Prompt engineering](https://learn.microsoft.com/en-us/azure/foundry/openai/concepts/prompt-engineering) |
| top_p | Another randomness control; change it or temperature, not both | [Prompt engineering](https://learn.microsoft.com/en-us/azure/foundry/openai/concepts/prompt-engineering) |
| RAG | Retrieve relevant data, add it to the prompt as grounding, and generate an answer that can cite it | [RAG in Foundry](https://learn.microsoft.com/en-us/azure/foundry/concepts/retrieval-augmented-generation) |
| Agent | A model paired with instructions and tools that can reason over a request and take action | [What is Microsoft Foundry](https://learn.microsoft.com/en-us/azure/foundry/what-is-foundry) |

**Which model for which job** ([Foundry Models overview](https://learn.microsoft.com/en-us/azure/foundry/concepts/foundry-models-overview), [embeddings](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/embeddings), [images in chat prompts](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/gpt-with-vision), [image generation](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/dall-e))

| Need | Model type |
| --- | --- |
| Chat, write, summarize, or answer questions | A large language model, or a small language model when a compact one is enough |
| Answer questions about an image | A multimodal (vision) chat model |
| Search by meaning, cluster, or recommend | An embedding model |
| Create a new image from text | An image generation model |
| Hard problems that need several steps of reasoning | A reasoning model |

**Text analysis techniques** ([Introduction to NLP concepts](https://learn.microsoft.com/en-us/training/modules/introduction-language/), [Azure Language](https://learn.microsoft.com/en-us/azure/ai-services/language-service/overview))

| Technique | Output | Example |
| --- | --- | --- |
| Language detection | The language of the text | Route tickets to the right team |
| Key term extraction | Important words and phrases | Topics in a set of reviews |
| Entity detection | People, places, organizations, dates, and other named entities | Tag news articles by who and where |
| PII detection | Personal data, found and redacted | Remove phone numbers from transcripts |
| Sentiment analysis | Positive, neutral, or negative | Track how customers feel about a launch |
| Summarization | A shorter text that keeps the main points | One paragraph from a long report |

**Computer vision tasks** ([computer vision tasks unit](https://learn.microsoft.com/en-us/training/modules/introduction-computer-vision/2-overview))

| Task | Output |
| --- | --- |
| Image classification | One label for the whole image |
| Object detection | A label and a location (bounding box) for each object |
| Semantic segmentation | A class for each pixel, which gives precise object outlines |
| Contextual image analysis | Descriptions, tags, and answers about what the image shows, from multimodal models |
| Image generation | A new image from a text prompt and optional reference images |

**Speech** ([Azure Speech overview](https://learn.microsoft.com/en-us/azure/ai-services/speech-service/overview), [SSML](https://learn.microsoft.com/en-us/azure/ai-services/speech-service/speech-synthesis-markup))

| Capability | What it does |
| --- | --- |
| Speech recognition (speech to text) | Turns spoken audio into text, live or from recorded files |
| Speech synthesis (text to speech) | Turns text into natural speech with neural voices |
| SSML | XML markup that sets pitch, pronunciation, speaking rate, and volume for synthesized speech |
| Speech translation | Translates spoken audio into text or speech in another language |
| Custom speech | A model trained on your text and audio to recognize domain terms and difficult audio |

### Microsoft Foundry

**Building blocks** ([What is Microsoft Foundry](https://learn.microsoft.com/en-us/azure/foundry/what-is-foundry), [endpoints](https://learn.microsoft.com/en-us/azure/foundry/foundry-models/concepts/endpoints), [deployment types](https://learn.microsoft.com/en-us/azure/foundry/foundry-models/concepts/deployment-types))

| Item | What to know |
| --- | --- |
| Foundry resource | The Azure resource that holds projects, model deployments, access control, and networking |
| Project | Where you build agents and apps; its endpoint looks like `https://<resource-name>.services.ai.azure.com/api/projects/<project-name>` |
| Deployment | A named instance of a model; your code calls the model by its deployment name |
| Deployment type | Global Standard is the usual start; Data Zone and Standard keep processing inside a zone or geography; Provisioned reserves throughput; Batch is cheaper and asynchronous |
| Playground | A portal page to try prompts, system messages, and parameters before writing code |
| Prompt agent | An agent defined by instructions, a model, and tools, built in the portal or with the SDK; Foundry runs it for you |
| Foundry Tools | Prebuilt AI services such as Azure Speech, Azure Language, Azure Translator, and Azure Content Understanding (formerly Azure AI Services) |

**Foundry SDK in Python** ([quickstart](https://learn.microsoft.com/en-us/azure/foundry/quickstarts/get-started-code))

- Create an `AIProjectClient` from `azure-ai-projects` with the project endpoint and a credential such as `DefaultAzureCredential` from `azure-identity`.
- Call `get_openai_client()` on the project client, then `responses.create()` with your deployment name as `model`.

**Agent tools** ([file search](https://learn.microsoft.com/en-us/azure/foundry/agents/how-to/tools/file-search), [code interpreter](https://learn.microsoft.com/en-us/azure/foundry/agents/how-to/tools/code-interpreter), [function calling](https://learn.microsoft.com/en-us/azure/foundry/agents/how-to/tools/function-calling))

| Tool | Use it when |
| --- | --- |
| File search | The agent must answer from files you upload |
| Code interpreter | The agent must run Python for math, data files, or charts |
| Function calling | The agent must use your own code: the model asks, your app runs the function and returns the result |

**Images in prompts** ([source](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/gpt-with-vision))

- Put the image (a URL or base64 data) and your text question together in the user message.
- The `detail` setting can be `low`, `high`, or `auto`; `low` uses fewer tokens.

**Content Understanding** ([overview](https://learn.microsoft.com/en-us/azure/ai-services/content-understanding/overview), [prebuilt analyzers](https://learn.microsoft.com/en-us/azure/ai-services/content-understanding/concepts/prebuilt-analyzers))

- Works on documents, images, audio, and video, and returns markdown or JSON fields.
- An analyzer holds the extraction settings, a field schema, and the models it uses. Use a prebuilt analyzer or build a custom one.
- Fields use one of three methods: extract (documents only), classify, or generate.
- Audio analyzers transcribe calls, separate speakers, and can return fields such as a summary or sentiment.

## Free official resources

- [AI-901 exam page](https://learn.microsoft.com/en-us/credentials/certifications/exams/ai-901/): scheduling, price by country, and languages.
- [AI-901 study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/ai-901): the skills outline this guide follows.
- [Course AI-901T00: Introduction to AI in Azure](https://learn.microsoft.com/en-us/training/courses/ai-901t00) and its two free learning paths: [AI concepts for developers and technology professionals](https://learn.microsoft.com/en-us/training/paths/ai-concepts/) and [Get started with AI applications and agents on Azure](https://learn.microsoft.com/en-us/training/paths/get-started-ai-apps-agents/).
- [Free practice assessment on AI Skills Navigator](https://aiskillsnavigator.microsoft.com/credentials/cert-83587e0a0754cfee561ade3e27d9fa1cdaf15ae03be52d2413b2b858d1b4eda4): sign in to start it.
- [Exam sandbox](https://aka.ms/examdemo): try the question formats and the exam interface.
- [Microsoft Foundry portal](https://ai.azure.com) and the [Microsoft Foundry documentation](https://learn.microsoft.com/en-us/azure/foundry/what-is-foundry).
- [Azure free account](https://azure.microsoft.com/pricing/purchase-options/azure-account) and [Azure for Students](https://azure.microsoft.com/free/students/) for the exercises.
- [Microsoft Q&A](https://learn.microsoft.com/en-us/answers/) for questions about the services.

## Practice questions

[practice-questions.md](practice-questions.md) has 15 original scenario questions split across the two domains by weight, each with an explanation and a link to the docs. For more, the [Examice AI-901 practice bank](https://examice.com/exams/microsoft/ai-901?utm_source=github&utm_medium=social&utm_campaign=ai-901-study-guide-and-practice-questions&utm_content=link_2) has 150+ questions with a written explanation and a discussion under each one, and the first 5 questions are free, explanations included.

## Exam day tips

- You get 45 minutes. Microsoft Learn isn't available during fundamentals exams, so you can't look anything up ([source](https://learn.microsoft.com/en-us/credentials/support/exam-duration-exam-experience)).
- Answer and review every question you've seen before you take a break: after a break you can't return to them, and the clock keeps running.
- Guessing costs nothing, and a question with several parts gives a point for each correct part, so answer everything ([source](https://learn.microsoft.com/en-us/credentials/certifications/exam-scoring-reports)).
- More than half the weight is on building with Foundry, so expect questions about code, SDK calls, and portal steps, not only definitions.
- If the exam isn't offered in your language, you can request 30 extra minutes.
- Register with a personal Microsoft account, not a work account, so your records stay with you if you change jobs.
- Expect current product names: Microsoft Foundry (formerly Azure AI Studio and Azure AI Foundry) and Foundry Tools (formerly Azure AI Services) ([source](https://learn.microsoft.com/en-us/azure/foundry/what-is-foundry)).

## FAQ

### How hard is AI-901?

It's a fundamentals exam, but it asks for more practical skill than AI-900 did. AI-900 required no data science or software engineering experience, while the AI-901 audience profile expects Python syntax and familiarity with Azure resources, and 55–60% of its weight is on building apps and an agent with Microsoft Foundry. You need a scaled score of 700 to pass ([AI-901 study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/ai-901), [AI-900 exam page](https://learn.microsoft.com/en-us/credentials/certifications/exams/ai-900/)).

### How long should I study for AI-901?

The course AI-901T00 runs 1 day with an instructor, and its two learning paths take about 9.5 hours by Microsoft's estimates ([source](https://learn.microsoft.com/en-us/training/courses/ai-901t00)). The three week plan above at about 5 hours a week leaves time for the labs and the practice assessment. If you've never written Python, add a week for the basics.

### Does the Azure AI Fundamentals certification expire?

No. Fundamentals certifications don't expire, so there's no renewal assessment ([source](https://learn.microsoft.com/en-us/credentials/certifications/renew-your-microsoft-certification)).

### What is the AI-901 retake policy?

After a first failed attempt you wait 24 hours. After that you wait 14 days between attempts, with at most 5 attempts in the 12 months from your first try. Each retake is paid, and you can't retake an exam you passed unless the certification has expired ([source](https://learn.microsoft.com/en-us/credentials/support/retake-policy)).

### What changed from AI-900 to AI-901?

AI-900 retired on June 30, 2026, and AI-901 is now the exam for Microsoft Certified: Azure AI Fundamentals ([source](https://learn.microsoft.com/en-us/credentials/certifications/exams/ai-900/)). AI-900 had five areas that asked you to describe AI workloads, machine learning, computer vision, natural language processing, and generative AI. AI-901 has two: AI concepts and capabilities (40–45%) and implementing solutions with Microsoft Foundry (55–60%). If you earned the certification through AI-900, you keep it: Microsoft says the certification itself isn't retiring, and fundamentals certifications don't expire ([June 2026 credentials roundup](https://techcommunity.microsoft.com/blog/skills-hub-blog/microsoft-credentials-roundup-june-2026/4528350)).

### Do I need to know how to code for AI-901?

Yes, at a basic level. The audience profile asks for knowledge of Python syntax and programming techniques, and the skills outline includes building small chat, agent, speech, vision, and extraction apps ([source](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/ai-901)).

## Contributing

Found a fact that changed or an answer you disagree with? Open an issue or a pull request and include a link to the Microsoft source. Exam facts in this guide were last checked on October 28, 2026.

## License

Text and questions © Examice, licensed under [CC BY 4.0](LICENSE).

Microsoft, Azure, and Microsoft Foundry are trademarks of the Microsoft group of companies. This guide is not affiliated with or endorsed by Microsoft.
