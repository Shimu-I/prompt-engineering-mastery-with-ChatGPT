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
