# Part 05: AI Engineering

*Outcome: the product has an AI feature that users can rely on, and you can measure how good it is.*

## At a glance

No AI change ships without going through the eval loop:

```mermaid
%%{init: {'theme': 'base', 'themeVariables': {'background': '#ffffff'}, 'flowchart': {'curve': 'basis'}}}%%
flowchart LR
    F["AI feature<br/><small>prompt and model</small>"] --> D["Run the eval set<br/><small>test examples</small>"]
    D --> S["Score<br/><small>checks and LLM judge</small>"]
    S --> Q{"Good enough?"}
    Q -->|"yes"| SH["Ship"]
    Q -.->|"no: change it"| F

    classDef start fill:#bfdbfe,stroke:#60a5fa,color:#1e3a5f
    classDef step fill:#ddd6fe,stroke:#a78bfa,color:#3b1f7a
    classDef done fill:#a7f3d0,stroke:#34d399,color:#064e3b
    classDef side fill:#fce7f3,stroke:#f472b6,color:#831843

    class F start
    class D,S,Q step
    class SH done

    linkStyle 0,1,2 stroke:#a78bfa,stroke-width:2px
    linkStyle 3 stroke:#34d399,stroke-width:3px
    linkStyle 4 stroke:#f472b6,stroke-width:2px,stroke-dasharray:5
```

## Planned episodes
- [Concept] How LLMs work for app developers: tokens, context windows, sampling
- [Build-along] Calling an LLM API: prompts and system prompts
- [Concept] Structured outputs and tool use
- [Concept] RAG: embeddings, vector search (pgvector), chunking
- [Concept] Agents: the agent loop, MCP, agent SDKs, and when not to use an agent
- [Concept] Evals: test datasets and LLM-as-judge
- [Build-along] An eval suite for the AI feature
- [Concept] Production concerns: cost, latency, caching, streaming, guardrails
- [Concept] When classical ML or a simple heuristic beats an LLM
- [Your Turn] Add one AI feature to your product, with evals

## Deliverable
An AI feature with an eval suite.
