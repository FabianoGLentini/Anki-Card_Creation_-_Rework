# Anki Card Creation & Rework — v2.4

> 📝 **Current Version:** v2.4 \
> 🗖️ **Last Updated:** August 1, 2025 \
> 📄 See [`CHANGELOG.md`](./CHANGELOG.md) for full update history.

**Anki Card Creation & Rework** is a custom GPT assistant designed to generate modular, responsive, and well-formatted Anki flashcards using clean, Anki-compatible HTML syntax. It follows best practices for flashcard design to optimize learning outcomes when using active recall and spaced repetition.

The assistant adapts to various subjects — including:

- **Mathematics**: Uses LaTeX for equations and formulas
- **Programming**: Outputs styled code with colors inspired by Visual Studio Code
- **Conceptual Subjects**: Handles summaries, structured notes, and terminology with clear semantic formatting

This assistant was built through hands-on prompt engineering and instructional design using:

- **Meta Prompting**: High-level prompts guiding the assistant's behavior and structure
- **Few-Shot Prompting**: Example-based calibration to establish output consistency
- **Instruction Fine-Tuning**: Iterative tuning of format rules, wording, and visual styling
- **HTML/CSS Design**: Custom-designed templates built with direct HTML/CSS knowledge for Anki compatibility

---

## ✨ Features

- 📋 Modular front/back HTML flashcards for the Anki App
- 🧪 LaTeX support for math and science-heavy content
- 💻 Syntax-colored code examples (e.g., Java, Python, JavaScript)
- 🖼️ Flashcard rework from uploaded images or messy text
- 📚 Accepts course codes, lecture slides, textbook summaries, or full topic prompts
- 🎨 Clear semantic color rules (orange = critical terms, green = supporting info)
- 📈 Follows science-backed flashcard principles to enhance flashcard effectiveness while using spaced repetition

---

## How It Works

This assistant runs directly within [ChatGPT's custom GPT framework](https://chat.openai.com/gpts) — no installation or configuration required.

### Usage Steps

1. **Open the GPT**
   → [Launch Assistant](https://chatgpt.com/g/g-677be93310d0819197dd79ee10475ce5-anki-card-creation-rework-v-2-4)

2. **Provide your input**
   → Summaries, textbook chapters, lecture slides, questions, or even flashcard screenshots. Optionally include:

   - School or course name
   - Course code
   - Topic list or learning goals

3. **Copy the output into Anki**
   → The assistant provides pre-formatted front and back HTML blocks, ready to paste into Anki.

---

## 📂 Repository Contents

| File                                | Description                                        |
| ----------------------------------- | -------------------------------------------------- |
| `assistant_instructions.md`         | Full version 2.4 prompt logic and formatting rules |
| `example_conversations.md`          | Sample use cases with real input/output            |
| `anki_templates/front_example.html` | Sample HTML output for the front of a flashcard    |
| `anki_templates/back_example.html`  | Sample HTML output for the back of a flashcard     |
| `CHANGELOG.md`                      | Version history and update notes                   |

---

## Example Use Cases

- **From a topic summary**:
  "Create flashcards from this overview of SQL filtering operators."

- **From handwritten cards or images**:
  Upload a screenshot or photo and ask to reformat it based on its instructions.

- **From a syllabus or lecture list**:
  Paste a course outline or index and get flashcards for each section.

See [`example_conversations.md`](./example_conversations.md) for real demos.

---

## License

This project is licensed under the [MIT License](./LICENSE).

### 💬 Feedback & Requests

If you have:

- Suggestions for improvement
- Requests for new features
- Questions or bugs

Open an **Issue** on GitHub using the "Issues" tab. You can also discuss new versions, styling feedback, or instructional improvements there.
