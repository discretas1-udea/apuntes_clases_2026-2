![Built with AI](https://img.shields.io/badge/Built%20with-AI-blue.svg)

# Clase 4 — Tablas de verdad y tipos de proposiciones

> **Fecha**: 18/08/2026 · **Modalidad**: Virtual sincrónica · **Apuntes**: [Diapositivas PDF](./apuntes_clase4.pdf) · [PPT](./apuntes_clase4.pptx) · [Manuscrito anotado](./apuntes_clase4_annotated.pdf)

## Objetivos de la clase

- Repasar los operadores lógicos, sus tablas de verdad y las reglas de prioridad y asociatividad vistas en clases anteriores.
- Enseñar el procedimiento para construir tablas de verdad y aplicarlo a la evaluación de proposiciones compuestas.
- Presentar la clasificación de las proposiciones en tautología, contradicción y contingencia.
- Introducir el concepto de equivalencia lógica y demostrar la primera Ley de De Morgan mediante tablas de verdad.

## Resumen

El profesor retomó los operadores lógicos y las reglas de prioridad y asociatividad, y explicó el procedimiento para construir tablas de verdad, aplicándolo en cuatro ejemplos progresivos. A partir de estos resultados presentó la clasificación de las proposiciones en tautología, contradicción y contingencia, y cerró la sesión introduciendo la equivalencia lógica: demostró la primera Ley de De Morgan y dejó la segunda como tarea. La clase concluyó anunciando que la siguiente sesión abordaría las variantes de las expresiones condicionales.

## Agenda

1. Repaso de los operadores lógicos (negación, conjunción, disyunción inclusiva y exclusiva, condicional y bicondicional) y sus tablas de verdad.
2. Repaso de las reglas de prioridad y asociatividad, con ejemplos de sustitución de valores.
3. Tablas de verdad: definición, pasos para construirlas y convención del curso (1 = Verdadero, 0 = Falso).
4. Ejemplos resueltos de tablas de verdad: `P ∧ ¬P`; `(P → Q) → (¬P ∨ Q)`; `P ∨ S → (Q ∨ ¬P)`; `(P → Q) ∧ (Q → R) → (P → R)`.
5. Clasificación de las proposiciones en tautología, contradicción y contingencia, con ejemplos de identificación.
6. Equivalencia lógica: definición y notación (`p ↔ q` equivale a `p ≡ q`).
7. Demostración mediante tabla de verdad de `¬p ∨ q ≡ p → q`.
8. Demostración de la primera Ley de De Morgan (`¬(p ∧ q) ≡ ¬p ∨ ¬q`); la segunda se dejó como tarea.
9. Identificación de equivalencias lógicas (contrarrecíproco, recíproco e inverso) a partir de una tabla de verdad dada.
10. Anuncio del tema de la próxima clase: variantes de las expresiones condicionales.

## Contenido temático

### 1. Repaso: operadores lógicos y reglas de prioridad

Como introducción, el profesor recordó las tablas de verdad de los seis operadores lógicos vistos en clases anteriores:

| p | q | p ∧ q | p ∨ q | p ⊕ q | p → q | p ↔ q |
|---|---|---|---|---|---|---|
| F | F | F | F | F | V | V |
| F | V | F | V | V | V | F |
| V | F | F | V | V | F | F |
| V | V | V | V | F | V | V |

También se repasó la tabla de prioridad y asociatividad de los operadores, reforzada con ejemplos de sustitución de valores (por ejemplo, con `P = V, Q = F, R = V`, evaluando `P ∧ (Q ∨ R)`):

| Prioridad | Operador | Asociatividad |
|---|---|---|
| 1 (la más alta) | ¬ | No aplica (unitario) |
| 2 | ∧ | Izquierda a derecha |
| 3 | ∨ | Izquierda a derecha |
| 4 | ⊕ | Izquierda a derecha |
| 5 | → | Derecha a izquierda |
| 6 (la más baja) | ↔ | Derecha a izquierda |

### 2. Tablas de verdad: definición, procedimiento y ejemplos

Una tabla de verdad es una herramienta tabular para analizar todos los posibles valores de verdad de una expresión lógica, alternativa a evaluarla directamente. El procedimiento presentado consta de seis pasos:

1. Identificar las variables proposicionales.
2. Determinar el número de filas necesarias: `F = 2ⁿ`, con `n` el número de variables.
3. Construir las columnas de las variables.
4. Agregar columnas auxiliares.
5. Evaluar la expresión lógica paso a paso.
6. Revisar y validar la tabla.

**Convención del curso**: en las tablas de verdad se usa notación binaria de ingeniería — `1` para Verdadero y `0` para Falso.

Se resolvieron cuatro ejemplos progresivos:

- **Ejemplo 1**: `P ∧ ¬P` (1 variable, `F = 2¹ = 2` filas) → resultado: **contradicción**.
- **Ejemplo 2**: `(P → Q) → (¬P ∨ Q)` (2 variables, `F = 2² = 4` filas) → resultado: **tautología**.
- **Ejemplo 3**: `P ∨ S → (Q ∨ ¬P)` (3 variables, `F = 2³ = 8` filas) → resultado: **contingencia**.
- **Ejemplo 4**: `(P → Q) ∧ (Q → R) → (P → R)` (3 variables, `F = 2³ = 8` filas) → resultado: **tautología**.

### 3. Clasificación de las proposiciones

En lógica proposicional, las proposiciones se clasifican según su valor de verdad en todas sus posibles interpretaciones:

- **Tautología**: verdadera en todos los casos posibles.
- **Contradicción**: falsa en todos los casos posibles.
- **Contingencia**: verdadera para ciertas combinaciones y falsa para otras.

Como ejercicio de identificación rápida se clasificaron:

| Expresión | Clasificación |
|---|---|
| `p ∨ ¬p` | Tautología |
| `p ∧ ¬p` | Contradicción |
| `[(¬q ∨ p) → ¬p] ∧ q` | Contingencia |

### 4. Equivalencia lógica

Dos proposiciones compuestas `p` y `q` son lógicamente equivalentes (o simplemente equivalentes) si `p ↔ q` es una tautología. Notación: una equivalencia se escribe como `p ↔ q`, lo que es lo mismo que `p ≡ q`.

Se trabajaron tres ejercicios:

1. Se demostró mediante tabla de verdad que `¬p ∨ q ≡ p → q` (el bicondicional entre ambas resultó ser una tautología).
2. Se demostraron las Leyes de De Morgan: se construyó la tabla de verdad para la primera ley, `¬(p ∧ q) ≡ ¬p ∨ ¬q`, verificando que sus columnas resultan idénticas. La segunda ley, `¬(p ∨ q) ≡ ¬p ∧ ¬q`, quedó **como tarea** para los estudiantes.
3. A partir de una tabla de verdad con las columnas Condicional (`p → q`), Recíproco (`q → p`), Contrarrecíproco (`¬q → ¬p`) e Inverso (`¬p → ¬q`), se identificaron por inspección las equivalencias:
   - `p → q ≡ ¬q → ¬p` (condicional y contrarrecíproco).
   - `q → p ≡ ¬p → ¬q` (recíproco e inverso).

Estas equivalencias dieron pie al anuncio del tema de la siguiente clase: las variantes de las expresiones condicionales.

**Para profundizar y practicar**: [Ver notas teóricas del sitio del curso](https://discretas1-udea.github.io/discretas1-udea-20262/lessons/mod1/clase2/) · [Diapositivas complementarias](https://discretas1-udea.github.io/discretas1-udea-20262/assets/slides/clase2.pdf)

## Pendientes

### Estudiantes

- [ ] Demostrar mediante tabla de verdad la segunda Ley de De Morgan (`¬(p ∨ q) ≡ ¬p ∧ ¬q`), dejada como tarea en clase.
- [ ] Revisar el calendario del curso disponible en la página del curso para consultar los temas vistos y los próximos.
- [ ] Completar el formulario de contacto compartido por el profesor, para conformar la lista de contactos del grupo y facilitar la formación de grupos de trabajo.
- [ ] Estudiar los apuntes de clase disponibles en la plataforma, incluyendo ejercicios de repaso, ejercicios propuestos con respuestas y ejercicios de autoevaluación con solucionario.

## Próxima clase

Se abordarán las variantes de las expresiones condicionales (recíproca, inversa y contrarrecíproca), a partir de un ejemplo con la proposición "si llueve, entonces el patio está mojado".
