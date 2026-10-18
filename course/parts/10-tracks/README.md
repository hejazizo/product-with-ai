# Part 10: Tracks

Pick the track that matches your goal, or watch both.

## At a glance

```mermaid
%%{init: {'theme': 'base', 'themeVariables': {'background': '#ffffff'}, 'flowchart': {'curve': 'basis'}}}%%
flowchart LR
    P["Your shipped product"] --> H["10A · Get Hired"]
    H --> C1["Case study<br/><small>and interview prep</small>"]
    P --> I["10B · Go Indie"]
    I --> C2["First 10 customers"]
    C1 --> X["Capstone<br/><small>rubric review</small>"]
    C2 --> X

    classDef start fill:#bfdbfe,stroke:#60a5fa,color:#1e3a5f
    classDef step fill:#ddd6fe,stroke:#a78bfa,color:#3b1f7a
    classDef done fill:#a7f3d0,stroke:#34d399,color:#064e3b
    classDef side fill:#fce7f3,stroke:#f472b6,color:#831843

    class P start
    class H,I,C1,C2 step
    class X done

    linkStyle 0,1,2,3 stroke:#a78bfa,stroke-width:2px
    linkStyle 4,5 stroke:#34d399,stroke-width:3px
```

## 10A: Get Hired
*Outcome: your product is a portfolio piece, and you're ready for interviews.*
- Writing a case study of your product
- Recording a demo video
- A GitHub profile that shows how you work
- A resume for AI-era roles: AI engineer, product engineer, founding engineer
- Interviews: coding with and without AI, take-home projects, light system design, product sense
- Freelancing as a bridge into work

## 10B: Go Indie
*Outcome: your product has its first paying customers.*
- Finding the first 10 customers
- Sales basics
- Customer support
- Unit economics
- Legal entity basics
- Bootstrapping vs. raising money

## Capstone
A live product and a case study, assessed against a published rubric: it works, spec quality, ticket hygiene, tests and evals, security checklist, and the write-up.
