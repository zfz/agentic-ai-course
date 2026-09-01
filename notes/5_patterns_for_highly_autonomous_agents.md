# Module 5

## Example: Planning with multiple agents

**System prompt:**
```
You are a marketing manager and have the following team of agents to
work with:

{description of agents}

Return a step-by-step plan to carry out the user's request.
```

**Agents:** researcher, graphic designer, writer

**User request:** "Create a summer marketing campaign for sunglasses" → LLM (marketing manager) → plan:
1. Ask **researcher** to research current sunglasses trends
2. Ask **graphic designer** to create ad images
3. Ask **writer** to create report
4. Review report

**Execution flow:**

```
Step 1 text ──────► researcher
                        │
                        ▼
Step 1 output,     graphic
Step 2 text  ─────► designer
                        │
                        ▼
Step 2 output,
Step 3 text  ─────► writer
```

## Other communication patterns

**Deeper hierarchy** — a manager delegates to leads, who each delegate to their own sub-agents:

```
                    marketing
                     manager
                   /    |     \
                  ▼     ▼      ▼
            researcher  graphic   writer
             /     \   designer   /    \
            ▼       ▼            ▼      ▼
          web     fact                style   citation
        researcher checker              writer  checker
```

**All-to-all** — every agent can communicate directly with every other agent:

```
  marketing manager  ◄──────►  researcher
        ▲  ╲               ╱      ▲
        │    ╲           ╱        │
        │      ╲       ╱          │
        │        ╲   ╱            │
        ▼        ╱   ╲            ▼
  graphic designer ◄──────►    writer
```

Every pair of agents (marketing manager, researcher, graphic designer, writer) has a bidirectional link to every other agent.
