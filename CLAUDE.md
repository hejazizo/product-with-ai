# Product with AI: working conventions

A free Pytopia course on YouTube. See [README.md](README.md) for the pitch and syllabus, and [course/README.md](course/README.md) for the episode index and conventions.

## Lessons are Claude artifacts

- Each episode is one Claude artifact. The artifact is the only copy of the lesson: no `lesson.html`, `notes.md` or other per-episode markdown in the repo.
- [course/README.md](course/README.md) is the single index of every part and episode. After publishing, put the artifact URL in the episode's **Lesson** column and update its **Status**.
- The lesson is also the recording outline. Every lesson follows the structure in "What every lesson contains" in course/README.md.
- To change a lesson, read the artifact by its URL, edit, and republish to the same URL so the link keeps working.
- An episode gets a folder, `course/episodes/pNN-eNN/`, only when it needs files beside its lesson (starter code, datasets, images).

## Mermaid diagrams in markdown

Use a diagram wherever a flow, a loop, a fork or an architecture is easier to see than to read. Don't add one if the list already says it clearly.

Every diagram uses this template:

````markdown
```mermaid
%%{init: {'theme': 'base', 'themeVariables': {'background': '#ffffff'}, 'flowchart': {'curve': 'basis'}}}%%
flowchart LR
    A["Start<br/><small>detail</small>"] --> B["Step<br/><small>detail</small>"]
    B --> C["Outcome"]
    B -.->|"loop back"| A

    classDef start fill:#bfdbfe,stroke:#60a5fa,color:#1e3a5f
    classDef step fill:#ddd6fe,stroke:#a78bfa,color:#3b1f7a
    classDef done fill:#a7f3d0,stroke:#34d399,color:#064e3b
    classDef side fill:#fce7f3,stroke:#f472b6,color:#831843

    class A start
    class B step
    class C done

    linkStyle 0 stroke:#a78bfa,stroke-width:2px
    linkStyle 1 stroke:#34d399,stroke-width:3px
    linkStyle 2 stroke:#f472b6,stroke-width:2px,stroke-dasharray:5
```
````

What the colors mean:

| Role | Nodes | Edges |
|---|---|---|
| Entry point | `start` (blue) | — |
| Normal step | `step` (purple) | purple, 2px |
| Outcome or result | `done` (green) | green, 3px, for the edge into the outcome |
| Feedback loop, alternative path, external system | `side` (pink) | pink, 2px, dashed |

Rules:
- Node labels: a short title, then optional detail as `<br/><small>…</small>`.
- Prefer `flowchart LR`; use `TB` only when a left-to-right diagram gets too wide.
- `linkStyle` indices count edges in the order they're written, starting at 0. Recount after adding or removing an edge. Comma lists are fine: `linkStyle 0,1,2 …`.
