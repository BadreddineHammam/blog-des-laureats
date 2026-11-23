# Prompt Engineering

# 1. Introduction to LLMs

## 1.1 What is an LLM?

**LLM** means **Large Language Model**.

An LLM is an AI model trained on a large amount of text and other language data. It can understand and generate text, answer questions, explain concepts, and help write code.

**In my own words:**

An LLM is an AI that can help me when I am learning web development. For example, I can ask it to explain PHP, JavaScript, or help me understand an error in my code.

**Example:**

I ask an AI:

"Explain the difference between `let` and `const` in JavaScript."

The AI can explain the difference and give me code examples.

## 1.2 How does an LLM work?

An LLM processes the text I give it and predicts what words or tokens are likely to come next. It uses patterns learned during training to generate a response.

**In my own words:**

When I ask an AI a question, it analyzes my message and generates an answer step by step by predicting what should come next.

**Example:**

I ask:

"Write a JavaScript function that adds two numbers."

The AI may generate:

```javascript
function add(a, b) {
    return a + b;
}
```

It generates this code because it has learned patterns from many examples of programming code.

## 1.3 What is an AI Hallucination?

An **AI Hallucination** happens when an AI generates information that sounds correct but is actually false, inaccurate, or invented.

**In my own words:**

Sometimes AI gives me an answer that looks correct, but when I check it, I discover that it is wrong or that something it mentions does not exist.

**Example:**

I ask an AI:

"Why is my PHP category system not working?"

The AI tells me:

"Your problem is caused by a missing `CategoryManager.php` file."

But my project does not contain that file, and I have not provided evidence that it is needed.

This is a hallucination because the AI invented an explanation.

**Important:** I should always test generated code and verify important information instead of trusting every AI answer.

---

## Quick Summary

| Concept | Simple meaning |
|---|---|
| LLM | An AI model that works with language and generates text. |
| How it works | It predicts likely next tokens to generate a response. |
| AI Hallucination | AI generates false or invented information. |

# 2. The RIO Method

The **RIO Method** is a way to organize a prompt into three important parts: Role, Instruction, and Output.

It helps me give AI clear instructions and explain what I expect from it.

## 2.1 Role (R)

**Definition:** The role tells AI who it should act as and what expertise it should use.

**In my own words:**

I tell AI which professional role it should take before doing the task. This helps it approach my request from the right perspective.

**Example:**

I ask AI:

"Act as an experienced PHP developer."

Now AI knows that I want it to approach my task as a PHP developer.

## 2.2 Instruction (I)

**Definition:** The instruction explains what AI must do and gives it the necessary context, tasks, and rules.

**In my own words:**

I explain exactly what I want AI to do. I can also give it information about my project and rules it must follow.

**Example:**

I ask AI:

"Create a PHP function that validates a category name. My project uses JSON files to store data. Do not use MySQL."

Now AI knows the task and the project rules.

## 2.3 Output (O)

**Definition:** The output explains how I want AI to organize and present its answer.

**In my own words:**

I tell AI what I expect to receive and how I want the answer to look.

**Example:**

I ask AI:

"Show me the complete PHP function, explain each important line, and use simple English."

Now AI knows the format and level of explanation I expect.

## 2.4 Complete Example of the RIO Method

I can combine the three parts into one prompt:

**Role:**
"Act as an experienced PHP developer."

**Instruction:**
"Create a PHP function that validates a category name. My project uses JSON files. Do not use MySQL."

**Output:**
"Show me the complete function and explain it using simple English."

## Quick Summary

| Part | Question | Purpose |
|---|---|---|
| Role (R) | Who should AI act as? | Defines AI's role. |
| Instruction (I) | What should AI do? | Defines the task and rules. |
| Output (O) | What should AI give me? | Defines the expected answer format. |

**Remember:** RIO = Role + Instruction + Output.

It helps me create clearer and more organized prompts.

# 3. Prompt Engineering Patterns

**Definition:** Prompt Engineering Patterns are reusable techniques that help me organize my instructions and guide AI to produce the results I expect.

There are six important patterns:

## 3.1 Persona Pattern

**Definition:** The Persona Pattern gives AI a specific role or professional identity.

**In my own words:**

I tell AI which expert or professional it should act as, so it can approach my task from that point of view.

**Example:**

I ask AI:

"Act as an experienced UI/UX designer. Review my website design and suggest improvements to make it easier to use."

**Purpose:** To give AI a clear role and area of expertise.

## 3.2 Template Pattern

**Definition:** The Template Pattern gives AI a specific structure or format to follow when producing its answer.

**In my own words:**

I show AI how I want the result to be organized instead of letting it choose the structure.

**Example:**

I ask AI:

"Create a bug report using this structure:

- Bug title
- Bug description
- Cause
- Solution"

AI must organize its answer using these four sections.

**Purpose:** To receive organized and consistent results.

