---
title: "Appendix"
summary: "A summary of the different AI terminology"
draft: true
url: "/ai/appendix"
ShowToc: false
TocOpen: false
tags: ["ai", "appendix"]
categories: ["ai"]
author: "Gary Thomas"
---

# Generative AI Dictionary

## Core Concepts

### Generative AI
- **Definition:** A class of artificial intelligence algorithms that learn from existing data to generate new, plausible data with similar characteristics.
- **Explanation:** Unlike discriminative AI, generative AI creates new data by learning the underlying probability distribution.
- **Examples:** GPT-4, DALL-E, Midjourney, Stable Diffusion
- **Related Terms:** Large Language Model (LLM), Diffusion Model, GANs

### Large Language Model (LLM)
- **Definition:** Deep neural networks with billions of parameters trained on massive text and code datasets.
- **Explanation:** Use the Transformer architecture to understand and generate human language.
- **Examples:** GPT-4, Claude, Bard, LLaMA, BERT (mainly discriminative but foundational)
- **Related Terms:** Transformer, Token, Context Window, Prompt Engineering

### Neural Network
- **Definition:** A computational model inspired by the structure and function of the human brain. It consists of interconnected nodes, called "neurons," organized in layers. Neural networks learn by adjusting the connections between neurons based on the data they process.
- **Explanation:** Neural networks are composed of layers of interconnected nodes (neurons). Each connection has a weight, and the network learns by adjusting these weights to minimize errors in its predictions. Different types of neural networks exist, including feedforward neural networks, recurrent neural networks (RNNs), and convolutional neural networks (CNNs), each suited for different tasks. They are fundamental to deep learning.
- **Related Terms:** Deep Learning, Neuron, Backpropagation, Transformer, GAN, VAE

### Probability Distribution
- **Definition:** A function describing the likelihood of outcomes in a random experiment.
- **Explanation:** Generative models learn this to sample and generate new data.

## Model Architectures

### Transformer
- **Definition:** A neural network architecture based on self-attention, processing sequences in parallel.
- **Explanation:** Captures long-range dependencies effectively.
- **Related Terms:** Attention Mechanism, LLM, Token, Embedding

### Diffusion Model
- **Definition:** Generates data by reversing a noise process.
- **Explanation:** Adds noise to data (forward process) and learns to remove it (reverse process).
- **Examples:** Stable Diffusion, Imagen, Midjourney
- **Related Terms:** Neural Network

### GAN (Generative Adversarial Network)
- **Definition:** Uses a generator and discriminator in competition to produce realistic data.
- **Explanation:** Generator tries to fool the discriminator, improving over time.
- **Related Terms:** Generative AI

### VAE (Variational Autoencoder)
- **Definition:** Encodes data to a latent space and decodes to generate new samples.
- **Explanation:** Uses probabilistic encoding for smooth and interpretable latent space.
- **Related Terms:** Latent Space

### Autoregressive Model
- **Definition:** Predicts the next item in a sequence using previous ones.
- **Explanation:** LLMs often use this structure for text generation.
- **Related Terms:** Sampling, LLM

### Normalizing Flow
- **Definition:** Transforms a simple distribution into a complex one using invertible functions.
- **Explanation:** Allows exact likelihood estimation and efficient sampling.

### Energy-Based Model (EBM)
- **Definition:** Uses energy functions to represent the likelihood of data.
- **Explanation:** Learns to assign low energy to real data and high energy to others.

## Key Components & Techniques

### Token
- **Definition:** Basic unit of input text for LLMs (word, subword, or character).
- **Explanation:** Token count affects model input length and performance.

### Context Window
- **Definition:** Max token length an LLM can consider at once.
- **Explanation:** Larger context window allows broader input comprehension.

### Prompt Engineering
- **Definition:** Crafting inputs to guide generative AI outputs.
- **Explanation:** Involves formatting, keywords, and few-shot examples.
- **Related Terms:** Chain-of-Thought Prompting

### Chain-of-Thought Prompting
- **Definition:** Technique guiding LLMs to show reasoning before answers.
- **Explanation:** Enhances complex reasoning and accuracy.

### Fine-tuning
- **Definition:** Adapting a pre-trained model to a specific task with additional training.
- **Explanation:** Uses less data than training from scratch.
- **Related Terms:** Transfer Learning

