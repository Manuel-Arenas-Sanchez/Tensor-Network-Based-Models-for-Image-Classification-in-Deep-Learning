# Aplicación de Tensor Networks como modelos de Deep Learning para Clasificación de Imágenes

Repositorio final de mi Trabajo Fin de Grado, realizado en el Grado en Física de la Universidad Europea de Madrid durante el curso 2025-2026.

El proyecto estudia la aplicación de las **Tensor Networks** como modelos entrenables de *deep learning* para clasificación de imágenes. La memoria combina una revisión teórica de las redes tensoriales con el desarrollo de una arquitectura basada en una *Tree Tensor Network*, entrenada y evaluada sobre ChemEq25, un conjunto de imágenes reales de material de laboratorio, y comparada con una arquitectura convolucional de referencia.

Este repositorio es la **entrega documental** del TFG: contiene la memoria en LaTeX, la bibliografía, las figuras y el PDF compilado. La versión final del documento está en `docs/thesis/output/main.pdf`.

## Compilación local

Para compilar la memoria desde la raíz del repositorio:

```bash
cd docs/thesis
latexmk -pdf main.tex
```

Si no se usa `latexmk`, también se puede compilar con el flujo clásico:

```bash
cd docs/thesis
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

Los artefactos temporales generados al compilar localmente están excluidos mediante `.gitignore`.

## Compilación en Overleaf

Para trabajar en Overleaf basta con subir el contenido de `docs/thesis/`:

- `main.tex`;
- `bibliografia.bib`;
- `chapters/`;
- `figures/`;
- `assets/`.

## Autoría

- **Autor:** Manuel Arenas Sánchez
- **Titulación:** Grado en Física, Universidad Europea de Madrid
- **Directores:** Alejandro Mata Ali y María Fuencisla Gilsanz Muñoz
- **Curso:** 2025-2026
