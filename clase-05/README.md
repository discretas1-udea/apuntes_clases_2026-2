![Built with AI](https://img.shields.io/badge/Built%20with-AI-blue.svg)

# Clase 05 — Enfoque axiomático

> **Fecha**: 20/08/2026, 25/08/2026, 27/08/2026 · **Modalidad**: Virtual sincrónica · **Apuntes**: [Diapositivas PDF](./apuntes_clase5.pdf) · [PPT](./apuntes_clase5.pptx) · [Manuscrito anotado](./apuntes_clase5_annotated.pdf) · [Corrección Ejemplo 4](./correccion_ejemplo4_annotated.pdf)

## Objetivos de la clase

- Repasar las variantes de la expresión condicional (recíproca, inversa y contrarrecíproca), las tablas de verdad, la clasificación de proposiciones y las equivalencias lógicas vistas en clases anteriores.
- Presentar el enfoque axiomático como alternativa a las tablas de verdad para demostrar equivalencias lógicas, simplificar expresiones y, más adelante, verificar la validez de argumentos.
- Establecer la tabla de identidades lógicas como el conjunto de reglas válidas ("axiomas") sobre las cuales se construyen las demostraciones del curso, y aplicar el formato de demostración afirmación-razón a ejercicios de equivalencia, simplificación y tautología.
- Reforzar, a partir de los errores cometidos en clase, que solo son válidas las transformaciones respaldadas explícitamente por la tabla de equivalencias.

## Resumen

La clase, dictada en tres sesiones, repasó primero las variantes del condicional, las tablas de verdad y las equivalencias lógicas, y presentó el enfoque axiomático con un ejemplo completo de demostración por afirmación-razón, cerrando con el planteamiento de seis ejercicios de repaso. En la segunda sesión se resolvieron sin problema los ejemplos de repaso 1 a 3, mientras que el ejemplo 4 (tautología) quedó sin concluir y el ejemplo 5 se dejó iniciado como pista. En la tercera sesión el profesor mostró en vivo un segundo intento del ejemplo 4, también incorrecto por usar una regla no contemplada en la tabla oficial, aclaró que el enunciado del ejemplo 5 tenía un error de transcripción, resolvió el ejemplo 6, y anunció el envío de la corrección del ejemplo 4 en un archivo aparte. La sesión cerró dando inicio al tema de argumentación lógica (Clase 6).

## Agenda

**Sesión 1 — 20/08/2026**

1. Anuncios y gestión del curso: apertura del cuestionario de seguimiento (Quiz 1) de lógica proposicional, formulario de lista de contactos y formación de un grupo de WhatsApp.
2. Repaso de las variantes de la expresión condicional (recíproca, inversa, contrarrecíproca) a partir del ejemplo "si llueve, entonces el patio está mojado".
3. Repaso de operadores lógicos, tablas de verdad, clasificación de proposiciones (tautología, contradicción, contingencia) y equivalencia lógica.
4. Repaso de algunas equivalencias lógicas notables (implicación, Leyes de Morgan, contrarrecíproco) y sus usos.
5. Analogía con el álgebra y la trigonometría: simplificación de expresiones aplicando identidades conocidas.
6. Introducción al enfoque axiomático: axiomas, identidades lógicas y la tabla de equivalencias lógicas como base del dominio lógico.
7. Comparación entre el enfoque basado en modelos (tablas de verdad) y el enfoque axiomático, repasando el ejemplo `P ∧ (P ∨ Q) ≡ P` con ambos métodos.
8. Formas de escribir demostraciones: en prosa (párrafo) y por afirmación-razón (dos columnas), con el desarrollo completo de `P ∧ (P ∨ Q) ≡ P` por este último método.
9. Planteamiento de seis ejercicios de repaso sobre demostraciones, para desarrollar en la siguiente sesión.

**Sesión 2 — 25/08/2026**

1. Actualizaciones administrativas: cronograma del repositorio actualizado, lista de contactos con 20 estudiantes registrados, y corrección en vivo de un error en el Quiz 1 reportado por un estudiante.
2. Ejemplo de repaso 1: demostración de equivalencia lógica (Ley de Morgan y doble negación).
3. Ejemplo de repaso 2: simplificación de una expresión lógica (distributividad y complemento).
4. Ejemplo de repaso 3: demostración con implicaciones anidadas (definición de implicación y Ley de Morgan).
5. Intento del ejemplo de repaso 4 (tautología): no se concluyó por extenderse más de lo esperado; queda para la siguiente sesión.
6. Ejemplo de repaso 5 iniciado, con un truco de identidad dejado como pista para que los estudiantes completen los pasos restantes.

**Sesión 3 — 27/08/2026**

1. Revisión del segundo intento del ejemplo 4: también resultó incorrecto, por emplear una "regla" (llamada informalmente "contrarrecíproco") que no está en la tabla oficial de equivalencias.
2. Ejemplo de repaso 6, usado también para confirmar formalmente que la regla inventada en el punto anterior era inválida.
3. Explicación del ejemplo de repaso 5: se aclaró que el enunciado había sido transcrito incorrectamente, por lo que la expresión resultó ser una contingencia y no una tautología.
4. Inicio del tema de argumentación lógica (contenido de la Clase 6).

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

### 3. Fundamentos del enfoque axiomático

El profesor introdujo el **enfoque axiomático**: un método para llegar a demostraciones partiendo de axiomas —enunciados que se aceptan sin demostración como punto de partida— y construyendo sobre ellos, mediante reglas de inferencia, una cadena de razonamiento hasta llegar a conclusiones válidas. En el dominio de la lógica proposicional, los axiomas son las identidades lógicas recogidas en la siguiente tabla, que funciona como la "Constitución" o "fuente de verdad" del curso: solo son válidas las transformaciones respaldadas explícitamente por ella (se proporciona en los parciales, no es necesario memorizarla). Cada `≡` puede leerse en ambos sentidos: de izquierda a derecha equivale a **expandir**, de derecha a izquierda equivale a **factorizar**.

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

El profesor ubicó ambos enfoques dentro de un mapa conceptual: una demostración puede referirse a la **equivalencia** o a la **validez** de proposiciones; para demostrar equivalencia existen el **enfoque basado en modelos** (tablas de verdad) y el **enfoque axiomático** (axiomas / identidades lógicas). Ambos permiten también demostrar validez de argumentos (tema que se profundiza en la Clase 6).

Como puente entre ambos enfoques, se repasó la demostración de `P ∧ (P ∨ Q) ≡ P` mediante tabla de verdad (enfoque basado en modelos), confirmando que la columna resultante es una tautología para las cuatro combinaciones de `P` y `Q`.

En el enfoque axiomático, el objetivo es demostrar una equivalencia `A ≡ B` mediante un proceso deductivo que usa los axiomas (identidades lógicas): se parte de un lado de la expresión (`A` o `B`, usualmente el más complejo) y, aplicando identidades lógicas, se transforma paso a paso en expresiones equivalentes hasta llegar a la expresión del lado opuesto (`A ≡ A₁ ≡ A₂ ≡ ... ≡ Aₙ ≡ B`).

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

**Para profundizar y practicar** (la página del curso, al momento de esta clase, llegaba hasta el contenido de la Clase 4): [Ver notas teóricas del sitio](https://discretas1-udea.github.io/discretas1-udea-20262/lessons/mod1/clase4/) · [Autoevaluación](https://discretas1-udea.github.io/discretas1-udea-20262/lessons/mod1/clase4_autoevaluacion/)

### 6. Aplicación del enfoque axiomático: ejemplos de repaso 1 a 3

Estos tres ejercicios se resolvieron sin contratiempos en la sesión del 25/08.

**Ejemplo 1** — Demostrar que `¬((¬p ∨ ¬q) ∨ ¬q) ≡ p ∧ q`:

| # | Afirmación | Razón |
|---|---|---|
| 1 | `¬((¬p ∨ ¬q) ∨ ¬q)` | Lado izquierdo |
| 2 | `¬(¬p ∨ (¬q ∨ ¬q))` | Asociatividad para el ∨ en (1) |
| 3 | `¬(¬p ∨ ¬q)` | Idempotencia para el ∨ en (2) |
| 4 | `¬(¬p) ∧ ¬(¬q)` | Ley de Morgan para el ∨ en (3) |
| 5 | `∴ p ∧ q` | Doble negación en (4) |

**Ejemplo 2** — Simplificar `(p ∨ ¬q) ∧ (¬p ∨ ¬q)`:

| # | Afirmación | Razón |
|---|---|---|
| 1 | `(p ∨ ¬q) ∧ (¬p ∨ ¬q)` | Expresión original |
| 2 | `¬q ∨ (p ∧ ¬p)` | Distributividad para el ∨ (D→I, factorización) en (1) |
| 3 | `¬q ∨ F` | Complemento para el ∧ en (2) |
| 4 | `∴ ¬q` | Identidad para el ∨ en (3) |

**Ejemplo 3** — Demostrar que `p → (q → r) ≡ (p ∧ q) → r`:

| # | Afirmación | Razón |
|---|---|---|
| 1 | `p → (q → r)` | Lado izquierdo |
| 2 | `¬p ∨ (q → r)` | Implicación en (1) |
| 3 | `¬p ∨ (¬q ∨ r)` | Implicación en (2) |
| 4 | `(¬p ∨ ¬q) ∨ r` | Asociatividad para el ∨ en (3) |
| 5 | `¬(p ∧ q) ∨ r` | Ley de Morgan para el ∧ en (4) |
| 6 | `∴ (p ∧ q) → r` | Implicación en (5) |

### 7. El ejemplo 4: dos intentos fallidos y la corrección enviada aparte

Ejercicio: demostrar que `[(p → q) ∧ (q → r)] → (p → r)` es una tautología.

El primer intento (25/08) se extendió sin llegar a una simplificación clara y quedó levantado para la sesión siguiente. El segundo intento (27/08, la "revancha") tampoco llegó a `Verdadero`: en la revisión se detectó que se había empleado una "regla" (`¬P ∨ Q ≡ ¬Q ∨ P`, llamada informalmente "contrarrecíproco") que **no existe** en la tabla oficial de equivalencias del curso — el profesor reconoció el error abiertamente ("suena a machete") y decidió no continuar el ejercicio en clase para no confundir, enviando la solución corregida en un archivo aparte.

La solución corregida ([`correccion_ejemplo4_annotated.pdf`](./correccion_ejemplo4_annotated.pdf)) sigue el camino correcto en 19 pasos, llegando efectivamente a `Verdadero`, confirmando que la expresión sí es una tautología:

| # | Afirmación | Razón |
|---|---|---|
| 1 | `[(p → q) ∧ (q → r)] → (p → r)` | Lado izquierdo |
| 2 | `¬[(p → q) ∧ (q → r)] ∨ (p → r)` | Implicación en (1) |
| 3 | `[¬(p → q) ∨ ¬(q → r)] ∨ (p → r)` | Ley de Morgan para el ∧ en (2) |
| 4 | `¬(p → q) ∨ [¬(q → r) ∨ (p → r)]` | Asociatividad para el ∨ en (3) |
| 5 | `¬(p → q) ∨ [¬(¬q ∨ r) ∨ (¬p ∨ r)]` | Implicación en (4) |
| 6 | `¬(p → q) ∨ [(¬¬q ∧ ¬r) ∨ (¬p ∨ r)]` | Ley de Morgan para el ∨ en (5) |
| 7 | `¬(p → q) ∨ [(q ∧ ¬r) ∨ (¬p ∨ r)]` | Doble negación en (6) |
| 8 | `¬(p → q) ∨ [(q ∨ (¬p ∨ r)) ∧ (¬r ∨ (¬p ∨ r))]` | Distributividad para el ∨ en (7)* |
| 9 | `¬(p → q) ∨ [(q ∨ (¬p ∨ r)) ∧ (¬p ∨ ¬r ∨ r)]` | Conmutatividad para el ∨ en (8) |
| 10 | `¬(p → q) ∨ [(q ∨ (¬p ∨ r)) ∧ (¬p ∨ (¬r ∨ r))]` | Asociatividad para el ∨ en (9) |
| 11 | `¬(p → q) ∨ [(q ∨ (¬p ∨ r)) ∧ (¬p ∨ V)]` | Complemento para el ∨ en (10) |
| 12 | `¬(p → q) ∨ [(q ∨ ¬p ∨ r) ∧ V]` | Dominación para el ∨ en (11) |
| 13 | `¬(p → q) ∨ [q ∨ (¬p ∨ r)]` | Identidad para el ∧ en (12) |
| 14 | `¬(¬p ∨ q) ∨ [q ∨ (¬p ∨ r)]` | Implicación en (13) |
| 15 | `¬(¬p ∨ q) ∨ [¬p ∨ q ∨ r]` | Conmutatividad para el ∨ en (14) |
| 16 | `¬(¬p ∨ q) ∨ [(¬p ∨ q) ∨ r]` | Asociatividad para el ∨ en (15) |
| 17 | `[¬(¬p ∨ q) ∨ (¬p ∨ q)] ∨ r` | Asociatividad para el ∨ en (16) |
| 18 | `V ∨ r` | Complemento para el ∨ en (17) |
| 19 | `∴ V` | Dominación para el ∨ en (18) |

\* *En el manuscrito de la corrección, la razón del paso 8 cita el paso (4) en vez del (7); se transcribe tal como aparece en el archivo original, aunque por la secuencia lógica la distributividad se aplica sobre la expresión del paso (7).*

### 8. El ejemplo 5: un enunciado con error de transcripción

El enunciado original del ejercicio (tomado del libro fuente) era `((p → q) ∧ ¬q) → ¬p` — la forma clásica de *modus tollens*, que es una tautología. Sin embargo, al transcribirlo se introdujo un error y lo que efectivamente se trabajó y explicó en clase fue `(¬p ∧ (p → q)) → ¬q`, una expresión distinta. El profesor aclaró en clase que el procedimiento era correcto — el error estaba en el enunciado transcrito, no en la demostración — y que en el parcial evitará este tipo de inconsistencias.

**Forma explicada en clase** — aplicando la tabla de identidades a `(¬p ∧ (p → q)) → ¬q` se llega a `¬P → ¬Q`, no a `Verdadero`; es decir, tal como quedó enunciada, la expresión es una **contingencia**, no una tautología:

| # | Afirmación | Razón |
|---|---|---|
| 1 | `(¬p ∧ (p → q)) → ¬q` | Lado izquierdo |
| 2 | `(¬p ∧ (¬p ∨ q)) → ¬q` | Implicación en (1) |
| 3 | `((¬p ∨ F) ∧ (¬p ∨ q)) → ¬q` | Identidad para el ∨ en (2) |
| 4 | `(¬p ∨ (F ∧ q)) → ¬q` | Distributividad para el ∨ (D→I, factorización) en (3) |
| 5 | `(¬p ∨ F) → ¬q` | Dominación para el ∧ en (4) |
| 6 | `∴ ¬p → ¬q` | Identidad para el ∨ en (5) |

**Forma más corta** (no explicada en clase — queda para que los estudiantes la analicen por su cuenta), llegando al mismo resultado por absorción:

| # | Afirmación | Razón |
|---|---|---|
| 1 | `(¬p ∧ (p → q)) → ¬q` | Lado izquierdo |
| 2 | `(¬p ∧ (¬p ∨ q)) → ¬q` | Implicación en (1) |
| 3 | `∴ ¬p → ¬q` | Absorción para el ∧ en (2) |

### 9. El ejemplo 6: verdadero o falso

Ejercicio: evaluar si la negación de "Si Susana es la madre de Luis, entonces Ali es su primo" es "Si Ali no es primo de Luis, entonces Susana no es la madre de Luis".

Traduciendo a lógica proposicional (`P`: Susana es la madre de Luis; `Q`: Ali es primo de Luis), la pregunta es si `¬(P → Q) ≡ ¬Q → ¬P`:

| # | Afirmación | Razón |
|---|---|---|
| 1 | `¬(p → q)` | Lado izquierdo |
| 2 | `¬(¬p ∨ q)` | Implicación en (1) |
| 3 | `¬(¬p) ∧ ¬q` | Ley de Morgan para el ∨ en (2) |
| 4 | `∴ p ∧ ¬q` | Doble negación en (3) |

Como `p ∧ ¬q` no puede transformarse en `¬q → ¬p` mediante las reglas de la tabla (de hecho, `¬q → ¬p ≡ ¬(¬q) ∨ ¬p ≡ q ∨ ¬p`, una expresión distinta), la afirmación es **falsa**: la negación de un condicional no es su contrarrecíproco.

Este resultado, además de resolver el ejercicio, sirvió como confirmación formal de que la "regla" usada por error en el segundo intento del ejemplo 4 (que trataba `¬P ∨ Q` como si fuera intercambiable con `¬Q ∨ P`) no tiene sustento en la tabla de equivalencias del curso.

## Medios de comunicación

1. Foro del curso: canal oficial para notificar la habilitación de los cuestionarios de seguimiento y el tiempo disponible para resolverlos.
2. Grupo de WhatsApp del curso: en formación a partir de la lista de contactos; el enlace se compartirá en el chat del curso una vez creado.

## Recursos del curso

| Recurso | Descripción | Enlace |
|---|---|---|
| Cronograma del curso | Actualizado en el repositorio, reemplazando el archivo Excel desactualizado; registrado hasta la sesión anterior a esta clase. | — |
| Lista de contactos | Formulario para consolidar nombres, correos y ubicación geográfica; 20 estudiantes registrados a la fecha, pensado para facilitar la formación de grupos de trabajo. | — |

## Evaluación

| Actividad | Detalle |
|---|---|
| Quiz 1 (Primer Seguimiento) | Disponible desde las 8:00 a.m. del 20/08/2026 hasta el 31/08/2026. 10 preguntas sobre lógica proposicional, sin límite de tiempo, se puede repetir las veces que se desee y se registra la nota más alta. Durante la sesión del 25/08 se corrigió en vivo un error reportado por un estudiante (una pregunta de selección múltiple estaba configurada como selección única); en la sesión del 27/08 se corrigió otra inconsistencia similar en un quiz posterior. |
| Cuestionarios de tablas de verdad, enfoque axiomático y argumentación lógica | Pendientes de habilitación al cierre de esta clase, a la espera de que el profesor revisara y corrigiera inconsistencias en sus enunciados. |
| Parcial (primera parte del curso) | Programado aproximadamente para el 12 de septiembre (fecha distinta a la de los cuestionarios de seguimiento, que se van habilitando en Moodle por separado). |

## Pendientes

### Docente

- [x] Enviar la solución corregida del ejemplo 4, aplicando únicamente reglas de la tabla de equivalencias (entregada por separado, ver [`correccion_ejemplo4_annotated.pdf`](./correccion_ejemplo4_annotated.pdf)).
- [ ] Habilitar los cuestionarios de tablas de verdad y enfoque axiomático, corrigiendo antes las inconsistencias detectadas en sus enunciados, y notificar por el foro.
- [ ] Habilitar el cuestionario de argumentación lógica una vez cubierto ese tema (Clase 6).
- [ ] Contactar a la coordinadora académica sobre el cruce de horarios reportado por una estudiante.
- [ ] Subir a la plataforma del curso las grabaciones de las sesiones del 25/08 y del 27/08.

### Estudiantes

- [ ] Resolver el ejercicio de variantes del condicional dejado como tarea en la sesión del 20/08.
- [ ] Completar el Quiz 1 de lógica proposicional antes del 31 de agosto (repetible; cuenta la nota más alta).
- [ ] Completar el formulario de lista de contactos, si aún no lo han hecho.
- [ ] Revisar los ejemplos resueltos de enfoque axiomático disponibles en la página del curso.
- [ ] Analizar por cuenta propia la segunda forma (más corta, vía absorción) de la demostración del ejemplo 5, no explicada en clase.
- [ ] Revisar el ejemplo de argumento con tabla de verdad de tres variables (A, B, C) resuelto al final de la sesión del 27/08, dejado como ejercicio de análisis autónomo.

## Próxima clase

1 de septiembre de 2026: continuación de argumentación lógica con el enfoque axiomático (tabla de silogismos/reglas de inferencia).