### Transfer Learning
- **Definition:** Using knowledge from one task/model to improve another.
- **Explanation:** Useful when labeled data is scarce.

### Attention Mechanism
- **Definition:** Assigns importance to different input parts.
- **Explanation:** Allows models to "focus" on relevant parts of input.

### Sampling
- **Definition:** Selecting the next token during generation.
- **Explanation:** Strategies include greedy, random, top-k, nucleus sampling.

### Temperature
- **Definition:** Parameter controlling randomness in sampling.
- **Explanation:** Higher values = more diverse outputs.

### Embedding
- **Definition:** Vector representations capturing semantic meaning.
- **Explanation:** Similar meanings are close in vector space.

### Latent Space
- **Definition:** Compressed vector representation learned by generative models.
- **Explanation:** Sampling here generates new outputs.
- **Related Terms:** VAE, GAN, Latent Variable

### Latent Variable
- **Definition:** Unobserved variable influencing observed data.
- **Explanation:** Key in generative model structure.

### Encoder / Decoder
- **Encoder Definition:** Maps input data to latent space.
- **Decoder Definition:** Reconstructs data from latent space.

## Infrastructure and Systems

### MCP (Model Control Plane)
- **Definition:** Manages AI model lifecycle (versioning, scaling, deployment).
- **Related Terms:** A2A, Deployment, Scaling

### A2A (AI-to-Application)
- **Definition:** Interfaces that integrate AI into apps.
- **Explanation:** Enables practical use of generative AI via APIs, SDKs.

### Context Caching
- **Definition:** Stores previously processed context to improve efficiency.
- **Explanation:** Useful in long conversations or documents.

## Applications

### Text-to-Image
- **Definition:** Generates images from text prompts.
- **Examples:** DALL-E, Midjourney, Stable Diffusion

### Text-to-Audio
- **Definition:** Generates speech/music from text.

### Synthetic Data Generation
- **Definition:** Creates artificial data resembling real data.
- **Explanation:** Useful for privacy-preserving AI training.

### Style Transfer
- **Definition:** Applies the style of one image to another.

### Image Inpainting
- **Definition:** Fills in missing parts of an image.

### Super-Resolution
- **Definition:** Increases image/video resolution using AI.

## Evaluation and Metrics

### Perplexity
- **Definition:** Measures how well a model predicts text.
- **Explanation:** Lower = better performance.

### Inception Score (IS)
- **Definition:** Evaluates image quality/diversity.
- **Explanation:** Higher score = better generation.

### Fréchet Inception Distance (FID)
- **Definition:** Measures similarity between generated and real images.
- **Explanation:** Lower score = more realistic output.

### BLEU Score
- **Definition:** Evaluates text generation quality.
- **Explanation:** Often used in translation tasks.

## Challenges and Considerations

### Hallucination
- **Definition:** When AI generates plausible but incorrect info.
- **Explanation:** Affects reliability in factual tasks.

### Prompt Injection
- **Definition:** Malicious prompt manipulation to bypass model safety.
- **Explanation:** A growing concern in AI security.

### Alignment
- **Definition:** Ensuring AI outputs align with human values.
- **Related Terms:** RLHF, AI Ethics, Constitutional AI

### Bias in Generative AI
- **Definition:** Systematic unfairness in AI outputs due to training data.
- **Explanation:** Can lead to discriminatory behavior.

## Popular Tools

### OpenAI GPT
- **Function:** LLM for text generation, chat, coding, etc.

### ChatGPT
- **Function:** Conversational interface using GPT models.

### DALL·E
- **Function:** Text-to-image generation.

### Midjourney
- **Function:** Artistic image generation from prompts.

### Stable Diffusion
- **Function:** Open-source diffusion model for image generation.

### Hugging Face Transformers
- **Function:** Pretrained models for NLP, vision, and audio.

### LangChain
- **Function:** Framework for building LLM-powered apps with tool orchestration.

### LlamaIndex
- **Function:** Connects LLMs to structured and unstructured data sources.

### Weights & Biases
- **Function:** Experiment tracking and model monitoring.

### TensorRT-LLM
- **Function:** NVIDIA toolkit for optimizing and deploying LLMs.

### Ollama
- **Function:** Runs LLMs locally on devices.

### Replicate
- **Function:** Cloud platform for deploying and running generative AI models.