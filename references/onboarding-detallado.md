# Onboarding detallado

Este archivo amplía la sección "Onboarding" del SKILL.md con el script completo y las variantes según cómo responda la persona. Úsalo solo cuando la persona dispara la skill por primera vez (no existe `config.json`).

Una vez ejecutado, escribe `config.json` y nunca vuelvas a correr este onboarding hasta que la persona pida "reconfigurar algoritmo mental".

---

## Antes de empezar

Verifica si existe `{ruta_workspace}/algoritmo-mental/config.json`.

- **Existe** → salta este archivo, ve directo al modo correspondiente.
- **No existe** → ejecuta este script.

Si la persona expresa molestia con el onboarding ("¿no podemos empezar ya?", "esto es mucho"), reconócelo y abrevía:

> "Tienes razón, son 4 preguntas rápidas que después no se vuelven a hacer. Te las paso seguidas y elegimos defaults razonables si dudas. ¿Vamos?"

---

## Paso 1 — Bienvenida y deslinde

**Versión por defecto:**

> "Hola. Antes de empezar tu primer registro te explico brevemente qué es esto y te hago 4 preguntas rápidas para configurarlo a tu modo. No volveremos a hacer estas preguntas a menos que tú lo pidas.
>
> El algoritmo mental es un ejercicio de Cerebrollo para registrar bloqueos de tiempo, energía o ideas. Cada registro tiene cinco partes: situación, pensamiento, reflexión, emoción y conducta. Con varios registros acumulados puedes ver patrones que de otro modo quedan invisibles.
>
> Importante: este ejercicio toma estructura del registro de pensamientos clásico de la psicología cognitivo-conductual y lo adapta al universo Cerebrollo. **No sustituye terapia.** Si en algún registro detecto algo que parece más profundo que un bloqueo creativo, te lo voy a nombrar y te voy a invitar a hablarlo con un profesional de salud mental.
>
> ¿Vamos con las 4 preguntas?"

**Variantes según respuesta:**

