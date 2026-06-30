# 📄 LaTeX Exam Generator Template

A reusable LaTeX framework for creating **Question Sheets**, **Answer Sheets**, and **Instructor Answer Keys** from a single source.

This template is designed for university courses and emphasizes **consistency**, **maintainability**, and **ease of reuse** across different courses and semesters.

> *"The measure of a great teacher is not what they know — but what they awaken in others."*  
---

# ✨ Features

- Generate an entire exam from a single project.
- Produce three documents automatically:
  - 📘 Question Sheet
  - ✍️ Answer Sheet
  - ✅ Answer Key
- Clean and reusable project structure.
- Automatic headers, footers, and exam metadata.
- Configurable answer-space allocation.
- Separate content from formatting.
- AI-friendly workflow using ChatGPT.

---

# 📂 Repository Structure

```text
Project/
│
├── Chapter7_8_Quiz/
│   ├── questions.tex
│   ├── answersheet.tex
│   └── keyanswers.tex
│
├── BZU_LOGO.png
├── LaTeX_Exam_Generator_Template.zip
├── main.tex
├── README.md
└── PROMPT.md
```

---

# 🚀 Quick Start

## 🌐 Online Template

This template is also available as a **read-only Overleaf project**, allowing you to preview, copy, and start using it instantly without downloading the repository.

🔗 **Open in Overleaf:**  
https://www.overleaf.com/read/fxpnxmztwfwq#20ac7e

> To create your own editable copy, open the project and select **Menu → Copy Project** (or use **Copy Project** if prompted). Overleaf allows projects to be shared via read-only links for viewing and copying. :contentReference[oaicite:0]{index=0}

### 1. Open `main.tex`

Update the exam information:

- Department
- Course
- Semester
- Exam title
- Instructor
- Duration
- Total marks

---

### 2. Edit the exam files

Inside the exam folder, edit:

```
questions.tex
answersheet.tex
keyanswers.tex
```

---

### 3. Compile

Compile

```
main.tex
```

The generated PDF will include:

1. Question Sheet
2. Answer Sheet
3. Extra Paper
4. Answer Key

---

# 📁 File Overview

| File | Purpose |
|------|---------|
| `main.tex` | Main LaTeX template and document controller |
| `questions.tex` | Contains the exam questions only |
| `answersheet.tex` | Contains blank answer spaces only |
| `keyanswers.tex` | Contains the instructor solutions only |
| `PROMPT.md` | ChatGPT prompt for generating exam files |
| `BZU_LOGO.png` | University logo used in the header |

---

# 🤖 AI Workflow

This template is designed to work seamlessly with **ChatGPT**.

The recommended prompt is available in

```
PROMPT.md
```

Provide ChatGPT with:

- the complete project (or ZIP file),
- the exam questions,
- and the prompt.

ChatGPT should generate:

```
questions.tex
answersheet.tex
keyanswers.tex
```

while preserving the existing template.

---

# ⚠️ Important

ChatGPT should modify **only**:

```
questions.tex
answersheet.tex
keyanswers.tex
```

It should **never** modify:

```
main.tex
document structure
package imports
page styles
headers
footers
template commands
```

---

# 📚 Creating a New Exam

1. Duplicate an existing exam folder.

Example:

```
Chapter7_8_Quiz
```

↓

```
Chapter9_Quiz
```

2. Replace:

```
questions.tex
answersheet.tex
keyanswers.tex
```

3. Update the input paths inside

```
main.tex
```

Example:

```latex
\input{Chapter9_Quiz/questions}
\input{Chapter9_Quiz/answersheet}
\input{Chapter9_Quiz/keyanswers}
```

4. Update the exam metadata.

Compile again.

---

# 💡 Design Philosophy

The template separates:

- **Content**
- **Formatting**
- **Solutions**
- **Student answer spaces**

This separation makes exams easier to maintain, reuse, and update while keeping the LaTeX source clean and organized.

---

# 🤝 Contributing

Contributions are welcome.

Feel free to:

- improve the template,
- add new layouts,
- enhance formatting,
- fix bugs,
- or suggest new features.

---

# 📜 License

This project is intended for educational use.

You are welcome to use, modify, and share it for teaching and academic purposes.

If you find it useful, a citation or acknowledgment is always appreciated.

---

**Developed with ❤️ by Ruwa AbuHweidi**
