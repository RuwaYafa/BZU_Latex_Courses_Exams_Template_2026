# LaTeX Exam Generator Prompt

I have a LaTeX template that automatically generates **three versions** of the same exam from a single source:

1. **Question Sheet** (student exam)
2. **Blank Answer Sheet** (for students to write their solutions)
3. **Answer Key** (for grading)

The template already contains:

* Course and exam metadata
* Page styles and headers
* Automatic question numbering
* Automatic marks display
* Configurable answer-space scaling
* Separate modes for Question Sheet, Answer Sheet, and Answer Key

## Your Task

Whenever I provide an exam, generate **three separate LaTeX files** that fit directly into my template:

### 1. `questions.tex`

This file contains only the exam questions.

Requirements:

* Use the existing `examquestion` environment.
* Use `\questiontext{...}` for all question text.
* Preserve all mathematical notation.
* Do not include solutions.
* Do not manually insert answer spaces.
* Keep the formatting compact and professional.

---

### 2. `answersheet.tex`

This file contains **only blank answer spaces**.

Requirements:

* Do **not** repeat the question statements.
* Create only the answer areas.
* Allocate writing space according to the expected solution length.
* Multiple-choice questions should use a clean answer table.
* Proofs should receive substantially more space.
* Diagram or graph questions should receive extra space suitable for drawing.
* If needed, begin a new page to improve readability.
* The answer sheet should look professional and comfortable for handwriting.

---

### 3. `keyanswers.tex`

This file contains the complete instructor solution.

Requirements:

* Include **only solutions**, never repeat the original question.
* Begin every solution with the final answer (when appropriate).
* Write complete mathematical proofs when required.
* Keep every sub-question independent.
* Use proper mathematical notation throughout.
* Produce polished textbook-quality solutions.

---

## Formatting Rules

* Preserve my LaTeX style.
* Do not modify my template.
* Do not change environments or package usage.
* Do not rename commands.
* Produce code that compiles immediately.
* Do not add explanations outside the requested LaTeX output.
* Use clean, readable mathematical formatting.
* Ensure the output is ready to copy directly into the corresponding files.

Whenever I provide a new exam, generate these three files following the above rules exactly.
