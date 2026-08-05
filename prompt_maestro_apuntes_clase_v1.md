# Prompt Maestro — Apuntes de Clase (Repositorio `apuntes_clases`)

**Versión**: 1.0
**Curso**: Matemáticas Discretas 1 — Universidad de Antioquia — Ingeniería de Sistemas (Ude@)
**Propósito**: Generar el archivo `claseN.md` del repositorio `apuntes_clases_20XX-X`, un resumen estructurado y navegable de cada sesión dictada, a partir del material producido en o para esa clase.

**Distinción respecto a otros prompts maestros del curso**: Este documento gobierna los **resúmenes de bitácora por clase** (repositorio `apuntes_clases`), no las notas teóricas de contenido (`claseN.md` del sitio GitHub Pages, gobernadas por `prompt_maestro_notas_clase_v4.md`) ni las autoevaluaciones (`prompt_maestro_autoevaluacion_discretas1_v4.md`). Un mismo número de clase puede tener ambos tipos de documento, con propósitos distintos: este es un registro operativo de lo ocurrido en la sesión (agenda, evaluación, pendientes); el otro es el material teórico de estudio.

---

## 1. Insumos de entrada

Para cada clase, el material de entrada puede incluir cualquier combinación de:

1. **PDF de apuntes manuscritos** de la clase (obligatorio si existe).
2. **Resumen generado por Zoom** (transcripción/resumen automático de la sesión, si la clase fue grabada).
3. **Apuntes adicionales** en cualquier formato (notas sueltas, capturas de pantalla, mensajes de foro relacionados, etc.).

Claude debe recibir estos insumos y **esperar instrucciones explícitas** antes de generar el archivo, salvo que Tigarto indique lo contrario (ver Fase 1).

---

## 2. Estructura fija del documento

El archivo generado debe seguir esta plantilla, en este orden. Las secciones marcadas **(condicional)** solo se incluyen si el contenido de la clase lo amerita; el resto son obligatorias en toda clase.

```markdown
# Clase N — [Título breve de la sesión]

> **Fecha**: DD/MM/AAAA · **Modalidad**: [Virtual asincrónica / Presencial] · **Apuntes**: [PDF](ruta-al-pdf)

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

- **Metadata en blockquote** (`>`) inmediatamente bajo el título — fecha, modalidad, enlace al PDF. Formato de una sola línea, escaneable.
- **Objetivos de la clase** son siempre 2-4 bullets, formulados como logros ("Presentar...", "Establecer...", "Introducir..."), nunca como temas sueltos.
- **Resumen** es prosa breve, no una lista. Máximo 4 líneas.
- **Agenda** refleja el orden real en que se dictó la clase (a partir del apunte manuscrito), no un orden idealizado.
- **Pendientes** siempre se dividen en **Docente** / **Estudiantes** cuando ambos tipos existen. Si solo hay pendientes de un tipo, se omite la subsección vacía (no se deja un encabezado sin contenido).
- **Próxima clase** es opcional de contenido pero obligatoria de aparecer como sección si hay información disponible sobre qué sigue; si no hay información, se omite la sección completa (no se deja "Por definir" como placeholder vacío).
- Las secciones condicionales (Datos del docente, Medios de comunicación, Recursos del curso, Evaluación) **solo aparecen si la clase trató o modificó ese tema**. No se repiten en cada clase por inercia — esto evita que el documento crezca innecesariamente en clases de contenido puramente teórico.
- **Contenido temático** es un enlace hacia afuera, no una reproducción. Este repositorio es bitácora operativa; el sitio GitHub Pages es el material de estudio. No duplicar contenido teórico aquí.

---

## 3. Reglas de fidelidad a la fuente

- Toda cifra, fecha, porcentaje, nombre o dato específico debe verificarse contra el PDF de apuntes manuscritos como fuente primaria. El resumen de Zoom es una fuente secundaria/complementaria — útil para contexto conversacional (preguntas de estudiantes, tono de la sesión) pero no para datos duros si hay conflicto con el apunte manuscrito.
- Si el PDF y el resumen de Zoom se contradicen en algún dato, **señalar la discrepancia explícitamente a Tigarto** antes de resolverla unilateralmente — nunca elegir silenciosamente una versión.
- No inventar ni completar información faltante (ej. una fecha de examen "por definir" no debe convertirse en una fecha supuesta).
- Los pendientes de "Docente" y "Estudiantes" deben extraerse preferentemente del resumen de Zoom cuando este distingue explícitamente "siguientes pasos" por responsable (como ocurre en los resúmenes automáticos de Zoom); el apunte manuscrito rara vez hace esta distinción con la misma claridad.

---

## 4. Flujo de trabajo (fases)

**Fase 1 — Recepción de material**
Claude recibe el/los archivo(s) (PDF manuscrito, resumen Zoom, otros apuntes) y confirma qué insumos tiene disponibles para esa clase. No genera nada todavía — espera instrucción explícita de Tigarto para proceder (patrón ya establecido: "Procede a realizar la primera actividad de las que propones" es un ejemplo de disparador válido).

**Fase 2 — Extracción y verificación**
Claude extrae la información relevante de cada fuente, aplicando las reglas de la Sección 3. Si detecta discrepancias entre fuentes, o secciones condicionales cuya pertinencia no es obvia, las señala antes de redactar.

**Fase 3 — Borrador**
Claude genera el `claseN.md` completo siguiendo la plantilla de la Sección 2, incluyendo solo las secciones condicionales que apliquen.

**Fase 4 — Revisión y ajuste**
Tigarto revisa y solicita ajustes de forma (tono, tablas vs. listas, reordenamiento) o de fondo (correcciones de datos). Los ajustes se aplican en rondas, no uno a uno sin confirmación previa cuando son varios.

**Fase 5 — Cierre**
Una vez aprobado, el archivo queda como definitivo para esa clase. Si en una clase posterior se anuncia un cambio a información ya publicada en un `claseN.md` anterior (ej. cambia el horario, se agrega un canal de comunicación), **no se edita retroactivamente el archivo antiguo** — el cambio se documenta en el `claseN.md` de la clase donde se anunció, manteniendo cada archivo como registro fiel de lo dicho en su momento.

---

## 5. Convenciones de formato heredadas del curso

- Registro formal (*usted*) en cualquier prosa dirigida a estudiantes; el resumen y los objetivos pueden mantener un tono neutro/descriptivo en tercera persona.
- Tablas en Markdown estándar (`|---|---|`), sin necesidad de LaTeX en este tipo de documento (a diferencia de `claseN.md` del sitio, este repositorio no contiene contenido matemático que requiera KaTeX/MathJax).
- Checkboxes de Markdown (`- [ ]`) para pendientes, permitiendo marcarlos como completados en commits posteriores.
- Nombres de archivo: `claseN.md`, consistente con la convención ya usada en `apuntes_clases_2026-2`.

---

## 6. Preguntas abiertas (a resolver con Tigarto en la primera clase de contenido teórico)

- Para clases de contenido teórico (no de presentación), confirmar si "Objetivos de la clase" y "Agenda" se mantienen igual, o si "Contenido temático" las reemplaza/complementa de otra forma.
- Definir si se desea un enlace cruzado explícito entre este documento y el `claseN.md` teórico del sitio (por ejemplo, un campo adicional en la metadata: `**Notas teóricas**: [Ver en el sitio](...)`).
