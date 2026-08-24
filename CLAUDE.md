# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

This is not a software project — it's the class-notes log ("bitácora") for the course **Matemáticas Discretas 1**, Universidad de Antioquia (Ude@), semester 2026-2. There is no code to build, lint, or test. The only artifact type produced here is Markdown (`README.md`) plus the original class materials (PDF slides/handwritten notes, PPTX, Xournal++ `.xopp` files, and images) checked in as sibling files.

Each `clase-0N/` directory holds one class session's materials and, once finalized, a `README.md` summarizing it. `clase-01` through `clase-03` have their `README.md` written; `clase-04` and `clase-05` currently contain only raw materials (PDF/PPTX/`.xopp`) and are pending write-up; `clase-06` is an empty directory with no materials yet; `clase-07` currently has only a `.pptx` file.

The root `README.md` is the course syllabus/schedule (cronograma) — a table of all sessions with links into each `clase-0N/` directory. When a new `clase-0N/README.md` is finalized, the corresponding row in the root table should be updated (notes link, content summary, observations).

## Generating a class README

The authoritative spec for writing `clase-0N/README.md` is **`prompt_maestro_apuntes_clase_v1.2.md`** (root of repo) — always read the latest-numbered `prompt_maestro_apuntes_clase_v*.md` file, since it supersedes older versions kept for history. Key points to internalize before writing or editing a class README:

- **Inputs**: handwritten notes PDF (primary source of truth), Zoom auto-summary (secondary — good for student Q&A tone and per-responsible pending items, not for hard facts), and any other loose materials. Wait for explicit instruction before generating — don't generate speculatively.
- **Fixed structure/order**: `Built with AI` badge → `# Clase N — Title` → metadata blockquote (date(s), modality, links to materials) → Objetivos de la clase → Resumen → Agenda → Contenido temático (conditional) → Datos del docente (conditional) → Medios de comunicación (conditional) → Recursos del curso (conditional) → Evaluación (conditional) → Pendientes (Docente/Estudiantes subsections, omit empty ones) → Próxima clase (omit if unknown, never write a "Por definir" placeholder).
- **Conditional sections only appear when that class actually touched/changed that topic** — do not repeat them every class out of habit.
- **Objetivos** are 2-4 bullets phrased as the instructor's session goals ("Presentar...", "Establecer...", "Definir..."), never as student-facing skills or bare topic names.
- **Agenda** reflects the order things were actually taught (per the handwritten notes), not an idealized slide order. If a class spanned multiple calendar days, split the Agenda by session with `**Sesión N — fecha**` subheadings.
- **Contenido temático** (as of v1.2) is an expanded theory recap organized in numbered `### N. Tema` subsections — explanations, tables/diagrams, formulas, and code actually used in class (never invented examples). Images referenced go in the same `clase-0N/` directory via relative path (`./nombre.png`). Link to the corresponding section of the course's theory site (`discretas1-udea.github.io/discretas1-udea-20262/...`) as a "profundizar" reference, not a replacement for this section.
- **Source-of-truth rule**: the handwritten PDF wins over the Zoom summary on any hard fact (dates, numbers, names). Report — don't silently resolve — any student-relevant discrepancy between sources. Never invent or complete missing data (e.g. a "por definir" exam date stays undefined).
- **Voice**: formal (*usted*) in any student-facing prose; refer to the instructor as "el profesor", never by name, in narrative sections.
- **File layout convention**: each class is `clase-0N/README.md` plus sibling material files (PDF slides, PPTX, annotated manuscript PDF, images) in the same directory, referenced with simple relative paths — no absolute paths or external URLs for files that live in-repo.
- Once a class `README.md` is approved, treat it as finalized: don't retroactively edit it if a later class announces a change (e.g. schedule change) — document the change in the later class's own `README.md` instead.

Two older spec versions (`prompt_maestro_apuntes_clase_v1.md`, `v1.1.md`) are kept in the repo root for history; do not follow them over v1.2.

## Naming conventions observed in the repo

Directory names inconsistently use `clase-0N` (dash) at the top level, but files inside sometimes use `clase0N`/`claseN` (no dash) — follow whatever naming the existing files in that specific directory already use rather than imposing a single convention across the repo.
