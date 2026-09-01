# Module 2

## Zero, one, and few-shot prompting

**Zero-shot (no examples)**
```
Convert to MM/DD/YYYY format

Input:
{input_date}
```

**One-shot (single example)**
```
Convert to MM/DD/YYYY format

Input: Jan 1st, 2025
Output: 01/01/2025

Input:
{input_date}
```

**Two-shot (two examples) / Few-shot (multiple examples)**
```
Convert to MM/DD/YYYY format

Input: Jan 1st, 2025
Output: 01/01/2025

Input: 21st June, 2025
Output: 06/21/2025

Input:
{input_date}
```

## Create a dataset of prompts and answers

Pipeline: "Which color of product has the highest total sales?" → LLM ("Generate SQL query") → LLM ("Reflect on V1 SQL, write V2 query") → **execute SQL** → V2 query results → LLM ("Answer question")

| Prompts | Ground truth answer | No reflection | With reflection |
|---|---|---|---|
| Number of items sold in May 2025? | 1201 | 980 | 1201 |
| Most expensive item? | Airflow sneaker | Airflow sneaker | Airflow sneaker |
| How many styles carried? | 14 | 14 | 14 |
| | | **87% correct** | **95% correct** |

Run each time you change reflection prompt

## Using an LLM as a judge

plot.png / plot_v2.png → LLM → "Which image is better?"

Known issues with using LLMs for comparison:
- Answers often not very good
- Position bias — LLM picks A more often (shown with boxed "A" next to "B")

## Grading with a rubric gives more consistent results

Rubric:
```
Assess the attached image against this quality rubric. Each item should receive a
score for 1 (true) or 0 (false). Return the scores for each item as a json object

1. Has clear title
2. Axis labels present
3. Appropriate chart type
4. Axes use appropriate numerical range
5. ...
```

| Input | No reflection | With reflection |
|---|---|---|
| User query 1 | 4 | 6 |
| User query 2 | 5 | 8 |
| ... | ... | ... |
| User query 10 | 5 | 7 |

## Evaluating reflection

- Objective evals
  - Code-based evals are easier
  - Build a dataset of ground truth examples
- Subjective evals
  - Use LLM as a judge
  - Rubric-based grading is better

## Return on investment on prompt engineering

Performance vs. Time spent prompt engineering:
- **No reflection** — rises then plateaus early (lowest curve)
- **With reflection** — breaks off from the no-reflection curve and rises higher before plateauing
- **Reflection with external feedback** — breaks off even higher, plateauing at the highest performance

## Other examples of tools to help reflection

| Challenge | Example | Source of feedback |
|---|---|---|
| Mentioning competitors | Our company's shoes are better than RivalCo | Pattern matching for competitor names |
| Fact checking an essay | The Taj Mahal was built in 1648 | Web search results |
| LLM won't follow output length guidelines | Essay is over word limit | Word count tool |
