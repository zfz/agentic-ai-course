# agentic-ai-course

Notes, assignments, and exercises for the DeepLearning.AI course **Agentic AI** by Andrew Ng (learn.deeplearning.ai).

## Syllabus

**Module 1: Introduction to Agentic Workflows**
- Welcome!
- What is agentic AI?
- Degrees of autonomy
- Benefits of agentic AI
- Agentic AI applications
- Task decomposition: Identifying the steps in a workflow
- Evaluating agentic AI (evals)
- Agentic design patterns
- Optional: Set up your local environment for the ungraded labs
- Module 1 quiz (Graded)
- Try the research agent

**Module 2: Reflection Design Pattern**
- Reflection to improve outputs of a task
- Why not just direct generation?
- Chart generation workflow
- Ungraded Lab: Chart Generation
- Evaluating the impact of reflection
- Using external feedback
- Ungraded Lab: Improving SQL Generation with Reflection
- Module 2 quiz (Graded)
- M2 Graded Lab (Graded Code Assignment)

**Module 3: Tool use**
- What are tools?
- Creating a tool
- Tool syntax
- Ungraded Lab: Turning functions into tools
- Ungraded Lab: Email Assistant Workflow
- Code execution
- MCP
- Module 3 quiz (Graded)
- M3 Graded Lab (Graded Code Assignment)

**Module 4: Practical Tips for Building Agentic AI**
- Evaluations (evals)
- Error analysis and prioritizing next steps
- More error analysis examples
- Component-level evaluations
- Ungraded Lab: Adding a component-level eval to the research workflow
- How to address problems you identify
- Latency, cost optimization
- Development process summary
- Module 4 quiz (Graded)

**Module 5: Patterns for Highly Autonomous Agents**
- Planning workflows
- Creating and executing LLM plans
- Planning with code execution
- Ungraded Lab: Customer Service Agent
- Multi-agentic workflows
- Ungraded Lab: Market Research Team
- Communication patterns for multi-agent systems
- Module 5 quiz (Graded)
- M5 Graded Assignment - Agentic Workflows (Graded Code Assignment)

- Conclusion
- Acknowledgments

## Structure

- `notes/` — per-module summary notes from the course slides
- `quizzes/` — per-module quiz questions and answers
- `assignments/` — course assignment notebooks
- `labs/` — ungraded lab notebooks
- `requirements.txt` — Python dependencies for the labs
- `.python-version` — pyenv-pinned Python version for this project

## Setup

```bash
pyenv local 3.11.9
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

## Key dependency

- `aisuite==0.1.11` — a uniform access layer for LLMs, co-authored by Andrew Ng, giving one consistent Python interface (`ai.Client()`) across multiple LLM providers, with model selection via `"provider:model"` strings (e.g. `"openai:gpt-4o"`, `"anthropic:claude-3-5-sonnet-20240620"`).
