# Module 4

## Looking at traces

Pipeline: "Write an essay on recent developments in black hole science" → LLM ("Search web") → **web search** tool → LLM ("Fetch 5 best sources") → **web fetch** / **PDF to text** tools → LLM ("Write essay draft") → document

**Trace** — the full sequence of inputs/outputs across the run. **Span** — one step within the trace.

Example trace contents:
- Search web output: "Black hole theories Einstein", "Event horizon telescope radio", "New physics black holes", "Galaxies black holes origins"
- Web search results: "Elementary school student cracks 30-year black hole mystery" — https://astrokidnews.com — "Bob Lee, in his yard, saw a bright light in the sky..."
- Fetch 5 best sources: https://astrokidnews.com, https://spaceblog2000.com, https://spacefunnews.com, https://astronautme.com

## Counting up the errors (research agent)

| Prompt | Search terms | Search results | Picking 5 best sources | ... | ... |
|---|---|---|---|---|---|
| Recent developments in black hole science | | Too many blog posts, not enough papers | | | |
| Renting vs buying a home in Seattle | | | Missed well-known blog | | |
| Robotics for harvesting fruit | Terms too generic | Website for elementary school students | | | |
| ... | ... | ... | ... | | |
| Batteries for electric vehicles | | Only selected US-based companies | Missed magazine | | |
| | **5%** | **45%** | **10%** | ... | ... |

## Tips for error analysis

- Develop a habit of looking at traces
- Carry out error analysis to figure out what component performed poorly, leading to a poor final output
- Use error analysis output to decide where to focus efforts

## Counting up the errors (invoice due-date extraction)

Select 10-100 invoices for which the agentic workflow extracted the wrong due date

| Input | PDF-to-text | LLM data extraction |
|---|---|---|
| Invoice 1 | Errors in extraction | |
| Invoice 2 | | Wrong date selected |
| Invoice 3 | | Wrong data selected |
| ... | ... | ... |
| Invoice 20 | Errors in extraction | Wrong data selected |
| | **15%** | **87%** |

## Example: research agent

Same pipeline as above (User query → LLM → web search → LLM → web fetch → LLM → document)

| Prompt | Issues |
|---|---|
| Recent black hole science | Missed high-profile result that had lots of news coverage |
| Renting vs buying a home in Seattle? | Seems to do a good job |
| Robotics for harvesting fruit | Didn't mention leading equipment company |

End-to-end eval is expensive!

### Evaluate web search tool only

- Create a list of gold standard web resources
- Write code that calculates how many results correspond to gold standard websites e.g. F1-score
- Track as you vary hyperparameters: e.g., search engine, number of results, dates

## Benefits of component-level evaluations

- Can provide clearer signal for specific errors
  - Avoid the noise in end-to-end system
- More efficient for focused team to optimize
  - Work on smaller, more targeted problems faster

## Improving LLM component performance

| Approach | Detail |
|---|---|
| Improve your prompts | Add more explicit instructions. Add one or more concrete example to the prompt (few-shot prompting) |
| Try a new model | Try multiple LLMs and use evals to pick the best |
| Split up the step | Decompose the task into smaller steps |
| Fine-tune a model | Fine tune on your internal data to improve performance |

## Developing intuition for model intelligence

- Play with models often
  - Having a personal set of evals might be helpful
  - Read other people's prompts for ideas of how to best use models
- Use different models in your agentic workflows
  - Which models work for which types of tasks?
  - aisuite makes it easy to quickly swap out models

## Development process summary

**Build** ⇄ **Analyze**

- Build
  - Build end-to-end system
  - Improve individual component
- Analyze
  - Examine outputs; traces
  - Build evals; compute metrics
  - Error analysis
  - Component-level evals
