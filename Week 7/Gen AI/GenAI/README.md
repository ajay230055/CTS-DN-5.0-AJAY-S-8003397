# GenAI (Generative AI) Fundamentals

A detailed reference guide covering the core concepts of Generative AI.

---

## Table of Contents
1. [What is Generative AI?](#1-what-is-generative-ai)
2. [How Generative AI Works](#2-how-generative-ai-works-high-level)
3. [Key Concepts & Terminology](#3-key-concepts--terminology)
4. [Types of Generative AI Models](#4-types-of-generative-ai-models)
5. [Underlying Architectures](#5-underlying-architectures)
6. [Common Use Cases](#6-common-use-cases)
7. [Challenges & Considerations](#7-challenges--considerations)
8. [Basic GenAI Workflow Example](#8-basic-genai-workflow-example-api-call-concept)

---

## 1. What is Generative AI?
Generative AI (GenAI) refers to AI systems capable of **creating new content** — text, images, audio, video, or code — based on patterns learned from training data, rather than just analyzing or classifying existing data.

Unlike traditional AI (which mostly predicts or classifies), Generative AI **produces original outputs** that resemble the data it was trained on.

## 2. How Generative AI Works (High Level)
1. **Training** — A model is trained on massive datasets to learn patterns, structures, and relationships in the data.
2. **Model Architecture** — Most modern GenAI models use **Transformer architecture**, which relies on a mechanism called **self-attention** to understand context and relationships between words/tokens.
3. **Generation** — Given a prompt (input), the model predicts and generates the most probable next output (word, pixel, sound, etc.) step by step, one token at a time.

## 3. Key Concepts & Terminology
- **LLM (Large Language Model)** — A model trained on vast text data to understand and generate human-like language (e.g., GPT, Claude, Gemini, LLaMA).
- **Token** — A unit of text (word or sub-word) that models process; text is broken into tokens for processing.
- **Prompt** — The input given to a GenAI model to guide its output.
- **Prompt Engineering** — The practice of crafting effective prompts to get desired outputs from a model.
- **Fine-tuning** — Further training a pre-trained model on a specific dataset to specialize it for a particular task/domain.
- **Embedding** — A numerical (vector) representation of data (text, images) that captures semantic meaning, used for search and similarity comparisons.
- **Context Window** — The amount of text (tokens) a model can consider at once when generating a response.
- **Hallucination** — When an AI model generates incorrect or fabricated information confidently.
- **RAG (Retrieval-Augmented Generation)** — A technique where the model retrieves relevant external data (e.g., from a database) before generating a response, improving accuracy.
- **Temperature** — A parameter controlling the randomness/creativity of model outputs (low = deterministic, high = more creative/random).

## 4. Types of Generative AI Models
| Type | Description | Examples |
|---|---|---|
| **Text Generation** | Generates human-like text | GPT-4, Claude, Gemini |
| **Image Generation** | Creates images from text prompts | DALL·E, Midjourney, Stable Diffusion |
| **Code Generation** | Writes/completes code | GitHub Copilot, Claude Code |
| **Audio/Speech Generation** | Generates voice or music | ElevenLabs, Suno |
| **Video Generation** | Creates video content | Sora, Runway |

## 5. Underlying Architectures
- **Transformers** — The foundational architecture behind most modern LLMs, introduced in the paper "Attention Is All You Need" (2017). Uses self-attention to weigh the importance of different words in a sequence.
- **GANs (Generative Adversarial Networks)** — Two neural networks (generator & discriminator) compete to produce realistic synthetic data, commonly used for images.
- **Diffusion Models** — Generate data by gradually removing noise from a random signal; widely used in image generation (e.g., Stable Diffusion).
- **VAEs (Variational Autoencoders)** — Encode data into a compressed representation and decode it back, useful for generating variations of data.

## 6. Common Use Cases
- Chatbots and virtual assistants
- Content creation (articles, marketing copy, summaries)
- Code generation and debugging assistance
- Image and design generation
- Data augmentation for training other models
- Personalized recommendations
- Document summarization and Q&A systems
- Language translation

## 7. Challenges & Considerations
- **Bias** — Models can inherit biases present in training data.
- **Hallucinations** — Models may generate plausible-sounding but incorrect information.
- **Data Privacy** — Concerns around training data and user input handling.
- **Compute Cost** — Training and running large models requires significant computational resources.
- **Ethical Use** — Concerns around misinformation, deepfakes, and intellectual property.
- **Explainability** — It can be difficult to understand exactly why a model produced a specific output.

## 8. Basic GenAI Workflow Example (API Call Concept)
```python
import anthropic

client = anthropic.Anthropic(api_key="YOUR_API_KEY")

response = client.messages.create(
    model="claude-sonnet-4-6",
    max_tokens=500,
    messages=[
        {"role": "user", "content": "Explain GenAI in simple terms."}
    ]
)

print(response.content)
```

---

*For deeper learning, refer to official documentation from providers like [Anthropic](https://docs.claude.com), [OpenAI](https://platform.openai.com/docs), and [Google AI](https://ai.google.dev/docs).*
