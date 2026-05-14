# Aplicacion de Tensor Networks en modelos de IA para clasificacion de imagenes

Repositorio de trabajo para la memoria de mi Trabajo Fin de Grado en el Grado en Fisica de la Universidad Europea de Madrid.

El proyecto estudia el uso de Tensor Networks (TN) como alternativa o complemento a modelos convencionales de deep learning en clasificacion de imagenes. La idea central es analizar si arquitecturas tensoriales como MPS y TTN pueden convertirse en modelos entrenables, compactos y evaluables sobre un problema visual realista, manteniendo una conexion clara entre teoria, implementacion y resultados experimentales.

## Estado actual

La memoria se encuentra en desarrollo activo. A fecha de la ultima revision del repositorio:

- La introduccion incluye motivacion, estado del arte y planteamiento del problema.
- El marco teorico explica deep learning, tensores, contracciones, notacion diagramatica, descomposiciones tensoriales y topologias MPS, TTN, MERA y PEPS.
- La metodologia describe el pipeline completo de clasificacion: dataset, transformaciones, embeddings, red tensorial, entrenamiento y evaluacion.
- El proyecto experimental descrito en la memoria se centra en ChemEq25, un dataset de material de laboratorio con 25 clases.
- La arquitectura final descrita combina un front-end espacial `AIMPatchEmbedding` con una red jerarquica `HybridCustomTTN`.

Quedan pendientes de cierre academico algunas partes finales de la memoria, especialmente resumen, abstract, agradecimientos, resultados, discusion, conclusiones y anexos.

## Alcance del repositorio

Este repositorio contiene principalmente:

- La memoria LaTeX del TFG.
- Figuras utilizadas en la memoria.
- Bibliografia en BibTeX.

## Estructura del proyecto

```text
.
├── docs/
│   └── thesis/
│       ├── assets/
│       │   └── logo_ue.png
│       ├── chapters/
│       │   ├── 1_preliminares.tex
│       │   ├── 2_indices.tex
│       │   ├── 3_Introduccion.tex
│       │   ├── 4_Objetivos.tex
│       │   ├── 5_Marco_Teorico.tex
│       │   ├── 6_metodologia.tex
│       │   ├── 8_Resultados.tex
│       │   ├── 9_discusion.tex
│       │   ├── 10_conclusiones.tex
│       │   ├── 12_referencias.tex
│       │   └── 13_anexos.tex
│       ├── figures/
│       │   ├── Pipeline_Scheme.png
│       │   ├── confusion_matrix.png
│       │   └── ... figuras de teoria y metodologia
│       ├── output/
│       │   └── main.pdf
│       ├── bibliografia.bib
│       └── main.tex
└── README.md
```

## Capitulos de la memoria

La memoria se organiza en los siguientes bloques:

1. `Preliminares`: resumen, abstract, agradecimientos y tabla resumen.
2. `Introduccion`: motivacion, estado del arte, contexto, planteamiento del problema, planificacion y recursos.
3. `Objetivos`: objetivos generales, especificos, limites del proyecto y beneficios.
4. `Marco Teorico`: fundamentos de deep learning, tensores, Tensor Networks y topologias principales.
5. `Metodologia`: pipeline computacional, dataset, embeddings, MPS, TTN, AIMPatchEmbedding, entrenamiento y diagnosticos.
6. `Resultados`: espacio reservado para resultados finales y comparativas.
7. `Discusion`: espacio reservado para analisis critico de resultados y limitaciones.
8. `Conclusiones`: conclusiones tecnicas y personales.
9. `Referencias` y `Anexos`.

## Bibliografia clave

Las referencias centrales para el estado del arte y el marco teorico son:

- `Tensor Networks Meet Neural Networks: A Survey and Future Perspectives`.
- `Supervised Learning with Quantum-Inspired Tensor Networks`.
- `Deep Tree Tensor Networks for Image Recognition`.
- `Tensor Networks for Dimensionality Reduction and Large-Scale Optimization`.
- `Tensor Decompositions and Applications`.
- `Tensor-Train Decomposition`.
- `Supervised learning with projected entangled pair states`.
- `Computational Complexity of Projected Entangled Pair States`.
- `TensorKrowch: Smooth integration of tensor networks in machine learning`.

La guia interna `docs/Contexto/Guia_bibliografia_estado_arte.md` resume para que sirve cada referencia y que precauciones hay que tener al citarla.

## Compilacion de la memoria

La raiz LaTeX esta en `docs/thesis`.

Compilacion completa recomendada:

```bash
cd docs/thesis
pdflatex -interaction=nonstopmode main.tex
bibtex main
pdflatex -interaction=nonstopmode main.tex
pdflatex -interaction=nonstopmode main.tex
cp main.pdf output/main.pdf
```

Si `latexmk` esta disponible:

```bash
cd docs/thesis
latexmk -pdf main.tex
cp main.pdf output/main.pdf
```

El PDF versionado de referencia queda en:

```text
docs/thesis/output/main.pdf
```

## Requisitos para compilar

Para generar el PDF se necesita:

- Una distribucion LaTeX completa, como TeX Live o MacTeX.
- BibTeX.
- Paquetes LaTeX usados en `main.tex`, entre ellos `babel`, `graphicx`, `hyperref`, `natbib`, `amsmath`, `physics`, `siunitx`, `tensor`, `tabularx`, `booktabs`, `listings` y `quantikz` si esta instalado.

## Convenciones de trabajo

- El archivo principal de la memoria es `docs/thesis/main.tex`.
- Los capitulos se editan en `docs/thesis/chapters/`.
- Las figuras deben colocarse en `docs/thesis/figures/` y referenciarse como `figures/nombre.png`.
- La bibliografia se mantiene en `docs/thesis/bibliografia.bib`.
- Los documentos de contexto estan en `docs/Contexto/` y sirven para conservar decisiones tecnicas, historial y guia bibliografica.
- El PDF final debe actualizarse en `docs/thesis/output/main.pdf` tras compilar.

## Pendientes principales

- Sustituir los textos plantilla de preliminares: resumen, abstract, agradecimientos, dedicatoria y tabla resumen.
- Completar el capitulo de resultados con metricas finales, curvas, matriz de confusion y comparativas.
- Redactar la discusion conectando resultados, limitaciones y decisiones metodologicas.
- Cerrar conclusiones tecnicas y personales.
- Revisar captions, figuras sugeridas y coherencia final de referencias cruzadas.
- Preparar anexos si se decide incluir configuraciones, detalles de ejecucion o material complementario.

## Autor

Manuel Arenas Sanchez

## Contexto academico

Trabajo Fin de Grado en Fisica  
Universidad Europea de Madrid  
Curso 2025-2026
