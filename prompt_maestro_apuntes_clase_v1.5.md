# Prompt Maestro — Apuntes de Clase (Repositorio `apuntes_clases`)

**Versión**: 1.5
**Curso**: Matemáticas Discretas 1 — Universidad de Antioquia — Ingeniería de Sistemas (Ude@)
**Propósito**: Generar el archivo `README.md` del directorio `clase_0N/` en el repositorio `apuntes_clases_20XX-X`, un resumen estructurado y navegable de cada sesión dictada, a partir del material producido en o para esa clase.

**Distinción respecto a otros prompts maestros del curso**: Este documento gobierna los **resúmenes de bitácora por clase** (repositorio `apuntes_clases`), no las notas teóricas de contenido (`claseN.md` del sitio GitHub Pages, gobernadas por `prompt_maestro_notas_clase_v4.md`) ni las autoevaluaciones (`prompt_maestro_autoevaluacion_discretas1_v4.md`). Un mismo número de clase puede tener ambos tipos de documento, con propósitos distintos: este es un registro operativo de lo ocurrido en la sesión (agenda, evaluación, pendientes), que **a partir de v1.2 también puede incorporar un resumen teórico expandido** de lo visto en clase; el sitio teórico sigue siendo el material de estudio canónico, completo y ejercitado.

