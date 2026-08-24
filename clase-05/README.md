![Built with AI](https://img.shields.io/badge/Built%20with-AI-blue.svg)

# Clase 5 — Enfoque axiomático

> **Fecha**: 20/08/2026 · **Modalidad**: Virtual sincrónica · **Apuntes**: [Diapositivas PDF](./apuntes_clase5.pdf) · [PPT](./apuntes_clase5.pptx) · [Manuscrito anotado](./apuntes_clase5_annotated.pdf)

> [!NOTE]
> Esta clase continúa el 25/08/2026 con el desarrollo de los seis ejercicios de repaso planteados al cierre de esta sesión (ver "Próxima clase" y "Pendientes"). Este README se actualizará una vez se documente esa continuación.

## Objetivos de la clase

- Repasar las variantes de la expresión condicional (recíproca, inversa y contrarrecíproca) y su relación de equivalencia con la proposición original.
- Repasar las tablas de verdad, la clasificación de proposiciones y las equivalencias lógicas vistas en clases anteriores.
- Introducir el enfoque axiomático como método alternativo a las tablas de verdad para demostrar equivalencias lógicas, mediante identidades lógicas y demostraciones por afirmación-razón.
- Presentar un ejemplo completo de demostración usando el enfoque axiomático.

## Resumen

La sesión, dictada en modalidad virtual sincrónica, tuvo dos partes: un repaso de las variantes del condicional, las tablas de verdad, la clasificación de proposiciones y las equivalencias lógicas vistas hasta el momento, y la introducción del enfoque axiomático como alternativa más eficiente que las tablas de verdad para demostrar equivalencias en expresiones con muchas variables. El profesor presentó la tabla de identidades lógicas como base del enfoque axiomático y desarrolló un ejemplo completo de demostración por afirmación-razón. La clase concluyó sin alcanzar a desarrollar los ejercicios de repaso planteados, los cuales quedaron pendientes para la sesión del 25/08/2026.

## Agenda

1. Repaso de las variantes de la expresión condicional (recíproca, inversa, contrarrecíproca) a partir del ejemplo "si llueve, entonces el patio está mojado".
2. Repaso de operadores lógicos, tablas de verdad, clasificación de proposiciones (tautología, contradicción, contingencia) y equivalencia lógica.
3. Repaso de algunas equivalencias lógicas notables (implicación, Leyes de Morgan, contrarrecíproco) y sus usos.
4. Analogía con el álgebra y la trigonometría: simplificación de expresiones aplicando identidades conocidas.
5. Introducción al enfoque axiomático: axiomas, identidades lógicas y la tabla de equivalencias lógicas como base del dominio lógico.
6. Comparación entre el enfoque basado en modelos (tablas de verdad) y el enfoque axiomático, repasando el ejemplo `P ∧ (P ∨ Q) ≡ P` con ambos métodos.
7. Formas de escribir demostraciones: en prosa (párrafo) y por afirmación-razón (dos columnas).
8. Desarrollo completo de la demostración por afirmación-razón de `P ∧ (P ∨ Q) ≡ P`.
9. Planteamiento de seis ejercicios de repaso sobre demostraciones, para desarrollar en la siguiente sesión (25/08/2026).

## Contenido temático

### 1. Variantes de la expresión condicional

A partir de una proposición condicional original `P → Q`, se derivan otras tres formas cambiando el orden de las proposiciones y/o negándolas:

| Caso | Expresión lógica | ¿Equivalente al original? |
|---|---|---|
| Original | `P → Q` | — |
| Recíproca | `Q → P` | No |
| Inversa | `¬P → ¬Q` | No |
| Contrarrecíproca | `¬Q → ¬P` | Sí |

El profesor ilustró esto con el enunciado "si llueve, entonces el patio está mojado" (`P` = "llueve", `Q` = "el patio está mojado"). Explicó que la recíproca ("si el patio está mojado, entonces llovió") y la inversa no son equivalentes al original, ya que existen otras causas posibles para que el patio esté mojado (por ejemplo, un tubo roto). En cambio, la contrarrecíproca ("si el patio no está mojado, entonces no llovió") sí es lógicamente equivalente al original, lo cual puede verificarse mediante tabla de verdad.

### 2. Repaso: tablas de verdad, clasificación de proposiciones y equivalencias lógicas

Se repasaron las tablas de verdad de los seis operadores lógicos y las reglas de prioridad y asociatividad vistas en clases anteriores, así como la clasificación de proposiciones:

- **Tautología**: verdadera en todos los casos posibles.
- **Contradicción**: falsa en todos los casos posibles.
- **Contingencia**: verdadera para ciertas combinaciones y falsa para otras.

Se recordó la definición de equivalencia lógica (`p` y `q` son equivalentes si `p ↔ q` es una tautología) y se repasaron dos resultados ya demostrados en la clase anterior: la doble negación (`¬(¬p) ≡ p`) y la primera Ley de De Morgan (`¬(p ∧ q) ≡ ¬p ∨ ¬q`, distinta de `¬p ∧ ¬q`).

Como cierre del repaso se presentó un cuadro de equivalencias lógicas notables y sus usos:

| Nombre | Equivalencia |
|---|---|
| Implicación | `¬p ∨ q ≡ p → q` |
| Leyes de Morgan | `¬(p ∧ q) ≡ ¬p ∨ ¬q` · `¬(p ∨ q) ≡ ¬p ∧ ¬q` |
| Contrarrecíproco | `¬p → ¬q ≡ ¬q → ¬p` |

Usos de estas equivalencias mencionados en clase: hacer demostraciones, simplificar expresiones lógicas, verificar la validez de argumentos (tema de una próxima clase) y derivar nuevas proposiciones.

### 3. Enfoque axiomático

El profesor introdujo el **enfoque axiomático**: un método para llegar a demostraciones partiendo de axiomas —enunciados que se aceptan sin demostración como punto de partida— y construyendo sobre ellos, mediante reglas de inferencia, una cadena de razonamiento hasta llegar a conclusiones válidas. En el dominio de la lógica proposicional, los axiomas son las identidades lógicas recogidas en la siguiente tabla, que funciona como la "fuente de verdad" del enfoque (cada `≡` puede leerse en ambos sentidos: para expandir o para factorizar una expresión):

| Nombre | Equivalencia lógica (∧) | Equivalencia lógica (∨) |
|---|---|---|
| Conmutatividad | `P ∧ Q ≡ Q ∧ P` | `P ∨ Q ≡ Q ∨ P` |
| Asociatividad | `P ∧ (Q ∧ R) ≡ (P ∧ Q) ∧ R` | `P ∨ (Q ∨ R) ≡ (P ∨ Q) ∨ R` |
| Distributividad | `P ∧ (Q ∨ R) ≡ (P ∧ Q) ∨ (P ∧ R)` | `P ∨ (Q ∧ R) ≡ (P ∨ Q) ∧ (P ∨ R)` |
| Idempotencia | `P ∧ P ≡ P` | `P ∨ P ≡ P` |
| Doble negación | `¬(¬P) ≡ P` | |
| Leyes de Morgan | `¬(P ∧ Q) ≡ ¬P ∨ ¬Q` | `¬(P ∨ Q) ≡ ¬P ∧ ¬Q` |
| Identidad | `P ∧ V ≡ P` | `P ∨ F ≡ P` |
| Dominación | `P ∧ F ≡ F` | `P ∨ V ≡ V` |
| Absorción | `P ∧ (P ∨ Q) ≡ P` | `P ∨ (P ∧ Q) ≡ P` |
| Complemento | `P ∧ ¬P ≡ F` | `P ∨ ¬P ≡ V` |
| Implicación | `P → Q ≡ ¬P ∨ Q` | |
| Contrarrecíproco | `P → Q ≡ ¬Q → ¬P` | |
| Equivalencia | `P ↔ Q ≡ (P → Q) ∧ (Q → P)` | |

Para motivar la utilidad del enfoque, el profesor trazó una analogía con el álgebra y la trigonometría: así como se simplifican expresiones racionales o trigonométricas aplicando propiedades e identidades ya conocidas (sin volver a demostrarlas cada vez), en lógica se simplifican o demuestran expresiones aplicando la tabla de identidades lógicas. También señaló que verificar una equivalencia por tabla de verdad es infalible pero impráctico cuando hay muchas variables (por ejemplo, 6 variables generan `2⁶ = 64` filas, y 10 variables generarían `2¹⁰ = 1024`).

### 4. Enfoque basado en modelos vs. enfoque axiomático

El profesor ubicó ambos enfoques dentro de un mapa conceptual: una demostración puede referirse a la **equivalencia** o a la **validez** de proposiciones; para demostrar equivalencia existen el **enfoque basado en modelos** (tablas de verdad) y el **enfoque axiomático** (axiomas / identidades lógicas), siendo este último el tema de la clase.

Como puente entre ambos enfoques, se repasó la demostración de `P ∧ (P ∨ Q) ≡ P` mediante tabla de verdad (enfoque basado en modelos), confirmando que la columna resultante es una tautología para las cuatro combinaciones de `P` y `Q`.

En el enfoque axiomático, el objetivo es demostrar una equivalencia `A ≡ B` mediante un proceso deductivo que usa los axiomas (identidades lógicas): se parte de un lado de la expresión (`A` o `B`) y, aplicando identidades lógicas, se transforma paso a paso en expresiones equivalentes hasta llegar a la expresión del lado opuesto (`A ≡ A₁ ≡ A₂ ≡ ... ≡ Aₙ ≡ B`).

### 5. Demostración por afirmación-razón

El profesor presentó dos formas de escribir demostraciones: en **prosa/narrativa** (párrafos continuos, forma estándar en libros universitarios) y por **afirmación-razón** (dos columnas, donde cada paso se numera y se indica explícitamente la regla aplicada), siendo esta última la adoptada para el curso.

Se desarrolló la demostración completa de `P ∧ (P ∨ Q) ≡ P` con este método:

| # | Afirmación | Razón |
|---|---|---|
| 1 | `P ∧ (P ∨ Q)` | Hipótesis (lado izquierdo) |
| 2 | `(P ∧ P) ∨ (P ∧ Q)` | Distributividad para el ∧ en (1) |
| 3 | `P ∨ (P ∧ Q)` | Idempotencia para el ∧ en (2) |
| 4 | `(P ∧ V) ∨ (P ∧ Q)` | Identidad para el ∧ en (3) |
| 5 | `P ∧ (V ∨ Q)` | Distributividad para el ∧ (factorización) en (4) |
| 6 | `P ∧ V` | Dominación para el ∨ en (5) |
| 7 | `P` | Identidad para el ∧ en (6) |

Al nombrar cada regla se debe indicar si se aplica para el operador `∧` o `∨`, y el sentido de aplicación cuando sea necesario (expandir o factorizar), para mayor claridad en la justificación de cada paso.

**Para profundizar y practicar**: [Ver notas teóricas del sitio del curso](https://discretas1-udea.github.io/discretas1-udea-20262/lessons/mod1/clase4/) · [Autoevaluación](https://discretas1-udea.github.io/discretas1-udea-20262/lessons/mod1/clase4_autoevaluacion/)

## Evaluación

| Actividad | Detalle |
|---|---|
| Quiz 1 (Primer Seguimiento) | Disponible desde las 8:00 a.m. del 20/08/2026 hasta el 31/08/2026. 10 preguntas sobre lógica proposicional, sin límite de tiempo, se puede repetir las veces que se desee y se registra la nota más alta. |

## Pendientes

### Estudiantes

- [ ] Resolver el ejercicio de variantes del condicional dejado como tarea en la primera parte de la clase.
- [ ] Realizar el Quiz 1 (Primer Seguimiento), disponible hasta el 31/08/2026.
- [ ] Completar el formulario de lista de contactos del curso, para facilitar la formación de grupos de estudio y trabajo.
- [ ] Revisar los ejemplos resueltos de enfoque axiomático disponibles en la página del curso, como preparación para la próxima sesión.
- [ ] Desarrollar los seis ejercicios de repaso sobre demostraciones planteados al cierre de la clase (pendientes para la sesión del 25/08/2026, aún no desarrollados en el manuscrito).

## Próxima clase

Se continuará con ejercicios de demostración usando el enfoque axiomático, desarrollando los seis ejercicios de repaso planteados al cierre de esta sesión (martes 25/08/2026).
