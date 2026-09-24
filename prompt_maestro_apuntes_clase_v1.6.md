# Prompt Maestro — Apuntes de Clase (Repositorio `apuntes_clases`)

**Versión**: 1.6
**Curso**: Matemáticas Discretas 1 — Universidad de Antioquia — Ingeniería de Sistemas (Ude@)
**Propósito**: Generar el archivo `README.md` del directorio `clase_0N/` en el repositorio `apuntes_clases_20XX-X`, un resumen estructurado y navegable de cada sesión dictada, a partir del material producido en o para esa clase.

**Distinción respecto a otros prompts maestros del curso**: Este documento gobierna los **resúmenes de bitácora por clase** (repositorio `apuntes_clases`), no las notas teóricas de contenido (`claseN.md` del sitio GitHub Pages, gobernadas por `prompt_maestro_notas_clase_v4.md`) ni las autoevaluaciones (`prompt_maestro_autoevaluacion_discretas1_v4.md`). Un mismo número de clase puede tener ambos tipos de documento, con propósitos distintos: este es un registro operativo de lo ocurrido en la sesión (agenda, evaluación, pendientes), que **a partir de v1.2 también puede incorporar un resumen teórico expandido** de lo visto en clase; el sitio teórico sigue siendo el material de estudio canónico, completo y ejercitado.

> **Registro de cambios v1.5 → v1.6** (surgidos al redactar `clase-09`): se crea una categoría propia para los **errores conceptuales del profesor** cometidos en clase — distinta de las inconsistencias internas menores de v1.3 — que se documentan de forma explícita (transcripción fiel + advertencia "Error del profesor en clase" + versión corregida + moraleja), sin suavizarlos y sin usar un resumen de Zoom "correcto" como prueba de que el error no ocurrió. Se adopta la convención **"Aclaración del apunte"** para distinguir todo contenido agregado al redactar (aclaraciones, deducciones, esquemas, citas de fuentes) de lo efectivamente dicho en clase, y un criterio para limitar esas aclaraciones a lo conceptualmente importante para la clase documentada. Se cubre el caso inverso al de v1.5: una clase que **empieza sobre el manuscrito de la clase anterior**. Se precisa que "Contenido temático" también sigue el orden real de la clase (no se reordena en teoría-luego-ejercicios). Se incorporan elementos de **autocontenido** (tabla de notación, definiciones previas, bloques plegables, subsección final de síntesis con errores y dudas de la clase), la distinción entre **figuras de clase** y **esquemas del apunte** en Mermaid, reglas de desambiguación de numeración de ejemplos, restricciones técnicas de renderizado en GitHub, principios recurrentes del curso con redacción fija, y citación de fuentes de ejemplos adaptados. En el flujo de trabajo se formaliza la recepción iterativa del material de Zoom, una revisión opcional desde tres perspectivas en la Fase 4 y la actualización del cronograma raíz en la Fase 5.
>
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

1. **PDF de apuntes manuscritos** de la clase (obligatorio si existe). **(A partir de v1.6)** Si una sesión de la clase empezó sobre el manuscrito de la clase anterior (identificable por una marca "Fin: DD/MM → Inicio: DD/MM" dentro de ese manuscrito), las páginas correspondientes de ese manuscrito también son insumo de la clase actual (ver Sección 2, reglas de estructura).
2. **Material derivado de Zoom** (transcripción/resumen automático de la sesión, si la clase fue grabada). Si la clase se dictó en más de un día calendario, puede haber material de Zoom por cada sesión. **(A partir de v1.5)** Además, una misma sesión puede tener **más de un artefacto derivado de Zoom** con distinto nivel de detalle — típicamente un **resumen narrativo** (útil para tono de la sesión, preguntas de estudiantes y pendientes por responsable) y unas **notas o "contenido general"** más granulares, con citas textuales y trazabilidad por bloque temático (útil para precisar redacción exacta, cifras y ejemplos). Ambos se tratan en conjunto como fuente secundaria frente al manuscrito, y se cruzan entre sí para verificar consistencia antes de usarlos. Cuando hay varios documentos (por sesión o por nivel de detalle), estos pueden cruzarse entre sí y con el manuscrito para resolver dudas sobre el enunciado real de un ejercicio, especialmente cuando una sesión posterior aclara explícitamente un error cometido o detectado en una sesión anterior (ver Sección 3).
3. **Apuntes adicionales** en cualquier formato (notas sueltas, capturas de pantalla, diagramas, fragmentos de código trabajados en clase, mensajes de foro relacionados, etc.), incluyendo archivos de corrección enviados aparte cuando el profesor rectifica un error después de dictada la clase (ver Sección 5).

