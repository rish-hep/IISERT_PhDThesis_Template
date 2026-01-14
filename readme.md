# PhD Thesis LaTeX Template - IISER Tirupati

This repository contains a modular LaTeX template designed for writing a PhD Thesis in Physics at the **Indian Institute of Science Education and Research (IISER) Tirupati**.

It is pre-configured to meet the formatting requirements regarding margins, font sizes for the cover page, and declaration/certificate text. It utilizes the `subfiles` package for modular writing and `biblatex` for flexible citation management.

---

## Important Disclaimers

### 1. Copyright & Logo
The IISER Tirupati logo included in this template (if present) or intended to be used is the **copyrighted property of the Indian Institute of Science Education and Research Tirupati**. It is used here strictly for academic thesis submission purposes. Users must ensure they have the appropriate rights or permissions to use institutional branding.

### 2. Formatting Compliance
This template was created based on the academic instructions available as of **January 14, 2026**. Academic guidelines are subject to change. **It is the student's responsibility to consult the Academic Office or the official student handbook for the most current formatting rules before submission.** This template serves as a starting point and does not guarantee strict compliance with future regulation changes.

---

## Getting Started

### 1. Personalize Your Data
Open `main.tex`. Scroll down to the **USER DATA** section. Fill in the fields inside the curly brackets `{}`. This will automatically update your Cover Page, Declaration, and Certificate.

\newcommand{\thesistitle}{Title of Your Thesis}
\newcommand{\studentname}{Your Name}
\newcommand{\rollnumber}{20XXXXX}
\newcommand{\supervisorname}{Dr. Supervisor Name}

### 2. Choose Your Font
The instructions require specific Arial-like fonts for the cover page (handled automatically by `helvet`). For the main text, you have options in the **FONT OPTIONS** section of `main.tex`:
* **Default:** Standard LaTeX (Computer Modern) - Best for heavy math/physics.
* **Times New Roman:** Uncomment `\usepackage{mathptmx}`.
* **Palatino:** Uncomment `\usepackage{newpxtext, newpxmath}`.

### 3. Choose Your Citation Style
Go to the **BIBLIOGRAPHY SETUP** section in `main.tex`. You will find three options provided. **Uncomment only one** style:

* **Option 1 (Numbered):** Standard Physics style (e.g., [1], [2-5]).
* **Option 2 (Superscript):** Chemistry/Nature style (e.g., Text¹). Note: Use `\autocite{}` if choosing this.
* **Option 3 (Author-Year):** The style originally requested in the guidelines (e.g., (Einstein, 1905)).

---

## Writing with Subfiles

This template uses the `subfiles` package. This allows you to work on one chapter at a time without compiling the entire thesis.

1.  Navigate to the `chapters/` folder.
2.  Open a file, e.g., `ch1_intro.tex`.
3.  **Compile `ch1_intro.tex` directly.**

It will generate a PDF containing *only* that chapter, but it will maintain the correct numbering, bibliography, and styling from `main.tex`.

---

## Technical Details

### Packages Included
* **geometry:** Sets margins to Left 1.5", Right 1.0", Top 1.0", Bottom 1.0".
* **physics:** Provides easy commands for braket notation, derivatives, and matrices.
* **hyperref:** Automatically creates clickable links in the PDF for citations and the Table of Contents.
* **biblatex:** Handles references (backend must be set to `biber`).

### Compilation
To compile the document locally, ensure you run the standard bibliography chain:
1.  pdflatex main
2.  biber main
3.  pdflatex main
4.  pdflatex main

If using **Overleaf**, this is handled automatically.

---

## Checklist Before Printing
- [ ] Check that `logo.png` is high resolution.
- [ ] Verify the "Month" and "Year" in the User Data section.
- [ ] Ensure the Supervisor and Co-Supervisor names are spelled correctly.
- [ ] Review the `references.bib` file to ensure all citations have the required fields (DOI, Volume, Pages).