- *"Sí" / "Vamos" / cualquier afirmación:* pasa al Paso 2.
- *"¿Qué pasa si no quiero responder ahora?":* "Puedes saltar el onboarding y registrar de una vez en modo conversación, sin guardar nada. Cuando quieras configurar real, dime 'configurar algoritmo mental'." → Si acepta, ve a [Modo conversación express](#modo-conversación-express).
- *"¿Qué pasa si tengo crisis ahora?":* aplica directamente la salvaguarda ética del SKILL.md y nombra recursos de salud mental locales si los conoces o invita a buscarlos. **No** sigas con el onboarding.

---

## Paso 2 — Dónde se respalda el registro

> "¿Dónde quieres que se respalden tus registros?
>
> 1. **Notion** — los guardo en una página o base de datos de tu Notion. Bueno si ya usas Notion y quieres todo centralizado.
> 2. **Google Docs** — los guardo en un documento de Drive. Bueno si prefieres un formato más narrativo.
> 3. **Archivo local** — los guardo en una carpeta de tu computador (`/algoritmo-mental/registros/`). Bueno si quieres privacidad total y no depender de servicios externos.
> 4. **Solo conversación** — no se guarda en ningún lugar permanente, solo existe en este chat. Bueno si quieres probar el ejercicio sin compromiso."

**Variantes según respuesta:**

### Si elige Notion (1)

> "Perfecto. ¿Tienes ya una página o base de datos de Notion específica donde quieres guardarlos, o quieres que cree una nueva?"

- *Tiene una existente:* pídele el URL o ID. Confirma acceso (lectura y escritura). Si no tienes acceso, dile cómo darte permiso (compartir la página con la integración de Claude).
- *Quiere una nueva:* sugiere crear una base de datos con propiedades coherentes con el SKILL.md (Resumen, Fecha, 5 categorías, Etiquetas multi-select, Notas). Marlinello tiene una plantilla pública en su Notion — puedes ofrecer duplicarla si la persona lo prefiere.

**Salvedad obligatoria:**

> "Importante: como vas a guardar en Notion, tú puedes editar o borrar esos registros directamente desde Notion. Yo trabajo con lo que esté ahí en el momento de cada análisis. Si después editas manualmente, esos cambios no pasan por mí. La consistencia a largo plazo queda en tu cancha."

### Si elige Google Docs (2)

> "Perfecto. ¿Tienes ya un documento donde quieres guardarlos o creo uno nuevo?"

- *Tiene uno existente:* pide el URL. Confirma acceso.
- *Quiere uno nuevo:* crea un Doc llamado "Algoritmo Mental — Registros" en una carpeta razonable.

**Salvedad obligatoria** (igual que la de Notion adaptada): la persona puede editar el Doc manualmente y esos cambios no pasan por la skill.

### Si elige Archivo local (3)

> "Perfecto. Voy a guardar los registros en `{ruta_workspace}/algoritmo-mental/registros/`. Cada registro será un archivo Markdown con fecha. Privacidad total, no salen de tu computador."

No necesita salvedad sobre edición manual porque la ruta es controlada por la skill, pero menciona:

> "Si mueves o borras los archivos manualmente, el análisis perderá visibilidad de esos registros."

### Si elige Solo conversación (4)

> "Perfecto. No voy a guardar nada en ningún lugar permanente. Cada registro existe solo en nuestra conversación actual. Si cambias de chat, se pierde. Bueno para probar, no para construir patrones a largo plazo."

Marca en `config.json`: `"destino_registro": "conversacion"`.

---

## Paso 3 — Formato del análisis

> "Cada vez que hagas un registro, te voy a devolver un análisis breve. ¿Cómo lo prefieres recibir?
>
> 1. **Inline** — al final del mismo registro, en el chat. Lo lees acá mismo y sigues con tu día.
> 2. **En el mismo destino del registro** — escrito junto al registro en {Notion / Docs / archivo local, según paso 2}. Bueno si quieres que el análisis quede archivado con el registro.
> 3. **Solo bajo pedido** — no devuelvo análisis automáticamente; tú me pides 'analiza mi último registro' o 'revisa mis patrones' cuando quieras."

**Si en el paso 2 eligió "solo conversación":** la opción 2 no aplica, ofrécele solo 1 o 3.

**Variantes:**

- Persona pregunta cuál recomiendo: "Para empezar suelo recomendar inline, porque te da feedback inmediato y aprendes el ejercicio más rápido. Después puedes cambiarlo. ¿Vamos con esa?"

---

## Paso 4 — Tono del análisis

> "El análisis es 70% datos (cuántas veces se repite algo, qué porcentaje de tus registros tocan un área) y 30% una a tres preguntas para que profundices. Las preguntas pueden ser:
>
> 1. **Descriptivas** — 'esto se repite, ¿lo notabas?'. Tono observacional, te muestro lo que veo y te pregunto si lo registrabas.
> 2. **Cuestionadoras estilo Cerebrollo** — '¿esto te está alimentando o te está restando?'. Tono más directo, las preguntas te empujan a tomar postura.
>
> ¿Cuál prefieres por defecto? Puedes cambiarlo después."

**Variantes:**

- Persona pide ejemplos de cada uno: dale uno corto de cada estilo aplicado a un caso ficticio.
- Persona dice "los dos" o "depende": ofrece "descriptivas por defecto y yo cambio a cuestionadoras cuando vea brecha pensamiento↔reflexión grande, ¿te sirve?".

---

## Paso 5 — Guardar configuración y confirmar

Escribe `config.json` con todas las respuestas. Confirma:

> "Listo. Configuración guardada. Para empezar tu primer registro, dime qué pasó. Si en algún momento quieres cambiar algo, dime 'reconfigurar algoritmo mental' (cambia todo) o 'cambiar [destino/formato/tono]' (cambia solo eso)."

Pasa directo al Caso A del flujo de registro (Situación primero).

---

## Modo conversación express

Si la persona pidió saltar el onboarding completo, no escribas `config.json`. Trata cada registro como modo conversación: paso a paso, palabras literales, sin guardar nada permanente. Al final del primer registro, ofrece:

> "Si quieres que esto quede guardado para ver patrones después, dime 'configurar algoritmo mental' y hacemos los 4 pasos en menos de 2 minutos."

---

## Reconfiguración

Si la persona dice "reconfigurar algoritmo mental":

> "Voy a borrar tu configuración actual y empezamos de cero las 4 preguntas. ¿Confirmas?"

Si confirma, borra `config.json` y vuelve al Paso 1.

Si dice "cambiar destino" / "cambiar formato" / "cambiar tono", solo actualiza ese campo del `config.json` con la pregunta correspondiente del paso 2/3/4. No vuelvas a correr el resto del onboarding.

---

## Errores comunes durante el onboarding

- **Persona se sale a media configuración:** guarda lo que ya respondió como respuestas parciales. La próxima vez que se active la skill, retoma desde el paso pendiente: "Te quedaba una pregunta del onboarding, ¿la terminamos?".
- **Persona pide registrar antes de configurar:** ofrece el modo conversación express. No fuerces el onboarding.
- **Persona elige Notion/Docs pero no tiene cuenta o conexión:** ofrece archivo local como alternativa: "Puedo guardar localmente mientras conectas tu Notion. ¿Te sirve?".
