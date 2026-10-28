# AI-901 practice questions

These 15 scenario questions cover the two AI-901 domains in proportion to their weights: 6 on AI concepts and capabilities and 9 on implementing AI solutions with Microsoft Foundry. Each answer explains why the right option works, why the others don't, and links to the Microsoft docs. Read the scenario, pick an answer, then open the explanation.

> Unofficial study notes by Examice. Not affiliated with or endorsed by Microsoft. The practice questions are original, written for this guide, and not taken from the exam.

### Question 1

*Identify AI concepts and capabilities*

A bank uses an AI model to recommend whether to approve loan applications. Regulators require the bank to tell each rejected applicant which factors led to the decision. Which responsible AI principle does this requirement address most directly?

- A. Transparency
- B. Inclusiveness
- C. Reliability and safety
- D. Privacy and security

<details><summary>Show answer</summary>

**A.** Transparency means people can understand how an AI system works and how it reaches decisions that affect them. Explaining the factors behind a decision is the interpretability part of transparency.

- B is wrong: inclusiveness is about making sure a solution doesn't shut some users out.
- C is wrong: reliability and safety is about the system working as designed and handling unexpected conditions safely.
- D is wrong: privacy and security is about protecting personal and business data.

Docs: [What is responsible AI?](https://learn.microsoft.com/en-us/azure/machine-learning/concept-responsible-ai)

</details>

### Question 2

*Identify AI concepts and capabilities*

A hospital deploys an AI system that drafts discharge summaries. Hospital policy says a clinician must review and sign every summary before it's released, and a named team owns the system's outcomes and audits every change to it. Which responsible AI principle does this policy reflect?

- A. Accountability
- B. Fairness
- C. Transparency
- D. Inclusiveness

<details><summary>Show answer</summary>

**A.** Accountability means the people and organizations that build and deploy AI answer for how it operates. A governance framework, clear ownership, and keeping a person in control of decisions that affect people's lives are how you apply it.

- B is wrong: fairness is about similar people getting similar outcomes and reducing bias.
- C is wrong: transparency is about people understanding how the system works and its limits.
- D is wrong: inclusiveness is about not excluding anyone from the benefits.

Docs: [What is responsible AI?](https://learn.microsoft.com/en-us/azure/machine-learning/concept-responsible-ai), [Responsible AI unit](https://learn.microsoft.com/en-us/training/modules/get-started-ai-fundamentals/7-responsible-ai)

</details>

### Question 3

*Identify AI concepts and capabilities*

Which statement best describes how a large language model produces a response to a prompt?

- A. It predicts the most probable next token, adds it to the sequence, and repeats until the response is complete
- B. It searches the internet at request time and copies the best matching paragraph
- C. It looks up the prompt in a database of stored questions and answers
- D. It runs a fixed set of rules that developers wrote for each topic

<details><summary>Show answer</summary>

**A.** A language model breaks text into tokens, turns them into embeddings that capture meaning, and uses a transformer's decoder to predict the most probable next token in the sequence that the prompt starts. Repeating that prediction produces the completion.

- B is wrong: a model generates text from what it learned in training; it only uses live data if you connect it to a tool or grounding data.
- C is wrong: the model doesn't store and retrieve fixed answers; it generates new text.
- D is wrong: rules engines follow fixed logic, while a language model learns patterns from data.

Docs: [Large language models unit](https://learn.microsoft.com/en-us/training/modules/fundamentals-generative-ai/3-language-models)

</details>

### Question 4

*Identify AI concepts and capabilities*

You want employees to search an internal knowledge base by meaning, so that a search for "time off" also finds documents about "vacation leave." Which kind of model turns text into the vectors this search needs?

- A. An embedding model
- B. An image generation model
- C. A text to speech model
- D. A speech to text model

<details><summary>Show answer</summary>

**A.** An embedding is a vector of numbers that represents the meaning of text. Similar text produces vectors that are close together, which is what vector search uses to match "time off" with "vacation leave."

- B is wrong: image generation models create images.
- C is wrong: text to speech turns text into spoken audio.
- D is wrong: speech to text turns audio into text.

Docs: [Generate embeddings](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/embeddings)

</details>

### Question 5

*Identify AI concepts and capabilities*

A chat app answers questions about company travel policy. When testers ask the same question twice, they get noticeably different wording and structure. The deployed model supports sampling parameters. Which change makes answers more focused and consistent?

- A. Lower the temperature
- B. Raise the temperature
- C. Raise both temperature and top_p
- D. Raise the maximum number of output tokens

<details><summary>Show answer</summary>

**A.** Temperature controls randomness. A low value, such as 0.2, makes output more focused and concrete, and a high value, such as 0.7, makes it more varied.

- B is wrong: a higher temperature makes answers vary more.
- C is wrong: both settings add randomness when raised, and Microsoft recommends changing one of them at a time, not both.
- D is wrong: the token limit caps the length of a response; it doesn't make answers more consistent.

Docs: [Prompt engineering techniques](https://learn.microsoft.com/en-us/azure/foundry/openai/concepts/prompt-engineering)

</details>

### Question 6

*Identify AI concepts and capabilities*

A news archive needs to tag each article with the people, organizations, and places it mentions. Which text analysis technique fits?

- A. Entity detection (named entity recognition)
- B. Sentiment analysis
- C. Key term extraction
- D. Text summarization

<details><summary>Show answer</summary>

**A.** Entity detection finds named entities in text and sorts them into categories such as people, places, organizations, and dates. In Foundry, Azure Language offers it as named entity recognition.

- B is wrong: sentiment analysis labels text as positive, neutral, or negative.
- C is wrong: key term extraction returns important words and phrases, but it doesn't categorize them as people or places.
- D is wrong: summarization shortens the text.

Docs: [Introduction to NLP concepts](https://learn.microsoft.com/en-us/training/modules/introduction-language/), [Named entity recognition](https://learn.microsoft.com/en-us/azure/ai-services/language-service/named-entity-recognition/overview)

</details>

### Question 7

*Implement AI solutions by using Microsoft Foundry*

You build a chat app on a deployed model in Microsoft Foundry. Every answer must be in Spanish and only about your company's products, whatever the user types. Where should you put these rules?

- A. In the system message
- B. In the user's first message of the conversation
- C. In the temperature setting
- D. In the deployment name

<details><summary>Show answer</summary>

**A.** The system message holds the instructions and context that guide every response: the assistant's role and boundaries, its tone, and its output format. Language and topic rules belong there.

- B is wrong: user messages carry what the user asks on each turn; the system message is where you define the assistant's behavior.
- C is wrong: temperature controls randomness, not language or topic.
- D is wrong: the deployment name only identifies which deployment your code calls.

Docs: [System message design](https://learn.microsoft.com/en-us/azure/foundry/openai/concepts/advanced-prompt-engineering)

</details>

### Question 8

*Implement AI solutions by using Microsoft Foundry*

You deploy a model in the Foundry portal and name the deployment `support-chat`. Your Python code calls the Responses API through the OpenAI client from your Foundry project. What value do you pass as the `model` parameter?

- A. `support-chat`
- B. The name of the Foundry resource
- C. The name of the Foundry project
- D. Your Azure subscription ID

<details><summary>Show answer</summary>

**A.** A deployment gives a model a name and a configuration, and your requests reach the model through that deployment name, passed in the `model` field.

- B is wrong: the resource name is part of the endpoint URL, not the model parameter.
- C is wrong: the project name is also part of the endpoint URL.
- D is wrong: requests never take a subscription ID as the model.

Docs: [Endpoints for Foundry Models](https://learn.microsoft.com/en-us/azure/foundry/foundry-models/concepts/endpoints)

</details>

### Question 9

*Implement AI solutions by using Microsoft Foundry*

You write a small Python chat client with the Foundry SDK (`azure-ai-projects`). Which two values do you pass when you create the `AIProjectClient`? Choose two.

- A. The project endpoint, in the form `https://<resource-name>.services.ai.azure.com/api/projects/<project-name>`
- B. A credential, such as `DefaultAzureCredential` from `azure-identity`
- C. The Azure region name
- D. The resource group name

<details><summary>Show answer</summary>

**A and B.** The quickstart creates the client with the project endpoint and a Microsoft Entra ID credential, then gets an OpenAI client from it to send requests.

- C is wrong: the endpoint already identifies the resource and project, so you don't pass a region.
- D is wrong: the client doesn't need the resource group; that's an Azure management detail.

Docs: [Quickstart: Get started with the Microsoft Foundry SDK](https://learn.microsoft.com/en-us/azure/foundry/quickstarts/get-started-code)

</details>

### Question 10

*Implement AI solutions by using Microsoft Foundry*

In the Foundry portal you create one agent that must answer employee questions from 40 HR policy PDFs that you upload. Which tool should you add to the agent?

- A. File search
- B. Code interpreter
- C. Function calling
- D. Image generation

<details><summary>Show answer</summary>

**A.** File search grounds an agent in your own documents. You upload the files into a vector store, and the agent retrieves the relevant passages to answer each question.

- B is wrong: code interpreter runs Python for calculations, data analysis, and charts.
- C is wrong: function calling lets the agent ask your app to run your own code.
- D is wrong: image generation creates pictures.

Docs: [File search tool](https://learn.microsoft.com/en-us/azure/foundry/agents/how-to/tools/file-search)

</details>

### Question 11

*Implement AI solutions by using Microsoft Foundry*

Support chat transcripts must be stored without customer names, phone numbers, or email addresses. You want a prebuilt Foundry Tool to find and redact them before storage. What should your app call?

- A. PII detection in Azure Language
- B. Text translation in Azure Translator
- C. Text to speech in Azure Speech
- D. Key phrase extraction in Azure Language

<details><summary>Show answer</summary>

**A.** PII detection identifies, classifies, and redacts personal data in text, conversations, and documents, and returns the redacted text.

- B is wrong: translation changes the language, not the personal data.
- C is wrong: text to speech produces audio.
- D is wrong: key phrase extraction lists main concepts; it doesn't redact anything.

Docs: [PII detection in Azure Language](https://learn.microsoft.com/en-us/azure/ai-services/language-service/personally-identifiable-information/overview)

</details>

### Question 12

*Implement AI solutions by using Microsoft Foundry*

A kiosk app must read its answers aloud in a natural voice, speak more slowly for some users, and pronounce your product names correctly. What should you use?

- A. Azure Speech text to speech, with SSML
- B. Azure Speech speech to text, with a phrase list
- C. Azure Translator document translation
- D. A vision chat model

<details><summary>Show answer</summary>

**A.** Text to speech turns text into natural speech with neural voices, and SSML lets you adjust pitch, pronunciation, speaking rate, and volume.

- B is wrong: speech to text transcribes audio; a phrase list improves recognition, not spoken output.
- C is wrong: document translation translates files.
- D is wrong: a vision chat model analyzes images and returns text.

Docs: [Text to speech](https://learn.microsoft.com/en-us/azure/ai-services/speech-service/text-to-speech), [SSML overview](https://learn.microsoft.com/en-us/azure/ai-services/speech-service/speech-synthesis-markup)

</details>

### Question 13

*Implement AI solutions by using Microsoft Foundry*

An insurance app lets customers upload a photo of a damaged car and ask, "Which parts look damaged?" You have a vision chat model deployed in Foundry. How should the app send the request?

- A. Put the text question and the image, as a URL or base64 data, together in the user message
- B. Send the photo to an image generation model and ask for a new picture
- C. Turn the photo into an embedding and send only the vector
- D. Send only the text question and describe the photo in the system message yourself

<details><summary>Show answer</summary>

**A.** Vision models accept message content that mixes text and images. The image can be an HTTP or HTTPS URL or base64 encoded data, and the model answers the question about it.

- B is wrong: image generation creates new images; it doesn't answer questions about one.
- C is wrong: an embedding supports similarity search, and the chat model needs the image itself to reason about it.
- D is wrong: the model would never see the photo.

Docs: [Use images in chat prompts](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/gpt-with-vision)

</details>

### Question 14

*Implement AI solutions by using Microsoft Foundry*

A marketing team wants new banner images created from a text description, such as "a mountain bike on a forest trail at sunrise." Which kind of model should you deploy?

- A. An image generation model
- B. A vision chat model
- C. An embedding model
- D. A speech to text model

<details><summary>Show answer</summary>

**A.** Image generation models create images from a text prompt and, optionally, reference images.

- B is wrong: vision chat models take images as input and return text.
- C is wrong: embedding models return vectors.
- D is wrong: speech to text models transcribe audio.

Docs: [How to use image generation models](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/dall-e)

</details>

### Question 15

*Implement AI solutions by using Microsoft Foundry*

A call center wants each recorded call turned into three fields: a short summary of the issue, whether the issue was resolved (yes or no), and the customer's sentiment. You want one Foundry Tool to handle the transcription and the fields together. What should you use?

- A. An Azure Content Understanding audio analyzer with a field schema
- B. Azure Translator document translation
- C. Azure Speech text to speech
- D. The semantic ranker in Azure AI Search

<details><summary>Show answer</summary>

**A.** Content Understanding audio analyzers transcribe calls, separate speakers, and extract structured fields such as summaries and sentiment. In the field schema, the summary uses the generate method and the resolved flag uses the classify method.

- B is wrong: document translation translates files; it doesn't process audio.
- C is wrong: text to speech produces audio from text.
- D is wrong: the semantic ranker reorders search results.

Docs: [Content Understanding audio overview](https://learn.microsoft.com/en-us/azure/ai-services/content-understanding/audio/overview), [What is Azure Content Understanding?](https://learn.microsoft.com/en-us/azure/ai-services/content-understanding/overview)

</details>

## More practice

The [Examice AI-901 practice bank](https://examice.com/exams/microsoft/ai-901?utm_source=github&utm_medium=social&utm_campaign=ai-901-study-guide-and-practice-questions&utm_content=link_3) has 150+ questions with a written explanation and a discussion under each one. The first 5 questions are free, explanations included.
