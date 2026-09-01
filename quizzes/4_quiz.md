# Module 4 Quiz

**Result:** Pass · 10/10 points earned (pass threshold: 8/10)

---

### Question 1
**In the initial stages of Agentic AI workflow development, why is building a quick prototype recommended over extensive time spent analyzing and perfecting the system?**

- ✅ It reveals actual error patterns and helps prioritize which components need focused improvement
- It enables comprehensive evaluation suites to be implemented from the start
- It minimizes development costs by avoiding complex architecture
- It immediately creates a production-ready system for user testing

> Building a working prototype allows developers to observe real system behavior, identify common failure modes, and make data-driven decisions about where to invest development effort.

---

### Question 2
**Why is error analysis important when deciding how to improve agentic AI systems?**

- ✅ Error analysis identifies which components cause most problems, allowing you to efficiently prioritize improvements in agentic AI systems.
- Error analysis compiles broad user feedback metrics, guiding occasional adjustments to peripheral modules across multiple domains in agentic AI systems.
- Error analysis quantifies overall system failure rates to determine maintenance schedules in agentic AI systems.
- Error analysis merges system interactions into a generic operational blueprint, helping you unify routine maintenance tasks in agentic AI systems.

> By pinpointing which parts of the system contribute most to errors, you can focus your efforts on areas with the highest impact.

---

### Question 3
**After building a prototype agentic system, what is the primary benefit of creating targeted evaluation sets?**

- To comprehensively test all possible system capabilities before deployment
- To replace the need for manual review of system outputs during development
- ✅ To systematically track improvements in areas where the prototype showed common error patterns
- To document system requirements and interface specifications for stakeholders

> The transcript shows how discovering specific issues (like date extraction errors) leads to building focused evals that can measure progress as you iterate on those particular problems.

---

### Question 4
**A loan approval system has multiple steps: credit score retrieval, income verification, debt-to-income calculation, and final approval decision. After examining traces from rejected applications that should have been approved, which approach best demonstrates proper error analysis?**

- ✅ In the wrongly rejected applications, examine each step's output to count how often credit score retrieval, income verification, or calculations produced subpar results
- Randomly select components to improve based on which ones seem most complex
- Immediately rebuild the entire system from scratch without analyzing individual components
- Focus only on cases where the final decision was correct to understand what worked well

> This matches the systematic trace analysis approach — focusing specifically on failure cases, then examining intermediate outputs of each component to quantify where errors occur most frequently and prioritize improvements.

---

### Question 5
**What is the primary benefit of examining traces and intermediate outputs in agentic workflows?**

- It provides comprehensive documentation for system auditing and compliance requirements
- It eliminates the need for end-to-end evaluation by providing complete system assessment
- ✅ It identifies which specific components are causing errors most frequently, enabling focused improvements
- It automatically fixes identified problems without requiring manual intervention

> Trace analysis reveals where in the workflow problems occur, allowing developers to prioritize fixing the components that contribute most to system failures.

---

### Question 6
**How do end-to-end and component-level evaluations differ?**

- End-to-end evaluations focus on individual components, while component-level evaluations measure overall performance
- ✅ End-to-end evaluations measure the complete workflow's final output, while component-level evaluations test individual parts
- End-to-end evaluations are more accurate than component-level evaluations
- End-to-end evaluations are faster to run than component-level evaluations

> End-to-end evals assess overall system performance, while component-level evals focus on specific components like web search quality or database query accuracy.

---

### Question 7
**A pizza delivery workflow has these measured times: order processing (2s), pizza making (8s), quality check (1s), delivery routing (14s). Based on this timing data, what should be the priority for latency optimization?**

- ✅ Prioritize delivery routing since it takes 14 seconds and offers the largest potential time savings
- Optimize quality check since food safety is the highest priority
- Focus on pizza making since it's the core product creation step
- Start with order processing since customers are waiting from the moment they place orders

> The timing data shows delivery routing consumes the most time, so optimizing this step through better algorithms or route planning would have the biggest impact on getting pizzas delivered faster.

---

### Question 8
**When the email drafting component in your customer service workflow is generating responses that don't follow company tone guidelines, which improvement approach should you try first?**

- ✅ Improve your prompts with clearer tone instructions or add examples of well-written company emails
- Fine-tune a custom model specifically for your company's tone
- Break email drafting into separate steps for content generation and tone adjustment
- Replace the email drafting step with a template-based system

> Prompt engineering is the most accessible and cost-effective first step — adding explicit tone guidelines or few-shot examples can often significantly improve LLM performance.

---

### Question 9
**A food delivery app processes orders through restaurant confirmation, driver assignment, and delivery tracking. After review, you find that 25% of customers complain about "poor communication during delivery." To understand what's causing these complaints, which evaluation approach would be most effective?**

- Subjective evaluation with per-example ground truth
- ✅ Subjective evaluation with no per-example ground truth (apply consistent criteria to evaluate communication quality across all orders)
- Objective evaluation with no per-example ground truth
- Objective evaluation with per-example ground truth

> You'd use human judgment to assess communication quality, and you'd apply the same evaluation criteria to all orders to identify patterns in what's causing poor communication.

---

### Question 10
**In the disciplined development process for agentic AI workflows, what are the two major activities that developers alternate between?**

- Planning (carefully defining strategic objectives for deployment) and monitoring (closely tracking resource consumption to adjust configuration settings).
- ✅ Building (writing code to improve the system) and analysis (examining outputs to decide what to improve next).
- Testing (verifying system reliability through repeated beta trials) and refinement (applying incremental fixes to maintain overall stability).
- Documenting (creating thorough reports for each enhancement) and integration (combining third-party services to manage transitions).

> Developers spend their time both writing code to improve the system and analyzing outputs to determine where further improvement is needed.
