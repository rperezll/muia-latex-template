# Plantilla TFM — UAX MUIA

Plantilla LaTeX para el Trabajo de Fin de Máster del **Máster Universitario en Inteligencia Artificial** de la Universidad Alfonso X el Sabio (Business Tech). Adaptada a los requisitos oficiales del TFM (UAX/25-26).

## Demo

En [Demo/main.pdf](Demo/main.pdf) hay una prueba del resultado de la plantilla compilada.

## Ejecución

### Con Docker (recomendado)

Requiere [VS Code](https://code.visualstudio.com/) con la extensión [Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) y Docker instalado.

1. Abre el repositorio en VS Code
2. `Ctrl+Shift+P` → **Dev Containers: Reopen in Container**
3. El entorno se construye sobre `texlive/texlive:latest` con LaTeX Workshop preconfigurado
4. El PDF se compila automáticamente al guardar cualquier `.tex`

### Sin Docker

Requiere TeX Live 2025 con `latexmk`.

```bash
latexmk -pdf main.tex
```

Para limpiar artefactos:

```bash
latexmk -c
```

## Estructura

```
.
├── main.tex                  # Main — orquesta todo el documento
├── Thesis.cls                # Clase del documento — márgenes, cabeceras, estilo
├── cover_asu.tex             # Portada UAX
├── abstract.tex              # Resumen (ES) y Abstract (EN)
├── Bibliography.bib          # Referencias en formato APA
├── Chapters/
│   ├── Chapter1.tex          # Introducción: Justificación + Presentación
│   ├── Chapter2.tex          # Objetivos: General + Específicos
│   ├── Chapter3.tex          # Marco Teórico / Estado del Arte
│   ├── Chapter4.tex          # Marco Metodológico
│   ├── Chapter5.tex          # Análisis, resultados y discusión
│   └── Chapter6.tex          # Conclusiones: Limitaciones + Prospectiva
├── Appendices/
│   └── AppendixA.tex         # Anexos (opcional)
└── Pictures/                 # Imágenes e ilustraciones
```

**`main.tex`** es el único archivo que se compila. Activa o desactiva secciones comentando/descomentando las líneas `\input{}`.

## Licencia

MIT — ver [LICENSE](LICENSE).

## Requisitos UAX

- Extensión: 50.000 – 60.000 palabras
- Citas: formato APA 6ª edición (`\citep{}` entre paréntesis, `\citet{}` en texto)
- Redacción en estilo impersonal: *Se ha realizado…*, *Se parte de…*
