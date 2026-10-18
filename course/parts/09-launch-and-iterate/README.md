# Part 09: Launch and Iterate

*Outcome: real people use the product, and you improve it based on what they say.*

## At a glance

```mermaid
%%{init: {'theme': 'base', 'themeVariables': {'background': '#ffffff'}, 'flowchart': {'curve': 'basis'}}}%%
flowchart LR
    L["Launch"] --> U["Real users"]
    U --> F["Feedback<br/><small>support and analytics</small>"]
    F --> T["Tickets<br/><small>prioritized with RICE</small>"]
    T --> S["Sprint"]
    S --> SH["Ship"]
    SH -.->|"next iteration"| U

    classDef start fill:#bfdbfe,stroke:#60a5fa,color:#1e3a5f
    classDef step fill:#ddd6fe,stroke:#a78bfa,color:#3b1f7a
    classDef done fill:#a7f3d0,stroke:#34d399,color:#064e3b
    classDef side fill:#fce7f3,stroke:#f472b6,color:#831843

    class L start
    class U,F,T,S step
    class SH done

    linkStyle 0,1,2,3 stroke:#a78bfa,stroke-width:2px
    linkStyle 4 stroke:#34d399,stroke-width:3px
    linkStyle 5 stroke:#f472b6,stroke-width:2px,stroke-dasharray:5
```

## Planned episodes
- [Concept] Positioning and landing page copy
- [Concept] Pricing
- [Concept] Launch channels: Product Hunt, communities, content, SEO basics
- [Build-along] Collecting feedback and support requests
- [Concept] Prioritization and roadmapping (RICE)
- [Build-along] Feedback → tickets → sprint → ship
- [Your Turn] Launch publicly and ship one iteration

## Deliverable
A public launch and one shipped iteration.
