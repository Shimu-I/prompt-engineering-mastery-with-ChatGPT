# **Frequently Asked Questions (FAQ)**

### **1. What is prompt design?**

Prompt design is the structured practice of writing instructions that guide AI models to produce desired outputs with clarity and consistency.

### **2. Why is it called “engineering”?**

Because it involves designing systems and experiments, not casual interaction. You measure, test, and refine systematically.

### **3. What are the key principles of prompt design?**

Clarity, specificity, contextuality, and structure.

### **4. What’s the difference between a “prompt” and a “query”?**

A query is a question; a prompt is a complete instruction, including role, context, and output structure.

### **5. What is role conditioning?**

It’s how a model modifies its style and reasoning when given a persona (e.g., “You are a scientist…”).

### **6. Why do constraints improve performance?**

They reduce uncertainty by narrowing the model’s response space, increasing precision.

### **7. How do you test prompt quality?**

By measuring consistency, accuracy, and relevance across multiple runs.

### **8. Why should prompts be structured?**

Because LLMs interpret text patterns; structured prompts make their task clearer, reducing confusion.

### **9. What happens if a prompt is vague?**

The model improvises—often incorrectly. Vagueness increases hallucination risk.

### **10. What’s a hybrid prompt?**

One that combines styles (instructional + contextual + evaluative) for complex tasks.

### **11. Can prompts include examples?**

Yes. That’s known as **few-shot prompting**, which will be explored in Chapter 3.

### **12. Why do models “hallucinate”?**

When the task is underspecified or context is missing, the model guesses to fill gaps.

### **13. How can formatting improve results?**

Consistent headers, bullet points, and delimiters make it easier for the model to parse intent.

### **14. What’s the difference between persona and role?**

A *role* defines expertise (e.g., lawyer), while a *persona* defines behavioral style (e.g., empathetic, formal).

### **15. Why is iteration important?**

Because prompts rarely work perfectly the first time. Iteration builds precision.

### **16. What’s a feedback loop?**

A process where model output informs the next version of the prompt until optimal results are achieved.

### **17. How can you measure consistency?**

Run the same prompt multiple times. If results vary wildly, it needs clearer constraints.

### **18. What is a schema prompt?**

A prompt that defines exact data structures (like JSON) for the model to follow.

### **19. What’s the fastest way to improve prompting skill?**

Experiment deliberately—change one variable at a time, document, and learn from results.

### **20. What mindset does a good prompt engineer have?**

They think like a scientist: precise, curious, data-driven, and never satisfied with the first result.

---

# **Chapter 2 Cheat Sheet — Quick Reference**

| **Concept** | **Definition / Key Idea** | **Example / Tip** |
| --- | --- | --- |
| **Prompt Design** | Engineering prompts for clarity, precision, and consistency. | Write instructions like specifications, not chat messages. |
| **Core Principles** | Clarity, specificity, context, structure. | Avoid vagueness; define scope. |
| **Role** | Who the model should be. | “You are a business analyst.” |
| **Persona** | The model’s behavior or tone. | “Friendly but formal expert.” |
| **Instructional Prompt** | Directly commands the model. | “Summarize this report.” |
| **Descriptive Prompt** | Requests creative or sensory details. | “Describe a futuristic classroom.” |
| **Interrogative Prompt** | Asks analytical questions. | “Why is context important in NLP?” |
| **Contextual Prompt** | Includes background data. | “Given the dataset below, find trends.” |
| **Hybrid Prompt** | Combines multiple types. | “Review and rewrite for tone and grammar.” |
| **Constraints** | Rules that restrict response. | “Limit to 3 bullet points.” |
| **Schema Prompt** | Enforces data format. | Output JSON or table. |
| **Formatting Tools** | Headers, delimiters, structure. | Use ``` for clarity. |
| **Iteration** | Repeated testing and improvement. | Modify one element per cycle. |
| **Feedback Loop** | Prompt–response–refinement cycle. | Use AI self-analysis. |
| **Evaluation Metrics** | Accuracy, relevance, consistency, tone. | Track results in a table. |
| **Common Mistakes** | Vagueness, missing context, unclear format. | Always specify structure and limits. |
| **Professional Mindset** | Engineer, test, refine, document. | Treat prompts like code. |

---

### **Memory Rules**

1. **LLMs don’t guess your intent—tell them exactly what you want.**
2. **Structure = clarity = accuracy.**
3. **Roles and constraints guide behavior; iteration perfects it.**
4. **Prompt design is not creative writing—it’s precision communication.**
5. **Always test prompts like prototypes—measure, refine, repeat.**
