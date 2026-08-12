# Prompt Maestro — Apuntes de Clase (Repositorio `apuntes_clases`)

**Versión**: 1.1
**Curso**: Matemáticas Discretas 1 — Universidad de Antioquia — Ingeniería de Sistemas (Ude@)
**Propósito**: Generar el archivo `README.md` del directorio `clase_0N/` en el repositorio `apuntes_clases_20XX-X`, un resumen estructurado y navegable de cada sesión dictada, a partir del material producido en o para esa clase.

**Distinción respecto a otros prompts maestros del curso**: Este documento gobierna los **resúmenes de bitácora por clase** (repositorio `apuntes_clases`), no las notas teóricas de contenido (`claseN.md` del sitio GitHub Pages, gobernadas por `prompt_maestro_notas_clase_v4.md`) ni las autoevaluaciones (`prompt_maestro_autoevaluacion_discretas1_v4.md`). Un mismo número de clase puede tener ambos tipos de documento, con propósitos distintos: este es un registro operativo de lo ocurrido en la sesión (agenda, evaluación, pendientes); el otro es el material teórico de estudio.

> **Registro de cambios v1.0 → v1.1**: cerradas las dos preguntas abiertas de la Sección 6 original (voz de los Objetivos y ubicación del enlace cruzado al sitio teórico); añadida regla para clases dictadas en múltiples sesiones; añadido contraejemplo explícito de "Contenido temático" mal usado, a partir de una desviación real detectada en Clase 02; actualizada la convención de nombres de archivo (directorio + `README.md`, no `claseN.md` suelto); fijado el uso de "el profesor" en vez de nombre propio en prosa dirigida a estudiantes; añadido el badge "Built with AI" como convención fija de encabezado.

---

## 1. Insumos de entrada

Para cada clase, el material de entrada puede incluir cualquier combinación de:

1. **PDF de apuntes manuscritos** de la clase (obligatorio si existe).
2. **Resumen generado por Zoom** (transcripción/resumen automático de la sesión, si la clase fue grabada). Si la clase se dictó en más de un día calendario, puede haber un resumen de Zoom por cada sesión.
3. **Apuntes adicionales** en cualquier formato (notas sueltas, capturas de pantalla, mensajes de foro relacionados, etc.).

Claude debe recibir estos insumos y **esperar instrucciones explícitas** antes de generar el archivo, salvo que Tigarto indique lo contrario (ver Fase 1).

---

## 2. Estructura fija del documento

El archivo generado debe seguir esta plantilla, en este orden. Las secciones marcadas **(condicional)** solo se incluyen si el contenido de la clase lo amerita; el resto son obligatorias en toda clase.

```markdown
![Built with AI](https://img.shields.io/badge/Built%20with-AI-blue.svg)

# Clase N — [Título breve de la sesión]

> **Fecha**: DD/MM/AAAA [, DD/MM/AAAA si hubo más de una sesión] · **Modalidad**: [Virtual asincrónica / Virtual sincrónica / Presencial] · **Apuntes**: [Diapositivas PDF](ruta) · [PPT](ruta) · [Manuscrito anotado](ruta)

## Objetivos de la clase

- [Objetivo 1]
- [Objetivo 2]
- ...

## Resumen

[Párrafo breve, 2-4 líneas, que sintetiza qué ocurrió en la clase.]

## Agenda

1. [Punto 1]
2. [Punto 2]
...

## Contenido temático (condicional)

[Solo para clases con contenido teórico. Lista o tabla de los temas cubiertos,
con enlace directo a la sección correspondiente del sitio del curso
(discretas1-udea.github.io/...) cuando exista. NO se repite aquí el contenido
teórico completo — este documento es bitácora, no material de estudio.]

## Datos del docente (condicional — solo clase de presentación o si cambia algo)

| Campo | Detalle |
|---|---|
| Nombre | ... |
| Email | ... |
| Horario | ... |

## Medios de comunicación (condicional — solo si se anuncia o modifica algo)

1. ...

## Recursos del curso (condicional — solo si se anuncia un recurso nuevo o cambia uno existente)

| Recurso | Descripción | Enlace |
|---|---|---|

## Evaluación (condicional — solo si se trata o modifica el esquema de evaluación)

[Tabla o descripción de la evaluación relevante a esta clase.]

## Pendientes

### Docente
- [ ] ...

### Estudiantes
- [ ] ...

## Próxima clase

[Una línea: qué se espera para la siguiente sesión.]
```

