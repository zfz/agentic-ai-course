# Module 1 Quiz

**Result:** Pass · 10/10 points earned (pass threshold: 8/10)

---

### Question 1
**Which of the following best describes an agentic AI workflow?**

- ✅ A process where an LLM-based app executes multiple steps to complete a task, such as planning, researching, drafting, and revising
- A workflow that requires constant human oversight and manual approval at every step.
- A system where an LLM writes content from start to finish in one go without any revisions or additional steps
- An automated process that only works for simple, repetitive tasks that don't require decision-making

> Agentic AI workflows break complex tasks into smaller steps that are executed iteratively, similar to how humans approach complex work with thinking, research, and revision.

---

### Question 2
**The following describes the four steps of an agentic AI workflow that performs competitor analysis for a new product launch. Which step would require the LLM to have access to a tool in order to complete?**

- Market Position Evaluation - LLM organizes the research into strengths, weaknesses, opportunities, and threats.
- Strategic Recommendations - LLM suggests how to position and launch the product.
- Product Comparison - LLM compares what different competitors offer and how much they charge.
- ✅ Market Research - LLM collects information about competitors, their product offerings, and current market information.

> This step requires web search tools to find real-time information about competitors and markets that the LLM doesn't already know.

---

### Question 3
**Why can agentic workflows achieve better performance than non-agentic approaches in AI applications?**

- Agentic workflows improve performance by using only the most advanced models available for every task.
- Agentic workflows work by eliminating parallelism to ensure tasks are completed in strict sequential order.
- Agentic workflows rely on direct generation to produce immediate results without any additional processing.
- ✅ Agentic workflows enable iterative improvement through reflection and revision, often delivering gains larger than upgrading to newer model generations.

> GPT-3.5 in an agentic workflow can outperform GPT-4 in non-agentic mode, with reflection and revision being key to this improvement.

---

### Question 4
**Which of the following tasks would NOT require an agentic AI workflow to implement effectively?**

- Writing a magazine article on recent developments in electric vehicle batteries by researching current breakthroughs and industry trends.
- Processing customer service inquiries that require checking inventory across multiple product categories and verifying return policies.
- Analyzing expense reports to categorize expenses, verify receipts against company policy, and flag items for manager approval.
- ✅ Writing a product description for a new smartphone based on a list of technical specifications.

> This is a straightforward text generation task that can be completed effectively with direct generation from an LLM without needing multiple steps or tool use.

---

### Question 5
**Which of the following conditions makes an agentic AI workflow harder to implement reliably?**

- The workflow includes human review before final outputs are delivered.
- The workflow processes text-only inputs like emails or documents.
- The task follows a clear step-by-step process that the business already uses.
- ✅ The required steps to complete the task are not known ahead of time and must be planned dynamically.

> When steps aren't predetermined, the agent must plan and solve as it goes, which tends to be harder, more unpredictable, and less reliable.

---

### Question 6
**When decomposing a complex task into steps for an agentic workflow, what is the key question to ask about each individual step?**

- Whether the step requires the most advanced AI model available.
- Whether the step can be completed faster than a human would take.
- Whether the step produces a measurable output for evaluation purposes.
- ✅ Whether the step can be implemented using either an LLM or available tools like APIs and function calls.

> The lessons emphasize this as the key question: "can this step be implemented with either an LLM or with one of the tools such as an API or a function call that I have access to?"

---

### Question 7
**What does "modularity" in agentic workflows allow developers to do?**

- ✅ Replace one RAG system with a different document retrieval system without modifying other parts of the workflow.
- Process multiple web pages simultaneously instead of one at a time.
- Use different LLMs for different steps of the same workflow.
- Run multiple tests with different inputs to check workflow performance.

> This demonstrates modularity's core advantage — the ability to swap out individual components (like changing from one retrieval system to another) while keeping the rest of the workflow unchanged.

---

### Question 8
**According to the task decomposition approach, what should you do if a step in your planned workflow cannot be implemented with either an LLM or available tools?**

- ✅ Break that step down into smaller sub-steps that can each be handled by an LLM or available tools.
- Use the most powerful LLM available and hope it can handle the complex step.
- Skip that step and proceed with the remaining workflow components.
- Redesign the entire workflow to avoid that particular step.

> The lessons emphasize this approach: "how would I as a human do this step? And is it possible to decompose this further or break this down into even smaller steps that then maybe is more amenable to implementation?"

---

### Question 9
**Why is a disciplined evaluation and error analysis process important when developing agentic workflows?**

- ✅ It enables developers to identify specific problems and make targeted improvements through iterative refinement.
- It generates performance reports that demonstrate the workflow's capabilities to stakeholders.
- It provides comprehensive data logs that satisfy regulatory compliance requirements.
- It automates the debugging process so workflows can self-correct without human intervention.

> Systematic evaluation helps pinpoint where workflows fail and guides focused improvements, supporting the iterative development process emphasized in building effective agentic systems.

---

### Question 10
**An agentic workflow for code generation works as follows: First, an LLM writes Python code for a given task. Then, the system runs the code to check for errors. If errors are found, the error messages are fed back to the LLM with instructions to fix the problems. The LLM then generates an improved version of the code. This process repeats until the code runs successfully. Which agentic design pattern is primarily being used in this workflow?**

- Tool use
- ✅ Reflection
- Multi-agent collaboration
- Planning

> This exemplifies the reflection pattern where an LLM examines its own outputs (the generated code) and uses external feedback (error messages) to iterate and improve its work through multiple versions.
