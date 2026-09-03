![Built with AI](https://img.shields.io/badge/Built%20with-AI-blue.svg)

# Clase 06 — Argumentación lógica

> **Fecha**: 27/08/2026, 01/09/2026 · **Modalidad**: Virtual sincrónica · **Apuntes**: [Diapositivas PDF](./apuntes_clase6.pdf) · [PPT](./apuntes_clase6.pptx) · [Manuscrito anotado](./apuntes_clase6_annotated.pdf)

## Objetivos de la clase

- Presentar el concepto de argumento lógico (premisas y conclusión) y sus tres formas de representación: estándar, tautología y simbólica.
- Definir la validez de un argumento y establecer el procedimiento para verificarla mediante el enfoque basado en modelos (tablas de verdad), incluyendo la identificación de renglones críticos.
- Introducir el silogismo y las reglas de inferencia como fundamento del enfoque axiomático, contrastando su eficiencia frente al enfoque basado en modelos.
- Aplicar el esquema de demostración afirmación-razón para validar argumentos y traducir un enunciado en lenguaje natural a lógica proposicional formal.

## Resumen

La clase se dictó en dos sesiones y cubrió los dos enfoques para demostrar la validez de un argumento. En la primera sesión (27 de agosto) se presentó el enfoque basado en modelos (tablas de verdad), con varios ejemplos resueltos, incluyendo el caso clásico de Sócrates. En la segunda sesión (1 de septiembre) se presentó el enfoque axiomático —silogismo, reglas de inferencia y esquema afirmación-razón—, aplicado en dos ejercicios resueltos en clase y en la traducción formal del dilema de Superman, cuya demostración completa quedó como ejercicio para los estudiantes.

## Agenda

**Sesión 1 — 27/08/2026**

1. Ubicación de la argumentación lógica en el mapa de tipos de demostración (equivalencia, vista en la clase anterior, frente a validez, tema de esta sesión) y de los dos métodos disponibles para demostrar validez: el enfoque basado en modelos (tema de hoy) y el enfoque axiomático (anunciado para la siguiente sesión).
2. Presentación de la expresión condicional como base del argumento matemático (premisa/hipótesis/antecedente → conclusión/tesis/consecuente) y de los dos métodos para construir argumentos matemáticos.
3. Definición formal de argumento en lógica proposicional (premisas y conclusión) y de sus tres formas de representación: estándar o vertical, tautología y forma simbólica.
4. Definición de argumento válido, ilustrada con la traducción a lenguaje formal del ejemplo clásico de Sócrates.
5. Procedimiento de validación de argumentos mediante tabla de verdad (identificar premisas y conclusión, construir la tabla, verificar los renglones críticos) y resolución de un primer ejemplo con tres premisas (no válido).
6. Tabla de adverbios o conectores que indican premisa o conclusión en lenguaje natural.
7. Resolución de dos ejemplos adicionales de validación mediante tabla de verdad: el argumento "del sombrero" sobre `2 = 3` (no válido) y un argumento con variables `A`, `B` y `C` (válido).

**Sesión 2 — 01/09/2026**

1. Presentación del silogismo (premisa mayor, premisa menor, conclusión) mediante el ejemplo de la contraseña de red, y su relación con el Modus Ponens.
2. Introducción a las reglas de inferencia: qué es una prueba, el papel de la intuición y la comparación de eficiencia frente al enfoque basado en tablas de verdad (crecimiento combinatorio `2ⁿ`); presentación de la tabla de reglas de inferencia.
3. Presentación del enfoque axiomático y del esquema de demostración afirmación-razón, ilustrado con un primer ejemplo resuelto en tablero.
4. Planteamiento y resolución completa en clase del Ejercicio 1 (demostración detallada, premisas enumeradas de una vez) y del Ejercicio 2 (estilo incremental, premisas extraídas conforme se necesitan).
5. Planteamiento del Ejercicio 3: traducción al lenguaje formal del dilema de Superman (proposiciones simples y premisas P1-P5), dejando su demostración axiomática completa como ejercicio para los estudiantes antes de la próxima clase.
6. Recordatorios administrativos de cierre: fecha del primer parcial (8 de septiembre), plazo del quiz de tablas de verdad (4 de septiembre) y recursos de repaso disponibles en la plataforma.

## Contenido temático

### 1. El argumento matemático y los métodos de demostración

El profesor ubicó la argumentación lógica dentro del mapa general de tipos de demostración presentado en la clase anterior: una demostración puede referirse a la **equivalencia** de proposiciones (tema de la clase anterior) o a la **validez** de argumentos (tema de esta clase), y para cada una existen dos métodos posibles: el **enfoque basado en modelos** (tablas de verdad) y el **enfoque axiomático** (axiomas / identidades lógicas). En la primera sesión se trabajó la validez con el enfoque basado en modelos; el enfoque axiomático se desarrolló en la segunda sesión (ver secciones 7 a 13).

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

> Si Sócrates es un hombre, entonces Sócrates es un mortal. <br>
> Sócrates es un hombre. <br>
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

> Si 2 = 3, entonces yo me comí mi sombrero. <br>
> Me comí mi sombrero. <br>
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
| Estándar | `B`, `(B ∧ C) → ¬A`, `B → C` ∴ `¬A` |
| Simbólica | `B, (B ∧ C → ¬A), (B → C) ⊢ ¬A` |

Con variables `A, B, C` (`n=3`, `2³=8` filas), se construyó la tabla completa:

| A | B | C | ¬A | B∧C | (B ∧ C) → ¬A | B → C | B ∧ ((B ∧ C) → ¬A) ∧ (B→C) | ¬A |
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

**Sesión 2 — 01/09/2026**

### 7. El silogismo y el Modus Ponens

Un **silogismo** es un tipo de argumento compuesto por dos premisas y una conclusión. La primera premisa se llama **premisa mayor** y la segunda, **premisa menor**; juntas conducen a la conclusión. El conector "por lo tanto" en el lenguaje natural es el marcador que separa las premisas de la conclusión.

El profesor ilustró el silogismo con un ejemplo de acceso a una red:

> Si tiene una contraseña vigente, puede iniciar sesión en la red. <br>
> Tiene una contraseña vigente. <br>
> Por lo tanto, puede iniciar sesión en la red.

Con `passOK`: "tiene una contraseña vigente" y `accessNet`: "puede iniciar sesión en la red":

| Forma | Representación |
|---|---|
| Estándar | `passOK → accessNet`, `passOK` ∴ `accessNet` |
| Tautología | `[(passOK → accessNet) ∧ passOK] → accessNet` |
| Simbólica (notación proposicional) | `(passOK → accessNet), passOK ⊢ accessNet` |

Esta forma de silogismo es la más famosa y se llama **Modus Ponens**.

### 8. Reglas de inferencia

Una **prueba** usa las hipótesis, axiomas y definiciones para llegar a una conclusión; cada paso de la prueba debe producir una conclusión intermedia válida. Al construir una prueba se usa con frecuencia la **intuición** como guía para elegir qué conclusión intermedia sacar en cada paso, aunque el proceso también puede formalizarse.

El enfoque basado en tablas de verdad, visto en la sesión anterior, puede volverse poco práctico cuando el número de variables proposicionales crece, porque el número de filas de la tabla es `2ⁿ` (por ejemplo, `n=10` implica `2¹⁰=1024` combinaciones, y `n=6` implica `2⁶=64`). Las **reglas de inferencia** —formas argumentales válidas ya demostradas— evitan esta explosión combinatoria y pueden usarse como elementos básicos para construir formas argumentales más complejas.

| Nombre | Regla de inferencia | Nombre | Regla de inferencia |
|---|---|---|---|
| Modus Ponens | `p→q`, `p` ∴ `q` | Simplificación | `p∧q` ∴ `p` |
| Modus Tollens | `p→q`, `¬q` ∴ `¬p` | Conjunción | `p`, `q` ∴ `p∧q` |
| Silogismo hipotético (Transitividad) | `p→q`, `q→r` ∴ `p→r` | Prueba de división por casos | `p∨q`, `p→r`, `q→r` ∴ `r` |
| Silogismo disyuntivo (Eliminación) | `p∨q`, `¬p` ∴ `q` | Resolución | `¬p∨r`, `p∨q` ∴ `q∨r` |
| Adición | `p` ∴ `p∨q` | | |

### 9. El enfoque axiomático: el esquema afirmación-razón

El enfoque axiomático combina las **equivalencias lógicas** (vistas en la clase anterior: conmutatividad, asociatividad, distributividad, doble negación, leyes de Morgan, implicación, contrarrecíproco, absorción, entre otras) con las **reglas de inferencia** de la sección anterior, y organiza la demostración en un esquema de **afirmación-razón**: una tabla con columnas `#`, `Afirmación` y `Razón`, donde las primeras filas enumeran las premisas (`P₁, P₂, …`) y cada fila siguiente aplica una equivalencia lógica o una regla de inferencia sobre filas anteriores, hasta llegar a la conclusión `Q`.

### 10. Ejemplo resuelto: introducción al esquema afirmación-razón

El profesor introdujo el esquema con un primer ejemplo resuelto en tablero:

```
Premisas:  p, p → q, s ∨ r, r → ¬q
∴ s∨t
```

| # | Afirmación | Razón |
|---|---|---|
| 1 | `p` | Premisa (a) |
| 2 | `p → q` | Premisa (b) |
| 3 | `q` | Modus Ponens en 1 y 2 |
| 4 | `r → ¬q` | Premisa (d) |
| 5 | `¬(¬q) → ¬r` | Contrarrecíproco en 4 |
| 6 | `q → ¬r` | Doble negación en 5 |
| 7 | `¬r` | Modus Ponens en 3 y 6 |
| 8 | `s ∨ r` | Premisa (c) |
| 9 | `s` | Eliminación en 7 y 8 |
| 10 | `∴ s ∨ t` | Adición en 9 |

### 11. Ejercicio 1: demostración axiomática detallada

Primer ejercicio de práctica, resuelto en clase enumerando todas las premisas de una vez:

```
Premisas:  ¬p∨q→r, s∨¬q, ¬t, p→t, ¬p∧r→¬s
∴ ¬q
```

| # | Afirmación | Razón |
|---|---|---|
| 1 | `¬p ∨ q → r` | Premisa (a) |
| 2 | `s ∨ ¬q` | Premisa (b) |
| 3 | `¬t` | Premisa (c) |
| 4 | `p → t` | Premisa (d) |
| 5 | `¬p ∧ r → ¬s` | Premisa (e) |
| 6 | `¬p` | Modus Tollens en 3 y 4 |
| 7 | `¬(¬p ∧ r) ∨ ¬s` | Implicación en 5 |
| 8 | `p ∨ ¬r ∨ ¬s` | Ley de Morgan para `∧` en 7 |
| 9 | `¬r ∨ ¬s` | Eliminación en 6 y 8 |
| 10 | `¬q ∨ ¬r` | Resolución en 2 y 9 |
| 11 | `¬(¬p ∨ q) ∨ r` | Implicación en 1 |
| 12 | `(p ∧ ¬q) ∨ r` | Ley de Morgan para `∨` en 11 |
| 13 | `¬q ∨ (p ∧ ¬q)` | Resolución en 11 y 12 [^1] |
| 14 | `∴ ¬q` | Absorción en 13 |

[^1]: Así aparece citado en el manuscrito y coincide con el resumen de la sesión. Lógicamente, la resolución que produce la fila 13 requiere el literal `r`/`¬r`, presente en las filas **10** y **12** (no en la 11), por lo que la razón debería citar los renglones 10 y 12. Se transcribe tal como fue anotado en clase, sin corregir el número de renglón citado.

Durante la resolución de este ejercicio, en el paso 7 (definición de implicación aplicada al renglón 5) el profesor omitió inicialmente la negación de todo el paréntesis; el estudiante Matías señaló el error y se corrigió aplicando correctamente la Ley de Morgan en el paso 8, tal como se refleja en la tabla anterior.

### 12. Ejercicio 2: demostración axiomática por estilo incremental

Segundo ejercicio, resuelto extrayendo premisas progresivamente conforme se necesitan, en vez de enumerarlas todas de entrada:

```
Premisas:  p → q, r ∨ s, ¬s → ¬t, ¬q ∨ s, ¬s, ¬p ∧ r → u, w ∨ t
∴ u ∧ r
```

| # | Afirmación | Razón |
|---|---|---|
| 1 | `¬s → ¬t` | Premisa (c) |
| 2 | `¬s` | Premisa (e) |
| 3 | `¬t` | Modus Ponens en 1 y 2 |
| 4 | `r ∨ s` | Premisa (b) |
| 5 | `r` | Eliminación en 2 y 4 |
| 6 | `w ∨ t` | Premisa (g) |
| 7 | `w` | Eliminación en 3 y 6 |
| 8 | `¬q ∨ s` | Premisa (d) |
| 9 | `¬q` | Eliminación en 2 y 8 |
| 10 | `p → q` | Premisa (a) |
| 11 | `¬p` | Modus Tollens en 9 y 10 |
| 12 | `¬p ∧ r` | Conjunción en 5 y 11 |
| 13 | `¬p ∧ r → u` | Premisa (f) |
| 14 | `u` | Modus Ponens en 12 y 13 |
| 15 | `∴ u ∧ r` | Conjunción en 5 y 14 |

Todas las premisas fueron utilizadas a lo largo de la demostración.

### 13. Ejercicio 3: el dilema de Superman

Como ejercicio de traducción, se planteó el siguiente argumento en lenguaje natural:

> Si Superman fuera capaz y estuviera dispuesto a prevenir el mal, lo haría. Si Superman fuera incapaz de prevenir el mal, sería impotente; si no estuviera dispuesto a prevenir el mal, sería malévolo. Superman no previene el mal. Si Superman existe, no es ni malévolo ni impotente; por lo tanto, Superman no existe.

Este ejercicio corresponde a un punto del parcial de un semestre anterior, en el que solo se pedía la traducción (no la demostración axiomática completa).

**Proposiciones simples** identificadas en clase:

- **`SCM`**: Superman es capaz de prevenir el mal
- **`SDM`**: Superman está dispuesto a prevenir el mal
- **`SM`**: Superman previene el mal
- **`SI`**: Superman sería impotente
- **`SMal`**: Superman sería malévolo
- **`SE`**: Superman existe

**Traducción formal** (con participación activa del estudiante Matías, quien interpretó que "lo haría" corresponde a **`SM`** y que el antecedente de la primera premisa es la conjunción de capacidad y disposición):

| Premisa | Traducción |
|---|---|
| P1 | `SCM ∧ SDM → SM` |
| P2 | `¬SCM → SI` |
| P3 | `¬SDM → SMal` |
| P4 | `¬SM` |
| P5 | `SE → (¬SMal ∧ ¬SI)` |
| Conclusión (Q) | `¬SE` |

La traducción se completó en clase; la **demostración axiomática completa no se realizó en la sesión** y quedó como ejercicio para que los estudiantes la intentaran antes de la clase siguiente. La siguiente tabla es la **solución de referencia preparada por el profesor** (no desarrollada en vivo el 1 de septiembre), destinada a que los estudiantes comparen su propio resultado:

| # | Afirmación | Razón |
|---|---|---|
| 1 | `SCM ∧ SDM → SM` | Premisa (a) |
| 2 | `¬SM` | Premisa (d) |
| 3 | `¬(SCM ∧ SDM)` | Modus Tollens en 1 y 2 |
| 4 | `¬SCM → SI` | Premisa (b) |
| 5 | `¬SDM → SMal` | Premisa (c) |
| 6 | `¬(¬SCM) ∨ SI` | Implicación en 4 |
| 7 | `¬(¬SDM) ∨ SMal` | Implicación en 5 |
| 8 | `SCM ∨ SI` | Doble negación en 6 |
| 9 | `SDM ∨ SMal` | Doble negación en 7 |
| 10 | `¬SCM ∨ ¬SDM` | Ley de Morgan para `∧` en 3 |
| 11 | `SI ∨ ¬SDM` | Resolución en 8 y 10 |
| 12 | `SI ∨ SMal` | Resolución en 9 y 11 |
| 13 | `¬(¬SI∧ ¬ SMal)` | Ley de Morgan (doble negación) en 12 |
| 14 | `SE→(¬SMal∧¬SI)` | Premisa (e) |
| 15 | `∴ ¬SE` | Modus Tollens en 13 y 14 |

### 14. Aclaraciones conceptuales surgidas en clase

- **¿Las reglas de inferencia usan uno o dos renglones?** Generalmente se usan dos renglones (a veces tres), a diferencia de las equivalencias lógicas, que pueden aplicarse a un solo renglón.
- **¿Importa el orden de los renglones?** No importa el orden entre sí, pero sí deben ser los renglones correctos que cumplan la forma de la regla; tampoco es necesario que sean consecutivos (por ejemplo, puede combinarse el renglón 3 con el renglón 6).
- **¿Se puede reutilizar una premisa ya usada?** Sí, es válido reutilizar premisas en distintos pasos de una misma demostración.

[Ver en el sitio](https://discretas1-udea.github.io/discretas1-udea-20262/lessons/mod1/clase5/) — la nota teórica del sitio agrupa el contenido de ambas sesiones (enfoque basado en modelos y enfoque axiomático) bajo "Clase 05"; no incluye el ejemplo del dilema de Superman.

## Evaluación

| Ítem | Detalle |
|---|---|
| Primer parcial | Sábado 12 de septiembre de 2026. Se recomienda repasar los parciales anteriores disponibles en la plataforma del curso. |
| Quiz de tablas de verdad | Activo hasta el viernes 4 de septiembre de 2026; requiere evaluar proposiciones lógicas y construir tablas de verdad según las preguntas planteadas. |

## Recursos del curso

| Recurso | Descripción | Enlace |
|---|---|---|
| Tallercitos de repaso | Ejercicios cortos de repaso. | En la plataforma del curso |
| Parciales anteriores | Enunciados y soluciones de parciales de semestres previos. | En la plataforma del curso |
| Talleres de lógica proposicional | Talleres con tipos de enunciados declarativos, fórmulas y ejercicios de equivalencias. | En la plataforma del curso |

## Pendientes

### Docente

- [x] Actualizar las notas de la clase en la plataforma.
- [x] Subir el ejercicio del dilema de Superman para que los estudiantes puedan acceder a él.

### Estudiantes

- [ ] Intentar la demostración axiomática completa del argumento de Superman (llegar a `¬SE`) antes de la próxima clase.
- [ ] Repasar talleres y parciales anteriores disponibles en la plataforma en preparación para el primer parcial (12 de septiembre).
- [ ] Tener a mano una ficha escrita con la tabla de reglas de inferencia y de equivalencias lógicas para los ejercicios y el parcial.
