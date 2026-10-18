# Part 04: Backend and Data

*Outcome: a working full-stack MVP with real data and real users.*

## At a glance

How the pieces connect by the end of this part:

```mermaid
%%{init: {'theme': 'base', 'themeVariables': {'background': '#ffffff'}, 'flowchart': {'curve': 'basis'}}}%%
flowchart LR
    U["Browser"] --> W["Next.js frontend"]
    W -->|"HTTP · JSON"| A["FastAPI backend<br/><small>business rules, auth</small>"]
    A --> DB[("Postgres")]
    A --> J["Background jobs"]
    A --> X["Third-party APIs"]
    X -.->|"webhooks"| A

    classDef start fill:#bfdbfe,stroke:#60a5fa,color:#1e3a5f
    classDef step fill:#ddd6fe,stroke:#a78bfa,color:#3b1f7a
    classDef done fill:#a7f3d0,stroke:#34d399,color:#064e3b
    classDef side fill:#fce7f3,stroke:#f472b6,color:#831843

    class U start
    class W,A,DB,J step
    class X side

    linkStyle 0,1,2,3,4 stroke:#a78bfa,stroke-width:2px
    linkStyle 5 stroke:#f472b6,stroke-width:2px,stroke-dasharray:5
```

## Planned episodes
- [Concept] APIs: HTTP, REST, status codes, designing endpoints
- [Build-along] FastAPI essentials
- [Concept] Databases: data modeling, SQL basics, Postgres
- [Build-along] Schema, ORM and migrations
- [Concept] Authentication and authorization
- [Build-along] Sign-in and roles
- [Concept] Background jobs, webhooks and file storage
- [Build-along] Integrating third-party APIs
- [Your Turn] Connect your frontend to a real backend

## Deliverable
A working full-stack MVP.
