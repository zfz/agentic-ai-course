# Module 2 Quiz

**Result:** Pass · 10/10 points earned (pass threshold: 7/10)

---

### Question 1
**In agentic AI workflows, what is the core mechanism of the reflection design pattern?**

- An LLM waits for human feedback before making any revisions to its initial output
- ✅ An LLM examines and critiques its own output, then generates improved versions, similar to how humans edit their work
- An LLM combines multiple different model outputs into a single consolidated response
- An LLM generates multiple random variations of output and selects the best one automatically

> The reflection pattern has LLMs review their own outputs and produce revised drafts, much like a human reading over an email and making improvements before sending it.

---

### Question 2
**Why does incorporating external feedback into the reflection process often lead to greater improvements in LLM-generated outputs compared to relying only on internal reflection?**

- Acquiring external feedback hinders reflection processes, prompting LLMs to fixate on trivial modifications and overlook improvements needed for accuracy.
- ✅ Incorporating external feedback provides new information, enabling LLMs to identify and correct issues they cannot detect internally.
- Incorporating external feedback introduces overly broad revisions, causing LLMs to ignore relevant domain insights derived from their initial output.
- Injecting external feedback dilutes important design elements, often making LLMs less attentive to subtle issues in their own reasoning.

> External feedback introduces facts or signals unavailable to the LLM itself, allowing more effective and targeted improvements.

---

### Question 3
**How does the reflection design pattern leverage multimodal capabilities when generating charts?**

- The LLM translates user requests into detailed plotting instructions for a separate model
- ✅ The LLM visually examines the generated chart to identify flaws and suggest better visualization types
- The LLM critiques only the Python code without examining the visual output
- Multimodal reflection only makes minor aesthetic adjustments to existing charts

> Multimodal LLMs can use visual reasoning to analyze the actual chart output and identify issues like unclear stacked bar plots, then suggest clearer alternatives like regular bar graphs.

---

### Question 4
**What is the recommended approach for evaluating subjective LLM outputs like chart quality?**

- Train a separate model specifically for judging output quality
- Ask the LLM to compare two outputs and choose which is better
- ✅ Use a rubric with specific binary criteria to evaluate individual outputs, then sum the scores
- Have the LLM rate outputs on a 1-5 scale for overall quality

> Binary yes/no criteria for individual items (like "Does the plot have a clear title?") provide more consistent results than comparisons or numerical scales.

---

### Question 5
**Why might a developer choose different LLMs for the initial code generation versus the reflection step?**

- Reflection requires models that can access external databases and APIs
- ✅ Different LLMs have different strengths, with some models being better at finding bugs during reflection
- The same model cannot be used for both generation and reflection in a single workflow
- Only reasoning models can execute code to check for errors

> Different LLMs have different strengths, and some models like reasoning models are particularly good at finding bugs.

---

### Question 6
**What is a potential drawback of implementing reflection in agentic workflows?**

- Reflection increases the risk of LLMs generating contradictory information
- Reflection requires much more powerful LLMs than direct generation
- ✅ Reflection can slow down the system by requiring additional LLM calls
- Reflection eliminates the need for prompt engineering, reducing control over outputs

> The lessons directly state that reflection "does slow down the system a little bit by needing to take an extra step" — this is the key trade-off developers must consider.

---

### Question 7
**To improve factual accuracy in a blog post through reflection, which external feedback would be most effective?**

- A sentiment analysis tool to assess emotional tone
- A word count utility to verify text length
- ✅ A web search tool to cross-reference claims against reputable sources
- A grammar checker to flag linguistic errors

> Web search allows the system to fact-check statements by comparing them against trusted external sources, directly addressing factual accuracy.

---

### Question 8
**An LLM generates instructions for "how to set up a home Wi-Fi network" but the steps have gaps that could confuse users. How would reflection best address this issue?**

- ✅ Prompt the reflection model to check the instructions for completeness and missing steps
- Have the reflection model translate the instructions into multiple languages
- Have the reflection model rewrite the instructions in a more formal tone
- Use the reflection model to shorten the instructions to make them more concise

> Using reflection to check instructions for coherence and completeness can help spot missing procedural steps that would confuse users trying to follow the process.

---

### Question 9
**An LLM generates email copy for a marketing campaign, but it sometimes includes competitor mentions which violates company policy. What external feedback tool would best help the reflection process address this issue?**

- ✅ A pattern matching tool that searches for competitor mentions in the generated text
- A sentiment analysis tool to ensure the email tone is professional
- A grammar checker to improve the writing quality of the email
- A web search tool to verify information about the company's products

> Remember using "regular expression pattern matching to search for competitors' names in the output" as external feedback that can flag policy violations and prompt the LLM to rewrite without mentioning competitors.

---

### Question 10
**Which task would require using an LLM as a judge when evaluating reflection performance?**

- Determining whether a generated database query returns the correct business data
- ✅ Assessing how engaging a marketing slogan sounds to potential customers
- Checking whether an email contains the correct recipient address and subject line
- Verifying if generated Python code produces the expected numerical output

> Engagement is subjective and would require LLM-as-judge evaluation with specific criteria since there's no objective right/wrong answer.
