![Built with AI](https://img.shields.io/badge/Built%20with-AI-blue.svg)

# Clase 11 — Demostraciones en lógica cuantificacional

> **Fecha**: 01/10/2026 · **Modalidad**: Virtual sincrónica · **Apuntes**: [Diapositivas PDF](./apuntes_clase11.pdf) · [PPT](./apuntes_clase11.pptx) · [Manuscrito anotado](./apuntes_clase11_annotated.pdf)
>
> Las anotaciones a mano sobre las diapositivas 1–22 se perdieron porque el programa de anotación se cerró sin guardar durante la clase. Esas diapositivas ya traen los ejemplos resueltos. El manuscrito anotado tiene tinta a partir del Ejercicio 1 (pág. 25).

<!-- Sesión 2 (06/10/2026): pendiente. Agregar la fecha a la metadata, la Agenda de la sesión 2, las secciones de la corrección del Ejercicio 2 y de los ejercicios 3–6, y actualizar la Síntesis y los Pendientes. -->

## Objetivos de la clase

- Repasar las herramientas acumuladas para el segundo parcial: formas aristotélicas, equivalencias y reglas de inferencia proposicionales.
- Presentar las cuatro reglas de inferencia con cuantificadores (instanciación y generalización, universal y existencial).
- Establecer el procedimiento para demostrar con cuantificadores: instanciar, aplicar reglas proposicionales y, si hace falta, generalizar.
- Aplicar el procedimiento en ejemplos resueltos y en los primeros ejercicios de repaso.

## Resumen

La clase empezó con los avisos sobre el segundo parcial y un repaso de las tablas que se entregarán en el examen. Se presentaron las cuatro reglas de inferencia con cuantificadores y se aplicaron en tres ejemplos (Sócrates, Josefina y el estudiante que no leyó el libro). En los ejercicios de repaso, se resolvió el Ejercicio 1. El Ejercicio 2 no salió porque su enunciado estaba mal copiado del libro: quedó para revisar en la siguiente sesión.

## Agenda

**Sesión 1 — 01/10/2026**

1. Avisos: segundo parcial, notas del primer parcial, primer 25 % y quices. [*(→ Evaluación)*](#evaluación)
2. Repaso: formas aristotélicas, equivalencias proposicionales y cuantificacionales, reglas de inferencia proposicionales. [*(→ sección 1)*](#1-repaso-para-el-segundo-parcial)
3. De la demostración proposicional a la cuantificacional. [*(→ sección 2)*](#2-de-la-demostración-proposicional-a-la-cuantificacional)
4. Reglas de inferencia con cuantificadores: UI, UG, EI y EG. [*(→ sección 3)*](#3-reglas-de-inferencia-con-cuantificadores)
5. Ejemplo 1: Sócrates es mortal. [*(→ sección 4)*](#4-ejemplo-1-sócrates-es-mortal)
6. Ejemplo 2: Josefina ha tomado un curso de informática. [*(→ sección 5)*](#5-ejemplo-2-josefina-ha-tomado-un-curso-de-informática)
7. Ejemplo 3: alguien que aprobó el examen no ha leído el libro. [*(→ sección 6)*](#6-ejemplo-3-alguien-que-aprobó-el-examen-no-ha-leído-el-libro)
8. Ejercicios de repaso: enunciados. [*(→ sección 7)*](#7-ejercicios-de-repaso)
9. Ejercicio 1: 4 es un número positivo. [*(→ sección 8)*](#8-ejercicio-1-4-es-un-número-positivo)
10. Ejercicio 2: intento con el enunciado erróneo; queda para revisar. [*(→ sección 9)*](#9-ejercicio-2-intento-con-el-enunciado-erróneo)

## Contenido temático

> [!NOTE]
> **Cómo leer este apunte.**
>
> - Las secciones numeradas siguen el orden en que se dictó la clase.
> - Las secciones 1 a 6 se basan en las diapositivas (que ya traen las soluciones) y en lo dicho en clase. Las secciones 8 y 9 se basan en el manuscrito anotado (págs. 25–26). La marca «Fin: 01/10/2026» está en la pág. 27.
> - Los párrafos que empiezan con *Aclaración del apunte* se agregaron al redactar: no se dijeron en clase. Sirven para conectar ideas o evitar confusiones.

**Notación usada en este apunte**

| Símbolo | Se lee | Observación |
|---|---|---|
| `∀x` | "para todo x" | Cuantificador universal. |
| `∃x` | "existe (al menos) un x" | Cuantificador existencial. |
| `c`, `a` | constantes | Nombran un individuo particular del universo. En las reglas, `c` es un individuo cualquiera; `a` es la constante **nueva** que introduce la instanciación existencial. |
| `∴` | "por lo tanto" | Precede a la conclusión de un argumento. |
| `⇒` | "de esto se infiere esto" | Se usa en la tabla de reglas con cuantificadores (`∀x P(x) ⇒ P(c)`): indica qué afirmación se puede escribir como paso siguiente. **No** es un conectivo dentro de una fórmula. |
| `→` | "si…, entonces…" | Conectivo **dentro** de una fórmula. |
| `≡` | "es equivalente a" | Afirma algo **sobre** dos fórmulas: tienen siempre el mismo valor de verdad. Las equivalencias se pueden usar en ambos sentidos; las reglas de inferencia, solo en uno. |
| `⊢` | "se deduce" | Forma simbólica de un argumento (sección 2). |
| UI, UG, EI, EG | instanciación universal, generalización universal, instanciación existencial, generalización existencial | Las cuatro reglas de la sección 3 (siglas en inglés). |

### 1. Repaso para el segundo parcial

Antes de las reglas nuevas, el profesor recordó todo lo que se acumula para el segundo parcial (págs. 2–7). Estas tablas se entregarán durante el examen ([Evaluación](#evaluación)): **lo que se evalúa no es memorizarlas, sino saber aplicarlas**.

**Formas aristotélicas** (págs. 2–3):

| Forma | Enunciado | Lógica de predicados | Ejemplo |
|---|---|---|---|
| A: universal afirmativa | Todos los S son P | `∀x (S(x) → P(x))` | Todos los hombres son mortales: `∀x (hombre(x) → mortal(x))` |
| E: universal negativa | Ningún S es P | `∀x (S(x) → ¬P(x))` | Ningún cuadrado es círculo: `∀x (cuadrado(x) → ¬circulo(x))` |
| I: particular afirmativa | Algún S es P | `∃x (S(x) ∧ P(x))` | Algún estudiante es ingeniero: `∃x (estudiante(x) ∧ ingeniero(x))` |
| O: particular negativa | Algún S no es P | `∃x (S(x) ∧ ¬P(x))` | Algún pájaro no vuela: `∃x (pajaro(x) ∧ ¬vuela(x))` |

**Equivalencias.** Todas las equivalencias de la lógica proposicional valen también en la lógica cuantificacional, aplicadas a las fórmulas dentro del alcance de los cuantificadores: basta cambiar las variables proposicionales (`P`, `Q`, `R`) por funciones proposicionales (`P(x)`, `Q(x)`, `R(x)`) (pág. 4). A ellas se suman las equivalencias propias de los cuantificadores, vistas en la [clase 9](../clase-09/README.md#9-tabla-de-equivalencias-cuantificacionales); el profesor resaltó las leyes de De Morgan para cuantificadores.

<details>
<summary>Tabla de equivalencias de lógica proposicional (pág. 4)</summary>

| Nombre | Equivalencia | |
|---|---|---|
| Conmutatividad | `P ∧ Q ≡ Q ∧ P` | `P ∨ Q ≡ Q ∨ P` |
| Asociatividad | `P ∧ (Q ∧ R) ≡ (P ∧ Q) ∧ R` | `P ∨ (Q ∨ R) ≡ (P ∨ Q) ∨ R` |
| Distributividad | `P ∧ (Q ∨ R) ≡ (P ∧ Q) ∨ (P ∧ R)` | `P ∨ (Q ∧ R) ≡ (P ∨ Q) ∧ (P ∨ R)` |
| Idempotencia | `P ∧ P ≡ P` | `P ∨ P ≡ P` |
| Doble negación | `¬(¬P) ≡ P` | |
| Leyes de De Morgan | `¬(P ∧ Q) ≡ ¬P ∨ ¬Q` | `¬(P ∨ Q) ≡ ¬P ∧ ¬Q` |
| Identidad | `P ∧ V ≡ P` | `P ∨ F ≡ P` |
| Dominación | `P ∧ F ≡ F` | `P ∨ V ≡ V` |
| Absorción | `P ∧ (P ∨ Q) ≡ P` | `P ∨ (P ∧ Q) ≡ P` |
| Complemento | `P ∧ ¬P ≡ F` | `P ∨ ¬P ≡ V` |
| Implicación | `P → Q ≡ ¬P ∨ Q` | |
| Contrarrecíproco | `P → Q ≡ ¬Q → ¬P` | |
| Equivalencia | `P ↔ Q ≡ (P → Q) ∧ (Q → P)` | |

</details>

<details>
<summary>Tabla de equivalencias de lógica cuantificacional (págs. 5–6)</summary>

| Nombre | Equivalencia |
|---|---|
| Negación de cuantificadores (De Morgan cuántico) | `¬∀x P(x) ≡ ∃x ¬P(x)` y `¬∃x P(x) ≡ ∀x ¬P(x)` |
| Distributividad del cuantificador universal sobre la conjunción | `∀x (P(x) ∧ Q(x)) ≡ ∀x P(x) ∧ ∀x Q(x)` |
| Distributividad (en un solo sentido) del cuantificador universal sobre la disyunción | `(∀x P(x) ∨ ∀x Q(x)) → ∀x (P(x) ∨ Q(x))` |
| Distributividad del cuantificador existencial sobre la disyunción | `∃x (P(x) ∨ Q(x)) ≡ ∃x P(x) ∨ ∃x Q(x)` |
| Distributividad (en un solo sentido) del cuantificador existencial sobre la conjunción | `∃x (P(x) ∧ Q(x)) → ∃x P(x) ∧ ∃x Q(x)` |
| Distribución de cuantificadores (restricciones), si la fórmula `Q` no contiene la variable cuantificada x | `∀x (P(x) ∨ Q) ≡ (∀x P(x)) ∨ Q` y `∃x (P(x) ∧ Q) ≡ (∃x P(x)) ∧ Q` |
| Intercambio del orden de cuantificadores iguales | `∀x ∀y P(x,y) ≡ ∀y ∀x P(x,y)` y `∃x ∃y P(x,y) ≡ ∃y ∃x P(x,y)` |
| No conmutatividad entre cuantificadores diferentes | `∀x ∃y P(x,y) ≢ ∃y ∀x P(x,y)` |

</details>

**Reglas de inferencia proposicionales** (pág. 7). Siguen valiendo dentro de las demostraciones con cuantificadores, una vez eliminados los cuantificadores (sección 3):

| Nombre | Premisas | Conclusión |
|---|---|---|
| Modus Ponens | `p → q`, `p` | `∴ q` |
| Modus Tollens | `p → q`, `¬q` | `∴ ¬p` |
| Silogismo hipotético (Transitividad) | `p → q`, `q → r` | `∴ p → r` |
| Silogismo disyuntivo (Eliminación) | `p ∨ q`, `¬p` | `∴ q` |
| Adición | `p` | `∴ p ∨ q` |
| Simplificación | `p ∧ q` | `∴ p` |
| Conjunción | `p`, `q` | `∴ p ∧ q` |
| Prueba de división por casos | `p ∨ q`, `p → r`, `q → r` | `∴ r` |
| Resolución | `¬p ∨ r`, `p ∨ q` | `∴ q ∨ r` |

[Ver en el sitio](https://discretas1-udea.github.io/discretas1-udea-20262/lessons/mod2/clase9/#parte-ii--repaso-equivalencias-y-reglas-de-inferencia-proposicionales) — Parte II: repaso de equivalencias y reglas de inferencia proposicionales.

### 2. De la demostración proposicional a la cuantificacional

**Demostración** (pág. 8): una cadena de razonamientos en la que cada paso sigue lógicamente del anterior, con el objetivo de justificar que una conclusión se sigue necesariamente de un conjunto de premisas.

- En **lógica proposicional**, las demostraciones se construyen a partir de los conectivos lógicos (`¬`, `∧`, `∨`, `→`, `↔`) siguiendo reglas como Modus Ponens, eliminación de la conjunción, entre otras.
- En **lógica de predicados**, además se usan cuantificadores (`∀`, `∃`) y se aplican reglas como la instanciación universal o la generalización existencial.

El profesor recordó las tres formas de escribir un mismo argumento, con el Modus Ponens como ejemplo:

| Notación estándar | Tautología | Forma simbólica |
|---|---|---|
| `p → q`, `p` `∴ q` (premisas encima de la línea, conclusión debajo) | `[(p → q) ∧ p] → q` | `(p → q), p ⊢ q` |

Los argumentos válidos con enunciados cuantificados son una secuencia de afirmaciones: cada afirmación es una premisa o se deduce de afirmaciones anteriores mediante reglas de inferencia. Esas reglas son de dos tipos: las de la **lógica proposicional** (sección 1) y las de los **enunciados cuantificados** (sección 3) (pág. 9).

[Ver en el sitio](https://discretas1-udea.github.io/discretas1-udea-20262/lessons/mod2/clase9/#parte-iv--de-la-demostración-proposicional-a-la-demostración-cuantificacional) — Parte IV: de la demostración proposicional a la demostración cuantificacional.

### 3. Reglas de inferencia con cuantificadores

**Tabla resumen** (pág. 9):

| Regla | Nombre | Forma |
|---|---|---|
| `∀I` | Instanciación universal (UI: *Universal Instantiation*) | `∀x P(x) ⇒ P(c)` |
| `∀G` | Generalización universal (UG: *Universal Generalization*) | `P(c) ⇒ ∀x P(x)` |
| `∃I` | Instanciación existencial (EI: *Existential Instantiation*) | `∃x P(x) ⇒ P(c)` |
| `∃G` | Generalización existencial (EG: *Existential Generalization*) | `P(c) ⇒ ∃x P(x)` |

Las dos **instanciaciones** quitan el cuantificador; las dos **generalizaciones** lo ponen. Cada regla tiene una condición que la tabla resumen no muestra, y que está en su diapositiva:

**Instanciación universal (UI)** (pág. 10). Permite pasar de una **afirmación general** (válida para todos los elementos del dominio) a una **afirmación particular** (válida para un caso específico).

- Forma general: `∀x P(x)` `∴ P(c)`. *Si algo es cierto para todos, también lo es para uno en particular.*
- Ejemplo: con `U = {todos los perros}`, la constante Firulais y `C(x)`: "x es cariñoso", de "Todos los perros son cariñosos" se sigue "Firulais es cariñoso": `∀x C(x)` `∴ C(Firulais)`.

**Generalización universal (UG)** (pág. 11). Permite afirmar que una propiedad se cumple para todos los elementos del dominio, si se logra demostrar que se cumple para un **individuo arbitrario**.

- Forma general: `P(c)` para un `c` **arbitrario** `∴ ∀x P(x)`.
- **Restricción fundamental** (diapositiva): «La variable x debe ser arbitraria, es decir, no debe depender de una premisa o suposición previa sobre un valor particular».
- Esta regla suele usarse a menudo de manera implícita en demostraciones matemáticas.

*Aclaración del apunte:* en la restricción, «la variable x» se refiere al individuo `c` de la forma general: lo que debe ser arbitrario es el individuo con el que se hizo la demostración.

**Instanciación existencial (EI)** (pág. 12). Permite tomar una afirmación del tipo `∃x P(x)` y asumir que existe un individuo `c` para el cual `P(c)` es verdadera.

- Forma general: `∃x P(x)` `∴ P(c)` para un `c` **nuevo**.
- Ejemplo: "Hay alguien que sacó un 5.0 en el curso". Con `U = {todos los estudiantes}` y `N(x)`: "x sacó un 5.0", si se introduce una constante nueva `a` para referirse a ese estudiante (cuya identidad real se desconoce), se puede decir que `a` sacó un 5.0: `∃x N(x)` `∴ N(a)`.

**Generalización existencial (EG)** (pág. 13). Permite pasar de una afirmación particular como `P(c)` a una existencial como `∃x P(x)`.

- Forma general: `P(c)` para algún elemento `c` `∴ ∃x P(x)`. *Si se conoce que alguien (o algo) cumple una propiedad, se puede afirmar que existe al menos uno que la cumple.*
- Ejemplo: con `U = {todos los estudiantes}` y `N(x)`: "x sacó un 5.0", si Bart sacó un 5.0 en la clase, se puede decir que al menos un estudiante sacó un 5.0: `N(Bart)` `∴ ∃x N(x)`.

**Procedimiento general.** El profesor resumió así la estrategia para demostrar con cuantificadores:

1. **Instanciar**: eliminar los cuantificadores con UI o EI, reemplazando la variable por una constante adecuada.
2. **Aplicar reglas proposicionales**: sin cuantificadores, usar Modus Ponens, simplificación, conjunción, eliminación, equivalencias, etc.
3. **Generalizar**, si la conclusión lo pide: volver a introducir el cuantificador con UG o EG.

> [!NOTE]
> Un estudiante preguntó en qué momento se reemplaza la variable por una constante. El profesor respondió que en el momento de eliminar el cuantificador: instanciar es justamente reemplazar la variable por una constante. Otro estudiante preguntó si, al generalizar, la constante desaparece y vuelve a ser variable. El profesor confirmó que sí: la constante se quita y la expresión vuelve a tener la variable con su cuantificador.

> [!IMPORTANT]
> **Aclaración del apunte: no toda constante se puede generalizar con `∀`.** La tabla resumen (págs. 9 y 16) escribe UG como `P(c) ⇒ ∀x P(x)`, sin condición, pero la diapositiva de la regla (pág. 11) exige que `c` sea **arbitrario**. Por eso, la respuesta anterior ("la constante vuelve a ser variable") vale siempre para EG, pero para UG solo si la constante es arbitraria:
>
> - De `mortal(Sócrates)` ([Ejemplo 1](#4-ejemplo-1-sócrates-es-mortal)) se puede concluir `∃x mortal(x)` (EG), pero **no** `∀x mortal(x)`: Sócrates es un individuo concreto, que viene de una premisa sobre él.
> - En el [Ejemplo 3](#6-ejemplo-3-alguien-que-aprobó-el-examen-no-ha-leído-el-libro), la constante `a` viene de una instanciación existencial: representa a un estudiante concreto, aunque no se sepa cuál. Por eso la demostración termina con **EG** (`∃x`) y no con UG.
>
> Es una de las cosas que conviene revisar al usar la tabla en el parcial.

[Ver en el sitio](https://discretas1-udea.github.io/discretas1-udea-20262/lessons/mod2/clase9/#parte-v--reglas-de-inferencia-con-cuantificadores) — Parte V: reglas de inferencia con cuantificadores.

### 4. Ejemplo 1: Sócrates es mortal

**Enunciado** (págs. 17–18): demuestre que las premisas "Todos los hombres son mortales" y "Sócrates es un hombre" implican la conclusión "Sócrates es mortal".

**Traducción.** Dominio: `U = {todos los seres vivos}`. Variable: `x`. Predicados: `hombre(x)`: "x es un hombre"; `mortal(x)`: "x es mortal".

| # | Enunciado | Representación |
|---|---|---|
| 1 | Premisa 1: Todos los hombres son mortales | `∀x (hombre(x) → mortal(x))` (a) |
| 2 | Premisa 2: Sócrates es un hombre | `hombre(Sócrates)` (b) |
| 3 | Conclusión: Sócrates es mortal | `mortal(Sócrates)` |

La premisa 1 es una forma A ([sección 1](#1-repaso-para-el-segundo-parcial)); la premisa 2 usa la constante Sócrates.

**Demostración** (pág. 18):

| # | Afirmación | Razón |
|---|---|---|
| 1 | `∀x (hombre(x) → mortal(x))` | Premisa a |
| 2 | `hombre(Sócrates) → mortal(Sócrates)` | Instanciación universal en 1 |
| 3 | `hombre(Sócrates)` | Premisa b |
| 4 | `mortal(Sócrates)` | Modus Ponens 2 y 3 |

En el paso 2, la UI se hace con x = Sócrates: se elige esa constante porque es la que aparece en la premisa b, y así el Modus Ponens del paso 4 puede usar las dos afirmaciones.

> [!NOTE]
> Un estudiante preguntó si se podía tomar directamente como universo "los hombres" para simplificar. El profesor respondió que sí es posible, pero que así se pierde la oportunidad de mostrar el uso completo de las premisas y puede generarse ambigüedad. En los ejercicios del curso, el universo suele venir dado en el enunciado.

### 5. Ejemplo 2: Josefina ha tomado un curso de informática

**Enunciado** (págs. 19–20): demuestre que las premisas "Todos en esta clase de matemáticas discretas han tomado un curso de informática" y "Josefina es una estudiante de esta clase" implican la conclusión "Josefina ha tomado un curso de informática".

**Traducción.** Dominio: `U = {todos los estudiantes}`. Variable: `x`. Predicados: `D(x)`: "x está en Matemáticas discretas"; `I(x)`: "x ha tomado un curso de informática".

| # | Enunciado | Representación |
|---|---|---|
| 1 | Premisa 1: Todos en esta clase de matemáticas discretas han tomado un curso de informática | `∀x (D(x) → I(x))` (a) |
| 2 | Premisa 2: Josefina es una estudiante de esta clase | `D(Josefina)` (b) |
| 3 | Conclusión: Josefina ha tomado un curso de informática | `I(Josefina)` |

**Demostración** (pág. 20):

| # | Afirmación | Razón |
|---|---|---|
| 1 | `∀x (D(x) → I(x))` | Premisa a |
| 2 | `D(Josefina) → I(Josefina)` | Instanciación universal en 1 |
| 3 | `D(Josefina)` | Premisa b |
| 4 | `I(Josefina)` | Modus Ponens 2 y 3 |

El profesor destacó que este ejemplo es "calcadito" al de Sócrates: otro enunciado, la misma estructura lógica.

### 6. Ejemplo 3: alguien que aprobó el examen no ha leído el libro

Este ejemplo agrega el cuantificador existencial, tanto en una premisa como en la conclusión.

**Enunciado** (págs. 21–22): demuestre que las premisas "Un estudiante de esta clase no ha leído el libro" y "Todos en esta clase aprobaron el primer examen" implican la conclusión "Alguien que aprobó el primer examen no ha leído el libro".

**Traducción.** Dominio: `U = {todos los estudiantes}`. Variable: `x`. Predicados: `C(x)`: "x está en esta clase"; `L(x)`: "x leyó el libro"; `A(x)`: "x aprobó el primer examen".

| # | Enunciado | Representación |
|---|---|---|
| 1 | Premisa 1: Un estudiante de esta clase no ha leído el libro | `∃x (C(x) ∧ ¬L(x))` (a) |
| 2 | Premisa 2: Todos en esta clase aprobaron el primer examen | `∀x (C(x) → A(x))` (b) |
| 3 | Conclusión: Alguien que aprobó el primer examen no ha leído el libro | `∃x (A(x) ∧ ¬L(x))` |

La premisa 1 y la conclusión son formas O; la premisa 2 es una forma A ([sección 1](#1-repaso-para-el-segundo-parcial)).

**Demostración** (pág. 22):

| # | Afirmación | Razón |
|---|---|---|
| 1 | `∃x (C(x) ∧ ¬L(x))` | Premisa a |
| 2 | `C(a) ∧ ¬L(a)` | Instanciación existencial en 1 |
| 3 | `C(a)` | Simplificación en 2 |
| 4 | `∀x (C(x) → A(x))` | Premisa b |
| 5 | `C(a) → A(a)` | Instanciación universal en 4 |
| 6 | `A(a)` | Modus Ponens 3 y 5 |
| 7 | `¬L(a)` | Simplificación en 2 |
| 8 | `A(a) ∧ ¬L(a)` | Conjunción en 6 y 7 |
| 9 | `∃x (A(x) ∧ ¬L(x))` | Generalización existencial en 8 |

Este ejemplo recorre el procedimiento completo de la [sección 3](#3-reglas-de-inferencia-con-cuantificadores): instanciar (pasos 2 y 5), aplicar reglas proposicionales (pasos 3, 6, 7 y 8) y generalizar (paso 9).

*Aclaración del apunte:* observe el orden de las instanciaciones. Primero se hace la EI (paso 2), que exige una constante **nueva**, `a`. Después se hace la UI (paso 5), que admite **cualquier** constante, y por eso puede usar la misma `a`. Si se hiciera al revés (primero UI con `a`, luego EI), la constante `a` ya no sería nueva y la EI no podría usarla.

### 7. Ejercicios de repaso

Estos son los enunciados de los ejercicios de repaso (págs. 23–24), **ya corregidos**:

1. Considere el conjunto de premisas dado por:
   - a. Todo número real es positivo o es negativo o es cero.
   - b. 4 no es un número negativo.
   - c. 4 no es cero.

   Y la siguiente conclusión: "4 es un número positivo".
2. El dominio de referencia es ℤ y se definen las siguientes premisas:
   - a. Para cada x, si x es un número par, entonces x + 4 es un número par.
   - b. Para cada x, si x es un número par, entonces x no es un número impar.
   - c. Dos es un número par.

   La conclusión que se sigue es: "2 + 4 no es un número impar".
3. "Alguien en esta clase disfruta observar ballenas, toda persona que disfruta observar ballenas se preocupa por la contaminación del océano". Por lo tanto, "hay una persona en esta clase que se preocupa por la contaminación del océano".
4. "Toda persona en Nueva Jersey vive a menos de 50 millas del océano. Alguien en Nueva Jersey nunca ha visto el océano". Por lo tanto, "alguien que vive a menos de 50 millas del océano nunca ha visto el océano".
5. Deduzca los teoremas con base en el sistema de lógica cuantificacional.
   - Premisas: `∀x ((x < 4) ∧ (4 < 5) → x < 5)`, `∀z ((−4 < −z) ↔ (z < 4))`, `4 < 5`, `−4 < −3`.
   - Conclusión: `3 < 5`.
6. Deduzca los teoremas con base en el sistema de lógica cuantificacional.
   - Premisas: `∀x (R(x) ∨ Z(x))`, `∀x (¬T(x) → ¬R(x))`, `∃x (¬Z(x) ∨ Q(x))`.
   - Conclusión: `∃x (T(x) ∨ Q(x) ∨ M(x))`.

> [!WARNING]
> **Los enunciados 2 y 5 se mostraron con errores en la sesión del 01/10.** Se copiaron mal del libro de donde se tomaron, y el profesor los corrigió después de la clase. Si repasa con el video, tenga en cuenta las diferencias:
>
> - **Ejercicio 2, premisa b.** En clase decía «…entonces x no es un número **par**». La versión correcta es «…entonces x no es un número **impar**». Por este error, la solución del Ejercicio 2 no salió ([sección 9](#9-ejercicio-2-intento-con-el-enunciado-erróneo)).
> - **Ejercicio 5, segunda premisa.** En clase decía `∀z ((−4 < z) ↔ (z < 4))`. La versión correcta es `∀z ((−4 < −z) ↔ (z < 4))`. El Ejercicio 5 no se alcanzó a trabajar en esta sesión.

### 8. Ejercicio 1: 4 es un número positivo

**Traducción** (manuscrito, pág. 25). Universo: `U = ℝ = (−∞, +∞)`. Variable: `x ∈ U`. Predicados: `x > 0`: "x es positivo"; `x < 0`: "x es negativo"; `x = 0`: "x es cero".

- (a) `∀x ((x > 0) ∨ (x < 0) ∨ (x = 0))`
- (b) `¬(4 < 0)`
- (c) `¬(4 = 0)`
- Conclusión: `∴ 4 > 0`

**Demostración** (transcripción del manuscrito, pág. 25):

| # | Afirmación | Razón |
|---|---|---|
| 1 | `∀x ((x > 0) ∨ (x < 0) ∨ (x = 0))` | Premisa (a) |
| 2 | `(4 > 0) ∨ (4 < 0) ∨ (4 = 0)` | UI en 1 (x = 4) |
| 3 | `¬(4 < 0)` | Premisa (b) |
| 4 | `(4 > 0) ∨ (4 = 0)` | Eliminación en 2 y 3 |
| 5 | `¬(4 = 0)` | Premisa (c) |
| 6 | `∴ (4 > 0)` | Eliminación en 4 y 5 |

La "eliminación" es el silogismo disyuntivo de la tabla de reglas ([sección 1](#1-repaso-para-el-segundo-parcial)): de una disyunción y la negación de uno de sus disyuntos, se concluye el resto de la disyunción.

*Aclaración del apunte:* en el paso 4, el disyunto que se elimina (`4 < 0`) está en el medio. La regla se escribe como `p ∨ q`, `¬p` `∴ q`, pero conmutatividad y asociatividad ([tabla de equivalencias](#1-repaso-para-el-segundo-parcial)) permiten reagrupar la disyunción para que el disyunto negado quede como `p`.

> [!NOTE]
> Un estudiante preguntó si en la premisa (a) no debería usarse el "o exclusivo", ya que un número no puede ser a la vez positivo y negativo. El profesor respondió que en el curso se trabaja solo con la disyunción inclusiva (`∨`): el "o exclusivo" no está en las tablas de equivalencias ni de reglas de inferencia que se manejan.

### 9. Ejercicio 2: intento con el enunciado erróneo

En clase, el Ejercicio 2 se mostró con este enunciado (versión anterior a la corrección):

> El dominio de referencia es ℤ y se definen las siguientes premisas:
>
> - a. Para cada x, si x es un número par, entonces x + 4 es un número par.
> - b. Para cada x, si x es un número par, entonces x no es un número **par**.
> - c. Dos es un número par.
>
> La conclusión que se sigue es: "2 + 4 no es un número impar".

*En el manuscrito anotado, la pág. 26 ya muestra de fondo el enunciado corregido, pero la solución escrita a mano corresponde a este enunciado erróneo.*

**Traducción** (manuscrito, pág. 26). Universo: `U = ℤ`. Variable: `x ∈ U`. Predicados: `par(x)`: "x es par"; `impar(x)`: "x es impar". Para traducir la conclusión, el profesor anotó `¬(impar(x)) = ¬(¬par(x)) = par(x)`: "no ser impar" es lo mismo que "ser par". Así quedó el argumento:

- (a) `∀x (par(x) → par(x+4))`
- (b) `∀x (par(x) → ¬par(x))`
- (c) `par(2)`
- Conclusión: `∴ par(2+4)`

**Intento de demostración** (transcripción del manuscrito, pág. 26):

| # | Afirmación | Razón |
|---|---|---|
| 1 | `∀x (par(x) → par(x+4))` | Premisa (a) |
| 2 | `par(2) → par(2+4)` | UI en 1 (x = 2) |
| 3 | `∀x (par(x) → ¬par(x))` | Premisa (b) |
| 4 | `par(2) → ¬par(2)` | UI en 3 (x = 2) |
| 5 | `¬par(2) ∨ par(2+4)` | Implicación en 2 (`P → Q ≡ ¬P ∨ Q`) |
| 6 | `¬par(2) ∨ ¬par(2)` | Implicación en 4 |
| 7 | `¬par(2)` | Idempotencia (∨) en 6 |
| 8 | `¬par(2) ∧ (¬par(2) ∨ par(2+4))` | Conjunción en 5 y 7 |

Al llegar aquí, el profesor anotó «Revisar…»: las expresiones no se cancelaban como esperaba, sospechó que el enunciado estaba mal copiado del libro y dejó el ejercicio para revisar en la siguiente sesión.

> [!WARNING]
> **Error del profesor en clase: enunciado mal copiado.** La premisa (b) que se mostró, «si x es par, entonces x **no es par**», se contradice con la premisa (c). Con x = 2, la premisa (b) dice que si 2 es par, entonces 2 no es par; por eso el paso 7 llega a `¬par(2)`, justo lo contrario de la premisa (c), `par(2)`. Un conjunto de premisas que se contradicen entre sí no describe ninguna situación posible, así que el ejercicio no tiene sentido tal como se planteó. La traducción `∀x (par(x) → ¬par(x))` sí era fiel al enunciado mostrado: el error estaba en el enunciado. La premisa correcta es «si x es par, entonces x **no es impar**» ([sección 7](#7-ejercicios-de-repaso)). La solución con el enunciado corregido se trabaja en la siguiente sesión.

> [!TIP]
> **Moraleja.** Antes de empezar a demostrar, lea las premisas en lenguaje natural y pregúntese si pueden ser verdaderas al mismo tiempo. Si una premisa contradice a otra, el problema está en el enunciado, no en la demostración.

### Síntesis de la clase

*Aclaración del apunte:* un resumen de lo esencial, sin contenido nuevo.

**Ideas clave:**

1. **Las tablas se entregan en el parcial; lo que se evalúa es saber aplicarlas.** Las equivalencias y reglas proposicionales siguen valiendo con cuantificadores ([sección 1](#1-repaso-para-el-segundo-parcial)).
2. **Demostrar con cuantificadores tiene tres pasos**: instanciar (UI, EI), aplicar reglas proposicionales y, si la conclusión lo pide, generalizar (UG, EG) ([sección 3](#3-reglas-de-inferencia-con-cuantificadores)).
3. **Cada regla tiene su condición**: UI admite cualquier constante; EI exige una constante nueva; UG exige un individuo arbitrario; EG admite cualquier constante ([sección 3](#3-reglas-de-inferencia-con-cuantificadores)).
4. **Primero se traduce**: universo, variables, predicados y la representación de cada premisa y de la conclusión. Después se demuestra ([secciones 4](#4-ejemplo-1-sócrates-es-mortal) a [6](#6-ejemplo-3-alguien-que-aprobó-el-examen-no-ha-leído-el-libro)).
5. **Las premisas deben tener sentido juntas**: si se contradicen, el error está en el enunciado ([sección 9](#9-ejercicio-2-intento-con-el-enunciado-erróneo)).

> [!IMPORTANT]
> **Errores y dudas de esta clase.** Lo que efectivamente ocurrió o se preguntó en la sesión:
>
> - **Enunciados 2 y 5 de los ejercicios de repaso mal copiados del libro** (error del profesor en clase). El Ejercicio 2 no salió por ese motivo. Ver la [advertencia de la sección 7](#7-ejercicios-de-repaso) y la [sección 9](#9-ejercicio-2-intento-con-el-enunciado-erróneo).
> - **¿Se puede restringir el universo a "los hombres"?** (pregunta de un estudiante). Sí, pero se pierde el uso completo de las premisas ([sección 4](#4-ejemplo-1-sócrates-es-mortal)).
> - **¿Cuándo se reemplaza la variable por una constante?** (pregunta de un estudiante). Al eliminar el cuantificador ([sección 3](#3-reglas-de-inferencia-con-cuantificadores)).
> - **¿Al generalizar, la constante vuelve a ser variable?** (pregunta de un estudiante). Sí; con UG, solo si la constante es arbitraria ([sección 3](#3-reglas-de-inferencia-con-cuantificadores)).
> - **¿Por qué no se usa el "o exclusivo"?** (pregunta de un estudiante). Porque no está en las tablas del curso ([sección 8](#8-ejercicio-1-4-es-un-número-positivo)).

## Evaluación

| Ítem | Detalle |
|---|---|
| Segundo parcial | Sábado **10/10/2026**, de 11:00 a 13:00. El horario no cambia: se verificó con la coordinación que no hay cruce con otros cursos. Cubre hasta lo visto en esta clase: lógica cuantificacional, con sus reglas de inferencia y demostraciones. |
| Tablas de consulta en el parcial | Se entregarán las tablas de formas aristotélicas, equivalencias de lógica proposicional, equivalencias de lógica cuantificacional, reglas de inferencia proposicionales y reglas de inferencia con cuantificadores ([secciones 1](#1-repaso-para-el-segundo-parcial) y [3](#3-reglas-de-inferencia-con-cuantificadores)). Lo fundamental es saber aplicarlas. |
| Notas del primer parcial | La mayoría ya estaban calificadas; el profesor enviaría el reporte de notas ese mismo día, para que los estudiantes puedan tomar decisiones sobre su situación académica. |
| Primer 25 % | El profesor lo reportará después de revisar los quices. |
| Quizzes 5–8 | Publicados en Ude@: Quiz 5 (traducción y formas aristotélicas), Quiz 6 (verdad y falsedad de enunciados cuantificados), Quiz 7 (negación y equivalencias cuantificacionales) y Quiz 8 (cuantificadores anidados). Cierran el sábado **17/10/2026 a las 23:59**. Intentos ilimitados; se toma la nota más alta. La idea es resolverlos **antes del parcial**, como repaso. |

## Pendientes

### Docente

- [ ] Enviar el reporte de notas del primer parcial.
- [ ] Reportar el primer 25 % de la nota, después de revisar los quices.
- [ ] Revisar en el libro fuente los enunciados de los Ejercicios 2 y 5, y presentar la solución del Ejercicio 2 corregido en la siguiente sesión.

### Estudiantes

- [ ] Resolver los Quizzes 5–8 en Ude@ antes del parcial del 10/10/2026, como repaso (cierran el 17/10/2026).
- [ ] Practicar con los parciales anteriores (con enunciados y soluciones) y los talleres de la página del curso, incluido el Taller 4.
- [ ] Repasar las tablas de equivalencias y de reglas de inferencia, proposicionales y con cuantificadores: se entregan en el parcial, y lo que se evalúa es saber aplicarlas.
- [ ] Estar pendientes de los anuncios en el foro del curso.

## Próxima clase

Sesión 2 de esta clase (06/10/2026): corrección del Ejercicio 2 y resolución de los demás ejercicios de repaso, incluido el Ejercicio 5 con el enunciado corregido.
