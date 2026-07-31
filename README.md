# Aplicación de Tensor Networks como modelos de Deep Learning para Clasificación de Imágenes

Repositorio final de mi Trabajo Fin de Grado, realizado en el Grado en Física de la Universidad Europea de Madrid durante el curso 2025-2026.

El proyecto estudia la aplicación de **Tensor Networks** como modelos entrenables de *deep learning* para clasificación de imágenes. La memoria combina una revisión teórica de redes tensoriales con el desarrollo experimental de un pipeline de clasificación implementado en PyTorch y TensorKrowch.

En su estado actual, este repositorio funciona como **entrega documental final** del TFG: contiene la memoria en LaTeX, el PDF compilado, la bibliografía y las figuras/resultados necesarios para la versión final del documento.

## Resumen técnico

El objetivo principal fue comprobar si una arquitectura basada en Tensor Networks podía integrarse de forma práctica en un flujo moderno de clasificación de imágenes.

La arquitectura final descrita en la memoria combina:

- `AIMPatchEmbedding`, que procesa la imagen como mapa 2D antes de convertirla en una secuencia;
- `HybridCustomTTN`, una Tree Tensor Network jerárquica con bloques tensoriales y transformaciones intermedias de PyTorch;
- una cabeza lineal de clasificación;
- entrenamiento con `AdamW`, `CrossEntropyLoss`, *warmup*, regularización L2, *label smoothing* y *data augmentation* suave.

El dataset principal fue **ChemEq25**, tratado como problema de clasificación de crops. Las imágenes originales contienen varios objetos de laboratorio, por lo que las anotaciones YOLO se usaron para generar recortes individuales asociados a una única clase.

## Estructura del repositorio

```text
.
├── README.md
├── .gitignore
└── docs/
    └── thesis/
        ├── assets/
        │   └── logo_ue.png
        ├── bibliografia.bib
        ├── chapters/
        │   ├── 1_preliminares.tex
        │   ├── 2_indices.tex
        │   ├── 3_Introduccion.tex
        │   ├── 4_Objetivos.tex
        │   ├── 5_Marco_Teorico.tex
        │   ├── 6_metodologia.tex
        │   ├── 7_Resultados.tex
        │   ├── 8_conclusiones.tex
        │   ├── 9_referencias.tex
        │   └── 10_anexos.tex
        ├── figures/
        │   ├── Experiments_logs/
        │   └── figuras usadas en la memoria
        ├── main.tex
        └── output/
            └── main.pdf
```

La copia compilada de referencia está en:

```text
docs/thesis/output/main.pdf
```

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

El archivo `docs/thesis/output/main.pdf` se mantiene como PDF final de referencia. Los artefactos temporales de LaTeX generados al compilar localmente están excluidos mediante `.gitignore`.

## Compilación en Overleaf

Para trabajar en Overleaf basta con subir el contenido de `docs/thesis/`:

- `main.tex`;
- `bibliografia.bib`;
- `chapters/`;
- `figures/`;
- `assets/`.

El documento usa paquetes habituales de LaTeX científico, entre ellos `babel`, `geometry`, `graphicx`, `booktabs`, `longtable`, `hyperref`, `cleveref`, `natbib`, `amsmath`, `physics`, `siunitx` y `tensor`. Si está disponible, `quantikz` se carga automáticamente; si no, el documento intenta usar `qcircuit` como alternativa.

## Datos, código y experimentos

La memoria describe un pipeline completo de investigación con PyTorch, TensorKrowch, configuraciones YAML, ejecución en servidor HPC y registro de experimentos. En esta versión del repositorio se conserva la **documentación final de la memoria** y las figuras necesarias para justificar los resultados.

No se incluyen:

- el dataset ChemEq25 completo;
- checkpoints de entrenamiento;
- carpetas completas de `runs/`;
- entornos virtuales o dependencias locales;
- bibliografía privada o contexto local ignorado por `.gitignore`.

Las figuras de `docs/thesis/figures/Experiments_logs/` recogen las curvas y matrices de confusión usadas en la memoria final.

## Autoría

- **Autor:** Manuel Arenas Sánchez
- **Titulación:** Grado en Física, Universidad Europea de Madrid
- **Directores:** Alejandro Mata Ali y María Fuencisla Gilsanz Muñoz
- **Curso:** 2025-2026
