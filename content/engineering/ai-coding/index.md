---
title: "AI Coding"
summary: "AI Coding Tooling Summary"
draft: false
tags: ["vibe", "coding", "agentic"]
categories: ["engineering", "ai"]
author: "Gary Thomas"
date: 2026-02-23
---

This has been updated from the origial to provide a broader view of AI tools in general rather than being specific to the concept of vibe coding.

I am attempting to keep a track on all of the different tools that I have been playing with as I am still looking for the right tool - I would like to use just one, but I am not sure that will happen. Maybe MCP will help me with this.

I can definitely say, that having worked a lot more with Curosr and Windsurfs recently I am finding that is currently the go to environment. Also, the integration with ChatGPT is proving to be very effective.

“Vibe coding” is a growing practice where you lean into letting a coding agent do most of the heavy lifting while you focus on the architecture and features of your application. But effective vibe coding isn’t just about one-shot prompting, accepting all recommendations, and hoping for the best. It involves structuring your work, refining your prompts, and using frameworks that lead to cleaner, more efficient code.

“Vibe coding,” coined by OpenAI cofounder Andrej Karpathy in February, describes giving AI prompts to write code. As Karpathy puts it, developers can “fully give in to the vibes” and “forget the code even exists.”

I am struggling with the term Vibe Coding, but I will get over it!

```markdown
An update on this which I think brings this point home comes from Andrew Ng, he said that the term Vibe Coding misleads people into thing that the engineer just "go with the vibes" or flow.
“It’s unfortunate that’s called vibe coding,” Ng said at a firechat chat in May at conference LangChain Interrupt. “It’s misleading a lot of people into thinking, just go with the vibes, you know — accept this, reject that.”
Coding with AI is "a deeply intellectual exercise". He is otherwise very positive about the advances in coding with AI.
```

One thing is clear having now attempted to use Agentic Coding is that the tools are very capable and advancing very quickly, and when used correctly and will definitely provide an engineer with a productivity boost.

## Feature-Based Comparison Matrix

### IDE-Based Tools & Agentic Extensions

| Tool           | Repo Context Awareness | Multi-File Edits | Ecosystem Maturity | Notes                                   |
|----------------|------------------------|------------------|--------------------|-----------------------------------------|
| Antigravity    | Deep                   | Complete Context | Advanced           | Deepmind's deeply integrated agentic framework |
| Windsurf       | High                   | Cascade          | Early              | Strong momentum, curated doc grounding  |
| Cursor         | Moderate               | Cursor Composer  | Growing            | Familiar VS Code UX, strong Composer AI |
| Cline          | Deep (External LLM)    | Open/Edit/Command| Early              | VS Code Extension, brings full agentic capability |
| Roo Code       | Deep (External LLM)    | Open/Edit/Command| Early              | Fork of Cline with UI improvements      |
| Cody           | Repo-aware via search  | Multi-IDE        | Mature             | Best with Sourcegraph infrastructure    |
| Copilot Edits  | Limited                | Multi-file       | Mature             | GitHub's answer to Composer/Cascade      |
| GitLab Duo     | MR assistance          | Test gen         | Mature             | Tied to GitLab platform                  |

### Terminal-Based CLI Agents

| Tool               | Codebase Awareness | Workflow Support     | Notes                              |
|--------------------|--------------------|----------------------|------------------------------------|
| Aider              | Deep (Git aware)   | Architect-Editor     | Gold standard open-source CLI agent|
| Claude Code        | Deep               | Inline Q&A, CLI      | Good for power-CLI workflows       |
| Jules.             | Deep               | Inline Q&A, CLI      | Good for power-CLI workflows       |
| OpenHands          | Deep sandbox       | Autonomous Engineer  | Formerly OpenDevin, local sandbox  |
| Amazon Q Developer | Multi-file planning| AWS aligned          | CLI autocomplete & Q&A bot         |

### Browser-Based Tools & Generators

| Tool           | Focus Area          | Notes                                |
|----------------|---------------------|--------------------------------------|
| v0 by Vercel   | UI builder          | React/Tailwind natural language gen  |
| Lovable        | Full-stack builder  | Next.js, Edge functions, Supabase    |
| Bolt.new       | Design-to-code      | Figma to full-stack apps scaffolding |
| Replit         | Collaborative coding| Built-in AI chat, Agentic beta       |
| Bind.ai        | Full-stack focus    | Multi-model integration options      |
| Firebase Studio| Firebase stack      | Narrower scope, Firebase ecosystem   |

### Specialized Tools

| Tool           | Functionality       | Notes                        |
|----------------|---------------------|------------------------------|
| Tempo          | React scaffolding   | Rapid React structural gen   |
| Creatr         | No/low-code builder | AI-powered app creation      |
| Kiro           | Spec-driven         | Specifies requirements & tests|
| n8n            | Workflow automation | Open source, AI + automation |
| Make.com       | Workflow automation | Integration & automation platform |
| Zapier         | Workflow automation | Popular enterprise integration tool |

### Agent Frameworks

| Tool           | Description                                  |
|----------------|----------------------------------------------|
| LangChain      | Popular framework for developing LLM apps    |
| AutoGen        | Multi-agent conversation framework by MS     |
| CrewAI         | Role-playing multi-agent framework           |
| Flowise        | Drag & drop UI to build LLM flows            |
| AgentOps       | Agent building & monitoring platform         |
| Haystack       | NLP framework for search & RAG               |
| Semantic Kernel| Microsoft's SDK for AI integration           |
| Superagent     | Open-source agent API                        |
| LlamaIndex     | Data framework for LLM applications          |

