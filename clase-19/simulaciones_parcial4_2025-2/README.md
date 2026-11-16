![Built with AI](https://img.shields.io/badge/Built%20with-AI-blue.svg)

# Simulaciones del parcial 4 de 2025-2 (circuitos digitales)

> **Parcial de referencia**: [Enunciado](https://discretas1-udea.github.io/discretas1-udea-20262/assets/exams/discretas1_parcial4_2025-2.pdf) · [Solución](https://discretas1-udea.github.io/discretas1-udea-20262/assets/exams/discretas1_parcial4_2025-2_sol.pdf)
>
> Estos circuitos son los puntos 1 y 2 del parcial 4 del semestre 2025-2 (*Álgebra booleana y sistemas numéricos*), listos para abrir en Logisim-evolution. Sirven para comprobar la solución publicada y para practicar con un parcial anterior.

Si todavía no tiene el simulador, siga la [guía de instalación de Logisim-evolution](../ejemplos_logisim/README.md#2-instalación-de-logisim-evolution). La [guía paso a paso](../ejemplos_logisim/README.md#4-ejemplo-guiado-el-ejemplo-1-de-la-clase) explica cómo abrir un `.circ`, cambiar las entradas y obtener la tabla de verdad. Ninguno de estos archivos tiene sondas y todas sus entradas y salidas tienen nombre, así que en **Proyecto → Analizar circuito** verá las letras del enunciado y las pestañas *Expresión* y *Minimizado* funcionan.

## Punto 1 — Deducir y simplificar un circuito

Es el mismo circuito del *Ejercicio tipo parcial* de la [clase 19](../clase19.pdf) (págs. 37–39). El enunciado pide deducir la expresión booleana del circuito, simplificarla con las identidades del álgebra booleana, dibujar el circuito simplificado y obtener su tabla de verdad y sus formas SOP y POS.

| Archivo | Contenido |
|---|---|
| [`circuito1.circ`](./circuito1.circ) | Circuito del enunciado, con entradas `x`, `y`, `z` y salida `f`: `f = y + ((x + y')' + x + z)'` |
| [`circuito1_simplificado.circ`](./circuito1_simplificado.circ) | Circuito simplificado de la solución, `f = y + x'·z'`: dos NOT, una AND y una OR. |

Tabla de verdad, la misma para la versión original y la simplificada:

| `x` | `y` | `z` | `f` |
|:-:|:-:|:-:|:-:|
| 0 | 0 | 0 | 1 |
| 0 | 0 | 1 | 0 |
| 0 | 1 | 0 | 1 |
| 0 | 1 | 1 | 1 |
| 1 | 0 | 0 | 0 |
| 1 | 0 | 1 | 0 |
| 1 | 1 | 0 | 1 |
| 1 | 1 | 1 | 1 |

**Cómo comprobarlo:**

1. Abra los dos archivos y recorra las ocho combinaciones de `x`, `y`, `z` con la herramienta de la mano. Los dos circuitos dan siempre la misma salida: simplificar cambia el circuito (de siete compuertas a cuatro), no la función.
2. En `circuito1.circ`, use **Proyecto → Analizar circuito → Minimizado**: Logisim propone una expresión simplificada que debe ser equivalente a `y + x'·z'`.

En el circuito simplificado, el cable de `y` cruza el de `x'` sin un punto de unión: según la convención de las diapositivas, esos cables no se tocan.

## Punto 2 — Alarma activa en BAJO

Un recipiente químico tiene un sensor de temperatura (`T`) y uno de presión (`P`). Cada sensor entrega `1` (ALTO) cuando su variable supera el límite. La alarma `A` es **activa en BAJO**: se activa con `0`. Por lo tanto `A = 0` en cuanto alguno de los sensores vale 1, y `A = 1` solo cuando ninguno supera su límite.

| Archivo | Contenido |
|---|---|
| [`circuito2.circ`](./circuito2.circ) | Circuito construido a partir de la SOP: `A = T'·P'` (dos NOT y una AND) |
| [`circuito2_nor.circ`](./circuito2_nor.circ) | El mismo sistema con una sola compuerta NOR: `A = (T + P)'` |

| `T` | `P` | `A` |
|:-:|:-:|:-:|
| 0 | 0 | 1 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 0 |

Los dos archivos tienen la misma tabla. Es un ejemplo de la ley de De Morgan: `T'·P' = (T + P)'`. Compruébelo abriendo ambos y cambiando las entradas con la herramienta de la mano.
