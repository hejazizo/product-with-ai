# Product with AI

A free Pytopia course on YouTube about building a complete product from scratch with AI, and covering every role a product needs: product management, design, frontend, backend, AI engineering, data, quality, deployment and launch.

AI coding agents now write much of the code. The skills that matter are deciding what to build, breaking it into tickets, directing the agent, reviewing what it produces, and getting the product in front of real users. This course teaches all of them.

## Who it's for

- You know a little programming: you can read basic Python and you've used a terminal.
- Everything else (web, databases, design, AI, deployment, product management) is taught from scratch.
- You don't need to master every detail. You need to understand each layer well enough to direct an AI agent, review its work and ship.

## What you'll get out of it

Everyone builds a real product of their own alongside the course. At the end, you choose a track:
- **Get Hired:** turn the product into a portfolio piece and prepare for AI-era engineering roles.
- **Go Indie:** turn the product into a business and find your first customers.

## How the course works

- **Self-paced videos**, 5–12 minutes each, in three types:
  - **Concept:** one idea explained on its own, useful outside the course.
  - **Build-along:** we apply it to the reference product on screen.
  - **Your Turn:** a short brief for applying it to your own product, as a ticket.
- **Two products in parallel:** we build the [reference product](project/) on camera, and you build your own idea.
- **The course is a Linear board.** Every lesson is a ticket you import and close as you go. See [course/linear/](course/linear/).
- **Catch-up points:** the reference product has a git tag at the end of every part (e.g. `part04-end`), so you can always pick up from there.
- **We review every diff.** If we can't explain AI-written code, we don't merge it.

## Syllabus

```mermaid
%%{init: {'theme': 'base', 'themeVariables': {'background': '#ffffff'}, 'flowchart': {'curve': 'basis'}}}%%
flowchart LR
    F["Foundations<br/><small>Part 00</small>"] --> P["Plan<br/><small>Parts 01–02 · PM, design</small>"]
    P --> B["Build<br/><small>Parts 03–06 · frontend, backend, AI, data</small>"]
    B --> S["Ship<br/><small>Parts 07–08 · quality, deploy</small>"]
    S --> L["Launch and iterate<br/><small>Part 09</small>"]
    L --> H["Get Hired<br/><small>Track 10A</small>"]
    L --> I["Go Indie<br/><small>Track 10B</small>"]
    L -.->|"user feedback"| P

    classDef start fill:#bfdbfe,stroke:#60a5fa,color:#1e3a5f
    classDef step fill:#ddd6fe,stroke:#a78bfa,color:#3b1f7a
    classDef done fill:#a7f3d0,stroke:#34d399,color:#064e3b
    classDef side fill:#fce7f3,stroke:#f472b6,color:#831843

    class F start
    class P,B,S,L step
    class H,I done

    linkStyle 0,1,2,3 stroke:#a78bfa,stroke-width:2px
    linkStyle 4,5 stroke:#34d399,stroke-width:3px
    linkStyle 6 stroke:#f472b6,stroke-width:2px,stroke-dasharray:5
```

| Part | Topic | You finish with |
|---|---|---|
| 00 | [Foundations](course/parts/00-foundations/) | A working setup and your first merged pull request |
| 01 | [Product Management](course/parts/01-product-management/) | A one-page spec and an MVP backlog |
| 02 | [Design](course/parts/02-design/) | A clickable prototype |
| 03 | [Frontend](course/parts/03-frontend/) | A UI running on mock data |
| 04 | [Backend and Data](course/parts/04-backend-and-data/) | A working full-stack MVP |
| 05 | [AI Engineering](course/parts/05-ai-engineering/) | An AI feature with an eval suite |
| 06 | [Data and Analytics](course/parts/06-data-and-analytics/) | A metrics dashboard |
| 07 | [Quality and Security](course/parts/07-quality-and-security/) | CI with passing tests and a security checklist |
| 08 | [Ship and Operate](course/parts/08-ship-and-operate/) | A live product on a custom domain, taking payments |
| 09 | [Launch and Iterate](course/parts/09-launch-and-iterate/) | A public launch and one shipped iteration |
| 10 | [Tracks: Get Hired / Go Indie](course/parts/10-tracks/) | A portfolio case study, or your first customers |

## Repository layout

```
product-with-ai/
├── course/
│   ├── parts/       # one folder per part, one subfolder per episode
│   ├── templates/   # templates for episode notes
│   └── linear/      # the course as an importable Linear backlog
└── project/         # the reference product built on camera
```

## Status

Planning: syllabus and repo structure.
