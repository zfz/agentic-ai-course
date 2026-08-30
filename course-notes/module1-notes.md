# Module 1

## What is "agentic"?

> Rather than arguing over which work to include or exclude as being a true agent, we can acknowledge that there are different degrees to which systems can be agentic.
>
> — Andrew Ng, X (Twitter) post, June 2024 ([source](https://x.com/AndrewYNg/status/1801295202788983136))

("Agentic Reasoning" talk — Andrew Ng, Sequoia Ascent, March 2024)

## Coding benchmark (HumanEval)

Legend: Non-agentic, Reflection, Tool Use, Planning, Multiagent

| Model | System | Score |
|---|---|---|
| GPT-3.5 | Non-agentic | 48% |
| GPT-3.5 | Intervenor (Multiagent) | ~73% |
| GPT-3.5 | ANPL (Tool Use) | ~74% |
| GPT-3.5 | Language Agent Tree Search (Planning) | ~83% |
| GPT-3.5 | LDB+Reflexion (Tool Use) | ~94% |
| GPT-4 | Non-agentic | 67% |
| GPT-4 | CodeT / MetaGPT / ANPL (Tool Use) | ~81% |
| GPT-4 | Reflexion (Reflection) | ~90% |
| GPT-4 | Language Agent Tree Search (Planning) | ~93% |
| GPT-4 | AgentCoder (Multiagent) | ~95% |

## Key benefits of agentic workflows

- Much better performance
- Faster than humans because of parallelization
- Modular: can add or update tools, swap out models

## What tasks is agentic AI suited to?

**Easier** ← → **Harder**

| Easier | Harder |
|---|---|
| Clear, step-by-step process | Steps not known ahead of time |
| Standard procedures to follow | Plan/solve as you go |
| Text assets only | Multimodal (sound, vision) |

## Using LLM as a judge

Pipeline: User query → LLM ("Search web") → **web search** tool → LLM ("Fetch 5 best sources") → **web fetch** / **PDF to text** tools → LLM ("Write essay draft") → document

Judge prompt: "Assign the following essay a quality score between 1 and 5, where 5 is the best: {essay}" → LLM → score

| Example prompt | Score |
|---|---|
| Black holes | 3 |
| Robotic harvesting | 4 |

## Agentic Design Patterns

1. Reflection
2. Tool use
3. Planning
4. Multi-agent collaboration
