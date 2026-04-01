# GENY Project

[cite_start]This repository contains the LaTeX source code for the report of the GENY group[cite: 23, 234]. The project has been refactored into a modular, clean, and highly maintainable structure to allow team members to collaborate easily without dealing with messy code or formatting conflicts.

## 📂 Project Layout

```text
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