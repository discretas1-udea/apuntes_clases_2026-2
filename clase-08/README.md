![Built with AI](https://img.shields.io/badge/Built%20with-AI-blue.svg)

# Clase 08 — Cuantificadores universal y existencial

> **Fecha**: 15/09/2026, 17/09/2026 · **Modalidad**: Virtual sincrónica · **Apuntes**: [Diapositivas PDF](./apuntes_clase8.pdf) · [PPT](./apuntes_clase8.pptx) · [Manuscrito anotado](./apuntes_clase8_annotated.pdf)

## Objetivos de la clase

- Recoger la retroalimentación de los estudiantes sobre el primer parcial y comunicar los ajustes previstos para las próximas evaluaciones.
- Formalizar los cuantificadores universal (∀), existencial (∃) y de unicidad (∃!), sus condiciones de verdad/falsedad y su dependencia del dominio de discurso.
- Establecer la precedencia de los cuantificadores frente a los operadores lógicos y su equivalencia con la conjunción/disyunción en dominios finitos.
- Afianzar estos conceptos mediante una batería extensa de ejercicios de evaluación de verdad y de traducción entre lenguaje natural y lógica de predicados, apoyada en las formas aristotélicas.

## Resumen

La clase se dictó en dos sesiones. La primera inició con un espacio de retroalimentación sobre el primer parcial (dificultad percibida, modalidad presencial, uso de apuntes, extensión del examen y comunicación de horarios) y continuó con la formalización de los cuantificadores universal, existencial y de unicidad, sus propiedades, su precedencia frente a los operadores lógicos y su relación con la conjunción/disyunción en dominios finitos, cerrando con el primer ejercicio de evaluación de verdad. La segunda sesión resolvió ocho ejercicios adicionales de evaluación de verdad de enunciados cuantificados, presentó el proceso de traducción de lenguaje natural a formal con las formas aristotélicas, y resolvió los tres primeros ejercicios de una nueva batería de traducción, quedando pendientes los siguientes para la sesión del 22 de septiembre.

## Agenda

**Sesión 1 — 15/09/2026**

1. Espacio de retroalimentación sobre el primer parcial: percepción de dificultad, aclaración sobre la modalidad presencial, uso de apuntes, gestión del tiempo y comunicación de cambios de horario. [*(→ Evaluación)*](#evaluación)
2. Repaso rápido de las equivalencias lógicas y reglas de inferencia de la lógica proposicional. [*(→ sección 1)*](#1-repaso-modelo-y-conceptos-previos-de-la-lógica-cuantificacional)
3. Repaso del concepto de modelo y de los conceptos fundamentales de la lógica cuantificacional (universo, objeto, predicado, variable) con el ejemplo de los Transformers. [*(→ sección 1)*](#1-repaso-modelo-y-conceptos-previos-de-la-lógica-cuantificacional)
4. Presentación formal del cuantificador universal (∀), con el ejemplo de las caritas felices y el método del contraejemplo. [*(→ sección 2)*](#2-cuantificadores-universal-existencial-y-de-unicidad)
5. Presentación formal del cuantificador existencial (∃), con el mismo ejemplo. [*(→ sección 2)*](#2-cuantificadores-universal-existencial-y-de-unicidad)
6. Presentación del cuantificador de unicidad (∃!) y su forma desarrollada en términos de ∃ y ∀. [*(→ sección 2)*](#2-cuantificadores-universal-existencial-y-de-unicidad)
7. Propiedades de los cuantificadores: el valor de verdad depende del predicado y del dominio, ilustrado con ℤ⁺, ℤ⁻ y el dominio finito {3,4,5}. [*(→ sección 3)*](#3-propiedades-de-los-cuantificadores-dependencia-del-predicado-y-del-dominio)
8. Precedencia de los cuantificadores frente a los operadores lógicos, y diferencia entre `∀x∃y P(x,y)` y `∃y∀x P(x,y)`. [*(→ sección 4)*](#4-precedencia-de-los-cuantificadores)
9. Relación entre el cuantificador universal y la conjunción, y entre el existencial y la disyunción, en dominios finitos. [*(→ sección 5)*](#5-cuantificadores-como-conjunción-y-disyunción-en-dominios-finitos)
10. Presentación de la lista de nueve ejercicios de evaluación de verdad de enunciados cuantificados. [*(→ sección 6)*](#6-ejercicios-de-evaluación-de-verdad-de-enunciados-cuantificados)
11. Resolución del Ejemplo 1 (verdad y falsedad de enunciados universales sobre D={1,...,5} y sobre ℝ, con contraejemplo). [*(→ sección 6)*](#6-ejercicios-de-evaluación-de-verdad-de-enunciados-cuantificados)

**Sesión 2 — 17/09/2026**

1. Resolución del Ejemplo 2 (verdad y falsedad de enunciados existenciales sobre ℤ⁺ y sobre el dominio finito {5,6,7,8}). [*(→ sección 6)*](#6-ejercicios-de-evaluación-de-verdad-de-enunciados-cuantificados)
2. Resolución del Ejemplo 3 (∀x P(x) con P(x): "x+1>x" sobre ℝ). [*(→ sección 6)*](#6-ejercicios-de-evaluación-de-verdad-de-enunciados-cuantificados)
3. Resolución del Ejemplo 4 (∀x Q(x) con Q(x): "x<2" sobre ℝ). [*(→ sección 6)*](#6-ejercicios-de-evaluación-de-verdad-de-enunciados-cuantificados)
4. Resolución del Ejemplo 5 (∀x P(x) con P(x): "x²>0" sobre ℝ). [*(→ sección 6)*](#6-ejercicios-de-evaluación-de-verdad-de-enunciados-cuantificados)
5. Resolución del Ejemplo 6 (interpretación de ∀x N(x) sobre el dominio de las computadoras del campus). [*(→ sección 6)*](#6-ejercicios-de-evaluación-de-verdad-de-enunciados-cuantificados)
6. Resolución del Ejemplo 7 (∀x(x²≥x), comparando el dominio real y el entero). [*(→ sección 6)*](#6-ejercicios-de-evaluación-de-verdad-de-enunciados-cuantificados)
7. Resolución del Ejemplo 8 (∃x P(x) con P(x): "x>3" sobre ℝ). [*(→ sección 6)*](#6-ejercicios-de-evaluación-de-verdad-de-enunciados-cuantificados)
8. Resolución del Ejemplo 9 (∃x Q(x) con Q(x): "x=x+1" sobre ℝ). [*(→ sección 6)*](#6-ejercicios-de-evaluación-de-verdad-de-enunciados-cuantificados)
9. Presentación del proceso de traducción de lenguaje natural a formal y de las formas aristotélicas (A, E, I, O), con el error común de la forma I. [*(→ sección 7)*](#7-formas-aristotélicas-y-proceso-de-traducción-de-lenguaje-natural-a-formal)
10. Ejemplo resuelto de traducción ("todo estudiante de lógica es curioso"). [*(→ sección 7)*](#7-formas-aristotélicas-y-proceso-de-traducción-de-lenguaje-natural-a-formal)
11. Presentación de una nueva batería de siete ejercicios de traducción entre lenguaje formal e informal. [*(→ sección 8)*](#8-ejercicios-de-traducción-entre-lenguaje-formal-e-informal)
12. Resolución del Ejemplo 1 de esta batería (tres enunciados formales traducidos a lenguaje informal). [*(→ sección 8)*](#8-ejercicios-de-traducción-entre-lenguaje-formal-e-informal)
13. Resolución del Ejemplo 2 (dos enunciados informales traducidos a lenguaje formal, sobre enteros y reales). [*(→ sección 8)*](#8-ejercicios-de-traducción-entre-lenguaje-formal-e-informal)
14. Resolución del Ejemplo 3 (traducción de "todos los triángulos tienen tres lados", "ningún perro tiene alas" y "algunos programas están estructurados", comparando dominios restringidos y amplios). [*(→ sección 8)*](#8-ejercicios-de-traducción-entre-lenguaje-formal-e-informal)

## Contenido temático

Notación adicional a la ya introducida en la clase anterior (ver [clase-07](../clase-07/)):

| Símbolo | Significado |
|---|---|
| `∃!x P(x)` | Existe exactamente un x tal que P(x) (cuantificador de unicidad) |
| `x₀` | Elemento específico del dominio usado como contraejemplo o testigo |

### 1. Repaso: modelo y conceptos previos de la lógica cuantificacional

Como continuación de lo visto en la clase anterior, el profesor repasó brevemente las tablas de equivalencias lógicas y reglas de inferencia de la lógica proposicional, y retomó el concepto de **modelo**: una interpretación que asigna significado a los símbolos de un lenguaje lógico y hace verdadero un conjunto de fórmulas. En lógica proposicional, un modelo `w` mapea símbolos a valores de verdad (ejemplo ya visto en clase-07: `w = {ClotildeDominaCalculo: 1, RamonDominaCalculo: 0} = {p, ¬q}`); en lógica cuantificacional, el mismo concepto se aplica al fijar un universo y asignar predicados concretos sobre él, como se hace a lo largo de esta sección.

A modo de repaso, se retomó la siguiente tabla con el ejemplo de los Transformers:

| Concepto | Representación | Expresión |
|---|---|---|
| Universo | Transformers (Autobots y Decepticons) | `U = {Optimus, Bumblebee, ...}` |
| Objeto | Optimus Prime | `Optimus` |
| Predicado | x está enfermo | `enfermo(x)` |
| Variable | Cualquier transformer | `x` |

### 2. Cuantificadores: universal, existencial y de unicidad

**Cuantificador universal (∀).** Afirma que la propiedad que le sigue es verdadera para todos los elementos del dominio considerado.

| Elemento | Detalle |
|---|---|
| Lectura | "Para todo", "para cada", "para cualquier" |
| Formato | `∀x P(x)`: "para todo x, la propiedad P es verdadera para x" |
| Verdadero cuando | Sin importar el elemento `a` del dominio que se elija, `P(a)` es verdadero |
| Falso cuando | Se encuentra un elemento `a` del dominio para el que `P(a)` es falso |

Con el ejemplo de las "caritas felices" (dominio D de caritas, predicado `smiling(x)`: "x es una carita feliz"): si todas las caritas están felices, `∀x smiling(x) = Verdadero`; si al menos una no lo está, `∀x smiling(x) = Falso`.

**Método del contraejemplo.** Técnica de refutación que consiste en encontrar un solo caso donde una proposición universal no se cumple: basta hallar un `x₀` tal que `P(x₀)` sea falso para concluir que `∀x P(x)` es falso.

**Cuantificador existencial (∃).** Afirma que hay al menos un elemento en el dominio que satisface la propiedad que le sigue.

| Elemento | Detalle |
|---|---|
| Lectura | "Existe al menos uno", "para algún", "hay algún" |
| Formato | `∃x P(x)`: "existe al menos un x tal que la propiedad P es verdadera para x" |
| Verdadero cuando | Se puede encontrar al menos un elemento `a` del dominio para el cual `P(a)` es verdadero |
| Falso cuando | Se comprueban todos los elementos y para ninguno `P(x)` es verdadero |

Con el mismo ejemplo de las caritas felices: basta que una sola esté feliz para que `∃x smiling(x) = Verdadero`; si ninguna lo está, es `Falso`.

**Cuantificador de unicidad (∃!).** Expresa que existe exactamente un elemento que cumple cierta propiedad ("existe un único", "existe exactamente un", "uno y solo uno"). El profesor señaló que este cuantificador no es estrictamente necesario, ya que puede expresarse combinando ∃ y ∀:

`∃! x P(x) ≡ ∃x (P(x) ∧ ∀y (P(y) → y = x))`

Esta forma desarrollada se compone de dos partes: **existencia** (`∃x P(x)`: existe al menos un x que cumple P) y **unicidad** (`∀y (P(y) → y = x)`: cualquier otro elemento que también cumpla P debe ser igual a x).

Tabla resumen comparativa, mostrada en clase:

| Característica | ∀ (universal) | ∃ (existencial) |
|---|---|---|
| Significado | La propiedad es verdadera para todos los elementos del dominio | La propiedad es verdadera para al menos uno del dominio |
| Estructura típica | `∀x P(x)` | `∃x P(x)` |
| Condición de verdad | `P(x)` es verdadero para todo x | Hay algún x para el cual `P(x)` es verdadero |
| Condición de falsedad | Hay algún x para el cual `P(x)` es falso | `P(x)` es falso para cada x |
| Palabras clave asociadas | Todos, cada, cualquiera, ninguno (con negación), siempre | Existe, algún, algunos, hay, al menos uno, a veces |

> [!NOTE]
> El valor de verdad de cualquiera de los cuantificadores depende del dominio, como se desarrolla en la sección 3.

### 3. Propiedades de los cuantificadores: dependencia del predicado y del dominio

El valor de verdad de `∀x P(x)` y de `∃x P(x)` depende tanto de la función proposicional `P(x)` como del dominio `U` considerado. El profesor lo ilustró con tres ejemplos:

1. Con `U = ℤ⁺` y `P(x)`: "x < 2", `∃x P(x)` es verdadero (x=1 lo satisface) pero `∀x P(x)` es falso.
2. Con `U = ℤ⁻` y el mismo `P(x)`: "x < 2", tanto `∃x P(x)` como `∀x P(x)` son verdaderos (todos los enteros negativos son menores que 2).
3. Con `U = {3, 4, 5}`, `Q(x)`: "x > 2" y `P(x)`: "x < 2": tanto `∃x Q(x)` como `∀x Q(x)` son verdaderos, mientras que tanto `∃x P(x)` como `∀x P(x)` son falsos.

**Aplicación:** este mismo principio —que un enunciado puede ser verdadero en un dominio y falso en otro— es la base de los Ejemplos 3, 4 y 7 de la sección 6, donde se evalúa la misma expresión sobre los reales y sobre los enteros.

### 4. Precedencia de los cuantificadores

Los cuantificadores ∀ y ∃ no tienen una precedencia "rígida" como los operadores aritméticos, pero su orden importa: tienen **mayor precedencia que todos los operadores lógicos**. Por ejemplo, `∀x P(x) ∨ Q(x)` es la disyunción de `∀x P(x)` y `Q(x)` — equivale a `(∀x P(x)) ∨ Q(x)` y no a `∀x (P(x) ∨ Q(x))`.

Además, el orden entre cuantificadores anidados cambia el significado de la expresión (tema que se profundizará más adelante en el curso):

| Expresión | Significado |
|---|---|
| `∀x ∃y P(x,y)` | Para cada x, existe un y (posiblemente distinto) que cumple P(x,y) |
| `∃y ∀x P(x,y)` | Hay un único y que sirve para todos los x |

> [!NOTE]
> La fila anterior reproduce textualmente la diapositiva del profesor. En rigor, `∃` solo garantiza que existe **al menos un** y con esa propiedad, no que sea el único; la unicidad estricta requeriría el cuantificador `∃!` presentado en la sección 2.

### 5. Cuantificadores como conjunción y disyunción en dominios finitos

En dominios finitos, los cuantificadores se relacionan estrechamente con la conjunción y la disyunción:

- **∀ ≈ conjunción**: en un dominio finito `U = {x₁, x₂, ..., xₙ}`, `∀x P(x) ≡ P(x₁) ∧ P(x₂) ∧ ... ∧ P(xₙ)`.
- **∃ ≈ disyunción**: en el mismo dominio, `∃x P(x) ≡ P(x₁) ∨ P(x₂) ∨ ... ∨ P(xₙ)`.

Ejemplo trabajado en clase: con el enunciado "Todos los estudiantes aprobaron" sobre el dominio `U = {Martin, Nelson, Bart}` y el predicado `aprobo(x)`: "x aprobó": `∀x aprobo(x) = aprobo(Martin) ∧ aprobo(Nelson) ∧ aprobo(Bart)`. De forma análoga, "Algunos estudiantes aprobaron" se traduce como `∃x aprobo(x) = aprobo(Martin) ∨ aprobo(Nelson) ∨ aprobo(Bart)`.

Esta relación **no se puede aplicar en dominios infinitos**, y es precisamente la técnica usada para resolver los ejercicios con dominio finito de la sección 6 (Ejemplos 1a y 2b).

### 6. Ejercicios de evaluación de verdad de enunciados cuantificados

A lo largo de las dos sesiones se resolvieron nueve ejercicios de evaluación de verdad. En cada caso se definió primero el dominio, la variable y el predicado antes de evaluar la expresión:

| # | Enunciado | Dominio | Valor de verdad | Justificación / método |
|---|---|---|---|---|
| 1a | `∀x (x² ≥ x)` | D = {1,2,3,4,5} | Verdadero | Se verifica caso por caso (conjunción): 1≥1, 4≥2, 9≥3, 16≥4, 25≥5, todos verdaderos |
| 1b | `∀x (x² ≥ x)` | ℝ | Falso | Contraejemplo x₀ = 1/2: (1/2)² = 1/4, y 1/4 ≥ 1/2 es falso |
| 2a | `∃m (m² = m)` | ℤ⁺ | Verdadero | Testigo m = 1: 1² = 1 |
| 2b | `∃m (m² = m)` | E = {5,6,7,8} | Falso | Disyunción de todos falsos: 25≠5, 36≠6, 49≠7, 64≠8 |
| 3 | `∀x (x+1 > x)` | ℝ | Verdadero | No se encuentra contraejemplo (x₀=2 da 3>2, verdadero); algebraicamente x+1>x ⟺ 1>0, siempre verdadero |
| 4 | `∀x (x < 2)` | ℝ | Falso | Contraejemplo x₀ = 2: 2 < 2 es falso |
| 5 | `∀x (x² > 0)` | ℝ | Falso | Contraejemplo x₀ = 0: 0² > 0 es falso |
| 6 | `∀x N(x)`, N(x): "x está conectada a la red" | Computadoras del campus | (interpretación, no evaluación) | Se traduce como "todas las computadoras del campus están conectadas a la red" |
| 7a | `∀x (x² ≥ x)` | ℝ | Falso | Contraejemplo x₀ = 1/2 (mismo análisis que 1b) |
| 7b | `∀x (x² ≥ x)` | ℤ | Verdadero | x² − x ≥ 0 ⟺ x(x−1) ≥ 0; los únicos valores que lo incumplen están en el intervalo abierto (0,1), que no contiene enteros |
| 8 | `∃x (x > 3)` | ℝ | Verdadero | Testigo x₀ = 4: 4 > 3 |
| 9 | `∃x (x = x+1)` | ℝ | Falso | La ecuación x = x+1 equivale a 0 = 1, falsa para todo x |

> [!TIP]
> El ejercicio 7 se resolvió explícitamente comparando ℝ y ℤ para reforzar que un mismo enunciado puede ser verdadero o falso según el dominio: en ℝ existe el valor 1/2 que actúa como contraejemplo, mientras que en ℤ el intervalo problemático (0,1) no contiene ningún entero.

Se destacaron dos métodos de demostración, ambos reforzados en el resumen de la sesión del 17/09: el **método del contraejemplo** (para refutar un `∀`, basta un `x₀` con `P(x₀)` falso) y el **método del testigo** (para verificar un `∃`, basta un `x₀` con `P(x₀)` verdadero).

> [!TIP]
> **Sobre el Ejemplo 3**: un estudiante preguntó si el resultado verdadero de evaluar `P(2)` (3>2) demostraba por sí solo el enunciado universal. El profesor aclaró que no: evaluar un único caso verdadero no demuestra un `∀`, solo la ausencia de cualquier contraejemplo posible lo hace. Por eso la conclusión se apoya en el argumento algebraico (`x+1>x ⟺ 1>0`, válido para todo `x∈ℝ`), y no en el caso x=2 aislado.

[Ver en el sitio](https://discretas1-udea.github.io/discretas1-udea-20262/lessons/mod2/clase7/) [[autoevaluación]](https://discretas1-udea.github.io/discretas1-udea-20262/lessons/mod2/clase7_autoevaluacion/) — página del sitio teórico dedicada específicamente a estos temas (unicidad, dependencia del dominio, método del contraejemplo, cuantificadores como conjunción/disyunción).

### 7. Formas aristotélicas y proceso de traducción de lenguaje natural a formal

Se retomó el proceso de traducción en seis pasos presentado en la clase anterior (identificar las proposiciones/propiedades, definir predicados y constantes, determinar el dominio, identificar la estructura de la oración, aplicar la forma aristotélica correspondiente, y escribir/verificar la expresión), y se repasaron las cuatro formas aristotélicas:

| Forma | Nombre | Enunciado típico | Traducción en LPO |
|---|---|---|---|
| A | Universal afirmativa | "Todo S es P" | `∀x (S(x) → P(x))` |
| E | Universal negativa | "Ningún S es P" | `∀x (S(x) → ¬P(x))` |
| I | Particular afirmativa | "Algún S es P" | `∃x (S(x) ∧ P(x))` |
| O | Particular negativa | "Algún S no es P" | `∃x (S(x) ∧ ¬P(x))` |

> [!WARNING]
> **Error común señalado nuevamente en esta clase**: usar `∃x (S(x) → P(x))` en la forma I en vez de `∃x (S(x) ∧ P(x))`, o usar `∧` en vez de `→` en las formas universales. Con `→`, la forma I sería trivialmente verdadera cuando `S(x)` es falso para algún x, lo cual no captura "algún S es P". Las formas aristotélicas son una guía, no una receta exhaustiva para todo el lenguaje natural.

Se resolvió un ejemplo de traducción: "Todo estudiante de lógica es curioso", con dominio = personas y predicados `EstudianteDeLogica(x)` y `Curioso(x)`, obteniendo `∀x (EstudianteDeLogica(x) → Curioso(x))` (forma A).

[Ver en el sitio](https://discretas1-udea.github.io/discretas1-udea-20262/lessons/mod2/clase7/) [[autoevaluación]](https://discretas1-udea.github.io/discretas1-udea-20262/lessons/mod2/clase7_autoevaluacion/) — nota: el sitio teórico menciona las formas aristotélicas pero no las desarrolla con la misma profundidad que esta sesión.

### 8. Ejercicios de traducción entre lenguaje formal e informal

Se presentó una nueva batería de siete ejercicios de traducción (unos de formal a informal, otros de informal a formal), de los cuales se resolvieron los tres primeros en esta clase. Los restantes —enunciados sobre hablantes de francés en el continente africano, estudiantes que tomaron un curso de Java, y el silogismo clásico de Sócrates— quedaron pendientes para la siguiente sesión (ver "Próxima clase").

**Ejemplo 1 — de formal a informal**, con dominio ℝ (incisos a y b) y ℤ⁺ (inciso c):

| Enunciado formal | Traducción a lenguaje informal |
|---|---|
| `∀x ∈ ℝ, x² ≥ 0` | "Todos los números reales tienen cuadrados no negativos" / "El cuadrado de todo número real es no negativo" |
| `∀x ∈ ℝ, x² ≠ 1` | "No hay números reales que tengan cuadrados iguales a 1" (nota del manuscrito: "ninguno es" o "no... son" equivalen a "todos no son") |
| `∃m ∈ ℤ⁺ tal que m² = m` | "Hay un entero positivo cuyo cuadrado es igual a sí mismo" / "Algún entero positivo es igual a su propio cuadrado" |

**Ejemplo 2 — de informal a formal**:

| Enunciado informal | Dominio y predicado | Traducción formal |
|---|---|---|
| "Para cualquier n, 2n es par" | ℤ; `P(n)`: "n es par" | `∀n ∈ ℤ, P(2n)` |
| "Existe al menos un número real x tal que x² ≤ 0" | ℝ; `Q(x)`: "x² ≤ 0" | `∃x ∈ ℝ, Q(x)` |

**Ejemplo 3 — traducción formal con cuantificadores y variables, comparando dominios.** Este ejercicio, resuelto para los tres incisos, ilustró que al ampliar el dominio se necesitan más predicados para capturar el mismo enunciado:

| Enunciado | Dominio restringido | Dominio amplio |
|---|---|---|
| "Todos los triángulos tienen tres lados" | Dominio = triángulos; `L₃(x)`: "x tiene tres lados" → `∀x L₃(x)` | Dominio = figuras geométricas; `T(x)`: "x es un triángulo", `L₃(x)`: "x tiene tres lados" → `∀x (T(x) → L₃(x))` (forma A) |
| "Ningún perro tiene alas" | Dominio = perros; `Alas(x)`: "x tiene alas" → `∀x ¬Alas(x)` | Dominio = animales; `P(x)`: "x es un perro", `Alas(x)` → `∀x (P(x) → ¬Alas(x))` (forma E) |
| "Algunos programas están estructurados" | Dominio = programas; `E(x)`: "x está estructurado" → `∃x E(x)` | Dominio = cosas; `P(x)`: "x es un programa", `E(x)` → `∃x (P(x) ∧ E(x))` (forma I) |

[Ver en el sitio](https://discretas1-udea.github.io/discretas1-udea-20262/lessons/mod2/clase7/) [[autoevaluación]](https://discretas1-udea.github.io/discretas1-udea-20262/lessons/mod2/clase7_autoevaluacion/) — página del sitio teórico dedicada específicamente a los cuantificadores; puede no cubrir aún la profundidad de los ejercicios de traducción trabajados en esta sesión.

## Evaluación

| Ítem | Detalle |
|---|---|
| Retroalimentación del primer parcial | La mayoría de los estudiantes calificó la dificultad del examen entre 6 y 7 sobre 10, dentro de lo esperado según el profesor. |
| Modalidad presencial | El profesor aclaró que la decisión de que el grupo presentara el parcial de forma presencial (a diferencia de otros grupos del curso) fue una decisión autónoma de cátedra, motivada por la desconfianza generada por el uso de inteligencia artificial en evaluaciones virtuales de semestres anteriores. |
| Uso de apuntes | Aunque el parcial permitía el uso de apuntes, en la sede de Andes no se autorizó su uso por una falla en la comunicación de las instrucciones al encargado de sala. El profesor reconoció el error y se comprometió a incluir una nota explícita al respecto en el enunciado del próximo parcial. |
| Extensión del examen | Varios estudiantes reportaron dificultades de tiempo (uno de ellos no alcanzó a terminar el último punto); el profesor reconoció que el parcial pudo ser extenso y tomó nota para ajustarlo en la siguiente evaluación. |
| Comunicación de horarios | El profesor se comprometió a comunicar con mayor anticipación cualquier cambio de horario de los parciales, en referencia al cambio repentino de horario del primer parcial (ver [clase-07](../clase-07/)). |
| Recomendación de repaso | El profesor recomendó revisar los parciales de semestres anteriores disponibles en el repositorio del curso, ya que la estructura de sus exámenes suele mantenerse, cambiando solo los enunciados. |

## Pendientes

### Docente

- [ ] Incluir una nota explícita en el enunciado del próximo parcial indicando que se permite el uso de apuntes.
- [ ] Ajustar la extensión del próximo parcial, considerado extenso por varios estudiantes.
- [ ] Comunicar con mayor anticipación cualquier cambio de horario de los parciales.

### Estudiantes

- [ ] Revisar los parciales de semestres anteriores disponibles en el repositorio del curso.
- [ ] Completar el cuestionario de configuración, con plazo extendido hasta el martes 22 de septiembre de 2026.
- [ ] Resolver por su cuenta los ejercicios de traducción que quedaron pendientes (Ejemplo 3 en adelante de la nueva batería) antes de la siguiente sesión.

## Próxima clase

Según quedó anotado en el manuscrito ("Inicio: 22/09/2026"), se continuará con la batería de ejercicios de traducción entre lenguaje formal e informal (hablantes de francés en el continente africano, estudiantes que tomaron un curso de Java, y el silogismo de Sócrates) y se abordarán las identidades cuantificacionales; esta sesión podría corresponder ya a la clase 9 de la bitácora.
