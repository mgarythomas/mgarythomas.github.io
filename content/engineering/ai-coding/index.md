---
title: "AI Coding"
summary: "AI Coding Tooling Summary"
draft: false
tags: ["vibe", "coding", "agentic"]
categories: ["engineering", "ai"]
author: "Gary Thomas"
date: 2025-08-17
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

### IDE-Based Tools

| Tool           | Repo Context Awareness | Multi-File Edits | AI Integration Level | Ecosystem Maturity | Notes                                   |
|----------------|------------------------|------------------|----------------------|--------------------|-----------------------------------------|
| Windsurf       | High                   | Cascade          | Recent changes       | Early              | Strong momentum, curated doc grounding  |
| Cursor         | Moderate               | Cascade-style    | Strong AI            | Growing            | Familiar VS Code UX                      |
| Kiro           | Spec-driven            | Task Breakdown   | Emerging             | Early              | Specifies requirements, designs, tests |
| Cody (Sourcegraph) | Repo-aware via search | Multi-IDE       | Moderate    s         | Mature             | Best with Sourcegraph infrastructure    |
| GitHub Copilot | Limited                | Inline           | Broad                | Mature             | Strong language coverage, test gen      |
| GitLab Duo     | MR assistance          | Test gen         | Integrated           | Mature             | Tied to GitLab platform                  |

### Terminal-Based Tools

| Tool           | Codebase Awareness | Workflow Support   | Integration Level | Notes                              |
|----------------|--------------------|--------------------|-------------------|----------------------------------|
| Claude Code    | Deep               | Inline Q&A, CLI    | Moderate          | Good for power-CLI workflows      |
| Amazon Q Developer | Multi-file planning | AWS aligned      | Strong            | Pricing Pro tier, AWS ecosystem   |

### Browser-Based Tools

| Tool           | Focus Area          | AI Integration Level | Notes                                |
|----------------|---------------------|----------------------|------------------------------------|
| Firebase Studio| Firebase stack      | Gemini integration   | Narrower scope, Firebase ecosystem |
| Bind.ai        | full-stack focus    | Support integrtion to multiple modelss | Aims to provide a multi-language multi model option |
| Bolt.new       | Design-to-code      | Moderate             | Figma to full-stack apps            |
| Replit         | Collaborative coding| Built-in AI chat     | Weaker repo-wide controls           |

### Specialized Tools

| Tool           | Functionality       | Notes                        |
|----------------|---------------------|------------------------------|
| v0 by Vercel   | UI builder          | React/Tailwind components     |
| Tempo          | React scaffolding   | Rapid scaffolding             |
| Lovable        | No/low-code builder | Non-technical app creation    |
| Creatr         | No/low-code builder | AI-powered app creation       |
| n8n            | Workflow automation | Open source, AI + automation  |

## Product Design Tools

| Tool       | Description                                                                 |
|------------|-----------------------------------------------------------------------------|
| uizard     | A tool that allows you to create a product UX flow using natural language prompts. Part of the Miro product family |
| galileo.ai | Another design tool that can create designs by prompting or the upload or images |

## Tool References and Resources

### IDE-Based Tools

- Windsurf: [Windsurf Official](https://windsurf.ai)
- Cursor: [Cursor AI](https://cursor.so)
- Kiro: [Kiro AI](https://kiro.ai)
- Cody (Sourcegraph): [Sourcegraph Cody](https://sourcegraph.com/cody)
- GitHub Copilot: [GitHub Copilot](https://copilot.github.com)
- GitLab Duo: [GitLab AI](https://about.gitlab.com/solutions/ai/)

### Terminal-Based Tools

- Claude Code: [Claude AI](https://claude.ai)
- Amazon Q Developer: [Amazon Q](https://aws.amazon.com/q/)

### Browser-Based Tools

- Firebase Studio: [Firebase Studio](https://firebase.google.com/studio)
- Bolt.new: [Bolt.new](https://bolt.new)
- Replit: [Replit](https://replit.com)

### Specialized Tools

- v0 by Vercel: [v0](https://v0.vercel.app)
- Tempo: [Tempo](https://tempo.io)
- Lovable: [Lovable](https://lovable.ai)
- Creatr: [Creatr](https://creatr.ai)
- n8n: [n8n](https://n8n.io)
- uizard: [uizard](https://uizard.io)
- galileo.ai: [galileo.ai](https://galileo.ai)

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