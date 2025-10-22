# **Chapter 3.0 — Zero-Shot and Few-Shot Prompting**

> “A true prompt engineer doesn’t just tell the model what to do—they teach it how to think through examples.”
> 
> 
> — Senior Prompt Engineering Faculty
> 

---

## **3.1 Understanding Zero-Shot and Few-Shot Prompting**

### **3.1.1 The Concept of “Shots”**

In machine learning and prompt engineering, a **“shot”** refers to an example provided within the prompt itself.

- **Zero-shot prompting** means you give **no examples**—only the task description.
- **Few-shot prompting** means you show **a few examples** of the desired input and output before asking for a new one.

Think of a “shot” like a **demonstration**.

If you ask a model to write a haiku without showing one first, that’s zero-shot.

If you show two sample haikus and then request a new one, that’s few-shot.

---

### **3.1.2 Why It Matters**

Zero-shot and few-shot techniques are how we make **LLMs generalize**.

Since the model can’t “learn” in real time, we teach it through context inside a single prompt.

This is called **in-context learning** — the model temporarily learns from examples you include in the input.

In short:

- Zero-shot = task defined by **instructions alone**.
- Few-shot = task defined by **examples plus instructions**.

---

### **3.1.3 Everyday Analogy**

Imagine teaching someone to fold paper airplanes:

- Zero-shot: you just say, “Fold a paper airplane.”
- Few-shot: you show them 2 or 3 airplanes first.

The second method gives them patterns to imitate—exactly what few-shot prompting does for a language model.

---

## **3.2 Zero-Shot Prompting**

### **3.2.1 What It Is**

**Zero-shot prompting** is the simplest and fastest way to interact with a model.

You give a direct instruction, and the model uses its internal knowledge to complete the task.

**Example:**

> “Summarize this article in one paragraph.”
> 

You provide no examples, only the command.

---

### **3.2.2 When Zero-Shot Works Best**

Zero-shot prompting works when:

1. The task is **common or intuitive** (e.g., summarization, translation).
2. You need a **quick or exploratory answer**.
3. You want the model to **demonstrate general knowledge**.

---

### **3.2.3 Common Limitations**

- Inconsistent style across runs.
- Overly generic outputs.
- Occasional misunderstanding of tone or structure.

Zero-shot prompts rely entirely on the model’s training distribution.

They are powerful for speed, but weak for consistency.

---

### **3.2.4 Example Comparison**

| Type | Prompt | Example Output |
| --- | --- | --- |
| Zero-Shot | “Write a short poem about winter.” | “Snow falls softly on silent streets…” |
| Few-Shot | “Example 1: A brief poem about summer…  Example 2: A short poem about spring…  Now write one about winter.” | “Frosted breath under quiet skies…” |

Few-shot produces more stylistically aligned and coherent results.

---

## **3.3 Few-Shot Prompting**

### **3.3.1 What It Is**

**Few-shot prompting** embeds demonstrations inside the prompt to show the model **how** to perform the task.

Each example serves as a mini training sample.

**Structure:**

```
Example 1:
Input: "I love pizza."
Sentiment: Positive

Example 2:
Input: "I hate traffic jams."
Sentiment: Negative

Now classify:
Input: "Sunsets make me happy."
Sentiment:

```

The model infers the correct label (“Positive”) by imitating the examples.

---

### **3.3.2 Why It Works**

Large language models have the ability to **infer rules from patterns** even within a single prompt.

This phenomenon, called **in-context learning**, allows them to generalize like humans who learn by example rather than code.

Few-shot prompting leverages that capability to control **format**, **tone**, and **output logic**.

---

### **3.3.3 Choosing the Right Number of Shots**

There is no universal rule, but generally:

- 2–5 examples work for small tasks (classification, tone control).
- 5–10 for complex reasoning tasks.

More examples improve consistency—but remember that every example consumes **tokens** within the context window.

---

### **3.3.4 Example Engineering**

Selecting examples is an art form:

1. **Diverse coverage:** Include a range of cases.
2. **Representative quality:** Each example should model the ideal output.
3. **Clarity over quantity:** Three great examples beat ten weak ones.
4. **Order matters:** Put the simplest examples first, and complex ones last.

---

### **3.3.5 Example of Few-Shot Prompt**

```
You are a helpful assistant that classifies feedback as Positive, Negative, or Neutral.

Example 1:
Feedback: "The support team resolved my issue quickly!"
Label: Positive

Example 2:
Feedback: "The website takes too long to load."
Label: Negative

Example 3:
Feedback: "Delivery was fine, nothing special."
Label: Neutral

Now classify:
Feedback: "I’m impressed by how fast the new system is!"
Label:

```

Expected output: **Positive**

---

## **3.4 Context Management in Few-Shot Prompting**

### **3.4.1 Token Budget Awareness**

Every LLM has a **token limit** (context window).

Each example and instruction consumes part of that limit.

For long tasks:

- Use concise examples.
- Truncate unnecessary text.
- Use separate sessions for large datasets.

### **3.4.2 Balancing Context and Instruction**

If the model starts missing the main task, it’s often because:

- Examples dominate the prompt.
- Instructions are buried or unclear.

Always end the prompt with a **clear final instruction**, such as:

> “Now generate a response following the same structure.”
> 

### **3.4.3 Reusable Prompt Templates**

Create reusable patterns with placeholders:

```
Example 1: {input_1} → {output_1}
Example 2: {input_2} → {output_2}
Now generate output for {new_input}.

```

This makes it easier to automate and scale few-shot prompting with code or spreadsheets.

---

## **3.5 Measuring Prompt Effectiveness**

### **3.5.1 Quantitative Evaluation**

You can measure prompt quality using metrics like:

- **Accuracy:** Did it give the correct answer?
- **Consistency:** Do multiple runs produce similar results?
- **Efficiency:** How concise and on-target is the response?

### **3.5.2 Qualitative Evaluation**

Ask yourself:

- Is the reasoning clear?
- Does tone match intent?
- Does the output follow examples faithfully?

Prompt engineering is part science, part craft—evaluation combines both.

---

## **3.6 Project 3 — Few-Shot Text Classifier**

### **Objective**

Build a few-shot classifier that categorizes text based on tone or intent, then compare it to a zero-shot version.

### **Steps**

1. Choose a dataset or topic (e.g., movie reviews, customer feedback).
2. Write a **zero-shot prompt** for classification.
3. Write a **few-shot prompt** with 3–5 labeled examples.
4. Test both using the same inputs.
5. Compare accuracy, tone consistency, and structure.
6. Document insights about performance differences.

### **Deliverable**

A short report (1–2 pages) showing your prompt versions, outputs, and analysis.

**Expected Learning Outcome:**

You’ll understand how examples influence reasoning, and gain practical control over model behavior for analytical tasks.

---