Claude debe recibir estos insumos y **esperar instrucciones explícitas** antes de generar el archivo, salvo que Tigarto indique lo contrario (ver Fase 1).

**(A partir de v1.6)** Tigarto, quien entrega los insumos, es el profesor titular del curso: los manuscritos anotados son suyos. En la prosa del `README.md` se le sigue llamando "el profesor" (ver Sección 5).

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
referencia complementaria para profundizar y ejercitar.

A partir de v1.6, la sección abre con una nota "Cómo leer este apunte" y
una tabla de notación, y cierra con una subsección "### Síntesis de la
clase" (ideas clave + recuadro de errores y dudas de la clase).]

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
  - **(A partir de v1.6) Clase que empieza sobre el manuscrito de la clase anterior**: es el caso inverso al anterior. Si una sesión de la clase actual se dictó sobre las últimas páginas del manuscrito de la clase previa (p. ej., ejercicios que quedaron pendientes, identificables por una marca "Fin: DD/MM → Inicio: DD/MM" dentro de ese manuscrito), ese contenido **sí** se incluye en la Agenda y en "Contenido temático" de la clase actual, porque se dictó en ella. El manuscrito anterior se enlaza en la metadata inicial con el rango de páginas (p. ej. `[Manuscrito anotado de la clase 8, págs. 48–58](../clase-08/apuntes_clase8_annotated.pdf)`), y sus ejercicios se rotulan con la clase de origen (`Ejemplo N (clase 8)`) para no confundirlos con la numeración propia. El `README.md` de la clase anterior, ya finalizado, no se modifica (ver Fase 5).
  - **(A partir de v1.5) Navegación por anclas**: cada ítem de la Agenda que referencia otra sección del documento (`(→ sección N)`, `(→ Evaluación)`, etc.) se expresa como un enlace ancla de Markdown al encabezado correspondiente, p. ej. `[*(→ sección 1)*](#1-tema)`, usando el slug que GitHub genera automáticamente a partir del texto del encabezado (minúsculas, espacios y puntuación reemplazados por guiones, tildes conservadas). Esto facilita el repaso en documentos largos. Esta convención aplica desde su adopción en adelante; no es obligatorio aplicarla retroactivamente a clases ya finalizadas (ver Fase 5).