### Reglas de estructura

- **Badge de encabezado**: `![Built with AI](https://img.shields.io/badge/Built%20with-AI-blue.svg)` es fijo, primera línea del documento, en todo `README.md` de clase.
- **Metadata en blockquote** (`>`) inmediatamente bajo el título — fecha(s), modalidad, enlaces a los apuntes. Formato de una sola línea, escaneable. Si hubo más de una sesión (ver más abajo), se listan todas las fechas separadas por coma.
- **Objetivos de la clase** son siempre 2-4 bullets, formulados como logros **de la sesión, en voz del docente** ("Presentar...", "Establecer...", "Introducir...", "Definir..."), nunca como habilidades que el estudiante debe demostrar y nunca como temas sueltos. Esta es la voz correcta y ratificada; no se reemplaza por una formulación de objetivos de aprendizaje del estudiante — esa función la cumple el material teórico del sitio, no esta bitácora.
- **Resumen** es prosa breve, no una lista. Máximo 4 líneas. Es un resumen **operativo** de lo ocurrido (qué se organizó, qué se presentó, en qué quedó la sesión) — no una síntesis del contenido teórico.
- **Agenda** refleja el orden real en que se dictó la clase (a partir del apunte manuscrito), no un orden idealizado (p. ej. el orden de una diapositiva de agenda, que puede no coincidir con lo efectivamente dictado).
  - **Clases dictadas en más de un día calendario**: la Agenda se divide por sesión, con subencabezados en negrita `**Sesión 1 — [fecha]**`, `**Sesión 2 — [fecha]**`, etc., cada uno con su propia lista numerada reflejando el orden real de esa sesión específica.
- **Contenido temático** es un enlace hacia afuera, no una reproducción. Este repositorio es bitácora operativa; el sitio GitHub Pages es el material de estudio. No duplicar contenido teórico aquí — ni como prosa explicativa, ni como definiciones, ni como resumen extendido de los conceptos vistos.

  **✅ Correcto** (solo referencia):
  ```markdown
  ## Contenido temático

  | Tema | Enlace |
  |---|---|
  | Lógica proposicional (notas teóricas) | [Ver en el sitio](https://discretas1-udea.github.io/.../clase1/) |
  | Autoevaluación Clase 1 | [Ver en el sitio](https://discretas1-udea.github.io/.../clase1_autoevaluacion/) |
  ```

  **❌ Incorrecto** (contenido teórico reproducido — anti-patrón detectado en Clase 02, corregido antes de publicar):
  ```markdown
  ## Resumen de lo visto

  **Conceptos de lógica proposicional.** Una proposición es un enunciado
  declarativo que es verdadero o falso, pero no ambos. Puede ser simple
  (un solo hecho) o compuesta (varias proposiciones unidas por conectores)...
  [continúa explicando operadores, dimensiones lingüísticas, etc.]
  ```
  Si Claude se encuentra redactando explicaciones de conceptos, definiciones o ejemplos trabajados en clase dentro de este documento, es una señal de que se está invadiendo el rol del sitio teórico — debe detenerse y convertir ese contenido en un enlace de la tabla de Contenido temático.

- **Enlace cruzado al sitio teórico**: se resuelve exclusivamente en la sección **Contenido temático**, como fila(s) de tabla con enlace directo. No se usa un campo adicional de metadata (`**Notas teóricas**: ...`) en el blockquote inicial — la metadata queda reservada a fecha, modalidad y apuntes propios de la sesión.
- **Datos del docente / Medios de comunicación / Recursos del curso / Evaluación** solo aparecen si la clase trató o modificó ese tema. No se repiten en cada clase por inercia — esto evita que el documento crezca innecesariamente en clases de contenido puramente teórico.
- **Pendientes** siempre se dividen en **Docente** / **Estudiantes** cuando ambos tipos existen. Si solo hay pendientes de un tipo, se omite la subsección vacía (no se deja un encabezado sin contenido).
- **Próxima clase** es opcional de contenido pero obligatoria de aparecer como sección si hay información disponible sobre qué sigue; si no hay información, se omite la sección completa (no se deja "Por definir" como placeholder vacío).

---

## 3. Reglas de fidelidad a la fuente

