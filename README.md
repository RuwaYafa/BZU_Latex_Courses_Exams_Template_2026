````markdown
# 📄 LaTeX Exam Generator Template

A reusable LaTeX framework for creating **Question Sheets**, **Answer Sheets**, and **Instructor Answer Keys** from a single source. The template is designed for university courses and emphasizes consistency, maintainability, and ease of reuse across different semesters.

> *"The measure of a great teacher is not what they know — but what they awaken in others."*  
> **— Ruwa AbuHweidi**

---

## ✨ Features

- Generate three exam documents from one project:
  - 📘 Question Sheet
  - ✍️ Answer Sheet
  - ✅ Answer Key
- Reusable for different courses and semesters.
- Consistent page layout and formatting.
- Automatic headers, footers, and exam metadata.
- Configurable answer-space allocation.
- AI-friendly workflow for generating exam content.

---

## 📂 Repository Structure

```text
Project/
│
├── Chapter7_8_Quiz/
│   ├── questions.tex
│   ├── answersheet.tex
│   └── keyanswers.tex
│
├── BZU_LOGO.png
├── main.tex
├── README.md
└── PROMPT.md
```

---

## 🚀 Quick Start

1. Open `main.tex`.
2. Update the exam metadata (course, semester, instructor, duration, etc.).
3. Edit or generate:
   - `questions.tex`
   - `answersheet.tex`
   - `keyanswers.tex`
4. Compile `main.tex`.

The generated PDF will contain:

1. Question Sheet
2. Answer Sheet
3. Extra Paper
4. Answer Key

---

## 🤖 AI Integration

This repository is designed to work seamlessly with ChatGPT.

The recommended prompt is provided in:

```text
PROMPT.md
```

Provide ChatGPT with the project (or ZIP file) together with `PROMPT.md`, and it will generate or update:

- `questions.tex`
- `answersheet.tex`
- `keyanswers.tex`

without modifying the template itself.

---
````

## File Descriptions

### `main.tex`

This is the main LaTeX template file.

It controls:

* Exam metadata
* Page layout
* Headers and footers
* Question sheet generation
* Answer sheet generation
* Answer key generation
* Page styles
* Logo and course information

In most cases, this file should not be changed except for exam metadata.

Typical metadata includes:

```latex
\newcommand{\Department}{Computer Science Department}
\newcommand{\CourseCodeName}{COMP233-Discrete Mathematics}
\newcommand{\Semester}{Spring 2026}
\newcommand{\ExamDetails}{Section \#4 | Quiz\#2 | Chapters 7,8.1}
\newcommand{\Duration}{40 Minutes}
\newcommand{\TotalMarks}{100}
\newcommand{\weight}{10}
\newcommand{\InstructorName}{Instructor Name}
```

---

### `Chapter7_8_Quiz/questions.tex`

This file contains the exam questions only.

It should include:

* Multiple-choice questions
* Written questions
* Proof questions
* Definitions
* Mathematical expressions
* Any question text students need to see

It should not include:

* Solutions
* Instructor notes
* Blank answer spaces
* Answer key content

---

### `Chapter7_8_Quiz/answersheet.tex`

This file contains the blank answer sheet only.

It should include:

* Answer tables for multiple-choice questions
* Blank spaces for written answers
* Larger spaces for proofs
* Extra space for diagrams or graphs when needed

It should not repeat the full question statements.

The goal is to give students a clean and comfortable place to write their answers.

---

### `Chapter7_8_Quiz/keyanswers.tex`

This file contains the full instructor answer key.

It should include:

* Final answers
* Complete solutions
* Clear mathematical reasoning
* Proofs where required
* Independent solutions for each question or sub-question

It should not repeat the full question statements unless absolutely necessary.

---

### `BZU_LOGO.png`

This file is the logo used in the exam header.

Make sure the image filename matches the name used in `main.tex`.

For example:

```latex
\includegraphics[width=4cm]{BZU_LOGO}
```

---

### `PROMPT.md`

This file contains the AI prompt used to generate or update the exam files.

The prompt should instruct the AI to generate:

* `questions.tex`
* `answersheet.tex`
* `keyanswers.tex`

while preserving the existing LaTeX template.

This file is useful when sharing the project with other instructors or teaching assistants.

---

## Recommended Workflow

### Step 1: Edit Exam Metadata

Open `main.tex` and update the exam information:

```latex
\newcommand{\CourseCodeName}{COMP233-Discrete Mathematics}
\newcommand{\Semester}{Spring 2026}
\newcommand{\ExamDetails}{Section \#4 | Quiz\#2 | Chapters 7,8.1}
\newcommand{\Duration}{40 Minutes}
\newcommand{\TotalMarks}{100}
\newcommand{\InstructorName}{Instructor Name}
```

---

### Step 2: Write or Generate `questions.tex`

Add the exam questions inside:

```text
Chapter7_8_Quiz/questions.tex
```

This file should contain the questions only.

---