### Vector Stores & Memory

| Tool           | Description                                  |
|----------------|----------------------------------------------|
| Pinecone       | Managed, cloud-native vector database        |
| Weaviate       | Open-source AI-native vector database        |
| Chroma         | Open-source embedding database               |
| FAISS          | Facebook AI Similarity Search library        |

### Deployment & Serving

| Tool           | Description                                  |
|----------------|----------------------------------------------|
| FastAPI        | Modern Python web framework for APIs         |
| Streamlit      | Fast way to build and share data apps        |
| Gradio         | Build UI for machine learning models         |
| Docker         | Containerization platform                    |
| Kubernetes     | Container orchestration system               |

### Monitoring & Evaluation

| Tool           | Description                                  |
|----------------|----------------------------------------------|
| LangSmith      | Tracing & evaluation for LLM apps (LangChain)|
| Prometheus     | Monitoring system & time series database     |
| Grafana        | Observability dashboards                     |
| OpenTelemetry  | High-quality, ubiquitous telemetry standard  |

## Product Design Tools

| Tool       | Description                                                                 |
|------------|-----------------------------------------------------------------------------|
| uizard     | A tool that allows you to create a product UX flow using natural language prompts. Part of the Miro product family |
| galileo.ai | Another design tool that can create designs by prompting or the upload or images |

## Tool References and Resources

### IDE-Based Tools & Agentic Extensions

- Antigravity: [Antigravity](internal/antigravity)
- Windsurf: [Windsurf Official](https://windsurf.ai)
- Cursor: [Cursor AI](https://cursor.so)
- Cline: [Cline](https://github.com/cline/cline)
- Roo Code: [Roo Code](https://github.com/RooVetGit/Roo-Code)
- Cody (Sourcegraph): [Sourcegraph Cody](https://sourcegraph.com/cody)
- GitHub Copilot: [GitHub Copilot](https://copilot.github.com)
- GitLab Duo: [GitLab AI](https://about.gitlab.com/solutions/ai/)

### Terminal-Based CLI Agents

- Aider: [Aider](https://aider.chat)
- Claude Code: [Claude AI](https://claude.ai)
- OpenHands: [OpenHands](https://github.com/All-Hands-AI/OpenHands)
- Amazon Q Developer: [Amazon Q](https://aws.amazon.com/q/)

### Browser-Based Tools & Generators

- v0 by Vercel: [v0](https://v0.vercel.app)
- Lovable: [Lovable](https://lovable.ai)
- Bolt.new: [Bolt.new](https://bolt.new)
- Replit: [Replit](https://replit.com)
- Firebase Studio: [Firebase Studio](https://firebase.google.com/studio)
- Bind.ai: [Bind.ai](https://bind.ai)

### Specialized Tools

- Tempo: [Tempo](https://tempo.io)
- Creatr: [Creatr](https://creatr.ai)
- Kiro: [Kiro AI](https://kiro.ai)
- n8n: [n8n](https://n8n.io)
- Make.com: [Make](https://make.com)
- Zapier: [Zapier](https://zapier.com)

### Agent Frameworks

- LangChain: [LangChain](https://langchain.com)
- AutoGen: [AutoGen](https://microsoft.github.io/autogen/)
- CrewAI: [CrewAI](https://crewai.com)
- Flowise: [Flowise](https://flowiseai.com)
- AgentOps: [AgentOps](https://agentops.ai)
- Haystack: [Haystack](https://haystack.deepset.ai)
- Semantic Kernel: [Semantic Kernel](https://github.com/microsoft/semantic-kernel)
- Superagent: [Superagent](https://superagent.sh)
- LlamaIndex: [LlamaIndex](https://llamaindex.ai)

### Vector Stores

- Pinecone: [Pinecone](https://pinecone.io)
- Weaviate: [Weaviate](https://weaviate.io)
- Chroma: [Chroma](https://trychroma.com)
- FAISS: [FAISS](https://github.com/facebookresearch/faiss)

### Deployment & Monitoring

- FastAPI: [FastAPI](https://fastapi.tiangolo.com)
- Streamlit: [Streamlit](https://streamlit.io)
- Gradio: [Gradio](https://gradio.app)
- LangSmith: [LangSmith](https://smith.langchain.com)
- Prometheus: [Prometheus](https://prometheus.io)
- Grafana: [Grafana](https://grafana.com)
- OpenTelemetry: [OpenTelemetry](https://opentelemetry.io)

### Design Tools

- Miro: [Miro](https://miro.com)

## Additional Analysis Resources

- [LangChain Interrupt Conference](https://langchain.com/interrupt)
- Andrew Ng Firechat on Vibe Coding: [YouTube Link](https://youtube.com/watch?v=example)
- Andrej Karpathy’s Vibe Coding Explanation: [OpenAI Blog](https://openai.com/blog/vibe-coding)

## Key Adoptions Considerations

The following outlines the different steps that can be considered for adoption:
s
### Beginners

- Start with IDE-based tools that offer inline suggestions to reduce cognitive load.
- Use tools with strong documentation and community support.

### Professional Development

- Explore multi-file editing capabilities for complex projects.
- Leverage AI for test generation and code refactoring.

### Team Collaboration

- Consider tools that integrate with existing version control and CI/CD pipelines.
- Use platforms that support code reviews and MR assistance.

### Cost Optimization

- Evaluate pricing tiers and free trial options.
- Choose tools aligned with your primary development ecosystem to reduce overhead.