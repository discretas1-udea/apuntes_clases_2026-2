![Built with AI](https://img.shields.io/badge/Built%20with-AI-blue.svg)

# Clase 06 — Argumentación lógica

> **Fecha**: 27/08/2026 · **Modalidad**: Virtual sincrónica · **Apuntes**: [Diapositivas PDF](./apuntes_clase6.pdf) · [PPT](./apuntes_clase6.pptx) · [Manuscrito anotado](./apuntes_clase6_annotated.pdf)

## Objetivos de la clase

- Presentar el concepto de argumento lógico (premisas y conclusión) y sus tres formas de representación: estándar, tautología y simbólica.
- Definir la validez de un argumento y establecer el procedimiento para verificarla mediante el enfoque basado en modelos (tablas de verdad), incluyendo la identificación de renglones críticos.

## Resumen

La clase presentó la argumentación lógica: la definición de argumento (premisas y conclusión), sus tres formas de representación y la validez de un argumento mediante el enfoque basado en modelos (tablas de verdad), con varios ejemplos resueltos, incluyendo el caso clásico de Sócrates. La sesión cerró anunciando la continuación del tema con el enfoque axiomático (silogismo y reglas de inferencia) para la siguiente clase.

## Agenda

1. Ubicación de la argumentación lógica en el mapa de tipos de demostración (equivalencia, vista en la clase anterior, frente a validez, tema de esta sesión) y de los dos métodos disponibles para demostrar validez: el enfoque basado en modelos (tema de hoy) y el enfoque axiomático (anunciado para la siguiente sesión).
2. Presentación de la expresión condicional como base del argumento matemático (premisa/hipótesis/antecedente → conclusión/tesis/consecuente) y de los dos métodos para construir argumentos matemáticos.
3. Definición formal de argumento en lógica proposicional (premisas y conclusión) y de sus tres formas de representación: estándar o vertical, tautología y forma simbólica.
4. Definición de argumento válido, ilustrada con la traducción a lenguaje formal del ejemplo clásico de Sócrates.
5. Procedimiento de validación de argumentos mediante tabla de verdad (identificar premisas y conclusión, construir la tabla, verificar los renglones críticos) y resolución de un primer ejemplo con tres premisas (no válido).
6. Tabla de adverbios o conectores que indican premisa o conclusión en lenguaje natural.
7. Resolución de dos ejemplos adicionales de validación mediante tabla de verdad: el argumento "del sombrero" sobre `2 = 3` (no válido) y un argumento con variables `A`, `B` y `C` (válido).

## Contenido temático

### 1. El argumento matemático y los métodos de demostración

El profesor ubicó la argumentación lógica dentro del mapa general de tipos de demostración presentado en la clase anterior: una demostración puede referirse a la **equivalencia** de proposiciones (tema de la clase anterior) o a la **validez** de argumentos (tema de esta clase), y para cada una existen dos métodos posibles: el **enfoque basado en modelos** (tablas de verdad) y el **enfoque axiomático** (axiomas / identidades lógicas). En esta sesión se trabajó la validez con el enfoque basado en modelos; el enfoque axiomático quedó anunciado para la siguiente sesión.

El punto de partida es la pregunta "¿Cuándo un argumento matemático es correcto?", que se responde a partir de la expresión condicional `P → Q`, donde `P` (premisa, hipótesis o antecedente) implica `Q` (conclusión, tesis o consecuente):

| P (Premisa) | Q (Conclusión) | P → Q |
|---|---|---|
| F | F | V |
| F | V | V |
| V | F | **F** |
| V | V | V |

El argumento **falla únicamente** cuando la premisa es verdadera y la conclusión, falsa.

### 2. Argumentos en lógica proposicional: definición y formas de representación

**Definición**: en lógica proposicional, un argumento es una secuencia de proposiciones; todas excepto la última se llaman **premisas** (`P₁, P₂, …, Pₙ`), y la última es la **conclusión** (`Q`). La **forma del argumento** hace alusión a la estructura lógica empleada en el razonamiento para llegar de las premisas a la conclusión, y existen tres formas de representarla:

| Forma | Representación |
|---|---|
| Estándar o vertical | `P₁`, `P₂`, …, `Pₙ` (una debajo de otra) y `∴ Q` (conclusión, separada por una línea) |
| Tautología | `P₁ ∧ P₂ ∧ ⋯ ∧ Pₙ → Q` |
| Simbólica | `P₁, P₂, ⋯, Pₙ ⊢ Q` (las comas reemplazan la conjunción entre premisas; el símbolo `⊢` indica la conclusión) |

El símbolo `∴`, usado en la forma estándar, se lee "por lo tanto".

### 3. Validez de un argumento: definición y el ejemplo de Sócrates

Un argumento es **válido** si, y solo si, para toda asignación de valores de verdad que haga verdaderas todas las premisas, la conclusión también es verdadera.

El profesor ilustró la traducción de un argumento en lenguaje natural a lenguaje formal con el ejemplo clásico de Sócrates:

> Si Sócrates es un hombre, entonces Sócrates es un mortal.
> Sócrates es un hombre.
> ∴ Sócrates es un mortal.

Con `P`: "Sócrates es un hombre" y `Q`: "Sócrates es un mortal", el argumento se representa en las tres formas:

| Forma | Representación |
|---|---|
| Estándar | `P → Q`, `P` ∴ `Q` |
| Tautología | `[(P → Q) ∧ P] → Q` |
| Simbólica | `(P → Q), P ⊢ Q` |

### 4. Validación de argumentos mediante tabla de verdad

El procedimiento para validar un argumento mediante tabla de verdad sigue tres pasos:

1. Identificar las premisas y la conclusión de la forma del argumento.
2. Construir una tabla de verdad que muestre los valores de verdad de todas las premisas y de la conclusión.
3. Un renglón de la tabla en el que todas las premisas son verdaderas se llama **renglón crítico**. Si en algún renglón crítico la conclusión es falsa, la forma del argumento es **no válida**; si la conclusión es verdadera en todos los renglones críticos, la forma del argumento es **válida**.

**Ejemplo** — dado el argumento

```
p → q ∨ ¬r
q → p ∧ r
∴ p → r
```

con variables `p, q, r` (`n = 3`, `2³ = 8` filas), se construyó la tabla completa:

| p | q | r | ¬r | q∨¬r | p∧r | p→q∨¬r | q→p∧r | p→r |
|---|---|---|---|---|---|---|---|---|
| 0 | 0 | 0 | 1 | 1 | 0 | 1 | 1 | 1 |
| 0 | 0 | 1 | 0 | 0 | 0 | 1 | 1 | 1 |
| 0 | 1 | 0 | 1 | 1 | 0 | 1 | 0 | — |
| 0 | 1 | 1 | 0 | 1 | 0 | 1 | 0 | — |
| 1 | 0 | 0 | 1 | 1 | 0 | 1 | 1 | **0** |
| 1 | 0 | 1 | 0 | 0 | 1 | 0 | 1 | — |
| 1 | 1 | 0 | 1 | 1 | 0 | 1 | 0 | — |
| 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 |

Los renglones críticos (ambas premisas verdaderas) son las filas 1, 2, 5 y 8. En la fila 5 (`p=1, q=0, r=0`) la conclusión `p→r` es falsa, aunque las premisas son verdaderas; ese renglón muestra que un argumento de esta forma puede tener premisas verdaderas y una conclusión falsa. Por lo tanto, **esta forma de argumento no es válida**.

### 5. Identificación de premisas y conclusión en lenguaje natural

Identificar las premisas y la conclusión en un argumento dado en lenguaje natural puede ser complejo. Para facilitarlo se utilizan indicadores o conectores argumentativos:

| Adverbios que indican premisa | Adverbios que indican conclusión |
|---|---|
| Puesto que | Por tanto |
| Dado que | Por consiguiente |
| Ya que | En consecuencia |
| Porque | Por lo que |
| Toda vez que | Se sigue que |
| Considerando que | Se infiere que |
| Tomando en cuenta que | Se deduce que |
| Como | Luego |
| Puesto que | Resulta que |

### 6. Más ejemplos de validación por tabla de verdad

**El argumento "del sombrero"** — representar simbólicamente y determinar la validez de:

> Si 2 = 3, entonces yo me comí mi sombrero.
> Me comí mi sombrero.
> ∴ 2 = 3

Con `p`: "2 = 3" y `q`: "Me comí mi sombrero":

| Forma | Representación |
|---|---|
| Estándar | `p → q`, `q` ∴ `p` |
| Tautología | `[(p → q) ∧ q] → p` |
| Simbólica | `(p → q), q ⊢ p` |

| p | q | p→q | q | p |
|---|---|---|---|---|
| 0 | 0 | 1 | 0 | 0 |
| 0 | 1 | 1 | 1 | **0** |
| 1 | 0 | 0 | 0 | 1 |
| 1 | 1 | 1 | 1 | 1 |

En el renglón crítico `p=0, q=1` ambas premisas (`p→q` y `q`) son verdaderas, pero la conclusión `p` es falsa; por lo tanto, **el argumento es inválido**. En palabras: si el argumento fuera válido, siempre que `p→q` y `q` fueran ciertas, `p` también debería serlo; pero basta que `p` sea falsa y `q` verdadera para que `p→q` y `q` sean ambas verdaderas sin que `p` lo sea.

**Ejemplo con tres variables** — dado el argumento lógico `[B ∧ ((B ∧ C) → ¬A) ∧ (B → C)] → ¬A`, se identificó primero que está expresado en forma de tautología, y se tradujo a las otras formas:

| Forma | Representación |
|---|---|
| Estándar | `B`, `(B∧C)→¬A`, `B→C` ∴ `¬A` |
| Simbólica | `B, (B∧C→¬A), (B→C) ⊢ ¬A` |

Con variables `A, B, C` (`n=3`, `2³=8` filas), se construyó la tabla completa:

| A | B | C | ¬A | B∧C | (B∧C)→¬A | B→C | B∧((B∧C)→¬A)∧(B→C) | ¬A |
|---|---|---|---|---|---|---|---|---|
| 0 | 0 | 0 | 1 | 0 | 1 | 1 | 0 | — |
| 0 | 0 | 1 | 1 | 0 | 1 | 1 | 0 | — |
| 0 | 1 | 0 | 1 | 0 | 1 | 0 | 0 | — |
| 0 | 1 | 1 | 1 | 1 | 1 | 1 | **1** | **1** |
| 1 | 0 | 0 | 0 | 0 | 1 | 1 | 0 | — |
| 1 | 0 | 1 | 0 | 0 | 1 | 1 | 0 | — |
| 1 | 1 | 0 | 0 | 0 | 1 | 0 | 0 | — |
| 1 | 1 | 1 | 0 | 1 | 0 | 1 | 0 | — |

El único renglón crítico (premisas verdaderas) es la fila 4 (`A=0, B=1, C=1`), donde la conclusión `¬A` también es verdadera. Por lo tanto, **el argumento lógico es válido**.

## Próxima clase

1 de septiembre de 2026: continuación de la argumentación lógica con el enfoque axiomático (silogismo, reglas de inferencia y demostración de validez por afirmación-razón).