# Teaching graph

## Split

```mermaid
flowchart LR
  you["You type it\n/grill-me  /to-spec  /implement"]
  model["Model may reach\ntdd  code-review  diagnose"]
  you -->|"may call"| model
  you -.->|"never"| you
```

User-invoked skills orchestrate. Their descriptions stay off the context tax until you type them.
Model-invoked skills are small discipline. The agent may reach for them.

A user skill may call a model skill. It may not call another user skill.

## Loop

```mermaid
flowchart LR
  grill[Grill] --> spec[Spec]
  spec --> tickets[Tickets]
  tickets --> impl[Implement]
  impl --> arch[Architecture]
  arch --> grill
```

Grill until language is shared. Write a spec, not a chat dump. Cut vertical slices. Implement with tests and review. Clean the architecture. Feed it back.

## Four pillars

```mermaid
flowchart TB
  t[Trigger — who starts it]
  s[Structure — steps here, references elsewhere]
  st[Steering — leading words, split the fat steps]
  p[Prune — one source, kill no-ops]
  t --> s --> st --> p
```

## How vs what

```
SKILL.md     how the agent works          you invoke
MCP server   what the agent can touch    a sheet, a box, a token
```

Third-party “skills as MCP tools” puts every description back in the window. That undoes `disable-model-invocation`. Do not do it.