## 3.3 Constraint Pattern

**Definition:** The Constraint Pattern defines rules and limits that AI must respect while performing a task.

**In my own words:**

I tell AI what it can and cannot do. This helps me keep the result within my project requirements.

**Example:**

I ask AI:

"Create a contact form using HTML, CSS, and JavaScript.

Rules:
- Do not use external libraries.
- Do not use PHP.
- Keep the code simple.
- Do not change the existing HTML structure."

**Purpose:** To prevent unwanted solutions and respect project rules.

## 3.4 Chain-of-Thought & Step-by-Step Pattern

**Definition:** This pattern asks AI to break a complex task into smaller, ordered steps and explain the important decisions.

**In my own words:**

Instead of asking AI to solve everything at once, I ask it to work through the task step by step so I can understand the process.

**Example:**

I ask AI:

"Help me find why my JavaScript form is not submitting.

Follow these steps:
1. Check the form HTML.
2. Check the JavaScript event listener.
3. Identify the problem.
4. Explain the cause.
5. Suggest a solution."

**Purpose:** To make complex tasks easier to understand and solve.

## 3.5 Few-Shot Pattern

**Definition:** The Few-Shot Pattern provides AI with one or more examples to guide the style, structure, or behavior of its response.

**In my own words:**

I give AI examples of what I want so it can follow the same style when performing a new task.

**Example:**

I give AI this example:

"Input: `john@example.com`

Output: `Valid email`"

Then I ask:

"Using the same format, create examples for invalid email addresses."

AI now has an example to follow.

**Purpose:** To help AI understand the expected result through examples.

## 3.6 Reflective Pattern

**Definition:** The Reflective Pattern asks AI to review and evaluate existing work before suggesting or making changes.

**In my own words:**

Before AI changes my project, I ask it to inspect the existing code, identify problems, and suggest a plan. I can review that plan before allowing changes.

**Example:**

I ask AI:

"Review my PHP category management system.

1. Inspect the relevant files.
2. Identify possible problems.
3. Explain what should be improved.
4. List the files that need changes.
5. Propose an action plan.

Do not modify any files until I approve the plan."

**Purpose:** To review work before making changes and avoid unwanted modifications.

---

## Quick Summary

| Pattern | Main purpose |
|---|---|
| Persona | Give AI a specific role. |
| Template | Give AI a structure to follow. |
| Constraint | Set rules and limits. |
| Chain-of-Thought & Step-by-Step | Break a task into smaller steps with explanations. |
| Few-Shot | Give AI examples to follow. |
| Reflective | Ask AI to review work before making changes. |

**Remember:** Each pattern solves a different problem. I can also combine several patterns in one prompt to give AI clearer instructions.

# 4. Context Engineering

Context Engineering is about preparing and providing the right information to AI so it can complete a task effectively.

It includes five important concepts:

## 4.1 Context Engineering

**Definition:** The process of selecting, organizing, and providing relevant information, instructions, rules, and files that AI needs to perform a task.

**In my own words:**

Before asking AI to solve a problem, I give it the necessary information about my project so it can understand what I am working on.

**Example:**

I ask AI to fix a bug in my PHP category system.

I provide:
- `CategoryService.php`
- `categoryDAO.php`
- `data.json`
- The error message.
- Project rules: Use JSON, do not use MySQL.

This helps AI understand my project before suggesting a solution.

**Purpose:** To give AI the right information instead of unnecessary details.

## 4.2 Context Window

**Definition:** The maximum amount of information an AI model can process at one time.

**In my own words:**

AI has a limited space for processing information. It cannot handle an unlimited amount of text in one context.

**Example:**

I give AI:
- My project instructions.
- Several PHP files.
- Error messages.
- Previous conversation messages.

All this information uses part of the available context window.

**Purpose:** To understand why AI has a limit on how much information it can process at once.

## 4.3 Tokens

**Definition:** Tokens are small units of text that an AI model processes.

A token can be:
- A complete word.
- Part of a word.
- A punctuation mark.

**In my own words:**

When I send a message to AI, the text is processed as tokens. The amount of tokens helps determine how much context is being used.

**Example:**

I send AI this sentence:

"Explain JavaScript arrays."

The sentence is divided into tokens before the model processes it.

**Purpose:** To understand how AI measures the text it processes.

## 4.4 Context Saturation

**Definition:** Context Saturation happens when too much information fills the available context window.

**In my own words:**

If I give AI too many files, instructions, and unnecessary messages, I can use up its available context capacity. This can make it harder to focus on the important information.

**Example:**

I ask AI to fix one PHP bug, but I provide:
- Every file in my project.
- Unrelated CSS and HTML files.
- Old conversations.
- Unnecessary documentation.

Instead, I should provide only the files and information related to the bug.

**Purpose:** To avoid overwhelming the available context with unnecessary information.

