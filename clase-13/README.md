![Built with AI](https://img.shields.io/badge/Built%20with-AI-blue.svg)

# Clase 13 — Operaciones entre conjuntos e identidades

> **Fecha**: 20/10/2026, 22/10/2026 · **Modalidad**: Virtual sincrónica · **Apuntes**: [Diapositivas PDF](./apuntes_clase13.pdf) · [PPT](./apuntes_clase13.pptx) · [Manuscrito anotado](./apuntes_clase13_annotated.pdf)
>
> La sesión del 20/10 cubre las págs. 1–31 del manuscrito; la del 22/10, las págs. 32–40 (marca «Fin: 20/10/2026 · Inicio: 22/10/2026» en la pág. 32).

## Objetivos de la clase

- Presentar las operaciones entre conjuntos (unión, intersección, diferencia, complemento y diferencia simétrica), con su definición formal y su representación en diagramas de Venn.
- Establecer la notación del curso para el álgebra de conjuntos (`+`, `·`, `'`, `1`, `0`) y su analogía con las leyes de la lógica proposicional, y aplicar las identidades a demostrar y simplificar expresiones.
- Introducir las identidades básicas de cardinalidad y aplicarlas a problemas con diagramas de Venn, incluido un problema de tipos de sangre.
- Informar cómo se organizará el supletorio del segundo parcial y anunciar el inicio del tema de relaciones.

## Resumen

En la sesión del 20/10 se vieron las cinco operaciones entre conjuntos con un mismo ejemplo (las letras de "cálculo" y de "matemáticas discretas"), la tabla de identidades del álgebra de conjuntos, una demostración y una simplificación con ellas, las identidades de cardinalidad y los ejemplos 1 a 6. En la sesión del 22/10 se resolvieron los ejemplos 7 a 10, con el problema de tipos de sangre. Con eso se cerró el tema de conjuntos; la próxima clase empieza el tema de relaciones.

## Agenda

**Sesión 1 — 20/10/2026**

1. Operaciones entre conjuntos y ejemplo de las letras: representación, conjunto universal y diagrama de Venn. [*(→ sección 1)*](#1-operaciones-entre-conjuntos)
2. Unión e intersección. [*(→ sección 2)*](#2-unión-e-intersección)
3. Diferencia. [*(→ sección 3)*](#3-diferencia)
4. Complemento. [*(→ sección 4)*](#4-complemento)
5. Diferencia simétrica. [*(→ sección 5)*](#5-diferencia-simétrica)
6. Resumen de las operaciones. [*(→ sección 6)*](#6-resumen-de-las-operaciones)
7. Identidades básicas para conjuntos y analogía con la lógica proposicional. [*(→ sección 7)*](#7-identidades-básicas-para-conjuntos)
8. Una demostración y una simplificación con identidades. [*(→ sección 8)*](#8-demostrar-y-simplificar-con-identidades)
9. Identidades básicas de cardinalidad. [*(→ sección 9)*](#9-identidades-básicas-de-cardinalidad)
10. Ejemplos 1 a 3: representación, cardinalidad y número de subconjuntos. [*(→ sección 10)*](#10-ejemplos-1-a-3-representación-cardinalidad-y-subconjuntos)
11. Ejemplos 4 a 6: diagramas de Venn y complemento. [*(→ sección 11)*](#11-ejemplos-4-a-6-diagramas-de-venn)

**Sesión 2 — 22/10/2026**

1. Repaso de las operaciones y de su álgebra.
2. Ejemplo 7: operaciones sobre un diagrama de Venn. [*(→ sección 12)*](#12-ejemplo-7-operaciones-sobre-un-diagrama-de-venn)
3. Ejemplo 8: cardinalidad a partir de un diagrama. [*(→ sección 13)*](#13-ejemplo-8-cardinalidad-desde-un-diagrama)
4. Ejemplo 9: tipos de sangre. [*(→ sección 14)*](#14-ejemplo-9-tipos-de-sangre)
5. Ejemplo 10: conjuntos de colores, con una tarea. [*(→ sección 15)*](#15-ejemplo-10-conjuntos-de-colores)
6. Avisos: supletorio del segundo parcial y actividades de repaso en el foro. [*(→ Evaluación)*](#evaluación)

## Contenido temático

> [!NOTE]
> **Cómo leer este apunte.**
>
> - Las secciones numeradas siguen el orden en que se dictó la clase.
> - **Sesión 1 (20/10), secciones 1 a 11**: manuscrito, págs. 1–31.
> - **Sesión 2 (22/10), secciones 12 a 15**: manuscrito, págs. 32–40.
> - Los "Ejemplos 1 a 11" son la batería de ejercicios de las págs. 19–25. Los ejemplos de las secciones 7 y 8 se llaman aquí *ejemplo de demostración* y *ejemplo de simplificación*, para no confundirlos con esa numeración.
> - Los párrafos que empiezan con *Aclaración del apunte* se agregaron al redactar: no se dijeron en clase. Sirven para conectar ideas o evitar confusiones.

**Notación usada en este apunte**

| Símbolo | Se lee | Observación |
|---|---|---|
| `A ∪ B` = `A + B` | unión | Las dos notaciones son equivalentes en el curso (sección 2). |
| `A ∩ B` = `A · B` = `AB` | intersección | Escribir dos conjuntos seguidos, sin símbolo, también es intersección: `ABC` es `A · B · C` (secciones 8 y 15). |
| `A − B` (o `A \ B`) | diferencia | Los elementos de `A` que no están en `B` (sección 3). |
| `A'` (o `Aᶜ`, `Ā`) | complemento de `A` | En el curso se usa sobre todo `A'` (sección 4). `A''` es el complemento del complemento. |
| `A ⊕ B` (o `A △ B`) | diferencia simétrica | Los elementos que están en uno solo de los dos conjuntos (sección 5). |
| `U` = `1` | conjunto universal | En el álgebra de conjuntos, `U` se escribe `1` (sección 7). |
| `∅` = `0` | conjunto vacío | En el álgebra de conjuntos, `∅` se escribe `0` (sección 7). |
| `\|A\|`, `n(A)`, `card(A)` | cardinalidad de `A` | Número de elementos de `A` ([clase 12](../clase-12/README.md#13-cardinalidad)). |
| `𝒫(A)` | conjunto potencia de `A` | `\|𝒫(A)\| = 2^\|A\|` ([clase 12](../clase-12/README.md#14-conjunto-potencia)). |
| `⊆` | "es subconjunto de" | [Clase 12](../clase-12/README.md#8-subconjuntos). |
| `Tipo(A)` | personas con sangre tipo A | Notación del manuscrito en el ejemplo 9 (sección 14); no es lo mismo que el conjunto `A` del diagrama. |

### 1. Operaciones entre conjuntos

Las operaciones entre conjuntos permiten **combinar o modificar conjuntos para crear nuevos conjuntos** (pág. 2). Las principales son: unión, intersección, diferencia, complemento y diferencia simétrica.

El profesor presentó cada operación junto con un mismo ejemplo (pág. 3): sea `A` el conjunto de todas las letras que conforman la palabra "cálculo" y `B` el conjunto de las letras que aparecen en "matemáticas discretas". Se pide determinar:

1. La representación por comprensión y por extensión de cada conjunto.
2. El conjunto universal.
3. El diagrama de Venn que represente el problema.
4. Las letras que aparecen en cualquiera de los dos conjuntos.
5. Las letras que aparecen en ambos conjuntos.
6. Las que solo aparecen en el conjunto `A` pero no están en el conjunto `B`.
7. Las que solo aparecen en el conjunto `B` pero no están en el conjunto `A`.
8. Las letras que no se encuentran en `A`.
9. Las letras que no se encuentran en `B`.
10. Las letras que están solo en `A` o solo en `B`.

Los puntos 1 a 3 se resolvieron primero (pág. 4); los demás, a medida que se presentaba cada operación.

**1. Representación de cada conjunto.**

| Conjunto | Por extensión | Por comprensión |
|---|---|---|
| `A` | `A = {c, a, l, u, o}` | `A = {x ∈ U \| x es una letra de 'cálculo'}` |
| `B` | `B = {m, a, t, e, i, c, s, d, r}` | `B = {x ∈ U \| x es una letra de 'matemáticas discretas'}` |

En el manuscrito, los rótulos "Comprensión" y "Extensión" de `A` y `B` quedaron intercambiados (la lista aparece bajo "Comprensión"); aquí se presentan en su lugar.

> [!NOTE]
> Un estudiante preguntó si la lista de elementos era una representación por comprensión o por extensión. El profesor respondió que **una lista de elementos es una representación por extensión**; la representación por comprensión usa una propiedad o condición que deben cumplir los elementos ([clase 12, sección 4](../clase-12/README.md#4-representación-por-extensión-y-por-comprensión)).

> [!NOTE]
> Un estudiante observó que la letra "c" se repite en "matemáticas discretas" (y la "a", la "t", la "e" y la "s" también). El profesor confirmó que **en un conjunto no se repiten elementos**: cada letra se escribe una sola vez.

**2. Conjunto universal.** Las letras minúsculas del abecedario español:

- Por comprensión: `U = {x | x es una letra minúscula del abecedario español}`.
- Por extensión: `U = {a, b, c, …, m, n, ñ, o, p, …, x, y, z}`.

**3. Diagrama de Venn.** Dentro del rectángulo de `U`, dos óvalos que se cortan: en la parte común quedan la `a` y la `c`; solo en `A`, la `l`, la `u` y la `o`; solo en `B`, la `m`, la `t`, la `e`, la `i`, la `s`, la `d` y la `r`; el resto del abecedario queda fuera de los dos óvalos.

### 2. Unión e intersección

**Unión** (pág. 5). La unión de `A` y `B` es el conjunto de todos los elementos que pertenecen a `A`, a `B`, o a ambos.

`A ∪ B = {x | x ∈ A ∨ x ∈ B}`

En el diagrama de Venn, la unión es toda el área cubierta por los dos círculos.

**Intersección** (pág. 6). La intersección de `A` y `B` es el conjunto de elementos que pertenecen a ambos conjuntos simultáneamente.

`A ∩ B = {x | x ∈ A ∧ x ∈ B}`

En el diagrama de Venn, la intersección es solo la región donde los dos círculos se superponen.

**Puntos 4 y 5 del ejemplo** (pág. 7). En clase se subrayó "cualquiera" (en `A`, en `B` o en ambos) y "en ambos conjuntos":

- 4. `A ∪ B = A + B = {l, u, o, m, t, e, i, s, d, r, c, a}`
- 5. `A ∩ B = A · B = {c, a}`

Aquí aparece por primera vez la notación del curso: la unión también se escribe `+` y la intersección `·` (se retoma en la [sección 7](#7-identidades-básicas-para-conjuntos)).

### 3. Diferencia

**Diferencia** (pág. 8). La diferencia (o complemento relativo) de `A` y `B` es el conjunto de elementos que están en `A` pero no en `B`.

`A − B = {x | x ∈ A ∧ x ∉ B}`

En el diagrama de Venn, `A − B` es la parte de `A` que queda fuera de `B`.

**Puntos 6 y 7 del ejemplo** (pág. 9). En clase, la diferencia se calculó quitando la intersección:

- 6. `A − B = A − A · B = {c, a, l, u, o} − {a, c} = {l, u, o}`
- 7. `B − A = B − B · A = {m, a, t, e, i, c, d, s, r} − {a, c} = {m, t, e, i, d, s, r}`

Observe que `A − B ≠ B − A`: el orden importa en la diferencia.

### 4. Complemento

**Complemento** (pág. 10). El complemento de `A` (`A'`) es el conjunto de elementos del universo `U` que no pertenecen a `A`.

`A' = U − A = {x ∈ U | x ∉ A}`

En el diagrama de Venn, `A'` es todo el rectángulo menos el círculo de `A`.

El complemento tiene tres notaciones equivalentes: `A'`, `Aᶜ` y `Ā`. El profesor indicó que en el curso se usará sobre todo la comilla, `A'`.

> [!NOTE]
> Un estudiante preguntó qué significaba la "comillita" junto a la letra del conjunto. El profesor respondió que la comilla (`A'`), la `c` como superíndice (`Aᶜ`) y la barra encima (`Ā`) son formas distintas de escribir lo mismo: los elementos del universo que no pertenecen al conjunto.

**Puntos 8 y 9 del ejemplo** (pág. 11):

- 8. `A' = U − A = {a, b, …, z} − {c, a, l, u, o}`. En el manuscrito, el resultado se abrevia con puntos suspensivos; escrito completo es `A' = {b, d, e, f, g, h, i, j, k, m, n, ñ, p, q, r, s, t, v, w, x, y, z}`.
- 9. `B' = U − B = {a, b, …, z} − {m, a, t, e, i, c, d, s, r}`. En clase se planteó la resta, pero el resultado quedó sin escribir.

*Aclaración del apunte:* el resultado del punto 9 es `B' = {b, f, g, h, j, k, l, n, ñ, o, p, q, u, v, w, x, y, z}`. Como `U` tiene 27 letras, se puede comprobar contando: `|A'| = 27 − 5 = 22` y `|B'| = 27 − 9 = 18` (es la identidad `|A'| = |U| − |A|` de la [sección 9](#9-identidades-básicas-de-cardinalidad)).

### 5. Diferencia simétrica

**Diferencia simétrica** (pág. 12). La diferencia simétrica de `A` y `B` es el conjunto de elementos que están en `A` o en `B`, pero no en ambos. Tiene tres definiciones formales equivalentes:

- `A ⊕ B = (A ∪ B) − (A ∩ B)`
- `A ⊕ B = (A − B) ∪ (B − A)`
- `A ⊕ B = {x | (x ∈ A ∧ x ∉ B) ∨ (x ∈ B ∧ x ∉ A)}`

En el diagrama de Venn, `A ⊕ B` son las dos partes laterales: toda la unión menos la región común.

**Punto 10 del ejemplo** (pág. 13). En clase se recordaron `A ∪ B` y `A ∩ B`, y se anotaron los dos caminos, `(A ∪ B) − (A ∩ B)` y `(A − B) ∪ (B − A) = {l, u, o} ∪ {m, t, e, i, s, r, d}`:

- 10. `A ⊕ B = {l, u, o, m, t, e, i, s, d, r}`

Por los dos caminos se llega al mismo conjunto: se quitan de la unión la `a` y la `c`, que son la intersección.

### 6. Resumen de las operaciones

La pág. 14 resume las cinco operaciones (en clase se resaltaron las notaciones `A ∪ B = A + B`, `A ∩ B = A · B`, `A − B`, `A ⊕ B` y `A' = Aᶜ = U − A`):

| Operación | Notación y definición formal | Definición | Ejemplo |
|---|---|---|---|
| Unión | `A ∪ B = A + B = {x \| x ∈ A ∨ x ∈ B}` | Conjunto de elementos que están en `A` o en `B` (o en ambos) | `A = {1, 2}`, `B = {2, 3}`: `A ∪ B = {1, 2, 3}` |
| Intersección | `A ∩ B = A · B = {x \| x ∈ A ∧ x ∈ B}` | Conjunto de elementos que están tanto en `A` como en `B` | `A = {1, 2}`, `B = {2, 3}`: `A ∩ B = {2}` |
| Diferencia | `A − B = {x \| x ∈ A ∧ x ∉ B}` | Conjunto de elementos que están en `A` pero no en `B` | `A = {1, 2, 3}`, `B = {2}`: `A − B = {1, 3}` y `B − A = { } = ∅` |
| Diferencia simétrica | `A ⊕ B = {x \| (x ∈ A ∧ x ∉ B) ∨ (x ∈ B ∧ x ∉ A)}` | Conjunto de elementos que están en `A` o en `B`, pero no en ambos | `A = {1, 2}`, `B = {2, 3}`: `A ⊕ B = {1, 3}` |
| Complemento | `A' = Aᶜ = U − A` | Conjunto de elementos que están en el universo pero no en `A` | `U = {1, 2, 3}`, `A = {1, 2}`: `A' = Aᶜ = {3}` |

*Aclaración del apunte:* compare las definiciones formales con los conectivos de la lógica proposicional: la unión usa `∨`, la intersección usa `∧`, y la diferencia y el complemento usan `∉` (la negación de `∈`). Esa correspondencia es la base de la sección siguiente.

### 7. Identidades básicas para conjuntos

**La analogía con la lógica proposicional** (pág. 15). La "Observación importante" de la diapositiva fija la notación del álgebra de conjuntos:

- La unión (`∪`) se representa por el operador `+` y la intersección (`∩`) por el operador `·`.
- El conjunto universal (`U`) se representa por `1` y el conjunto vacío (`∅`) por `0`.

En clase se anotó la correspondencia con la lógica proposicional:

| Lógica proposicional | Conjuntos | Álgebra de conjuntos |
|---|---|---|
| "y" (`∧`) | `∩` | `·` |
| "o" (`∨`) | `∪` | `+` |
| verdadero (`V`) | `U` | `1` |
| falso (`F`) | `∅` | `0` |

Gracias a esta correspondencia, las identidades de los conjuntos son las mismas leyes de equivalencia de la lógica proposicional, escritas con `·`, `+`, `'`, `1` y `0`:

| Nombre | Con `·` (intersección) | Con `+` (unión) |
|---|---|---|
| Idempotencia | `A · A = A` | `A + A = A` |
| Identidad | `A · 1 = A` | `A + 0 = A` |
| Dominación | `A · 0 = 0` | `A + 1 = 1` |
| Conmutativa | `A · B = B · A` | `A + B = B + A` |
| Asociativa | `A · (B · C) = (A · B) · C` | `A + (B + C) = (A + B) + C` |
| Distributiva | `A · (B + C) = A · B + A · C` | `A + (B · C) = (A + B) · (A + C)` |
| Complemento | `A · A' = 0` | `A + A' = 1` |
| Doble negación | `A'' = A` | |
| Absorción | `A · (A + B) = A` | `A + A · B = A` |
| De Morgan | `(A · B)' = A' + B'` | `(A + B)' = A' · B'` |

En clase se marcó con una flecha la distributiva de la intersección leída **de derecha a izquierda**: `A · B + A · C = A · (B + C)` es "sacar factor común", como en el álgebra. También se resaltó la ley del complemento `A + A' = 1`: un conjunto unido con su complemento da el universo.

En términos de conjuntos, por ejemplo: `A ∩ U = A` (identidad), `A ∪ A' = U` (complemento) y `(A ∩ B)' = A' ∪ B'` (De Morgan: al complementar, la unión cambia a intersección y viceversa, y cada conjunto se complementa).

### 8. Demostrar y simplificar con identidades

**Ejemplo de demostración** (pág. 16). Aplicando las leyes fundamentales del álgebra de conjuntos, demuestre que:

`(A + (B · C))' = (C' + B') · A'`

Se parte del lado izquierdo (`I`) y se llega al derecho (`D`). En clase se anotó la traducción de los operadores: `+` corresponde a `∨` y `·` a `∧`.

| # | Afirmación | Razón |
|---|---|---|
| 1 | `(A + (B · C))'` | Lado izquierdo de la expresión |
| 2 | `A' · (B · C)'` | Ley de De Morgan en (1) |
| 3 | `A' · (B' + C')` | Ley de De Morgan en (2) |
| 4 | `(B' + C') · A'` | Ley conmutativa en (3) |
| 5 | `(C' + B') · A'` | Ley conmutativa en (4) |

Debajo de la tabla, el profesor escribió la misma demostración como una cadena de igualdades:

`(A + (B · C))' = A' · (B · C)' = A' · (B' + C') = (B' + C') · A' = (C' + B') · A'`

*Aclaración del apunte:* el paso 2 aplica De Morgan a la unión de `A` con `B · C` (`(X + Y)' = X' · Y'`, con `X = A` y `Y = B · C`), y el paso 3 la aplica a `(B · C)'`. El paso 4 conmuta los dos factores de la intersección y el paso 5 los dos términos de la unión.

**Ejemplo de simplificación** (pág. 17). Aplicando las leyes fundamentales del álgebra de conjuntos, simplifique:

`ABC + ABC' + AB'C + AB'C' + A'BC + A'BC' + A'B'C + A'B'C'`

| # | Afirmación | Razón |
|---|---|---|
| 1 | `ABC + ABC' + AB'C + AB'C' + A'BC + A'BC' + A'B'C + A'B'C'` | Expresión inicial |
| 2 | `(ABC + ABC') + (AB'C + AB'C') + (A'BC + A'BC') + (A'B'C + A'B'C')` | Asociatividad en (1) |
| 3 | `AB · (C + C') + AB' · (C + C') + A'B · (C + C') + A'B' · (C + C')` | Distributividad en (2) |
| 4 | `AB · 1 + AB' · 1 + A'B · 1 + A'B' · 1` | Complemento en (3) |
| 5 | `AB + AB' + A'B + A'B'` | Identidad en (4) |
| 6 | `(AB + AB') + (A'B + A'B')` | Asociatividad en (5) |
| 7 | `A · (B + B') + A' · (B + B')` | Distributividad en (6) |
| 8 | `A · 1 + A' · 1` | Complemento en (7) |
| 9 | `A + A'` | Identidad en (8) |
| 10 | `1` | Complemento en (9) |

En clase, la razón del paso 1 ("Lado izquierdo" en la diapositiva) se cambió a "Expresión inicial", porque aquí no hay una igualdad que demostrar sino una expresión que simplificar. Junto a la distributividad del paso 3 se anotó "factor común": se usa de derecha a izquierda, como en la [sección 7](#7-identidades-básicas-para-conjuntos).

La expresión completa se simplifica a `1`, es decir, al conjunto universal `U`.

*Aclaración del apunte:* en esta expresión, `ABC` es `A · B · C` (intersección) y `+` es unión, y se opera primero la intersección y luego la unión, como en el álgebra el producto antes que la suma. El resultado tiene sentido: los ocho términos recorren todas las combinaciones de estar o no estar en `A`, en `B` y en `C`, así que entre todos cubren el universo completo.

### 9. Identidades básicas de cardinalidad

Recordemos que la cardinalidad es la cantidad de elementos que un conjunto tiene: `|A| = card(A) = n(A)` (pág. 18). Las identidades que se trabajaron en clase (marcadas y resaltadas en el manuscrito) son:

| # | Identidad | Se lee |
|---|---|---|
| 1 | `\|∅\| = 0` | El vacío no tiene elementos. |
| 2 | `A · B = ∅ → \|A + B\| = \|A\| + \|B\|` | Si `A` y `B` son disyuntos, la cardinalidad de la unión es la suma de las cardinalidades. |
| 3 | `\|A + B\| = \|A\| + \|B\| − \|A · B\|` | En general, se suman y se resta la intersección, que quedó contada dos veces. |
| 4 | `\|A − B\| = \|A\| − \|A · B\|` | A los elementos de `A` se les quitan los que también están en `B`. |
| 7 | `\|A'\| = \|U\| − \|A\|` | El complemento tiene los elementos del universo que no están en `A`. |

<details>
<summary>Identidades 5, 6, 8, 9 y 10 de la tabla (desigualdades; no se trabajaron en clase)</summary>

| # | Identidad |
|---|---|
| 5 | `\|A · B\| ≤ \|A\|` |
| 6 | `\|A\| ≤ \|A + B\|` |
| 8 | `a ≤ \|A\| ≤ b ↔ \|U\| − b ≤ \|A'\| ≤ \|U\| − a` |
| 9 | `Max(\|A\|, \|B\|) ≤ \|A + B\| ≤ Min(\|A\| + \|B\|, \|U\|)` |
| 10 | `Max(0, \|A\| + \|B\| − \|U\|) ≤ \|A · B\| ≤ Min(\|A\|, \|B\|)` |

</details>

El profesor indicó que en el curso se trabajarán principalmente las cinco identidades de la primera tabla. Las desigualdades se explican en los videos de la profesora del curso (ver el ejemplo 11 en la [sección 10](#10-ejemplos-1-a-3-representación-cardinalidad-y-subconjuntos)).

### 10. Ejemplos 1 a 3: representación, cardinalidad y subconjuntos

Las págs. 19–25 presentan la batería de ejemplos 1 a 11, que se resolvió en el resto de la clase. El **ejemplo 11** no se resolvió en clase (pág. 25): *"Al menos el 45 % de los estudiantes NO aprueban Matemáticas Discretas y el 15 % de los estudiantes NO aprueban Lógica 1. ¿Cuál es el porcentaje máximo de estudiantes que aprueban ambas asignaturas?"*. En el manuscrito se anotó "Ver video de la profe": el video [*Ejercicio 5: teoría de conjuntos*](https://www.youtube.com/watch?v=l8BmbuFp7iE) lo resuelve.

**Ejemplo 1** (pág. 26). Represente cada uno de los siguientes conjuntos por el método que usted elija.

- **Conjunto de todos los cuadrados que también son círculos.** En clase se subrayó "que también" y se anotó que corresponde a la intersección (`∩`). Con `Cu = {■, □, …}` (cuadrados) y `Cir = {●, ○, …}` (círculos), ninguna figura es cuadrado y círculo a la vez, así que:

  `Cu ∩ Cir = ∅`

- **Conjunto de todos los equipos de fútbol de la liga profesional colombiana.** Con el universo `U = {x | x es un equipo de fútbol de Colombia}`:
  - Por comprensión: `P = {x | x es un equipo profesional}`.
  - Por extensión: `P = {Nal, Dim, Millos, …}` (Nacional, Medellín, Millonarios, …).
  - `P ⊆ U`: en el diagrama, el óvalo de `P` queda dentro del rectángulo de `U`, y fuera del óvalo quedan otros equipos de fútbol de Colombia que no son profesionales.

**Ejemplo 2** (pág. 27). Dados los siguientes conjuntos, determine la cardinalidad.

| Conjunto | Cardinalidad |
|---|---|
| `P = {Snuzzle, Butterscotch, Blue Belle, Minty, Blossom, Cotton Candy}` | `n(P) = \|P\| = 6` |
| `F = {1/9, 2/9, 3/9, 4/9, 5/9, 6/9, 7/9, 8/9, 9/9}` | `n(F) = \|F\| = 9` |
| `C = {n³ \| n es un miembro de ℕ} = {0³, 1³, 2³, 3³, 4³, …} = {0, 1, 8, 27, 64, …}` | `n(C) = \|C\| = ∞` |

En la diapositiva, el quinto elemento de `C` aparece como 256; aquí se escribe 64, porque `4³ = 64`.

**Ejemplo 3** (pág. 28). Para los siguientes conjuntos, obtenga el número total de subconjuntos que se pueden formar. Es el número de elementos del conjunto potencia, `|𝒫(A)| = 2^|A|` ([clase 12, sección 14](../clase-12/README.md#14-conjunto-potencia)):

- `C = {Adele, Beyonce, Cher, Madonna, Shakira}`: `n(C) = |C| = 5`, luego `n(𝒫(C)) = |𝒫(C)| = 2^|C| = 2⁵ = 32`.
- `A = {3}`: `|A| = 1`. Listando, `𝒫(A) = {∅, {3}}`, así que `|𝒫(A)| = 2`; con la fórmula, `n(𝒫(A)) = |𝒫(A)| = 2^|A| = 2¹ = 2`.

> [!NOTE]
> Un estudiante preguntó si, cuando un ejercicio da el universo además del conjunto, el universo también entra al calcular el conjunto potencia. El profesor respondió que **la fórmula se aplica al conjunto que indique el enunciado**, no al universo (a menos que el enunciado pida el del universo). Si se pide, por ejemplo, el conjunto potencia de `A ∪ B`, primero se calcula la unión, luego su cardinalidad y al final se aplica `2^n`. Lo ilustró al lado del ejemplo 3: con `A = {1, 2}` y `B = {2, 3, 4}`, `A ∪ B = {1, 2, 3, 4}`, `|A ∪ B| = 4` y `|𝒫(A ∪ B)| = 2^|A ∪ B| = 2⁴ = 16`.

### 11. Ejemplos 4 a 6: diagramas de Venn

**Ejemplo 4** (pág. 29). Dibuje un diagrama de Venn que represente las siguientes relaciones:

- **Todas las bicicletas y todos los carros tienen ruedas, pero ninguna bicicleta es un carro.** El universo son las cosas que tienen ruedas:
  - `U = R = {x | x tiene ruedas}`
  - `B = {x | x es una bicicleta}`, luego `B ⊆ U`.
  - `C = {x | x es un carro}`, luego `C ⊆ U`.
  - "Ninguna bicicleta es un carro": `B ∩ C = ∅`. En clase se anotó "no ambos (disyunto)": `B` y `C` son conjuntos disyuntos ([clase 12, sección 11](../clase-12/README.md#11-conjuntos-disyuntos)). En el diagrama, los dos óvalos van dentro del rectángulo de `U`, sin tocarse, y fuera de ellos quedan otras cosas con ruedas (en el dibujo, un camión).
- **Todas las mujeres son personas.** El universo son las personas:
  - `U = {x | x es una persona}`
  - `M = {x ∈ U | x es mujer}`, luego `M ⊆ U`. En el diagrama, el óvalo de `M` queda dentro del rectángulo de `U`, y fuera de él quedan las demás personas.

> [!NOTE]
> El profesor explicó que "ninguna bicicleta es un carro" significa que la intersección de las bicicletas y los carros es vacía: ambos son subconjuntos del universo de las cosas con ruedas, pero sus óvalos no se superponen.

*Aclaración del apunte:* compare con las formas aristotélicas de la [clase 8](../clase-08/README.md): "todas las mujeres son personas" es una afirmación universal (`M ⊆ U`), y "ninguna bicicleta es un carro" es una negativa universal (`B ∩ C = ∅`).

**Ejemplo 5** (pág. 30). Dibuje el diagrama de Venn donde se muestre claramente la relación entre `U = {0, 1, 2, 3, 4, 5, 6, 7, 8, 9}`, `A = {2, 3, 5, 7}` y `A' = {0, 1, 4, 6, 8, 9}`. En clase se resaltaron en `U` los elementos de `A` y los de `A'` con colores distintos, y se dibujó el círculo de `A` con el 2, el 3, el 5 y el 7 dentro; el 0, el 1, el 4, el 6, el 8 y el 9 quedan en el rectángulo, fuera del círculo.

**Ejemplo 6** (pág. 31). Para los siguientes ejercicios, use el diagrama de Venn para determinar `A`, `A'` y `U`. Cada diagrama muestra un círculo `A` dentro del rectángulo `U`:

| `U` | `A` | `A' = U − A` |
|---|---|---|
| `{0, 1, 2, 3, 4, 5, 6, 7, 8, 9}` | `{1, 2, 4, 8}` | `{0, 1, …, 9} − {1, 2, 4, 8} = {0, 3, 5, 6, 7, 9}` |
| `{l, i, s, t, e, n}` | `{n, e, t}` | `{l, i, s, t, e, n} − {n, e, t} = {l, i, s}` |

### 12. Ejemplo 7: operaciones sobre un diagrama de Venn

La sesión del 22/10 empezó con un repaso de las operaciones y de su álgebra ([secciones 2](#2-unión-e-intersección) a [7](#7-identidades-básicas-para-conjuntos)), y siguió con el ejemplo 7 (pág. 32). Teniendo en cuenta el siguiente diagrama de Venn, encuentre las operaciones de la tabla. El diagrama tiene `U = {0, 1, 2, 3, 4, 5, 6, 7, 8, 9}` y dos círculos que se cortan:

| Región | Elementos |
|---|---|
| Solo en `A` | 1, 9 |
| En `A` y en `B` | 3, 5, 7 |
| Solo en `B` | 2 |
| Fuera de `A` y de `B` | 0, 4, 6, 8 |

Primero se leyeron los conjuntos y sus complementos: `A = {1, 9, 3, 5, 7}`, `A' = U − A = {0, 2, 4, 6, 8}`, `B = {2, 3, 5, 7}` y `B' = U − B = {0, 1, 4, 6, 8, 9}`.

| Operación | Desarrollo | Resultado |
|---|---|---|
| `A ∩ B` | `{1, 3, 5, 7, 9} ∩ {2, 3, 5, 7}` | `{3, 5, 7}` |
| `A ∪ B` | `{1, 3, 5, 7, 9} ∪ {2, 3, 5, 7}` | `{1, 2, 3, 5, 7, 9}` |
| `A ∪ B'` | `{1, 3, 5, 7, 9} ∪ {0, 1, 4, 6, 8, 9}` | `{0, 1, 3, 4, 5, 6, 7, 8, 9}` |
| `n(A ∪ B')` | Se cuentan los elementos de la fila anterior | `9` |
| `(A ∪ B)'` | `U − (A ∪ B) = U − {1, 2, 3, 5, 7, 9}` | `{0, 4, 6, 8}` |
| `(A ∩ B)'` | `U − (A ∩ B) = U − {3, 5, 7}` | `{0, 1, 2, 4, 6, 8, 9}` |
| `(A' ∩ B)'` | `= A ∪ B'` (De Morgan), ya calculado | `{0, 1, 3, 4, 5, 6, 7, 8, 9}` |
| `(A' ∪ B')'` | `= A ∩ B` (De Morgan), ya calculado | `{3, 5, 7}` |

Las dos últimas filas no se calcularon elemento por elemento: se usó De Morgan para llegar a una operación que ya estaba resuelta. *Aclaración del apunte:* por De Morgan, `(A' ∩ B)' = A'' ∪ B'`, y por doble negación `A'' = A`; lo mismo en la última fila: `(A' ∪ B')' = A'' ∩ B'' = A ∩ B`.

En el manuscrito hay dos erratas menores, corregidas aquí. Para `(A' ∩ B)'` se escribió la cardinalidad, `|(A' ∩ B)'| = |A ∪ B'| = 9`, en lugar del conjunto que pide el enunciado. Y los complementos se anotaron como `A' = U − {A}` y `B' = U − {B}`; se escribe `U − A`, porque `U − {A}` quitaría de `U` un *elemento* llamado `A`, no los elementos de `A`.

### 13. Ejemplo 8: cardinalidad desde un diagrama

**Ejemplo 8** (pág. 33). El siguiente diagrama de Venn está dibujado de acuerdo a la **cardinalidad** de cada uno de los conjuntos: cada número es la cantidad de elementos de esa región, no un elemento. Teniendo en cuenta esta información, y sustentando mediante la aplicación de las identidades básicas de cardinalidad ([sección 9](#9-identidades-básicas-de-cardinalidad)), determine lo pedido.

| Región | Cantidad de elementos |
|---|---|
| Solo en `A` | 7 |
| En `A` y en `B` | 5 |
| Solo en `B` | 2 |
| Fuera de `A` y de `B` | 8 |

Primero se leyeron del diagrama: `|A| = 7 + 5 = 12`, `|B| = 2 + 5 = 7`, `|A ∩ B| = 5` y `|U| = 7 + 5 + 2 + 8 = 22`. Luego:

| Pedido | Desarrollo | Resultado |
|---|---|---|
| `\|A\| = n(A)` | `7 + 5` | `12` |
| `\|B\| = n(B)` | `2 + 5` | `7` |
| `\|A · B\|` | Región común | `5` |
| `\|A + B\|` | `\|A\| + \|B\| − \|A · B\| = 12 + 7 − 5` (identidad 3) | `14` |
| `\|U\|` | `7 + 5 + 2 + 8` | `22` |
| `\|(A + B)'\|` | `\|U\| − \|A + B\| = 22 − 14` (identidad 7) | `8` |
| `\|A'\|` | `\|U\| − \|A\| = 22 − 12` (identidad 7) | `10` |
| `\|A · B'\|` | Región "solo en `A`" | `7` |

Para `|A · B'|` se anotó además "otra forma", con identidades:

`|A · B'| = |A · (U − B)| = |A · U − A · B| = |A − A · B| = |A| − |A · B| = 12 − 5 = 7`

*Aclaración del apunte:* `B'` está formado por las regiones de 7 y de 8 elementos (todo lo que no está en `B`), pero `A · B'` solo conserva la parte que además está en `A`, que es la región de 7: la de 8 queda fuera de `A`. Por definición de diferencia, `A · B'` (estar en `A` y no estar en `B`) es lo mismo que `A − B`, así que también se puede usar directamente la identidad 4: `|A · B'| = |A − B| = |A| − |A · B| = 12 − 5 = 7`.

> [!NOTE]
> En clase, un estudiante señaló un error en un primer cálculo de `|A · B'|`, y el profesor lo corrigió: el resultado es 7.

### 14. Ejemplo 9: tipos de sangre

**Ejemplo 9** (pág. 34). Utilice el diagrama de Venn a continuación, que muestra los tipos de sangre de 100 personas que donaron sangre en una clínica local, para responder las preguntas.

El diagrama (pág. 35) tiene tres círculos dentro del universo `U` (los tipos de sangre de las 100 personas): `A` (tienen el factor A), `B` (tienen el factor B) y `Rh⁺` (tienen el factor Rh positivo). Cada región tiene un tipo de sangre y su cantidad de personas:

| Tipo | Personas | ¿En `A`? | ¿En `B`? | ¿En `Rh⁺`? |
|---|---|---|---|---|
| `A⁻` | 6 | Sí | No | No |
| `AB⁻` | 1 | Sí | Sí | No |
| `B⁻` | 2 | No | Sí | No |
| `AB⁺` | 3 | Sí | Sí | Sí |
| `A⁺` | 36 | Sí | No | Sí |
| `B⁺` | 8 | No | Sí | Sí |
| `O⁺` | 37 | No | No | Sí |
| `O⁻` | 7 | No | No | No |
| **Total** | **100** | | | |

En clase se verificó que la suma de las ocho regiones da `|U| = 100`. Las regiones no se cortan entre sí, así que son conjuntos disyuntos y, por la identidad 2 de la [sección 9](#9-identidades-básicas-de-cardinalidad), sus cardinalidades se pueden sumar directamente.

**Pregunta 1** (pág. 36). ¿Cuántas personas con factor sanguíneo A donaron sangre?

En la lista de los ocho tipos se encerraron `A⁺` y `A⁻` y se tacharon los demás (también `AB⁻` y `AB⁺`). En el diagrama se marcó como `Tipo(A)` solo la parte del círculo `A` que queda fuera de `B`:

`|Tipo(A)| = |A⁻| + |A⁺| = 6 + 36 = 42`

> [!NOTE]
> Un estudiante señaló la diferencia entre "tipo A" (los perfiles `A⁺` y `A⁻`) y "el conjunto A" del diagrama (todos los que tienen el factor A, incluidos `AB⁺` y `AB⁻`). El profesor reconoció que el diagrama podía generar esa confusión. Otro estudiante preguntó si los tipos dentro de `A` son disyuntos; el profesor respondió que sí: están en regiones separadas del diagrama, sin cruce entre ellas, y por eso sus cardinalidades se suman.

*Aclaración del apunte:* la diapositiva usa "factor sanguíneo A" tanto en esta pregunta como en la de Julio, pero las respuestas lo leen de forma distinta. Aquí se cuenta a quienes tienen sangre **tipo A**: en conjuntos, `Tipo(A) = A − B`, la región de `A` sin la parte `AB`. En la pregunta de Julio se usa el **conjunto `A` completo**, con `AB⁺` y `AB⁻`, porque ellos también tienen el factor A. Las dos cuentas encajan con la identidad 4: `|Tipo(A)| = |A − B| = |A| − |A · B| = 46 − 4 = 42`.

**Pregunta 2** (pág. 37). Julio tiene el tipo sanguíneo `B⁺`. Si necesita una cirugía que requiera una transfusión de sangre, puede aceptar sangre de cualquier persona que no tenga el factor sanguíneo A. ¿Cuántas personas donaron sangre que Julio puede aceptar?

En la lista de los ocho tipos se tacharon "todas las que tienen la A" (`A⁺`, `A⁻`, `AB⁺` y `AB⁻`). Quedan `B⁺`, `B⁻`, `O⁺` y `O⁻`, que son el complemento del conjunto `A`:

`|Tipo(B⁺, B⁻, O⁺, O⁻)| = |A'| = |U| − |A| = |U| − (|A⁺| + |A⁻| + |AB⁺| + |AB⁻|) = 100 − (36 + 6 + 3 + 1) = 100 − 46 = 54`

> [!NOTE]
> Un estudiante preguntó si el 100 salía del complemento de `A`. El profesor respondió que no: el 100 es la cardinalidad del universo, las 100 personas que donaron sangre, según el enunciado.

**Pregunta 3** (pág. 38). ¿Cuántas personas que donaron sangre no tienen el factor sanguíneo Rh⁺?

Se tacharon los tipos con `+` y se encerraron los `Rh⁻`: `A⁻`, `B⁻`, `AB⁻` y `O⁻`. Se resolvió por dos caminos:

- Con el complemento: `|Tipo(Rh⁻)| = |U| − |Rh⁺| = 100 − (36 + 3 + 8 + 37) = 100 − 84 = 16`.
- Sumando las regiones, que son disyuntas: `|Tipo(Rh⁻)| = |A⁻ + AB⁻ + B⁻ + O⁻| = |A⁻| + |AB⁻| + |B⁻| + |O⁻| = 6 + 1 + 2 + 7 = 16`.

Los dos caminos dan el mismo resultado.

**Pregunta 4** (pág. 39). ¿Cuántas personas tenían sangre tipo A y tipo B?

Se subrayó "tipo A y tipo B" y se anotó "ambas (receptor universal)": son las personas con sangre `AB`, la región común de los círculos `A` y `B`, es decir, `A · B`. Se tacharon todos los tipos menos `AB⁺` y `AB⁻`:

`|Tipo(AB)| = |AB⁻| + |AB⁺| = 1 + 3 = 4`

> [!NOTE]
> Un estudiante preguntó por qué "tipo A y tipo B" se interpreta como el tipo `AB`, en lugar de buscar por separado a quienes tienen A y a quienes tienen B. El profesor respondió que tener A y B a la vez es justamente el tipo `AB`, que en el contexto del ejercicio es el receptor universal: puede recibir de donantes tipo A y tipo B. Por eso es la intersección de los dos conjuntos.

### 15. Ejemplo 10: conjuntos de colores

**Ejemplo 10** (pág. 40). Dados los siguientes conjuntos, realice las operaciones indicadas:

- `U = {red, orange, yellow, green, blue, indigo, violet} = {R, O, Y, G, B, I, V}`
- `A = {red, yellow, blue} = {R, Y, B}`
- `B = {orange, green, violet} = {O, G, V}`
- `C = {red, green, indigo} = {R, G, I}`

*Aclaración del apunte:* para resolver, el profesor abrevió cada color con su inicial en inglés. Dentro de las llaves, la **`B` es *blue***, no el conjunto `B`: por ejemplo, `A = {R, Y, B}` dice que el azul está en `A`.

| Operación | Desarrollo | Resultado |
|---|---|---|
| `A + B + C` | `{R, Y, B} + {O, G, V} + {R, G, I}` | `{R, Y, B, O, G, V, I}` |
| `A · C + B` | `{R, Y, B} · {R, G, I} + {O, G, V} = {R} + {O, G, V}` | `{R, O, G, V}` |
| `U · (B + C)` | `1 · (B + C) = B + C = {O, G, V} + {R, G, I}` | `{O, G, V, R, I}` |
| `B · A · U` | `(B · A) · 1 = B · A = {O, G, V} · {R, Y, B}` | `∅` |
| `A · (B · C)'` | `{R, Y, B} · {R, O, Y, B, I, V}` | `{R, Y, B}` |
| `A'(B + C)` | Quedó de tarea | — |

Para `A · (B · C)'` se calculó primero `B · C = {G}` (el verde es el único color de `B` y de `C` a la vez), y luego `(B · C)' = U − (B · C) = {R, O, Y, B, I, V}`. Arriba de la página se anotó que, con De Morgan y la distributiva, la misma expresión se puede escribir `A · (B · C)' = A · (B' + C') = A · B' + A · C'`.

En `U · (B + C)` y `B · A · U` se usó la identidad `A · 1 = A` ([sección 7](#7-identidades-básicas-para-conjuntos)): intersecar con el universo no cambia el conjunto.

> [!NOTE]
> Un estudiante preguntó si, en caso de olvidar una identidad, se puede resolver el ejercicio por el camino largo: listar los elementos de `U` y hacer la intersección directamente. El profesor respondió que sí: la propiedad `A ∩ U = A` garantiza que el resultado es el mismo. Así como a un mismo destino se puede viajar en avión, en bus o en carro, en matemáticas hay varios caminos válidos para llegar al mismo resultado, siempre que estén bien fundamentados.

*Aclaración del apunte:* como se resolvió en clase, `A · C + B` se lee `(A · C) + B`: primero la intersección y después la unión. Observe también que `A + B + C = U` (están los siete colores) y que `B · A = ∅` (`A` y `B` no comparten colores: son disyuntos).

La última operación, `A'(B + C)`, es decir `A' ∩ (B ∪ C)`, quedó como tarea.

Para practicar lo visto en esta clase puede usar el [Taller 6 – Conjuntos](https://discretas1-udea.github.io/discretas1-udea-20262/resources/talleres/taller6/) del sitio del curso. El taller también incluye temas que todavía no se han visto, como el producto cartesiano.

### Síntesis de la clase

*Aclaración del apunte:* un resumen de lo esencial, sin contenido nuevo.

**Ideas clave:**

1. **Cada operación entre conjuntos corresponde a un conectivo lógico**: la unión a `∨`, la intersección a `∧`, y la diferencia y el complemento a `∉`. En un diagrama de Venn, cada una es una región ([secciones 2](#2-unión-e-intersección) a [6](#6-resumen-de-las-operaciones)).
2. **El complemento depende del universo**: `A' = U − A`. Sin `U` no se puede calcular ([sección 4](#4-complemento)).
3. **Las identidades de conjuntos son las leyes de la lógica proposicional** escritas con `+` (unión), `·` (intersección), `1` (universo) y `0` (vacío), y sirven para demostrar igualdades y simplificar expresiones paso a paso ([secciones 7](#7-identidades-básicas-para-conjuntos) y [8](#8-demostrar-y-simplificar-con-identidades)).
4. **Para contar, no sume dos veces la intersección**: `|A + B| = |A| + |B| − |A · B|`. Si los conjuntos son disyuntos, las cardinalidades se suman directamente ([secciones 9](#9-identidades-básicas-de-cardinalidad), [13](#13-ejemplo-8-cardinalidad-desde-un-diagrama) y [14](#14-ejemplo-9-tipos-de-sangre)).
5. **Hay varios caminos válidos**: listar elementos, leer regiones del diagrama o aplicar identidades llevan al mismo resultado si están bien fundamentados ([secciones 12](#12-ejemplo-7-operaciones-sobre-un-diagrama-de-venn) a [15](#15-ejemplo-10-conjuntos-de-colores)).

> [!IMPORTANT]
> **Errores y dudas de esta clase.** Lo que efectivamente ocurrió o se preguntó en las sesiones:
>
> - **"Tipo A" frente al conjunto `A`** (observación de un estudiante, 22/10). La primera pregunta del ejemplo 9 cuenta solo a `A⁺` y `A⁻` (42); la de Julio usa el conjunto `A` completo, con `AB` (46). Ver la [sección 14](#14-ejemplo-9-tipos-de-sangre).
> - **Primer cálculo de `|A · B'|` en el ejemplo 8** (señalado por un estudiante y corregido en clase, 22/10). El resultado es 7. Ver la [sección 13](#13-ejemplo-8-cardinalidad-desde-un-diagrama).
> - **Erratas menores**, corregidas en este apunte: los rótulos "Comprensión" y "Extensión" intercambiados ([sección 1](#1-operaciones-entre-conjuntos)), `4³ = 256` en la diapositiva del ejemplo 2 ([sección 10](#10-ejemplos-1-a-3-representación-cardinalidad-y-subconjuntos)), y en el ejemplo 7 `U − {A}` en lugar de `U − A` y la cardinalidad de `(A' ∩ B)'` en lugar del conjunto ([sección 12](#12-ejemplo-7-operaciones-sobre-un-diagrama-de-venn)).
> - **¿Una lista de elementos es representación por comprensión o por extensión?** (pregunta de un estudiante, 20/10). Por extensión ([sección 1](#1-operaciones-entre-conjuntos)).
> - **¿La "c" repetida en "matemáticas discretas" se cuenta dos veces?** (observación de un estudiante, 20/10). No: en un conjunto no se repiten elementos ([sección 1](#1-operaciones-entre-conjuntos)).
> - **¿Qué significa la "comillita"?** (pregunta de un estudiante, 20/10). Es el complemento: `A'`, `Aᶜ` y `Ā` son equivalentes ([sección 4](#4-complemento)).
> - **¿El universo entra al calcular el conjunto potencia?** (pregunta de un estudiante, 20/10). No: la fórmula se aplica al conjunto que pida el enunciado, por ejemplo `A ∪ B` ([sección 10](#10-ejemplos-1-a-3-representación-cardinalidad-y-subconjuntos)).
> - **¿Los tipos de sangre dentro de `A` son disyuntos?** y **¿el 100 sale del complemento de `A`?** (preguntas de estudiantes, 22/10). Sí son disyuntos, y el 100 es `|U|` ([sección 14](#14-ejemplo-9-tipos-de-sangre)).
> - **¿Por qué "tipo A y tipo B" es el tipo `AB`?** (pregunta de un estudiante, 22/10). Porque tener los dos factores a la vez es la intersección `A · B` ([sección 14](#14-ejemplo-9-tipos-de-sangre)).
> - **¿Se puede resolver por el camino largo, listando `U`?** (pregunta de un estudiante, 22/10). Sí, si está bien fundamentado ([sección 15](#15-ejemplo-10-conjuntos-de-colores)).

## Recursos del curso

| Recurso | Descripción | Enlace |
|---|---|---|
| Video *Ejercicio 5: teoría de conjuntos* | Video de la profesora del curso (Udearroba) que resuelve el ejemplo 11 (porcentaje máximo de estudiantes que aprueban dos asignaturas) con las identidades de cardinalidad, incluidas las desigualdades. Recomendado en clase. | [YouTube](https://www.youtube.com/watch?v=l8BmbuFp7iE) |

## Evaluación

| Ítem | Detalle |
|---|---|
| Supletorio del segundo parcial | El profesor creará un formulario para identificar a los estudiantes que no presentaron el segundo parcial. La propuesta es que lo presenten el mismo día del tercer parcial, para evitar un viaje adicional; la fecha está sujeta a confirmación con la coordinación (22/10). |
| Alcance de las identidades de cardinalidad | En el curso se trabajarán principalmente las cinco identidades de la [sección 9](#9-identidades-básicas-de-cardinalidad); las desigualdades no se profundizaron en clase (20/10). |
| Actividades de repaso | Se publicarán en el foro del curso actividades de repaso sobre el tema de conjuntos (22/10). |

## Pendientes

### Docente

- [ ] Crear y publicar el formulario para identificar a quienes no presentaron el segundo parcial.
- [ ] Confirmar con la coordinación la fecha del supletorio del segundo parcial (propuesta: el mismo día del tercer parcial).
- [ ] Publicar en el foro las actividades de repaso sobre conjuntos.

### Estudiantes

- [ ] Resolver la tarea del ejemplo 10: `A'(B + C)`, es decir `A' ∩ (B ∪ C)`.
- [ ] Si no presentó el segundo parcial, diligenciar el formulario cuando el profesor lo publique.
- [ ] Estar pendiente del foro para las actividades de repaso sobre conjuntos.
- [ ] Ver el [video del ejemplo 11](https://www.youtube.com/watch?v=l8BmbuFp7iE).
- [ ] Repasar las operaciones, las identidades y la cardinalidad con los ejemplos resueltos y el [Taller 6 – Conjuntos](https://discretas1-udea.github.io/discretas1-udea-20262/resources/talleres/taller6/).

## Próxima clase

Martes 27/10/2026: inicio del tema de relaciones, con una introducción general, el producto cartesiano, una visión general de las funciones y, como tema central, las relaciones.
