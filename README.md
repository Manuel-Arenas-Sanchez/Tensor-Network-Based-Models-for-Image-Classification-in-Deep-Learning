# Tensor-Network-Based Models for Image Classification in Deep Learning

This repository contains the material for my Bachelor's Thesis in Physics at Universidad Europea de Madrid.

## Project Overview

The thesis studies Tensor Networks as an alternative or complementary framework to conventional Deep Learning models for image classification. The current stage of the project focuses on the theoretical background needed to connect:

- Deep Learning fundamentals
- Tensor algebra and tensor contractions
- Tensor Network architectures such as MPS, TTN, MERA, and PEPS
- Their application to supervised image classification

The repository is currently centered on the thesis manuscript. Code and experiments will be added later in a separate project structure.

## Current Status

- Thesis manuscript in active development
- Literature review and theoretical background substantially expanded
- Bibliography under continuous revision
- Experimental and implementation sections still in progress

## Repository Structure

```text
.
├── docs/
│   └── thesis/
│       ├── assets/          # Static resources such as logos
│       ├── figures/         # Figures used in the manuscript
│       ├── output/          # Compiled PDF output
│       ├── bibliografia.bib # BibTeX bibliography
│       └── main.tex         # Main LaTeX source
├── .gitignore
└── README.md
```

## Build Instructions

The manuscript source is located in `docs/thesis/`.

To compile the thesis manually:

```bash
cd docs/thesis
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
cp main.pdf output/main.pdf
```

If `latexmk` is available:

```bash
cd docs/thesis
latexmk -pdf main.tex
cp main.pdf output/main.pdf
```

The versioned PDF snapshot is stored in `docs/thesis/output/main.pdf`.

## Requirements

To compile the manuscript you will need:

- A LaTeX distribution such as TeX Live or MacTeX
- BibTeX
- The LaTeX packages imported in `main.tex`

## Notes

- This repository is intended to track the development of the thesis manuscript.
- Source files and generated output are separated to keep the project easier to navigate.
- Experimental code, datasets, and reproducible training pipelines will be added in future updates.

## Author

Manuel Arenas Sánchez

## Academic Context

Bachelor's Thesis in Physics  
Universidad Europea de Madrid
