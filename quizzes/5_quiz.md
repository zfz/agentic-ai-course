# Module 5 Quiz

**Result:** Pass · 10/10 points earned (pass threshold: 8/10)

---

### Question 1
**What distinguishes the planning design pattern from hardcoded workflows in agentic AI systems?**

- Planning enables agents to request user feedback during task execution for better results
- Planning patterns require human approval before executing each step of the workflow
- Planning patterns focus on storing and retrieving information from previous interactions
- ✅ Planning allows agents to dynamically determine the sequence of actions needed for different tasks rather than following predetermined steps

> This captures the key advantage — instead of hardcoding specific sequences, planning lets agents autonomously decide what steps to take based on the specific request, like determining whether to check inventory first or search descriptions first.

---

### Question 2
**What is a key advantage of allowing an LLM to generate and execute code as a form of planning, instead of providing a predefined tool for every possible task?**

- Letting an LLM generate and execute code enables automated reuse of previously generated code snippets to streamline similar future tasks.
- Letting an LLM generate and execute code reduces manual data preparation by automatically handling edge cases and validating inputs in the generated script.
- ✅ Letting an LLM generate and execute code enables flexible, complex planning without needing to predefine specific tools for every task.
- Letting an LLM generate and execute code reduces the occurrence of runtime errors compared to using predefined tools.

> By allowing the LLM to write and execute code, it can leverage the full power of programming languages and libraries to solve a wide variety of tasks without requiring a separate tool for each scenario.

---

### Question 3
**How does planning differ from simply giving an LLM access to multiple tools?**

- ✅ Planning enables the LLM to determine both which tools to use and in what order, rather than just deciding when to call predefined tools
- Planning requires the LLM to use all available tools in a predetermined sequence
- Planning only works when the LLM has access to code execution tools specifically
- Planning eliminates the need for the LLM to have access to any external tools

> With planning, the LLM creates a multi-step strategy that decides the sequence and combination of tool usage, whereas basic tool access only lets the LLM choose whether to call individual tools.

---

### Question 4
**Why might you design a multi-agent system instead of using a single agent for complex tasks?**

- Multi-agent systems automatically run faster because multiple agents work simultaneously
- Multi-agent systems eliminate the need for prompt engineering since each agent has preset instructions
- ✅ Just like hiring a team with different roles, you can focus on building specialized agents for different subtasks rather than one agent trying to do everything
- Multi-agent systems use fewer computational resources than single comprehensive agents

> The lessons use the analogy of hiring people with different roles — a researcher, graphic designer, and writer each have specialized skills, making it easier to develop and manage each part of the system.

---

### Question 5
**What is a key trade-off when adopting planning and multi-agent design patterns in agentic AI systems?**

- Increased flexibility allows narrower task coverage while strengthening developer oversight of multi-agent coordination and performance outcomes
- Increased flexibility in planning and multi-agent workflows simplifies coordination protocols and enhances developer control over agent decisions
- Increased flexibility allows dynamic resource reallocation and improves developer oversight over agent decision-making
- ✅ Increased flexibility allows broader task coverage but reduces predictability and control over agent actions and outcomes

> By allowing agents to plan or coordinate dynamically, you enable them to handle a wider variety of tasks, but you also lose some direct oversight and predictability over their actions and final outputs.

---

### Question 6
**When prompting an LLM to create a plan, what output format is recommended for reliable execution?**

- ✅ JSON format with clearly defined keys and values for each step
- XML format is the only acceptable option for plan generation
- Plain text descriptions that can be easily read by humans
- Markdown format with numbered lists and bullet points

> JSON format allows downstream code to cleanly parse exactly what the steps are, what tools to use, and what arguments to pass, making execution more reliable and unambiguous.

---

### Question 7
**A software development team uses multiple agents: a Code Reviewer that checks for bugs, a Documentation Writer that creates user guides, and a Deployment Agent that handles releases. If they want the Code Reviewer to coordinate the work of the other two agents, which communication pattern would they be implementing?**

- Linear communication, where each agent works sequentially without coordination
- Peer-to-peer communication, where agents share equal status in decision-making
- ✅ Hierarchical communication, where the Code Reviewer acts as a manager directing the other agents
- All-to-all communication, where every agent can communicate with every other agent freely

> In hierarchical communication, one agent (the Code Reviewer) takes a management role, coordinating and directing the work of subordinate agents (Documentation Writer and Deployment Agent).

---

### Question 8
**Which statement best compares the structure and coordination of linear, hierarchical, and all-to-all communication patterns in multi-agent systems?**

- ✅ Linear patterns pass outputs stepwise between agents; hierarchical patterns use a manager to coordinate; all-to-all allows unrestricted agent communication.
- Linear patterns revolve around iterative tasks among participants; hierarchical patterns grant shared authority; all-to-all restricts messaging to specific agent groups.
- Linear patterns forward messages in cycles among agents; hierarchical patterns distribute control equally; all-to-all uses channels for limited coordination.
- Linear patterns prompt each agent to broadcast data; hierarchical patterns rely on peer consensus; all-to-all assigns oversight for collaboration.

> Linear patterns connect agents in a sequence, hierarchical patterns organize agents under a central coordinator, and all-to-all patterns let any agent communicate with any other.

---

### Question 9
**Why is planning with code execution often more powerful than planning with predefined tool calls for data analysis tasks?**

- Code execution provides better error messages when plans fail to execute properly
- Code execution allows agents to store intermediate results more efficiently than tool-based approaches
- ✅ Code execution gives access to hundreds of built-in functions from libraries like Pandas, avoiding the need to create custom tools for every possible data query
- Code execution runs faster than individual tool calls because it processes data locally

> Rather than creating separate tools for each type of analysis (filtering, grouping, calculating statistics), agents can use the rich ecosystem of programming libraries that already contain extensive functionality.

---

### Question 10
**After completing this course on agentic AI workflows, what application building skills have you developed?**

- Design Patterns for Agentic AI systems
- How to let LLMs use tools
- How to create evals and carry out error analysis of Agentic AI workflows
- ✅ All of the above

> Congratulations on making it to the end of the course!
