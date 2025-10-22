# **Frequently Asked Questions (FAQ)**

### **1. What is a “shot” in prompting?**

A shot means an example. Zero-shot = no examples; few-shot = a few examples inside the prompt.

### **2. What is zero-shot prompting used for?**

For simple, well-known tasks that the model already understands—summarization, translation, explanations.

### **3. What are the weaknesses of zero-shot prompting?**

Inconsistent style, occasional misinterpretation, and lack of control over structure or tone.

### **4. How does few-shot prompting help?**

It shows the model what you expect, aligning tone, reasoning, and output structure through examples.

### **5. What is in-context learning?**

The model’s ability to learn temporarily from examples within a single prompt, without retraining.

### **6. How many examples should I use?**

2–5 for simple tasks; 5–10 for complex reasoning. Balance examples against token limits.

### **7. What makes a good example?**

Clear, representative, correctly formatted, and similar to the task you want performed.

### **8. Can order of examples affect results?**

Yes. Start with simple examples and progress to complex ones—models tend to mirror sequence patterns.

### **9. Why do examples improve model accuracy?**

They reduce ambiguity and show the model exactly what output form and tone you want.

### **10. What happens if examples are inconsistent?**

The model produces mixed or erratic outputs, because it tries to average inconsistent styles.

### **11. Can I combine few-shot with role prompting?**

Absolutely. Define the role first, then include examples—this strengthens both context and consistency.

### **12. What’s the risk of using too many examples?**

You can hit token limits or dilute focus, causing the model to ignore your final instruction.

### **13. What’s the difference between fine-tuning and few-shot prompting?**

Fine-tuning permanently changes model weights; few-shot prompting only conditions behavior temporarily inside one session.

### **14. How do I evaluate success?**

Run multiple trials and score outputs on accuracy, consistency, and style alignment.

### **15. Is few-shot prompting deterministic?**

No—language models are probabilistic, so even with examples, small variations may occur.

### **16. When should I prefer zero-shot?**

For straightforward, familiar tasks or when speed and token efficiency matter.

### **17. When should I prefer few-shot?**

When precision, tone, or consistency is crucial—such as grading, classification, or style control.

### **18. Can I mix few-shot with chain-of-thought reasoning?**

Yes. Provide reasoning examples so the model learns how to explain steps (covered in Chapter 4).

### **19. How do I make few-shot prompts scalable?**

Store examples in templates or scripts, and inject them dynamically with APIs or tools like LangChain.

### **20. How can I minimize bias in examples?**

Use balanced, diverse samples and neutral wording to prevent skewed results.

---

# **Chapter 3 Cheat Sheet — Quick Reference**

| **Concept** | **Definition / Purpose** | **Example / Tip** |
| --- | --- | --- |
| **Shot** | An example inside a prompt. | Few-shot = multiple examples. |
| **Zero-Shot** | Task without examples. | “Summarize this text.” |
| **Few-Shot** | Task with examples. | “Example 1… Example 2… Now do X.” |
| **In-Context Learning** | Model imitates patterns from examples in the same prompt. | Teaches structure & tone. |
| **When to Use Zero-Shot** | Familiar, simple, factual tasks. | Summaries, definitions. |
| **When to Use Few-Shot** | Need stylistic or structural consistency. | Classification, creative tone. |
| **Good Example Rules** | Clear, representative, consistent. | Use 2–5 high-quality samples. |
| **Order of Examples** | Simple → complex. | Models learn pattern flow. |
| **Token Budget** | Total text limit of model. | Keep examples concise. |
| **Prompt Template** | Reusable example pattern with variables. | `Example 1: {input} → {output}` |
| **Evaluation Metrics** | Accuracy, consistency, tone alignment. | Compare zero vs few-shot. |
| **Common Pitfalls** | Too many/weak examples, vague final task. | Always end with clear instruction. |
| **Fine-Tuning vs Few-Shot** | Fine-tuning = retrain; Few-shot = contextual demo. | Few-shot is faster, temporary. |
| **Role + Few-Shot** | Best for professional systems. | “You are a lawyer… Example 1… Now review this case.” |

---

### **Memory Rules**

1. **Zero-shot = command; few-shot = demonstration.**
2. **Examples teach structure, not new facts.**
3. **Short, clear, consistent examples beat long ones.**
4. **Always end prompts with a direct final instruction.**
5. **Think like a teacher: show, then ask.**