> **Registro de cambios v1.4 → v1.5**: se precisa que una misma sesión puede tener **más de un artefacto derivado de Zoom** con distinto nivel de detalle (un resumen narrativo y unas notas o "contenido general" más granulares, con citas textuales), tratados en conjunto como fuente secundaria. Se añade una tercera vía para resolver auditorías de otras herramientas de IA sobre un `README.md` ya redactado: cuando el señalamiento es válido pero el contenido cuestionado es una cita fiel de lo mostrado o dicho por el profesor, la corrección correcta no es reescribir la cita ni rechazar el señalamiento en bloque, sino preservar la cita textual y agregar junto a ella una nota aclaratoria breve. Se aclara el caso en que el manuscrito o el PPTX traen, más allá del corte de la última sesión de la clase documentada, contenido ya preparado para una clase posterior aún no dictada: ese contenido se excluye de "Contenido temático" y solo se referencia, si aporta información legítima, en "Próxima clase". Se adopta como convención fija que los ítems de la Agenda que referencian otra sección del documento se expresen como enlaces ancla de Markdown, para facilitar la navegación en documentos largos.
>
> **Registro de cambios v1.3 → v1.4**: se añade una regla de fidelidad para el caso de auditorías o revisiones hechas con otras herramientas de IA (Gemini, ChatGPT, etc.) sobre un `README.md` ya redactado: cada corrección propuesta debe verificarse contra el manuscrito antes de aplicarse, y se rechazan las que reemplacen contenido transcrito fielmente (terminología, ejemplos, fórmulas del profesor) por una versión más rigurosa de libro de texto que no fue efectivamente dictada — el criterio de estas auditorías suele ser "¿es esto correcto según la teoría formal?", mientras que el de este repositorio es "¿es esto fiel a lo que pasó en el salón?". Se precisa el procedimiento para ubicar el corte real entre sesiones de una clase multi-sesión: buscar marcas de fecha explícitas dentro del propio manuscrito (a menudo anotadas a mano entre una diapositiva y la siguiente) y cruzarlas con los resúmenes de Zoom de cada sesión — no asumir que el corte coincide con un tema "redondo" o con el orden de una diapositiva de agenda. Se actualiza la regla de diagramas/capturas de "Contenido temático" para admitir explícitamente diagramas en Mermaid (bloques ` ```mermaid `, renderizados nativamente por GitHub) como alternativa a las capturas de imagen — preferible cuando el diagrama es una relación conceptual entre los términos ya definidos en el texto (no un dato nuevo), evitando además archivos binarios adicionales en el repositorio — y se agrega una nota de criterio: reservar las capturas del manuscrito para cuando aporten información visual que el texto/tabla no pueda reproducir fielmente, no como decoración.
>
> **Registro de cambios v1.2 → v1.3**: se precisa que una clase dictada en varias sesiones puede tener un resumen de Zoom por sesión, y que estos resúmenes —cruzados entre sí y con el manuscrito— son la vía para resolver discrepancias sobre el enunciado real de un ejercicio cuando estas surgen (p. ej., un enunciado transcrito incorrectamente y aclarado en una sesión posterior). Se añade que las demostraciones trabajadas en clase (formato afirmación-razón) pueden reproducirse completas en "Contenido temático", extraídas fielmente del manuscrito anotado, cuando aporten claridad al apunte. Se añade una regla para inconsistencias internas del propio manuscrito (p. ej., un número de paso mal referenciado en una demostración): se transcriben tal cual, señaladas con una nota aclaratoria, sin corregirlas silenciosamente. Se actualiza la convención de archivos hermanos para admitir un archivo de corrección enviado aparte (`correccion_ejemploN_annotated.pdf`) cuando el profesor rectifica un error después de la clase.
>
> **Registro de cambios v1.1 → v1.2**: cambio de fondo en la sección "Contenido temático" — deja de ser exclusivamente una tabla de enlaces al sitio teórico y pasa a admitir un **resumen teórico expandido** (explicaciones, diagramas, capturas, fragmentos de código, fórmulas) directamente en el README de bitácora, inspirado en un formato usado en otra materia. Se retira la prohibición y el contraejemplo de la v1.1 sobre reproducir contenido teórico. Se añaden reglas de fidelidad para código/imágenes incluidos en esta sección, y se actualiza la convención de archivos hermanos para incluir imágenes.
>
> **Registro de cambios v1.0 → v1.1**: cerradas las dos preguntas abiertas de la Sección 6 original (voz de los Objetivos y ubicación del enlace cruzado al sitio teórico); añadida regla para clases dictadas en múltiples sesiones; actualizada la convención de nombres de archivo (directorio + `README.md`, no `claseN.md` suelto); fijado el uso de "el profesor" en vez de nombre propio en prosa dirigida a estudiantes; añadido el badge "Built with AI" como convención fija de encabezado.

---

## 1. Insumos de entrada

Para cada clase, el material de entrada puede incluir cualquier combinación de:

1. **PDF de apuntes manuscritos** de la clase (obligatorio si existe).
2. **Material derivado de Zoom** (transcripción/resumen automático de la sesión, si la clase fue grabada). Si la clase se dictó en más de un día calendario, puede haber material de Zoom por cada sesión. **(A partir de v1.5)** Además, una misma sesión puede tener **más de un artefacto derivado de Zoom** con distinto nivel de detalle — típicamente un **resumen narrativo** (útil para tono de la sesión, preguntas de estudiantes y pendientes por responsable) y unas **notas o "contenido general"** más granulares, con citas textuales y trazabilidad por bloque temático (útil para precisar redacción exacta, cifras y ejemplos). Ambos se tratan en conjunto como fuente secundaria frente al manuscrito, y se cruzan entre sí para verificar consistencia antes de usarlos. Cuando hay varios documentos (por sesión o por nivel de detalle), estos pueden cruzarse entre sí y con el manuscrito para resolver dudas sobre el enunciado real de un ejercicio, especialmente cuando una sesión posterior aclara explícitamente un error cometido o detectado en una sesión anterior (ver Sección 3).
3. **Apuntes adicionales** en cualquier formato (notas sueltas, capturas de pantalla, diagramas, fragmentos de código trabajados en clase, mensajes de foro relacionados, etc.), incluyendo archivos de corrección enviados aparte cuando el profesor rectifica un error después de dictada la clase (ver Sección 5).

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

[Solo para clases con contenido teórico. Resumen teórico expandido de los
temas cubiertos en la sesión, organizado en subtítulos numerados por tema
(### 1. [Tema], ### 2. [Tema], ...). Cada subtema puede incluir explicación
en prosa o bullets, diagramas/capturas relevantes, fórmulas, fragmentos de
código, y demostraciones efectivamente trabajadas en clase (incluyendo, cuando
aporte claridad, la tabla completa de afirmación-razón). Al final de la
sección (o de cada subtema, si aplica) se agrega el enlace a la sección
correspondiente del sitio del curso (discretas1-udea.github.io/...) como
referencia complementaria para profundizar y ejercitar.]

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
- **Objetivos de la clase** son siempre 2-4 bullets, formulados como logros **de la sesión, en voz del docente** ("Presentar...", "Establecer...", "Introducir...", "Definir..."), nunca como habilidades que el estudiante debe demostrar y nunca como temas sueltos.
- **Resumen** es prosa breve, no una lista. Máximo 4 líneas. Es un resumen **operativo** de lo ocurrido (qué se organizó, qué se presentó, en qué quedó la sesión) — no reemplaza a "Contenido temático"; ese es el lugar para el detalle teórico.
- **Agenda** refleja el orden real en que se dictó la clase (a partir del apunte manuscrito), no un orden idealizado (p. ej. el orden de una diapositiva de agenda, que puede no coincidir con lo efectivamente dictado).
  - **Clases dictadas en más de un día calendario**: la Agenda se divide por sesión, con subencabezados en negrita `**Sesión 1 — [fecha]**`, `**Sesión 2 — [fecha]**`, etc., cada uno con su propia lista numerada reflejando el orden real de esa sesión específica.
  - **(A partir de v1.4) Ubicación del corte real entre sesiones**: antes de asignar un tema a una sesión u otra, buscar en el manuscrito una marca de fecha explícita entre diapositivas (a menudo anotada a mano, p. ej. "Fin: DD/MM → Inicio: DD/MM") que indique dónde terminó una sesión y empezó la siguiente. Si el manuscrito no trae esa marca en todos los puntos de corte, cruzar el contenido de cada tema con los resúmenes de Zoom de cada sesión (qué se discutió, qué preguntas surgieron) para inferir el corte correcto. No asumir que el corte coincide con el final "redondo" de un tema o con el orden de una diapositiva de agenda inicial — esa suposición puede llevar a asignar contenido a la sesión equivocada.
  - **(A partir de v1.5) Contenido de una clase futura incluido en el mismo manuscrito**: en ocasiones el manuscrito o el PPTX traen, más allá del corte de la última sesión de la clase que se está documentando, diapositivas ya preparadas para una clase posterior (identificable por una marca de fecha que no corresponde a ninguna de las fechas de la clase actual, p. ej. "Fin: DD/MM → Inicio: DD/MM" con una fecha de inicio varios días después de la última sesión efectivamente dictada). Ese contenido **no se incluye** en "Contenido temático" de la clase actual, porque no fue efectivamente dictado, y solo se referencia — si aporta información legítima sobre lo que sigue — en la sección "Próxima clase", nunca presentado como ya cubierto.
  - **(A partir de v1.5) Navegación por anclas**: cada ítem de la Agenda que referencia otra sección del documento (`(→ sección N)`, `(→ Evaluación)`, etc.) se expresa como un enlace ancla de Markdown al encabezado correspondiente, p. ej. `[*(→ sección 1)*](#1-tema)`, usando el slug que GitHub genera automáticamente a partir del texto del encabezado (minúsculas, espacios y puntuación reemplazados por guiones, tildes conservadas). Esto facilita el repaso en documentos largos. Esta convención aplica desde su adopción en adelante; no es obligatorio aplicarla retroactivamente a clases ya finalizadas (ver Fase 5).
- **Contenido temático** (a partir de v1.2) es un **resumen teórico expandido**, no solo un enlace de salida:
  - Se organiza en subtítulos numerados (`### 1. [Tema]`, `### 2. [Tema]`, ...) que reflejan los temas efectivamente cubiertos.
  - Puede incluir explicaciones de conceptos, diagramas o capturas (como archivos hermanos en `clase_0N/`, referenciados con ruta relativa `./nombre_imagen.png`), fórmulas, y fragmentos de código **efectivamente trabajados en la sesión** (no ejemplos inventados ni generalizaciones del tema).
  - **(A partir de v1.4)** Un diagrama también puede expresarse como bloque Mermaid (` ```mermaid `), que GitHub renderiza de forma nativa sin necesidad de generar ni almacenar un archivo de imagen — es la opción preferida cuando el diagrama visualiza una relación conceptual entre términos que la propia clase ya definió (p. ej. una jerarquía entre conceptos), no cuando introduce información nueva. Las capturas del manuscrito, en cambio, se reservan para cuando el contenido visual (una tabla con anotaciones a mano, un ejemplo con imágenes propias del profesor) no se pueda reproducir fielmente como texto o tabla de Markdown — no se agregan solo para "enriquecer" visualmente una sección cuyo contenido ya está bien cubierto en prosa/tabla.
  - **(A partir de v1.3)** Cuando la clase trabajó demostraciones en formato afirmación-razón, estas pueden reproducirse **completas** (tabla con columnas `#`, `Afirmación`, `Razón`) cuando aporten claridad al apunte, extraídas fielmente del manuscrito anotado o de un archivo de corrección enviado aparte — no es obligatorio resumirlas solo en prosa. Esto aplica igual a intentos fallidos o parciales que sean pedagógicamente relevantes (p. ej., un error de razonamiento identificado en clase), siempre que se documente su desenlace.
  - Cuando exista una nota teórica correspondiente en el sitio del curso, se agrega el enlace (`[Ver en el sitio](https://discretas1-udea.github.io/...)`) como referencia complementaria para profundizar y practicar — el sitio sigue siendo el material completo de estudio; esta sección es un resumen de lo dictado en *esta* sesión, no una reescritura exhaustiva del tema. Si el sitio va rezagado respecto a la clase (p. ej. solo publicada hasta una clase anterior), se enlaza la página disponible más reciente, no una URL de la clase actual sin confirmar que existe.
  - Si la clase se dictó en varias sesiones y cada una cubrió temas distintos, los subtítulos pueden agruparse o anotarse por sesión cuando ayude a la trazabilidad (a criterio de Claude, según lo que sea más legible).
- **Enlace cruzado al sitio teórico**: se resuelve dentro de la sección **Contenido temático** (al final de la sección o de cada subtema), no como campo adicional de metadata en el blockquote inicial — la metadata queda reservada a fecha, modalidad y apuntes propios de la sesión.
- **Datos del docente / Medios de comunicación / Recursos del curso / Evaluación** solo aparecen si la clase trató o modificó ese tema. No se repiten en cada clase por inercia — esto evita que el documento crezca innecesariamente por secciones que no aportan información nueva.
- **Pendientes** siempre se dividen en **Docente** / **Estudiantes** cuando ambos tipos existen. Si solo hay pendientes de un tipo, se omite la subsección vacía (no se deja un encabezado sin contenido).
- **Próxima clase** es opcional de contenido pero obligatoria de aparecer como sección si hay información disponible sobre qué sigue; si no hay información, se omite la sección completa (no se deja "Por definir" como placeholder vacío).

---

## 3. Reglas de fidelidad a la fuente

- Toda cifra, fecha, porcentaje, nombre o dato específico debe verificarse contra el PDF de apuntes manuscritos como fuente primaria. El material de Zoom es una fuente secundaria/complementaria — útil para contexto conversacional (preguntas de estudiantes, tono de la sesión, pendientes por responsable) pero no para datos duros si hay conflicto con el apunte manuscrito.
- Si el PDF y el material de Zoom se contradicen en algún dato **relevante para el estudiante** (fechas, nombres, cifras), señalar la discrepancia explícitamente a Tigarto antes de resolverla unilateralmente — nunca elegir silenciosamente una versión.
- Discrepancias que son evidentemente errores de transcripción automática de Zoom sin relevancia pedagógica (p. ej. un símbolo matemático mal transcrito, o una fecha que no corresponde a ningún dato del curso, cuando el manuscrito lo muestra con claridad) se resuelven usando el manuscrito como fuente de verdad, sin necesidad de nota visible — el manuscrito es "el corazón" de la clase.
- **(A partir de v1.3)** Cuando un mismo ejercicio presenta enunciados distintos según la fuente (p. ej., la lista de ejercicios de las diapositivas frente a la resolución efectivamente trabajada en el manuscrito, o una tercera versión en el resumen de Zoom), se señala la discrepancia a Tigarto antes de redactar. Si un resumen de Zoom posterior aclara explícitamente el origen del error (p. ej., "el enunciado fue transcrito incorrectamente del libro fuente"), esa aclaración se toma como fuente de verdad para documentar lo ocurrido, sin necesidad de seguir preguntando.
- **(A partir de v1.3)** Si el propio manuscrito contiene una inconsistencia interna menor (p. ej., un paso de una demostración que cita el número de un paso anterior distinto al que lógicamente corresponde), se transcribe tal como aparece en la fuente y se señala con una nota aclaratoria breve (pie de tabla o comentario), en vez de corregirla silenciosamente — alterar el contenido de la fuente, aunque parezca un error menor, no es fidelidad.
- No inventar ni completar información faltante (ej. una fecha de examen "por definir" no debe convertirse en una fecha supuesta).
- **Código y ejemplos en "Contenido temático"**: cualquier fragmento de código, fórmula, ejemplo o demostración incluido en esta sección debe corresponder a algo efectivamente mostrado o trabajado en la sesión (según el manuscrito y/o el material de Zoom). No se generan ejemplos nuevos ni se completa código o pasos de demostración que no fueron mostrados en clase, aunque sea "lo esperable" para el tema.
- **(A partir de v1.4) Auditorías o revisiones hechas con otras herramientas de IA**: cuando Tigarto comparte un dictamen o una lista de "correcciones" generada por otro asistente de IA (Gemini, ChatGPT u otro) sobre un `README.md` ya redactado, cada corrección propuesta debe verificarse individualmente contra el manuscrito antes de aplicarse — nunca aplicarlas en bloque por venir de una auditoría. El patrón de falla observado es que estas herramientas evalúan el documento como si fuera un capítulo de libro de texto de la disciplina (p. ej. lógica de primer orden) y proponen reemplazar contenido transcrito fielmente del manuscrito o dicho literalmente por el profesor (terminología, ejemplos, fórmulas, simplificaciones) por una versión más rigurosa que nunca se dictó en clase. Esas correcciones se rechazan, citando la página o el resumen de Zoom donde consta la redacción original del profesor, aunque la corrección propuesta sea académicamente válida en abstracto — el criterio de este repositorio es la fidelidad a lo dictado, no la corrección formal frente a un estándar externo. Sí se aplican las correcciones que señalan errores de redacción propios (no del profesor) o inconsistencias genuinas entre secciones del propio `README.md`.
  - **(A partir de v1.5) Tercera vía — nota aclaratoria sin reescribir la fuente**: cuando el señalamiento de la auditoría es válido (p. ej. una inconsistencia real con otro concepto introducido en la misma clase, o una ambigüedad genuina que podría confundir a un estudiante) pero el contenido cuestionado es una cita fiel de lo mostrado o dicho por el profesor (diapositiva, manuscrito o material de Zoom), la corrección correcta no es reescribir la cita ni rechazar el señalamiento en bloque: se **preserva la cita textual** y se agrega junto a ella una nota aclaratoria breve (`[!NOTE]` o `[!TIP]`) que resuelve la ambigüedad sin alterar lo que efectivamente se dictó. Esta vía aplica especialmente cuando el propio material de Zoom registra que el profesor aclaró el punto en vivo (p. ej. respondiendo una pregunta de un estudiante); en ese caso la nota aclaratoria debe basarse en esa aclaración real y citada, no en una reformulación genérica propuesta por la herramienta auditora.
- Los pendientes de "Docente" y "Estudiantes" deben extraerse preferentemente del material de Zoom cuando este distingue explícitamente "siguientes pasos" por responsable (como ocurre en los resúmenes automáticos de Zoom); el apunte manuscrito rara vez hace esta distinción con la misma claridad. Los checkboxes reflejan el estado **a la fecha de la clase**, no un tracker sincronizado con la fecha de hoy — no se eliminan ni se marcan `[x]` pendientes vencidos sin una fuente que confirme que efectivamente se completaron.

---

## 4. Flujo de trabajo (fases)

**Fase 1 — Recepción de material**
Claude recibe el/los archivo(s) (PDF manuscrito, material(es) de Zoom, otros apuntes) y confirma qué insumos tiene disponibles para esa clase. No genera nada todavía — espera instrucción explícita de Tigarto para proceder.

**Fase 2 — Extracción y verificación**
Claude extrae la información relevante de cada fuente, aplicando las reglas de la Sección 3. Si detecta discrepancias relevantes entre fuentes, o secciones condicionales cuya pertinencia no es obvia, las señala antes de redactar.

**Fase 3 — Borrador**
Claude genera el `README.md` completo siguiendo la plantilla de la Sección 2, incluyendo solo las secciones condicionales que apliquen.

**Fase 4 — Revisión y ajuste**
Tigarto revisa y solicita ajustes de forma (tono, tablas vs. listas, reordenamiento) o de fondo (correcciones de datos). Los ajustes se aplican en rondas, no uno a uno sin confirmación previa cuando son varios.

**Fase 5 — Cierre**
Una vez aprobado, el archivo queda como definitivo para esa clase. Si en una clase posterior se anuncia un cambio a información ya publicada en un `README.md` anterior (ej. cambia el horario, se agrega un canal de comunicación), **no se edita retroactivamente el archivo antiguo** — el cambio se documenta en el `README.md` de la clase donde se anunció, manteniendo cada archivo como registro fiel de lo dicho en su momento. Esto también aplica a convenciones de formato adoptadas en una versión posterior del prompt maestro (p. ej. las anclas de navegación de v1.5): no es obligatorio retrofitarlas en clases ya finalizadas.

---

## 5. Convenciones de formato heredadas del curso

- Registro formal (*usted*) en cualquier prosa dirigida a estudiantes; el resumen y los objetivos pueden mantener un tono neutro/descriptivo en tercera persona.
- **Se refiere al docente como "el profesor"**, no por su nombre propio, en toda prosa dirigida a estudiantes (Resumen, Agenda, Contenido temático, y cualquier otra sección narrativa). Del mismo modo, los nombres propios de estudiantes que aparezcan en preguntas o comentarios registrados en el material de Zoom se anonimizan como "un estudiante" / "los estudiantes" en el README.
- Tablas en Markdown estándar (`|---|---|`), sin necesidad de LaTeX en este tipo de documento (a diferencia de `claseN.md` del sitio, este repositorio no contiene contenido matemático que requiera KaTeX/MathJax salvo fórmulas simples en texto plano dentro de "Contenido temático").
- Checkboxes de Markdown (`- [ ]`) para pendientes, permitiendo marcarlos como completados en commits posteriores.
- `[!TIP]` / `[!NOTE]` / `[!WARNING]` en formato nativo de GitHub (sin conversión a IAL) — este repositorio es Markdown plano leído directamente en GitHub, no pasa por Jekyll. La conversión a IAL solo aplica al sitio de apuntes teóricos (`discretas1-udea-20262`).
- **Estructura de archivos**: cada clase es un directorio `clase_0N/` que contiene `README.md` junto con sus materiales asociados (diapositivas PDF/PPTX, manuscrito anotado en PDF, imágenes/capturas usadas en "Contenido temático", y, cuando aplique, un archivo de corrección enviado aparte para un ejercicio puntual — p. ej. `correccion_ejemploN_annotated.pdf` — cuando el profesor rectifica un error después de la clase) como archivos hermanos en la misma ruta. Los enlaces dentro del `README.md` a estos materiales son rutas relativas simples (`./nombre_archivo.pdf`, `./nombre_imagen.png`), no rutas absolutas ni URLs externas. Un archivo de corrección se enlaza tanto en la metadata inicial (junto a los demás apuntes) como en el punto de "Contenido temático" donde se referencia el ejercicio corregido.
- **Bloques de código** en "Contenido temático" usan cercas con el lenguaje indicado (` ```python `) para resaltado de sintaxis en GitHub. Los diagramas en Mermaid (a partir de v1.4) usan la cerca ` ```mermaid ` bajo el mismo criterio.
- **(A partir de v1.5) Anclas de navegación en la Agenda**: ver Sección 2, "Reglas de estructura", bullet de Agenda.

---

## 6. Preguntas abiertas

*(Sin preguntas abiertas pendientes a la fecha de esta versión.)*
