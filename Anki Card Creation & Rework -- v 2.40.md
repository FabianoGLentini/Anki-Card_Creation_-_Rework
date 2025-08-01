---
# **Anki Card Creation & Rework -- v 2.4**
---

### **Instructions for Creating Anki Flashcards**

I am creating flashcards to learn new subjects, topics and skill for school or work. I need you to create responsive, human-readable **HTML flashcards** for Anki with a focus on **clarity, readability, and emphasizing key concepts**. The cards must follow a **modular HTML format** for easy direct copy-pasting.

I will provide:

- The School name [Optional]
- Course Code (and or name)
- Topics or information I want to make flashcards from

**Purpose**: Create responsive, human-readable **HTML flashcards** for Anki with a focus on **clarity, readability, and emphasizing key concepts**. The cards must follow a **modular HTML format** for easy direct copy-pasting.

---

## **General Workflow Rules**

1. **Always prioritize modular HTML flashcards** with separate, fully copy-pasteable front and back sections.
   - Avoid formatting the flashcards as large batch documents or for textdoc-based editing unless explicitly requested.
2. **Flashcard-Mode Output Only**: Each card must be a **self-contained pair of HTML blocks**—one for the front and one for the back.
3. Use the terminology:
   - **Active Recall Output**: Modular HTML flashcards for direct use in Anki.
   - **Document Mode**: Reserved only for batch-style editing or when explicitly requested.
4. Avoid any output that introduces context drift, glitches, or unnecessary formatting layers that make the HTML difficult to copy and paste.

---

## **Formatting Rules (Strict Compliance Required)**

> **Important Rule:**
>
> - **Do NOT use `**bold**`markdown or`_italic_` markdown under any circumstances.**
> - **All emphasis must be applied using HTML-based formatting:**
>   - `<span style="color: orange;">...</span>` → **For primary highlights (critical terms).**
>   - `<span style="color: rgb(85, 255, 0);">...</span>` → **For supporting details.**
>   - `<strong>...</strong>` → **For general bold emphasis (only if necessary).**

---

## **Front of Flashcard**

### **1. Content Guidelines:**

- Pose a **clear, concise question** that promotes **active recall**.
- Highlight **key terms** or **important elements**:
  - **Orange (`color: orange`)** → For **primary highlights** or critical terms.
  - **Green (`color: rgb(85, 255, 0)`)** → For **supporting details**.
- **One concept per card** → Avoid cognitive overload.

### **2. Formatting:**

- Each **front of the card** must be provided as an **independent, fully copy-pasteable HTML block**.
- Use this structure:

```html
<div
  style="margin: 15px; line-height: 1.6; font-size: 1rem; word-wrap: break-word; text-align: left;"
>
  <!-- Question Content -->
</div>
```

- Ensure **critical terms** are emphasized with `<span style="color: orange;">...</span>`.

---

## **Back of Flashcard**

### **1. Content Guidelines:**

- Provide **detailed and well-structured answers** with:
  - **Key definitions or explanations** → Highlighted in orange.
  - **Supporting details** → Highlighted in green.
- Use ordered (`<ol>`) or unordered (`<ul>`) lists for structure:
  - `<ul>` → For unordered lists of **key concepts**.
  - `<ol>` → For **steps, examples, or ordered processes**.
- Include examples where applicable to reinforce understanding.

### **2. Formatting:**

- Each **back of the card** must be provided as an **independent, fully copy-pasteable HTML block**.
- Use this structure:

```html
<div
  style="margin: 15px; line-height: 1.6; font-size: 1rem; word-wrap: break-word; text-align: left;"
>
  <b>Key Points to Mention:</b>
  <ul>
    <li>Main point 1</li>
    <li>Main point 2</li>
    <li>Main point 3</li>
  </ul>
  <hr />
  <!-- Detailed Explanation -->
  <ul>
    <li>Key Point 1</li>
    <li>Key Point 2</li>
  </ul>
  <ol>
    <li>Step 1</li>
    <li>Step 2</li>
  </ol>
  <!-- Include LaTeX for math-heavy examples -->
</div>
```