## 4.5 Persistent Memory

**Definition:** Persistent Memory is information that can be saved and made available to AI across different conversations through a memory feature.

**In my own words:**

When I start a new conversation, AI does not necessarily know everything from my previous conversation. Persistent Memory can help it retain useful information between sessions.

**Example:**

In one conversation, I explain:

"My PHP project uses JSON files instead of MySQL."

If this information is saved in a memory feature, it may be available in a future conversation without me explaining it again.

**Purpose:** To make useful information available across different conversations.

---

## Quick Summary

| Concept | Simple meaning |
|---|---|
| Context Engineering | Preparing the right information for AI. |
| Context Window | The maximum information AI can process at one time. |
| Tokens | Small units of text processed by AI. |
| Context Saturation | Filling the available context with too much information. |
| Persistent Memory | Saving useful information for future conversations. |

**Remember:** Context Engineering is about giving AI the right information, while the Context Window is about how much information it can process at one time.
# 5. Research Questions

## 5.1 LLM Hallucination and Probabilistic Completion

### What is Probabilistic Completion?

**Definition:** Probabilistic Completion is the process of predicting which token is likely to come next when generating text or code.

**In my own words:**

When I ask AI a question, it uses patterns learned during training to predict what should come next and build an answer.

**Example:**

I ask AI:

"Write a JavaScript function that adds two numbers."

AI generates:

```javascript
function add(a, b) {
    return a + b;
}
```

It generates this code because it has learned common patterns in JavaScript.

### What is an LLM Hallucination?

**Definition:** An LLM Hallucination happens when AI generates information that sounds correct but is false, inaccurate, or invented.

**In my own words:**

Sometimes AI gives me an answer that looks correct, but the information is not true or does not exist.

**Example:**

I ask AI to explain an error in my PHP project.

AI tells me:

"Your problem is caused by a missing `CategoryManager.php` file."

But this file does not exist in my project, and AI has no evidence that I need it.

This is a hallucination.

**Relationship between the two:**

Probabilistic Completion explains how AI generates responses by predicting likely next tokens. Hallucination is one possible result when the generated information is incorrect.

**Important:** I should verify AI-generated information and test its code instead of trusting every answer.

## 5.2 Zero-Shot vs Few-Shot Prompting

These are two approaches to giving instructions to AI.

### Zero-Shot Prompting

**Definition:** Asking AI to perform a task without providing examples.

**In my own words:**

I explain what I want AI to do, but I don't give it an example to follow.

**Example:**

I ask AI:

"Create a JavaScript function that checks whether a number is even or odd."

AI generates a solution without receiving an example from me.

### Few-Shot Prompting

**Definition:** Providing AI with one or more examples to guide its response.

**In my own words:**

I give AI examples of the result I expect so it can follow the same format or style.

**Example:**

I give AI this example:

```text
Input: 4
Output: Even
```

Then I ask:

"Using the same format, create examples for checking whether other numbers are even or odd."

AI now has an example to follow.

### Main Difference

| Zero-Shot | Few-Shot |
|---|---|
| No examples provided. | One or more examples provided. |
| AI works from the instruction alone. | AI uses the instruction and examples. |
| Useful for simple tasks. | Useful when a specific format or style is expected. |

**Important:** Few-Shot gives AI more guidance, but it does not guarantee a correct answer.

## 5.3 Negative Constraints and Reproducibility

### What are Negative Constraints?

**Definition:** Negative Constraints are rules that tell AI what it must not do.

**In my own words:**

I give AI clear limits to prevent it from doing things I don't want in my project.

**Example:**

I ask AI:

"Create a PHP function to save a category."

Rules:
- Do not use MySQL.
- Do not use external libraries.
- Do not change the existing architecture.
- Store the category in a JSON file.

These rules limit the solutions AI can suggest.

### What is Reproducibility?

**Definition:** Reproducibility is the ability to obtain consistent or similar results when repeating the same task under the same conditions.

**In my own words:**

When I ask AI to perform the same task several times with the same instructions, I want the results to follow the same requirements.

**Example:**

I ask AI three times:

"Create a PHP function to save a category. Use JSON and do not use MySQL."

The generated code may be different each time, but all three results should respect the project rules.

### Relationship between Negative Constraints and Reproducibility

Clear negative constraints reduce unwanted variations in AI's responses because they define what the solution must avoid.

**Important:** Constraints can improve consistency, but they do not guarantee identical results every time.

---

## Quick Summary

| Concept | Simple meaning |
|---|---|
| Probabilistic Completion | AI predicts likely next tokens to generate a response. |
| LLM Hallucination | AI generates false or invented information. |
| Zero-Shot | Asking AI without providing examples. |
| Few-Shot | Giving AI examples to follow. |
| Negative Constraints | Telling AI what it must not do. |
| Reproducibility | Getting consistent results under the same conditions. |