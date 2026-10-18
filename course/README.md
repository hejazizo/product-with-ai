# Course materials

## Structure

- `parts/NN-name/README.md`: the part's outcome, episode list and deliverable.
- `parts/NN-name/NN-episode-name/notes.md`: the script outline for one episode, including the prompts used on camera. Start from [templates/episode-notes.md](templates/episode-notes.md).
- `parts/NN-name/NN-episode-name/lesson.html`: the episode's interactive lesson, published as a Claude artifact. Students follow the video with this page open.
- `linear/`: every lesson as a ticket, for students to import.

## How a lesson works

```mermaid
%%{init: {'theme': 'base', 'themeVariables': {'background': '#ffffff'}, 'flowchart': {'curve': 'basis'}}}%%
flowchart LR
    T["Ticket in Linear<br/><small>the next lesson</small>"] --> C["Concept<br/><small>the idea</small>"]
    C --> B["Build-along<br/><small>reference product</small>"]
    B --> Y["Your Turn<br/><small>your product</small>"]
    Y --> D["Ticket closed"]
    Y -.->|"stuck?"| K["Catch-up tag<br/><small>pNN-eNN-end</small>"]

    classDef start fill:#bfdbfe,stroke:#60a5fa,color:#1e3a5f
    classDef step fill:#ddd6fe,stroke:#a78bfa,color:#3b1f7a
    classDef done fill:#a7f3d0,stroke:#34d399,color:#064e3b
    classDef side fill:#fce7f3,stroke:#f472b6,color:#831843

    class T start
    class C,B,Y step
    class D done
    class K side

    linkStyle 0,1,2 stroke:#a78bfa,stroke-width:2px
    linkStyle 3 stroke:#34d399,stroke-width:3px
    linkStyle 4 stroke:#f472b6,stroke-width:2px,stroke-dasharray:5
```

## Episode types

| Type | What it is | Re-recording |
|---|---|---|
| **Concept** | One idea explained on its own (whiteboard or slides) | Rarely; keep it tool-independent |
| **Build-along** | Applying the idea to the reference product (screencast) | When tools change; keep these short |
| **Your Turn** | A brief and a ticket for the student's own product | Rarely |

## Conventions

- Episode IDs: `pNN-eNN` (e.g. `p04-e03`).
- Build-along episodes have git tags in `project/` for their start and end state: `p04-e03-start` → `p04-e03-end`.
- Every part ends with a catch-up tag: `part04-end`.
- Each lesson's artifact URL goes in its `notes.md` and in the part README's episode list.
- Tool-specific details also go in the episode notes, so small changes can be fixed in writing without re-recording.
- When the AI agent makes a mistake on camera, keep it in the edit and debug it.
