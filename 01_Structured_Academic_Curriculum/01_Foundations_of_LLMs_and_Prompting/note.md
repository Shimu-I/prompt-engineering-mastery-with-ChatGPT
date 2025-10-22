# **Chapter 1 — Frequently Asked Questions (FAQ)**

### **1. What exactly is a Large Language Model (LLM)?**

An LLM is an AI system trained on enormous amounts of text to understand and generate human language. It predicts the next word or phrase based on context, allowing it to answer questions, write, summarize, or reason through problems.

---

### **2. Why are they called “large”?**

Because they contain billions or even trillions of *parameters* — the internal numbers the model learns during training. More parameters mean higher capacity to learn patterns, language nuances, and reasoning structures.

---

### **3. What is a “parameter”?**

A parameter is a learned weight — a numerical value inside the neural network that determines how much influence one piece of data has over another. Collectively, parameters form the “memory” of the model.

---

### **4. What is the Transformer architecture?**

It’s the modern backbone of LLMs. The Transformer introduced **self-attention**, which allows the model to look at all words in a sentence at once and focus on the most relevant parts. This enables deep contextual understanding.

---

### **5. What does “self-attention” mean in simple terms?**

It’s how the model figures out which words are important to each other.

For example, in “The trophy didn’t fit in the suitcase because it was too small,” self-attention helps the model see that “it” refers to *suitcase*, not *trophy.*

---

### **6. What is a token?**

A token is a small piece of text — a word, subword, or punctuation mark.

Models don’t process words directly; they process these tokens as numbers.

---

### **7. What are embeddings?**

Embeddings are numerical representations of tokens that capture meaning. They allow the model to understand relationships — for example, that *king* and *queen* are related, while *banana* is not.

---

### **8. What is a “context window”?**

It’s the maximum amount of text the model can consider at once.

Older models like GPT-3 had 4,000 tokens; newer ones like GPT-4-Turbo can handle 128,000+. Beyond that, earlier context is forgotten.

---

### **9. How does an LLM generate text?**

It predicts one token at a time based on probability. Each new token depends on the ones before it. This is called **auto-regressive generation.**

---

### **10. What is “temperature” in prompting?**

Temperature controls randomness. Lower values (0.1–0.3) make output factual and consistent; higher ones (0.7–1.0) make it more creative and varied.

---

### **11. What is “top-p” or “nucleus sampling”?**

Top-p decides how many potential next words the model considers.

At top-p = 1.0, it considers all options; at 0.8, it limits itself to the top 80 % of likely choices.

---

### **12. What are “presence” and “frequency” penalties?**

They control repetition and topic diversity.

- *Presence penalty* encourages new ideas.
- *Frequency penalty* discourages repeating the same phrases.

---

### **13. What is prompt engineering?**

It’s the practice of writing structured instructions that make an AI perform a specific task accurately, coherently, and safely. It’s the interface between human intent and machine reasoning.

---

### **14. Why does “role” matter in a prompt?**

Roles (e.g., “You are a financial analyst…”) condition the model’s tone, vocabulary, and focus. They narrow behavior to match a professional context.

---

### **15. What are the four essential parts of an effective prompt?**

1. **Role** — defines who the model should be.
2. **Context** — provides background or data.
3. **Instruction** — states what to do.
4. **Constraints** — specify limits, tone, or format.

---

### **16. How do you evaluate whether a prompt works well?**

By checking for **accuracy, coherence, relevance, faithfulness, and creativity** depending on the goal. Professional engineers often test multiple variations and log results.

---

### **17. What causes poor model outputs?**

- Vague instructions.
- Missing or conflicting constraints.
- Overloaded or irrelevant context.
- Lack of explicit structure or formatting.

---

### **18. How do LLMs “hallucinate”?**

When a model lacks sufficient context or is forced to guess, it fabricates plausible but incorrect details. Precision in instructions and factual grounding minimize this.

---

### **19. What is the role of evaluation in prompt engineering?**

Evaluation ensures reliability and helps you measure improvements. Each new version of a prompt should be tested against defined metrics, like accuracy or consistency.

---

### **20. What mindset should a prompt engineer have?**

Treat every prompt as an experiment. Change one factor at a time, observe results, and document outcomes. Consistency and curiosity build expertise faster than intuition alone.

---

# **Chapter 1 Cheat Sheet — Quick Reference**

| **Concept** | **Explanation (Simplified)** | **Example / Key Insight** |
| --- | --- | --- |
| **LLM** | A machine trained to understand and generate language using billions of learned patterns. | ChatGPT, Claude, Gemini |
| **Transformer** | Architecture using self-attention to understand context among all words. | “Attention Is All You Need” (2017) |
| **Self-Attention** | Lets the model see which words matter most to others. | “It” refers to *suitcase*, not *trophy.* |
| **Token** | A small text piece (word, subword, punctuation). | “ChatGPT is great!” → [Chat, G, PT, is, great, !] |
| **Embedding** | Numeric meaning representation of tokens. | “cat” ≈ “dog” in embedding space |
| **Context Window** | How much text the model can consider at once. | GPT-4-Turbo: up to 128 k tokens |
| **Auto-Regressive Generation** | Produces text one token at a time using probabilities. | “The capital of France is → Paris” |
| **Parameter** | A learned weight controlling relationships inside the model. | GPT-3 ≈ 175 B parameters |
| **Temperature** | Controls randomness of output. | 0.2 = focused ; 0.8 = creative |
| **Top-p** | Restricts how many possible next words are considered. | 0.9 = wide choice; 0.6 = narrow |
| **Presence Penalty** | Encourages introducing new ideas. | Avoids repeating same topic |
| **Frequency Penalty** | Prevents repetition of words or phrases. | Stops looping sentences |
| **Prompt Engineering** | Crafting precise instructions to guide LLM behavior. | “You are a data analyst…” |
| **Prompt Components** | Role + Context + Instruction + Constraint. | Defines clear AI behavior |
| **Formatting** | Clean structure improves results. | Use headings, delimiters, JSON |
| **Evaluation Metrics** | Accuracy, coherence, relevance, faithfulness, creativity. | Used to compare prompt versions |
| **Common Mistakes** | Vague, conflicting, or overloaded prompts. | “Write about AI” → too broad |
| **Iteration** | Improve prompts by testing and refining one element at a time. | Adjust temperature, rephrase |
| **Professional Mindset** | Treat prompting like engineering, not chatting. | Observe, measure, improve |

---

### **Practical Memory Rules**

1. **LLM = Text prediction system powered by attention.**
2. **Transformers read all context at once; RNNs read one token at a time.**
3. **Temperature up → creativity up; Temperature down → precision up.**
4. **Prompt = Role + Context + Task + Constraint.**
5. **Good prompting = clear thinking written down.**

---

### **For Interviews**

Be prepared to explain:

- How attention works in simple terms.
- The relationship between temperature and creativity.
- The four parts of a high-quality prompt.
- The difference between tokenization and embedding.
- How to diagnose a poor LLM response.
- What you’d do to make a model more consistent or creative.