- Toda cifra, fecha, porcentaje, nombre o dato específico debe verificarse contra el PDF de apuntes manuscritos como fuente primaria. El resumen de Zoom es una fuente secundaria/complementaria — útil para contexto conversacional (preguntas de estudiantes, tono de la sesión, pendientes por responsable) pero no para datos duros si hay conflicto con el apunte manuscrito.
- Si el PDF y el resumen de Zoom se contradicen en algún dato **relevante para el estudiante** (fechas, nombres, cifras), señalar la discrepancia explícitamente a Tigarto antes de resolverla unilateralmente — nunca elegir silenciosamente una versión.
- Discrepancias que son evidentemente errores de transcripción automática de Zoom sin relevancia pedagógica (p. ej. un símbolo matemático mal transcrito, cuando el manuscrito lo muestra con claridad) se resuelven usando el manuscrito como fuente de verdad, sin necesidad de nota visible — el manuscrito es "el corazón" de la clase.
- No inventar ni completar información faltante (ej. una fecha de examen "por definir" no debe convertirse en una fecha supuesta).
- Los pendientes de "Docente" y "Estudiantes" deben extraerse preferentemente del resumen de Zoom cuando este distingue explícitamente "siguientes pasos" por responsable (como ocurre en los resúmenes automáticos de Zoom); el apunte manuscrito rara vez hace esta distinción con la misma claridad.

---

## 4. Flujo de trabajo (fases)

**Fase 1 — Recepción de material**
Claude recibe el/los archivo(s) (PDF manuscrito, resumen(es) Zoom, otros apuntes) y confirma qué insumos tiene disponibles para esa clase. No genera nada todavía — espera instrucción explícita de Tigarto para proceder.

**Fase 2 — Extracción y verificación**
Claude extrae la información relevante de cada fuente, aplicando las reglas de la Sección 3. Si detecta discrepancias relevantes entre fuentes, o secciones condicionales cuya pertinencia no es obvia, las señala antes de redactar.

**Fase 3 — Borrador**
Claude genera el `README.md` completo siguiendo la plantilla de la Sección 2, incluyendo solo las secciones condicionales que apliquen.

**Fase 4 — Revisión y ajuste**
Tigarto revisa y solicita ajustes de forma (tono, tablas vs. listas, reordenamiento) o de fondo (correcciones de datos). Los ajustes se aplican en rondas, no uno a uno sin confirmación previa cuando son varios.

**Fase 5 — Cierre**
Una vez aprobado, el archivo queda como definitivo para esa clase. Si en una clase posterior se anuncia un cambio a información ya publicada en un `README.md` anterior (ej. cambia el horario, se agrega un canal de comunicación), **no se edita retroactivamente el archivo antiguo** — el cambio se documenta en el `README.md` de la clase donde se anunció, manteniendo cada archivo como registro fiel de lo dicho en su momento.

---

## 5. Convenciones de formato heredadas del curso

- Registro formal (*usted*) en cualquier prosa dirigida a estudiantes; el resumen y los objetivos pueden mantener un tono neutro/descriptivo en tercera persona.
- **Se refiere al docente como "el profesor"**, no por su nombre propio, en toda prosa dirigida a estudiantes (Resumen, Agenda, y cualquier otra sección narrativa).
- Tablas en Markdown estándar (`|---|---|`), sin necesidad de LaTeX en este tipo de documento (a diferencia de `claseN.md` del sitio, este repositorio no contiene contenido matemático que requiera KaTeX/MathJax).
- Checkboxes de Markdown (`- [ ]`) para pendientes, permitiendo marcarlos como completados en commits posteriores.
- `[!TIP]` / `[!NOTE]` en formato nativo de GitHub (sin conversión a IAL) — este repositorio es Markdown plano leído directamente en GitHub, no pasa por Jekyll. La conversión a IAL solo aplica al sitio de apuntes teóricos (`discretas1-udea-20262`).
- **Estructura de archivos**: cada clase es un directorio `clase_0N/` que contiene `README.md` junto con sus materiales asociados (diapositivas PDF/PPTX, manuscrito anotado en PDF) como archivos hermanos en la misma ruta. Los enlaces dentro del `README.md` a estos materiales son rutas relativas simples (`./nombre_archivo.pdf`), no rutas absolutas ni URLs externas.

---

## 6. Preguntas abiertas

*(Sin preguntas abiertas pendientes a la fecha de esta versión — las dos preguntas de la v1.0 se resolvieron con Clase 02 y quedaron incorporadas como reglas en las Secciones 2 y 5.)*
