---
marp: true
theme: default
paginate: true
style: |
  section {
    font-family: "Segoe UI", Arial, sans-serif;
    background: #f8fafc;
    color: #0f172a;
  }
  h1 { color: #2563eb; }
  h2 { color: #1e293b; }
  strong { color: #2563eb; }
  code { background: #e2e8f0; }
  .lead { text-align: center; }
  .columns {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 40px;
  }
  img { border-radius: 16px; }
---
## Comprendre les LLM, structurer les prompts et maîtriser le contexte

- **Apprenant :** Badreddine Hammam
- **Encadrant :** ESSARRAJ Fouad
- **Établissement :** Solicode Tanger
- **Branche :** `sprint1`
- **Date :** 20 novembre 2026

---

# Prompt Engineering

## Communicate clearly with AI

![width:720px](assets/llm-flow.svg)

---

# What is an LLM?

<div class="columns">

- Large Language Model
- Trained on text and code
- Understands and generates language
- Predicts likely next tokens

**Example**

> "Explain `let` and `const` in JavaScript."

</div>

---

# AI Hallucination

## Confident answer. Incorrect fact.

- AI may invent missing details
- Example: a nonexistent `CategoryManager.php`
- Always test generated code
- Always verify important information

---

# The RIO Method

![width:760px](assets/rio-method.svg)

**RIO = Role + Instruction + Output**

---

# RIO in Practice

### Role

Act as an experienced PHP developer.

### Instruction

Validate a category name. Use JSON. Do not use MySQL.

### Output

Return the complete function and explain each line simply.

---

# Six Prompt Patterns

- **Persona** - define an expert role
- **Template** - define the structure
- **Constraint** - set rules and limits
- **Step-by-Step** - solve in an ordered process
- **Few-Shot** - learn from examples
- **Reflective** - review before modifying

---

# Persona + Constraints

> Act as a UI/UX designer.

Review my website and suggest improvements.

**Constraints**

- Do not add external libraries
- Keep existing HTML structure
- Keep the solution simple

---

# Few-Shot Prompting

### Give one or more examples

```text
Input: 4
Output: Even
```

```text
Input: 7
Output: Odd
```

Now check: **12**

AI follows the demonstrated format.

---

# Context Engineering

## Give AI the right information

- Relevant project files
- Error messages
- Clear project rules
- No unrelated details

The goal is **focus**, not maximum volume.

---

# Context Window

![width:760px](assets/context-window.svg)

**Tokens** are small units of text processed by the model.

---

# Persistent Memory

## Useful context across conversations

Saved fact:

> "My PHP project uses JSON instead of MySQL."

- Reduces repeated explanations
- Saves useful project information
- Only store relevant preferences

---

# Zero-Shot vs Few-Shot

<div class="columns">

## Zero-Shot

- No examples
- Instruction only
- Best for simple tasks

## Few-Shot

- One or more examples
- Specific style or format
- More guidance

</div>

---

# Constraints + Reproducibility

### Negative constraints

Tell AI what it **must not do**:

- No MySQL
- No external libraries
- No architecture changes

### Reproducibility

Similar tasks should produce consistent results
under the same instructions.

---

# Review Before Changing

## Reflective Pattern

1. Inspect relevant files
2. Identify possible problems
3. Explain improvements
4. List affected files
5. Wait for approval

**Do not modify until I approve.**

---

# Key Takeaways

- Define a **role**
- Write a clear **instruction**
- Specify the **output**
- Provide only relevant **context**
- Use examples for specific formats
- Add constraints to reduce unwanted solutions
- Verify important answers and test code