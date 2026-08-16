![Built with AI](https://img.shields.io/badge/Built%20with-AI-blue.svg)

# Clase 3 — Axiomas de verdad: operadores lógicos, jerarquía y evaluación de expresiones

> **Fecha**: 11/08/2026, 13/08/2026 · **Modalidad**: Virtual sincrónica · **Apuntes**: [Diapositivas PDF](./apuntes_clase3.pdf) · [PPT](./apuntes_clase3.pptx) · [Manuscrito anotado](./apuntes_clase3_annotated.pdf)

## Objetivos de la clase

- Presentar los axiomas de verdad (tablas de verdad) de los operadores lógicos: negación, conjunción, disyunción inclusiva y exclusiva, condicional y bicondicional.
- Ilustrar la traducción entre lenguaje natural y lenguaje lógico mediante ejemplos cotidianos.
- Establecer la jerarquía de precedencia y asociatividad de los operadores lógicos.
- Guiar la evaluación del valor de verdad de expresiones lógicas compuestas mediante ejercicios resueltos en clase.

## Resumen

El profesor retomó la traducción entre lenguaje natural y lenguaje lógico y presentó, mediante tablas de verdad, el comportamiento de los seis operadores lógicos básicos. Con ejemplos cotidianos —Batman, Zinedine Zidane, Anselmo, la milla de John, entre otros— condujo a los estudiantes a identificar conectores principales y evaluar proposiciones compuestas. La sesión, dictada en dos días (11 y 13 de agosto), cerró con la jerarquía de precedencia de los operadores y ejercicios de evaluación, dejando una tarea para la siguiente clase.

## Agenda

**Sesión 1 — 11/08/2026**

1. Traducción entre lenguaje natural y lenguaje lógico.
2. Axiomas de verdad: tablas de verdad de negación, conjunción, disyunción inclusiva y exclusiva, condicional y bicondicional.
3. Ejemplo de negación con la proposición "Batman es un villano".
4. Ejemplo de doble negación con "Hoy es lunes".
5. Ejemplo de conjunción con proposiciones sobre Zinedine Zidane.

**Sesión 2 — 13/08/2026**

1. Revisión de la tarea de traducción de proposiciones asignada en la sesión anterior (ej. el problema del pianista).
2. Ejemplo de disyunción inclusiva con la proposición "Anselmo estudia o trabaja".
3. Ejemplo de disyunción exclusiva con "Me gusta el pan o la torta, pero no ambos".
4. Condicional: la relación como "contrato" entre hipótesis (antecedente) y conclusión (consecuente), con ejemplos de traducción.
5. Bicondicional (equivalencia): ejemplos de evaluación de verdad.
6. Jerarquía de operadores: prioridad y asociatividad.
7. Ejercicios de evaluación de expresiones lógicas compuestas, resueltos en clase.
8. Asignación de la tarea para la próxima clase y anuncio del cuestionario previo del Foro.

## Contenido temático

### 1. Traducción entre lenguaje natural y lenguaje lógico

El profesor explicó el proceso de traducción entre lenguaje natural y lenguaje lógico como una correspondencia de ida y vuelta: se identifican las proposiciones simples, se les asigna una variable proposicional y se ensambla la fórmula con los conectores correspondientes. Ejemplo trabajado: "Hoy es lunes y cumplo años" se tradujo como `L ∧ A`.

### 2. Operadores lógicos y sus tablas de verdad

| Operador | Símbolo | Se lee "verdadero" cuando... |
|---|---|---|
| Negación | ¬p | p es falsa |
| Conjunción | p ∧ q | ambas proposiciones son verdaderas |
| Disyunción inclusiva | p ∨ q | al menos una de las dos es verdadera |
| Disyunción exclusiva | p ⊕ q | exactamente una de las dos es verdadera (no ambas) |
| Condicional | p → q | p (hipótesis) implica q (conclusión); solo es falsa cuando p es verdadera y q es falsa |
| Bicondicional (equivalencia) | p ↔ q | ambas proposiciones tienen el mismo valor de verdad |

**Negación**

| p | ¬p |
|---|---|
| F | V |
| V | F |

Ejemplo: con `B` = "Batman es un villano" (falsa), su negación `¬B` = "Batman es un héroe" es verdadera. También se mostró que la doble negación equivale a la proposición original: `¬(¬L) ≡ L`.

**Conjunción**

| p | q | p ∧ q |
|---|---|---|
| F | F | F |
| F | V | F |
| V | F | F |
| V | V | V |

Ejemplo: `P` = "Zidane fue jugador del Real Madrid" (V), `Q` = "Zidane es francés" (V) → `P ∧ Q ≡ V`. Con `R` = "Zidane es colombiano" (F): `P ∧ R ≡ F`, mientras que `P ∧ ¬R ≡ V`.

**Disyunción inclusiva**

| p | q | p ∨ q |
|---|---|---|
| F | F | F |
| F | V | V |
| V | F | V |
| V | V | V |

Ejemplo: `e` = "Anselmo estudia", `t` = "Anselmo trabaja" → `e ∨ t` es verdadera si Anselmo hace al menos una de las dos cosas (o ambas).

**Disyunción exclusiva**

| p | q | p ⊕ q |
|---|---|---|
| F | F | F |
| F | V | V |
| V | F | V |
| V | V | F |

Ejemplo: "Me gusta el pan o la torta, pero no ambos" → `P ⊕ T`, verdadera solo si exactamente una de las dos proposiciones lo es.

**Condicional**

| p | q | p → q |
|---|---|---|
| F | F | V |
| F | V | V |
| V | F | F |
| V | V | V |

El profesor la presentó como un "contrato" entre hipótesis (antecedente) y conclusión (consecuente): solo es falsa cuando la hipótesis se cumple pero la conclusión no. Ejemplos traducidos en clase:

- "Si la guerra terminara, entonces viviríamos mejor" → `guerra → vivir_mejor`.
- "Si un país no tiene analfabetismo, nadie muere allí" → `¬A → ¬M`.
- "Si todos amáramos a la selección Colombia, no habría guerra" → `C → ¬G`.

**Bicondicional (equivalencia)**

| p | q | p ↔ q |
|---|---|---|
| F | F | V |
| F | V | F |
| V | F | F |
| V | V | V |

Es verdadera cuando ambas proposiciones tienen el mismo valor de verdad. Ejemplos:

- "7 > 10 si y solo si -8 > -16" → `P ↔ Q` con `P = F` y `Q = V` ⇒ resultado `F`.
- "El sol es amarillo si y solo si 10 > 9" → `S ↔ M` con ambas verdaderas ⇒ resultado `V`.

### 3. Jerarquía de operadores

| Prioridad | Operador | Asociatividad |
|---|---|---|
| 1 (más alta) | ¬ (negación) | No aplica (unitario) |
| 2 | ∧ (conjunción) | Izquierda a derecha |
| 3 | ∨ (disyunción inclusiva) | Izquierda a derecha |
| 4 | ⊕ (disyunción exclusiva) | Izquierda a derecha |
| 5 | → (condicional) | Derecha a izquierda |
| 6 (más baja) | ↔ (bicondicional) | Derecha a izquierda |

Cuando dos o más operaciones tienen igual orden de precedencia, se resuelven según su asociatividad; los paréntesis siempre alteran este orden.

### 4. Evaluación de expresiones lógicas compuestas

Ejercicios resueltos en clase, aplicando reemplazo de valores y la jerarquía de operadores:

- Con `h` = "Hace calor" (V) y `s` = "El día está soleado" (F): `¬h ∧ s ≡ F` y `¬h ∧ ¬s ≡ F`.
- Para `(p ∨ q) ∧ ¬(p ∧ q)`: con `p = V, q = V` el resultado es `F`; con `p = V, q = F` el resultado es `V`.
- Dado que `R ∨ P ≡ F`, `Q ∧ P ≡ F` y `P ≡ F`, se dedujo que `Q ≡ F` y `R ≡ F`.

**Para profundizar y practicar**: [Ver notas teóricas del sitio del curso](https://discretas1-udea.github.io/discretas1-udea-20262/lessons/mod1/clase1/) · [Diapositivas](https://discretas1-udea.github.io/discretas1-udea-20262/assets/slides/clase1.pdf)

## Pendientes

### Docente

- [ ] Revisar los ejercicios/actividades correspondientes a los números "13.0.8.20.26" mencionados durante la clase.
- [ ] Abrir en el Foro el cuestionario previo de lógica (selección lógica / fundamento 16) y notificar a los estudiantes cuando esté disponible.
- [ ] Subir la grabación y los apuntes de la sesión del 11/08 para que los estudiantes puedan revisarlos.

### Estudiantes

- [ ] Deducir los valores de verdad de P, Q y R sabiendo que `(Q → R) → [P ∧ Q ∨ R] ≡ F` (tarea para la próxima clase, según el manuscrito).
- [ ] Realizar el cuestionario previo de lógica en el Foro dentro de los 8 días posteriores a su apertura.

## Próxima clase

Se revisará la tarea sobre los valores de verdad de P, Q y R, y se espera que el cuestionario previo de lógica del Foro esté disponible (plazo de 8 días desde su apertura).