---

### **3. Example Guidelines:**

- Use a **descriptive example** to clarify abstract concepts:
  - Highlight the **Example** heading in **green** using:
    ```html
    <b style="color: rgb(85, 255, 0);">Example:</b>
    ```
  - For **non-programming examples**, use regular text formatting (e.g., `<p>`), NOT a black box.
- **Use a black box only for coding/programming-related examples:**

```html
<div
  style="background-color: black; padding: 10px; font-family: 'Courier New', monospace; border-radius: 5px;"
>
  <!-- Example Code -->
</div>
```

---

## **Code-Based Flashcard Styling (Visual Standards)**

### Use the following visual scheme when formatting Java (or similar) code in Composite Pattern flashcards or similar topics:

| Code Element                                                  | Color (Hex) | Description                              |
| ------------------------------------------------------------- | ----------- | ---------------------------------------- |
| `class`, `public`, `private`, `implements`, `void`, `extends` | `#00BFFF`   | Java modifiers & keywords                |
| Class names                                                   | `#1ABC9C`   | Concrete classes (e.g., `Composite`)     |
| Interface names                                               | `orange`    | Interface references (e.g., `Component`) |
| Data types                                                    | `#6DB3F2`   | `String`, `List`, `ArrayList`, etc.      |
| Method names                                                  | `#FACC15`   | Any declared or called method            |
| Control words                                                 | `#00FFFF`   | `new`, `this`, `for`, etc.               |
| String literals                                               | `#FF7F50`   | Anything in quotes                       |
| Static method calls                                           | `#7CFC00`   | e.g., `System.out.println`               |
| Variables/fields                                              | `#FFFFFF`   | Default white                            |

### Additional Code Styling Notes:

- Always wrap code in:

```html
<div
  style="background-color: black; color: white; padding: 12px; font-family: 'Courier New', monospace; border-radius: 6px;"
>
  <!-- Code goes here with colored spans -->
</div>
```

- Leave `@Override` unstyled (white/default).
- Match code indentation and structure to real Java IDE look (like VS Code).
- Use super-class calls like `super.method()` where appropriate to demonstrate inheritance.

---

## **Placeholder Instruction for Agnostic Code Comments**

### Rule for Empty Code Bodies:

- When showing where logic would exist but want to keep the body general:
  - Insert comment placeholders like:
    ```java
    // ... Perform Task A for this leaf
    ```
  - This comment must be styled as:
    ```html
    <span style="color: rgb(170, 255, 127);">// ... Perform Task A</span>
    ```
- These indicate where user-defined logic would go, but allow the structure to remain reusable and generic.
- These comments should **never replace essential logic like for-loops or conditionals** used consistently in patterns.

---

## **Enhanced Validation Workflow**

### **1. Modular Output Verification:**

- Each flashcard must have:
  - A **separate, copy-pasteable front HTML block.**
  - A **separate, copy-pasteable back HTML block.**
- Avoid any formatting that makes it difficult to copy HTML directly into Anki.

### **2. Readability and Clarity:**

- Ensure text contrast and colors are optimized for readability:
  - Use **black text on light backgrounds** for tables and structured content.
  - Avoid combinations like light text on light backgrounds or dark text on dark backgrounds.

### **3. Final Validation Steps:**

- Test sample output to ensure it meets:
  - **Modular HTML format** (front and back blocks).
  - **Human readability** and direct compatibility with Anki.
  - Proper LaTeX rendering for math-heavy content.

---

## **Avoiding Mode-Switching Issues**

- **Always prioritize Flashcard-Mode Output**, focusing on:
  - Modular HTML front and back sections.
  - Clear, copy-pasteable formatting.
- Use document-mode or batch processing ONLY when explicitly requested.
- Recalibrate immediately if errors in output format are detected (e.g., switching from document-style to modular flashcard formatting).
