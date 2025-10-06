# Contributing Guide

Thank you for your interest in contributing to the **SoK: Preconfirmations** project!  
This guide explains how authors can edit or add content to the **core LaTeX source** (`main.tex`), which generates the main PDF artifact.

---

## 🧭 Overview

All contributions — whether fixing typos, improving explanations, or adding new sections — are welcome.  
This document covers:

1. [Types of contributions](#types-of-contributions)  
2. [Setup & prerequisites](#setup--prerequisites)  
3. [Repository structure](#repository-structure)  
4. [Contribution workflow](#contribution-workflow)  
5. [LaTeX conventions](#latex-conventions)  
6. [Figures, tables, and references](#figures-tables-and-references)  
7. [Review and merge process](#review-and-merge-process)  
8. [License and attribution](#license-and-attribution)  
9. [Communication and code of conduct](#communication-and-code-of-conduct)  

---

## 1. Types of Contributions

You can propose:

- ✏️ **Text updates** – improve clarity, correctness, or structure  
- 📚 **New content** – sections, examples, discussions, or explanations  
- 🧩 **Figures & tables** – visual aids or supporting data  
- 🔍 **References** – bibliographic additions or corrections  
- 🧹 **Minor fixes** – typos, formatting, and consistency improvements  

If it improves readability, precision, or completeness, it’s welcome.

---

## 2. Setup & Prerequisites

You’ll need:

- A working **LaTeX** distribution (TeX Live, MikTeX, or equivalent)  
- `latexmk` for automated builds (recommended)  
- `bibtex` or `biber` for bibliography handling  
- A text editor or IDE with LaTeX syntax support  
- `git` for version control

To build locally:

```bash
latexmk -pdf main.tex
```

This should generate the core PDF (`SoK__Preconfirmations.pdf`).

---

## 3. Repository Structure

```
.
├── main.tex                  # Root LaTeX file
├── manual_references.bib     # Bibliography database
├── figures/                  # Figures and diagrams
├── SoK__Preconfirmations.pdf # Generated PDF (do not edit directly)
└── LICENSE
```

Edit **`main.tex`** and related files only. Avoid manual edits to the compiled PDF.

---

## 4. Contribution Workflow

1. **Fork** this repository  
2. **Create a branch** (e.g. `add-section-intro`, `fix-typos-acknowledgements`)  
3. **Make changes** in `main.tex` and supporting files  
4. **Build locally** to confirm it compiles without errors  
5. **Commit** with a clear message  
6. **Push** your branch to your fork  
7. **Open a Pull Request (PR)** targeting the `main` branch  
8. Engage in review discussions — adjust as needed  
9. Once approved, the maintainers will merge your PR and regenerate the main PDF

🔊 *Keep PRs focused and atomic when possible — separate unrelated changes into different PRs.*

---

## 5. LaTeX Conventions

Please follow these guidelines for consistent style:

- Use standard sectioning commands (`\section`, `\subsection`, etc.)  
- Reference elements with `\label{}` and `\ref{}` (or `\autoref{}`)  
- Add new macros to the preamble, not inline in the document body  
- Introduce new LaTeX packages only if essential — maintain portability

---

## 6. Figures, Tables, and References

- Store figures in `figures/` with clear filenames (e.g. `protocol_flow.pdf`)  
- Use vector formats (`.pdf`, `.eps`) when possible  
- Include figures via `\includegraphics{figures/filename}`  
- Label and reference every figure/table (`\label{fig:…}`)  
- Add citations to `manual_references.bib` and cite via `\cite{key}`  
- Run `bibtex` / `biber` and rebuild to check for missing references  

---

## 7. Review and Merge Process

All PRs are reviewed for:

- ✅ Successful PDF compilation  
- ✅ Consistent formatting and structure  
- ✅ Correct cross-references and citations  
- ✅ Logical accuracy and clarity  

---

## 8. License and Attribution

This project is licensed under **Apache 2.0**.  
By contributing, you agree that your submissions are licensed under the same terms.

- Attribute external sources properly via citations  
- Ensure that any included figures or data respect original licenses  

---

## 9. Communication and Code of Conduct

- Be clear, constructive, and respectful in all discussions  
- Provide context and rationale when proposing edits  

---

💬 **Need help?**  
Open a GitHub Discussion or comment in your Pull Request for feedback.  

---

*Maintained by the Nethermind research team — contributions welcome from the broader Ethereum research community.*
