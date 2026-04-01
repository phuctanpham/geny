# GENY Project 
This repository contains the LaTeX source code for the report of the GENY project. The project has been refactored into a modular, clean, and highly maintainable structure to allow team members to collaborate easily without dealing with messy code or formatting conflicts.

## 📂 Project Layout

    📦 geny-project
     ┣ 📂 assets/               # Contains all images, logos, and signatures
     ┃ ┣ 📜 Logo_UIT.svg
     ┃ ┣ 📜 signature_phucpt.png
     ┃ ┣ 📜 signature_vint.png
     ┃ ┗ 📜 signature_truongtm.png
     ┣ 📂 src/                  # Contains all main content files
     ┃ ┣ 📂 libs/
     ┃ ┃ ┗ 📜 setup.tex         # Centralized LaTeX configuration and packages
     ┃ ┣ 📜 geny01.tex          # Appendix 1: Group Contract
     ┃ ┣ 📜 geny02.tex          # Main Content: Full Stack Developer Report
     ┃ ┗ 📜 geny03.tex          # Appendix 2: Meeting Minutes
     ┗ 📜 main.tex              # The Master File (Cover, TOC, and inputs)

## 📄 File Explanations

### 1. `main.tex` (The Orchestrator)
This is the **Master Document**. It contains the official Cover Page and the Table of Contents. It uses the `\input{}` command to stitch all the individual files (`geny01`, `geny02`, `geny03`) together into one cohesive PDF. It relies on the `docmute` package to safely ignore the preambles of the child files when combining them. 

### 2. `src/libs/setup.tex` (The Engine)
This is the single source of truth for all project configurations. It contains:
* All `\usepackage{}` declarations (fonts, spacing, tables, graphics, etc.).
* Global styling rules (margins, link colors).
* Shared Header configurations.
* Custom commands (like `\subsecheading`).
Because every file inputs this setup, changing a font or a margin here instantly updates the entire project.

### 3. `src/geny02.tex` (Main Report)
This file contains the core research report about the **Full Stack Developer** role, including market analysis, salary details, required skills, and JD analysis.

### 4. `src/geny01.tex` & `src/geny03.tex` (Appendices)
* **`geny01.tex`**: Contains the Group Contract (Hợp đồng làm việc nhóm), detailing roles, deadlines, and conflict resolution rules.
* **`geny03.tex`**: Contains the Meeting Minutes (Biên bản cuộc họp), logging the team's discussions and task assignments.

### 5. `assets/` (Media Folder)
A centralized folder for all visual assets. Thanks to the `\graphicspath` and `\svgpath` configurations in `setup.tex`, LaTeX will automatically look inside this folder whenever an image is called, keeping the root directory clean.

## 🚀 How to Compile

**To generate the complete report:**
Compile the `main.tex` file. This will generate the full PDF with the cover, table of contents, main report, and all appendices properly numbered.

**To work on a specific section:**
You can open and compile `src/geny01.tex`, `src/geny02.tex`, or `src/geny03.tex` **independently**. Because each file still has its own `\begin{document}` and imports `libs/setup.tex`, you can preview your specific section without having to compile the entire book. (When you compile `main.tex` later, it will automatically strip their standalone wrappers and merge them perfectly).