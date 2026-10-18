# Part 00: Foundations

*Outcome: your machine is set up, you can read code well enough to review it, and you've merged your first pull request with an AI agent's help.*

## At a glance

The loop you'll use for every change in the course:

```mermaid
%%{init: {'theme': 'base', 'themeVariables': {'background': '#ffffff'}, 'flowchart': {'curve': 'basis'}}}%%
flowchart LR
    P["Plan<br/><small>you write the ticket</small>"] --> A["Agent builds<br/><small>code and tests</small>"]
    A --> R["You review<br/><small>read the diff</small>"]
    R --> M["Merge"]
    R -.->|"can't explain it"| A

    classDef start fill:#bfdbfe,stroke:#60a5fa,color:#1e3a5f
    classDef step fill:#ddd6fe,stroke:#a78bfa,color:#3b1f7a
    classDef done fill:#a7f3d0,stroke:#34d399,color:#064e3b
    classDef side fill:#fce7f3,stroke:#f472b6,color:#831843

    class P start
    class A,R step
    class M done

    linkStyle 0,1 stroke:#a78bfa,stroke-width:2px
    linkStyle 2 stroke:#34d399,stroke-width:3px
    linkStyle 3 stroke:#f472b6,stroke-width:2px,stroke-dasharray:5
```

## Planned episodes
- [Concept] How a product works end to end: client, server, database, API, cloud
- [Build-along] Terminal and files
- [Build-along] Git and GitHub: commits, branches, pull requests
- [Concept] Code literacy: reading Python and TypeScript (variables, functions, objects, async)
- [Concept] Working with AI coding agents: the plan → build → review loop
- [Build-along] Project instructions and context files for your agent
- [Your Turn] Import the course Linear board, create your repo, merge your first pull request

## Deliverable
Your own repo with a first merged pull request.