### Step 3: Write or Generate `answersheet.tex`

Add the blank answer sheet inside:

```text
Chapter7_8_Quiz/answersheet.tex
```

This file should provide suitable writing space for each question.

---

### Step 4: Write or Generate `keyanswers.tex`

Add the instructor solutions inside:

```text
Chapter7_8_Quiz/keyanswers.tex
```

This file should contain the complete answer key.

---

### Step 5: Compile `main.tex`

Compile the project from:

```text
main.tex
```

The output PDF will include:

1. Question Sheet
2. Answer Sheet
3. Extra Paper
4. Answer Key

---

## Using the Template with ChatGPT

This project is designed to work well with ChatGPT.

When using ChatGPT, provide:

1. The exam questions
2. The project files or ZIP file
3. The prompt from `PROMPT.md`

Then ask ChatGPT to generate or update:

```text
questions.tex
answersheet.tex
keyanswers.tex
```

Important instruction:

ChatGPT should only modify these three files:

```text
Chapter7_8_Quiz/questions.tex
Chapter7_8_Quiz/answersheet.tex
Chapter7_8_Quiz/keyanswers.tex
```

ChatGPT should not modify:

```text
main.tex
BZU_LOGO.png
page styles
package imports
template commands
document structure
```

---

## Important Notes

* Do not place full solutions inside `questions.tex`.
* Do not repeat long question statements inside `answersheet.tex`.
* Do not place blank answer spaces inside `keyanswers.tex`.
* Keep each file focused on its purpose.
* Always compile from `main.tex`.
* If a new exam folder is created, update the `\input{...}` paths in `main.tex`.

For example:

```latex
\input{Chapter7_8_Quiz/questions}
\input{Chapter7_8_Quiz/answersheet}
\input{Chapter7_8_Quiz/keyanswers}
```

---

## Creating a New Exam

To create a new exam:

1. Duplicate the folder:

```text
Chapter7_8_Quiz
```

2. Rename it, for example:

```text
Chapter9_Quiz
```

3. Replace the content of:

```text
questions.tex
answersheet.tex
keyanswers.tex
```

4. Update the input paths in `main.tex`:

```latex
\input{Chapter9_Quiz/questions}
\input{Chapter9_Quiz/answersheet}
\input{Chapter9_Quiz/keyanswers}
```

5. Update the exam metadata in `main.tex`.

---

## Minimal Example

### `questions.tex`

```latex
\begin{examquestion}{1}{10}
\questiontext{
Choose the correct answer:

\begin{enumerate}[label=\textbf{(\alph*)}]
    \item The function $f:\mathbb{Z}\to\mathbb{Z}$ defined by $f(n)=2n+1$ is:
    \begin{tasks}(2)
        \task onto but not one-to-one
        \task one-to-one but not onto
        \task both one-to-one and onto
        \task neither one-to-one nor onto
    \end{tasks}
\end{enumerate}
}
\end{examquestion}
```

---

### `answersheet.tex`

```latex
\noindent\textbf{Question 1 (10 Marks):}\\
Fill your final answer clearly in the table below.

\vspace{0.3cm}
\renewcommand{\arraystretch}{2.2}
\begin{tabularx}{\textwidth}{|p{2cm}|>{\centering\arraybackslash}X|}
\hline
\textbf{Question} & \textbf{1} \\ \hline
\textbf{Answer} & \\ \hline
\end{tabularx}
```

---

### `keyanswers.tex`

```latex
\section*{Question 1}

\textbf{Answer: b) one-to-one but not onto.}

Let $f:\mathbb{Z}\to\mathbb{Z}$ be defined by $f(n)=2n+1$.

If $f(a)=f(b)$, then
\[
2a+1=2b+1.
\]
Thus,
\[
a=b.
\]
Therefore, $f$ is one-to-one.

However, $f$ is not onto because $f(n)=2n+1$ is always odd.

Therefore,
\[
\boxed{\text{$f$ is one-to-one but not onto.}}
\]
```

---

## Troubleshooting

### The logo does not appear

Check that the logo file name is exactly:

```text
BZU_LOGO.png
```

and that `main.tex` uses:

```latex
\includegraphics[width=4cm]{BZU_LOGO}
```

---

### The exam does not compile

Check the following:

* All braces `{}` are closed.
* All environments are properly ended.
* The input paths in `main.tex` are correct.
* The folder name matches exactly.
* The file names are correct.

---

### The answer sheet is too short

Increase the blank space in `answersheet.tex`, for example:

```latex
\vspace*{8cm}
```

or adjust the global scale in `main.tex`:

```latex
\newcommand{\AnswerSpaceScale}{7}
```

---

## Best Practices

* Keep `main.tex` stable.
* Put all exam content inside the exam folder.
* Use clear folder names.
* Keep the answer sheet clean and readable.
* Give proofs enough writing space.
* Keep the answer key complete but concise.
* Test compile before sharing the exam.

---

## License

This template may be used, modified, and shared for educational purposes.

```
```