- **Contenido temático** (a partir de v1.2) es un **resumen teórico expandido**, no solo un enlace de salida:
  - Se organiza en subtítulos numerados (`### 1. [Tema]`, `### 2. [Tema]`, ...) que reflejan los temas efectivamente cubiertos.
  - **(A partir de v1.6) Orden cronológico**: los subtítulos siguen el **orden real en que se dictó la clase**, igual que la Agenda. No se reordenan con un criterio de libro de texto (p. ej. "teoría primero, ejercicios después"), aunque parezca más pedagógico: hacerlo cuenta una clase distinta a la que ocurrió. Si un ejercicio usa un concepto que se repasa más adelante en el mismo documento (porque ya se conocía de una clase previa), se resuelve con una línea de referencia cruzada ("formas vistas en la clase 8; se repasan en la sección 3"), no reordenando.
  - **(A partir de v1.6) Autocontenido**: el apunte debe poder leerse sin el manuscrito al lado. Para ello:
    - Al inicio de la sección, una nota **"Cómo leer este apunte"** (orden cronológico, origen de los ejercicios si hay más de un manuscrito, convención "Aclaración del apunte") y una **tabla de notación** con los símbolos que se usan, en especial los nuevos o los que se confunden fácilmente (p. ej. `≡` frente a `→`: el primero es una afirmación *sobre* dos fórmulas, el segundo un conectivo *dentro* de una fórmula).
    - Todo término técnico se define antes de usarse o se enlaza a donde se define (en el mismo documento o en el `README.md` de una clase anterior).
    - Las tablas largas de referencia que la clase usó pero no desarrolló (p. ej. la tabla completa de equivalencias proposicionales) pueden incluirse en un bloque plegable `<details><summary>…</summary> … </details>`, que mantiene el documento autocontenido sin alargarlo visualmente (dejar líneas en blanco dentro del bloque para que el Markdown se renderice).
    - Al final de la sección, una subsección **`### Síntesis de la clase`** (sin número, fuera de la numeración de temas) con 4–5 ideas clave enlazadas a su sección, **sin contenido nuevo**, seguida de un recuadro **"Errores y dudas de esta clase"** que recoja solo lo que efectivamente ocurrió o se preguntó en la sesión (errores en clase, dudas de estudiantes, advertencias del profesor), indicando el origen de cada ítem.
  - **(A partir de v1.6) Numeración de ejemplos**: cuando dos numeraciones chocan dentro del mismo documento (p. ej. la batería de la clase anterior y la de la actual, o ejemplos internos de una diapositiva teórica), se desambiguan rotulando por clase (`Ejemplo 4 (clase 8)`) o por contenido (`Ejemplo de Bart y Milhouse`, `Ejemplo 5 de los cachivaches`), también en las referencias cruzadas.
  - Puede incluir explicaciones de conceptos, diagramas o capturas (como archivos hermanos en `clase_0N/`, referenciados con ruta relativa `./nombre_imagen.png`), fórmulas, y fragmentos de código **efectivamente trabajados en la sesión** (no ejemplos inventados ni generalizaciones del tema).
  - **(A partir de v1.4)** Un diagrama también puede expresarse como bloque Mermaid (` ```mermaid `), que GitHub renderiza de forma nativa sin necesidad de generar ni almacenar un archivo de imagen — es la opción preferida cuando el diagrama visualiza una relación conceptual entre términos que la propia clase ya definió (p. ej. una jerarquía entre conceptos), no cuando introduce información nueva. Las capturas del manuscrito, en cambio, se reservan para cuando el contenido visual (una tabla con anotaciones a mano, un ejemplo con imágenes propias del profesor) no se pueda reproducir fielmente como texto o tabla de Markdown — no se agregan solo para "enriquecer" visualmente una sección cuyo contenido ya está bien cubierto en prosa/tabla.
  - **(A partir de v1.6) Figuras de clase frente a esquemas del apunte**: un diagrama Mermaid puede ser (a) una **figura de clase**, que reproduce algo efectivamente mostrado o dibujado en la sesión (p. ej. el grafo de una figura de la diapositiva, o un diagrama de decisión que el profesor trazó a mano), y se presenta citando la página del manuscrito; o (b) un **esquema del apunte**, una síntesis propia de pasos o relaciones que sí se usaron en clase pero que el profesor no dibujó como tal (p. ej. un flujo del procedimiento para negar), que se rotula explícitamente como *Esquema del apunte*. Nunca se presenta un esquema propio como si fuera material de clase. Si un diagrama requiere un paso o una relación que no se mostró en clase, no se incluye.
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
- **(A partir de v1.6) Errores conceptuales del profesor en clase**: distinto de la inconsistencia interna menor del punto anterior (un número de paso mal citado), un **error conceptual** es una respuesta o traducción incorrecta que el estudiante vio en el manuscrito y en la grabación (p. ej. una traducción al lenguaje formal que cambia el sentido del enunciado). Cuando Tigarto confirma que se trata de un error, se documenta así:
  1. Se transcribe la versión del manuscrito **tal cual**, rotulada "(transcripción del manuscrito)".
  2. Inmediatamente después, un `[!WARNING]` que empieza con **"Error del profesor en clase."** y explica, en términos de **sentido** (qué dice la fórmula frente a qué dice el enunciado) y no solo de forma, por qué es incorrecta, y muestra la **versión corregida**. Si en el propio material de clase hay un ejemplo correcto con la misma estructura, se cita como apoyo.
  3. Un `[!TIP]` con la **moraleja**: la lección que el error deja para estudiantes y profesor. Si hay varios errores relacionados, una sola moraleja los cubre.
  4. El error se incluye también en el recuadro "Errores y dudas de esta clase" de la síntesis final.

  No se suaviza la redacción (p. ej. "se anotó de forma distinta a como se explicó"): el objetivo es que el error sea un momento de aprendizaje. Que un resumen de Zoom registre la versión correcta **no prueba** que el error no ocurrió: los estudiantes repasan con el video, donde el tablero muestra el error, y la IA que genera los resúmenes de Zoom puede "corregir" lo que resume.
- **(A partir de v1.6) Convención "Aclaración del apunte"**: todo contenido que no fue dicho ni mostrado en clase, pero que se agrega al redactar para dar claridad (una deducción directa de los datos de un ejercicio que el manuscrito deja sin resolver, una observación que conecta dos conceptos de la clase, un esquema, la cita de la fuente de un ejemplo adaptado, una lectura correcta de una paráfrasis ambigua), se rotula **"Aclaración del apunte"**: como párrafo que empieza con *Aclaración del apunte:* en cursiva, o como recuadro cuando conviene destacarlo. Los recuadros que relatan una pregunta de un estudiante y la respuesta del profesor quedan reservados para lo que efectivamente ocurrió en la sesión. Así el estudiante siempre puede distinguir qué dijo el profesor y qué agregó el apunte. Cuando se conozca la fuente de un ejemplo adaptado (p. ej. un libro de texto), se cita con esta misma convención.
- **(A partir de v1.6) Límite de las aclaraciones**: una aclaración del apunte solo se agrega si es **conceptualmente importante para la clase documentada**. No se abre un tema que la clase no trabajó, aunque un diagrama o una tabla lo dejen a la vista (p. ej. una discrepancia entre una figura y los enunciados de un ejemplo de repaso): en ese caso basta una línea neutra que evite la confusión, sin desarrollar el tema. Si la aclaración toca una decisión sobre el material (p. ej. cuál de dos versiones prevalece), se consulta a Tigarto antes de escribirla.
- **Código y ejemplos en "Contenido temático"**: cualquier fragmento de código, fórmula, ejemplo o demostración incluido en esta sección debe corresponder a algo efectivamente mostrado o trabajado en la sesión (según el manuscrito y/o el material de Zoom). No se generan ejemplos nuevos ni se completa código o pasos de demostración que no fueron mostrados en clase, aunque sea "lo esperable" para el tema.
- **(A partir de v1.4) Auditorías o revisiones hechas con otras herramientas de IA**: cuando Tigarto comparte un dictamen o una lista de "correcciones" generada por otro asistente de IA (Gemini, ChatGPT u otro) sobre un `README.md` ya redactado, cada corrección propuesta debe verificarse individualmente contra el manuscrito antes de aplicarse — nunca aplicarlas en bloque por venir de una auditoría. El patrón de falla observado es que estas herramientas evalúan el documento como si fuera un capítulo de libro de texto de la disciplina (p. ej. lógica de primer orden) y proponen reemplazar contenido transcrito fielmente del manuscrito o dicho literalmente por el profesor (terminología, ejemplos, fórmulas, simplificaciones) por una versión más rigurosa que nunca se dictó en clase. Esas correcciones se rechazan, citando la página o el resumen de Zoom donde consta la redacción original del profesor, aunque la corrección propuesta sea académicamente válida en abstracto — el criterio de este repositorio es la fidelidad a lo dictado, no la corrección formal frente a un estándar externo. Sí se aplican las correcciones que señalan errores de redacción propios (no del profesor) o inconsistencias genuinas entre secciones del propio `README.md`.
  - **(A partir de v1.5) Tercera vía — nota aclaratoria sin reescribir la fuente**: cuando el señalamiento de la auditoría es válido (p. ej. una inconsistencia real con otro concepto introducido en la misma clase, o una ambigüedad genuina que podría confundir a un estudiante) pero el contenido cuestionado es una cita fiel de lo mostrado o dicho por el profesor (diapositiva, manuscrito o material de Zoom), la corrección correcta no es reescribir la cita ni rechazar el señalamiento en bloque: se **preserva la cita textual** y se agrega junto a ella una nota aclaratoria breve (`[!NOTE]` o `[!TIP]`) que resuelve la ambigüedad sin alterar lo que efectivamente se dictó. Esta vía aplica especialmente cuando el propio material de Zoom registra que el profesor aclaró el punto en vivo (p. ej. respondiendo una pregunta de un estudiante); en ese caso la nota aclaratoria debe basarse en esa aclaración real y citada, no en una reformulación genérica propuesta por la herramienta auditora.
- Los pendientes de "Docente" y "Estudiantes" deben extraerse preferentemente del material de Zoom cuando este distingue explícitamente "siguientes pasos" por responsable (como ocurre en los resúmenes automáticos de Zoom); el apunte manuscrito rara vez hace esta distinción con la misma claridad. Los checkboxes reflejan el estado **a la fecha de la clase**, no un tracker sincronizado con la fecha de hoy — no se eliminan ni se marcan `[x]` pendientes vencidos sin una fuente que confirme que efectivamente se completaron.

---

## 4. Flujo de trabajo (fases)

**Fase 1 — Recepción de material**
Claude recibe el/los archivo(s) (PDF manuscrito, material(es) de Zoom, otros apuntes) y confirma qué insumos tiene disponibles para esa clase. No genera nada todavía — espera instrucción explícita de Tigarto para proceder.

**(A partir de v1.6)** El primer paso es entregar un checklist de insumos disponibles y faltantes (incluyendo las fechas de sesión detectadas en el manuscrito). Luego, Tigarto suele entregar el material de Zoom **de a uno**: con cada material, Claude confirma que lo recibió, identifica a qué sesión corresponde y de qué tipo es (resumen narrativo o notas/"contenido general"), anota brevemente lo relevante y pide el siguiente, hasta que Tigarto indique explícitamente que no hay más. La fecha que trae un material de Zoom puede estar corrida un día (p. ej. por zona horaria); la sesión se identifica por su contenido cruzado con el manuscrito.

**Fase 2 — Extracción y verificación**
Claude extrae la información relevante de cada fuente, aplicando las reglas de la Sección 3. Si detecta discrepancias relevantes entre fuentes, o secciones condicionales cuya pertinencia no es obvia, las señala antes de redactar.

**Fase 3 — Borrador**
Claude genera el `README.md` completo siguiendo la plantilla de la Sección 2, incluyendo solo las secciones condicionales que apliquen.

**Fase 4 — Revisión y ajuste**
Tigarto revisa y solicita ajustes de forma (tono, tablas vs. listas, reordenamiento) o de fondo (correcciones de datos). Los ajustes se aplican en rondas, no uno a uno sin confirmación previa cuando son varios.

**(A partir de v1.6) Revisión desde tres perspectivas (opcional)**: a pedido de Tigarto, Claude revisa el borrador como (1) **estudiante de primer semestre** (¿se entiende?, ¿qué confunde?, ¿qué repasaría para el parcial?), (2) **profesor titular** (¿es fiel a lo dictado?, ¿hay datos por confirmar?, ¿se puede publicar?) y (3) **editor académico de textos universitarios de matemáticas** (autocontenido, términos definidos antes de usarse, notación, estructura, diagramas), con una nota de 0 a 100 por perspectiva y una lista priorizada de ajustes. Las propuestas del editor que choquen con la fidelidad (reordenar el contenido, agregar rigor formal no dictado, pasar a LaTeX) se descartan explícitamente, con el mismo criterio de la Sección 3 para las auditorías de otras herramientas de IA.

**Fase 5 — Cierre**
Una vez aprobado, el archivo queda como definitivo para esa clase. Si en una clase posterior se anuncia un cambio a información ya publicada en un `README.md` anterior (ej. cambia el horario, se agrega un canal de comunicación), **no se edita retroactivamente el archivo antiguo** — el cambio se documenta en el `README.md` de la clase donde se anunció, manteniendo cada archivo como registro fiel de lo dicho en su momento. Esto también aplica a convenciones de formato adoptadas en una versión posterior del prompt maestro (p. ej. las anclas de navegación de v1.5): no es obligatorio retrofitarlas en clases ya finalizadas.

**(A partir de v1.6) Actualización del cronograma raíz**: al finalizar una clase se agregan sus filas a la tabla visible del `README.md` raíz (una fila por sesión). La semana, el número de clase, la fecha y el título ("Lógica cuantificacional - Parte N", etc.) se toman de las filas planeadas del bloque comentado (`<!-- ... -->`); la semana se escribe solo en la primera fila de cada semana. Las columnas "Notas de clase", "Contenido" y "Observaciones" siguen el formato de las filas visibles ya existentes (`Recursos [[link]](clase-0N/) Manuscrito [[pdf]](...)`, texto de repaso con enlaces `[[link]]` / `[[autoevaluacion]]` al sitio teórico), y el "Contenido" refleja **lo que efectivamente se vio**, no lo planeado (si un tema se aplazó, no aparece). Solo se enlaza el manuscrito de la clase actual, aunque una sesión haya empezado sobre el de la anterior (el `README.md` de la clase ya lo documenta). El bloque comentado, que es el plan original, no se edita.

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
- **(A partir de v1.6) Principios recurrentes del curso**: algunos principios pedagógicos se repiten a propósito, clase tras clase, con **redacción fija** para que el estudiante los reconozca e interiorice. P. ej.: *"Las formas aristotélicas son una guía, no una receta exhaustiva para todo el lenguaje natural."* Se repiten solo donde un ejemplo real de la clase los ilustra, nunca como coletilla.
- **(A partir de v1.6) Restricciones de renderizado en GitHub**:
  - Los recuadros `[!NOTE]`, `[!TIP]`, `[!WARNING]`, etc. no se renderizan dentro de ítems de lista: van fuera de la lista (la numeración siguiente se retoma escribiendo el número explícito).
  - Debe haber una línea en blanco entre un recuadro y la lista o el párrafo que le sigue; si no, esa línea queda absorbida dentro del recuadro.
  - Los bloques Mermaid van fuera de listas.
  - Una barra vertical `|` dentro de código en una celda de tabla se escribe `\|` (p. ej. `` `U = {x \| x es una persona}` ``).
  - Los recuadros se reservan para lo que conviene destacar (errores, moralejas, preguntas de clase, advertencias); el resto de aclaraciones va en párrafos, para evitar la saturación de recuadros.

---

## 6. Preguntas abiertas

*(Sin preguntas abiertas pendientes a la fecha de esta versión.)*
