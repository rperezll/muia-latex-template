# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

LaTeX thesis template for **Universidad Alfonso X el Sabio (UAX)**, Business Tech — Máster Universitario en Inteligencia Artificial. Structure follows the official UAX TFM template (UAX/25-26 Plantilla TFM MUIA.docx). Do not modify `Thesis.cls` for layout/aesthetic changes.

## Building

```bash
# Recommended
latexmk -pdf main.tex

# Manual
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

Compiler: pdfLaTeX (TeX Live 2025). Output: `main.pdf`.

## Structure

### Entry point
**`main.tex`** — orchestrates the whole document. Toggle sections by commenting/uncommenting `\input{}` lines.

### Document class
**`Thesis.cls`** — controls all visual style: margins, spacing, headers, chapter formatting. Do not edit for content changes. Metadata variables (`\thesistitle`, `\authors`, `\supervisor`, etc.) are set here.

### Front matter
| File | Purpose |
|------|---------|
| `cover_asu.tex` | Portada UAX (actively maintained) |
| `abstract.tex` | Resumen (ES) + Palabras clave + Abstract (EN) + Keywords |

### Chapters (UAX required structure)
| File | Chapter |
|------|---------|
| `Chapters/Chapter1.tex` | Cap. 1 — Introducción: Justificación + Presentación del proyecto |
| `Chapters/Chapter2.tex` | Cap. 2 — Objetivos: Objetivo general + Objetivos específicos |
| `Chapters/Chapter3.tex` | Cap. 3 — Marco Teórico / Estado del Arte |
| `Chapters/Chapter4.tex` | Cap. 4 — Marco Metodológico (5 subsecciones) |
| `Chapters/Chapter5.tex` | Cap. 5 — Análisis, resultados y discusión (3 subsecciones) |
| `Chapters/Chapter6.tex` | Cap. 6 — Conclusiones: Limitaciones + Prospectiva + Consideraciones finales |

### Back matter
- `Bibliography.bib` — referencias en formato APA (estilo `apalike`)
- `Appendices/AppendixA.tex` — Anexos (opcional, máx. ~20% del total)

## UAX requirements
- **Extensión**: mínimo 50.000 palabras, máximo 60.000
- **Citas**: formato APA (6ª edición) — `\citep{}` para citas entre paréntesis, `\citet{}` para citas en texto
- **Estilo de redacción**: impersonal — *Se ha realizado…*, *Se parte de…*
- **Bibliografía**: estilo `apalike` configurado en `main.tex`

## UAX thesis details
- Grado: Master Universitario en Inteligencia Artificial
- Curso académico: 2025/2026
