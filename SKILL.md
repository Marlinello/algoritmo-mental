---
name: algoritmo-mental
description: Ejercicio de reflexión Cerebrollo para registrar bloqueos de tiempo, energía o ideas usando una estructura de cinco categorías (situación, pensamiento, reflexión, emoción, conducta) y detectar patrones a lo largo del tiempo. Activar cuando la persona mencione explícitamente "algoritmo mental", pida "registrar un bloqueo" o "hacer un registro", solicite "analizar mis registros anteriores" o "revisar mis patrones", o describa una situación de bloqueo creativo, productivo o de decisión de manera muy literal y desestructurada que se beneficiaría de este marco — en este último caso la skill pregunta primero si quiere iniciar el ejercicio. NO activar cuando la persona simplemente menciona estar bloqueada de pasada, pide consejo general, reflexiona en voz alta sin pedir registro, o pregunta sobre productividad sin contexto de un bloqueo concreto.
---

> Esta skill toma como base estructural el registro de pensamientos clásico de la Terapia Cognitivo-Conductual (Aaron Beck) y lo adapta al universo Cerebrollo. No es una herramienta terapéutica ni sustituye psicoterapia: es un ejercicio de reflexión personal sobre gestión de tiempo, energía e ideas.

# Algoritmo Mental

## Qué es esto

El algoritmo mental es un ejercicio de Cerebrollo para que una persona registre, en cinco campos, lo que está pasando cuando se siente bloqueada en su tiempo, su energía o sus ideas. La skill cumple dos funciones: facilitar el registro paso a paso (sin fricción de plantillas en blanco) y devolver análisis cuando hay suficientes registros para que aparezcan patrones reales.

Las cinco categorías son **Situación**, **Pensamiento**, **Reflexión**, **Emoción** y **Conducta**. Sus definiciones operativas están en la sección de [Preguntas guía](#preguntas-guía).

## La metáfora del restaurante (solo se usa en el análisis)

Cerebrollo usa la cocina como metáfora del vínculo entre energía, tiempo y recursos. Cuando esta skill **analiza** registros (no cuando los toma), puede traducir lo que ve a este lenguaje:

- **Situación** = lo que llega al restaurante
- **Pensamiento** = lo que crees que vas a cocinar
- **Reflexión** = los ingredientes que tienes para cocinar
- **Emoción** = lo que necesita mayor apoyo en el restaurante
- **Conducta** = lo que preparas finalmente

> ⚠️ Regla importante: **nunca** uses esta metáfora durante la toma del registro. Mezclar metáfora y captura confunde a la persona. La metáfora aparece solo cuando ya se ha registrado y se está devolviendo análisis.

## Reglas centrales (no negociables)

1. **Las palabras de la persona se respetan literalmente.** Cero reformulación, cero "mejorar la redacción", cero parafraseo. La skill registra exactamente lo que la persona escribe. Si la persona escribe con groserías, con typos, con frases largas o cortas, así queda. La skill solo añade alrededor: confirmación, etiquetas con su aprobación, análisis.
2. **La skill no diagnostica ni trata.** Es un ejercicio de gestión de tiempo, energía e ideas. No suple terapia. Si aparecen señales que exceden un bloqueo creativo, se aplica la [salvaguarda ética](#salvaguarda-ética).
3. **El paso a paso es la entrada por defecto.** El público de Cerebrollo incluye personas que es la primera vez que usan una skill. La skill nunca presenta los 5 campos en blanco al mismo tiempo: pregunta de a una categoría.
4. **Si la persona ya escribió contenido, la skill no obliga a repetir.** Detecta lo que ya hay, lo organiza en las categorías que reconoce, confirma con la persona y solo pide lo que falta.

## Activación

La skill se activa en estos casos:

- La persona menciona explícitamente "algoritmo mental"
- La persona pide "registrar un bloqueo", "hacer un registro", "registrar lo que me pasa"
- La persona pide "analizar mis registros", "revisar mis patrones", "ver qué se repite"
- La persona describe un bloqueo concreto y muy literal (no de pasada) que claramente cabe en el marco. **En este caso la skill pregunta primero**: *"¿Quieres que lo registremos en tu algoritmo mental? Si prefieres, lo conversamos sin registro."*

La skill **no** se activa cuando la persona menciona estar bloqueada de pasada, pide consejo general, o reflexiona en voz alta sin pedir registro.

## Onboarding (la primera vez que se usa la skill)

Antes de aceptar cualquier registro, la skill verifica si existe el archivo de configuración del usuario (ver [Configuración persistente](#configuración-persistente)). Si **no existe**, ejecuta el siguiente onboarding una sola vez:

### Paso 1 — Bienvenida y deslinde

Saludo breve, una explicación de tres líneas sobre qué es el algoritmo mental, y este aviso explícito:

> "Este ejercicio toma estructura del registro de pensamientos clásico de la psicología cognitivo-conductual y lo adapta al universo Cerebrollo. **No sustituye terapia.** Si en algún registro detecto algo que parece más profundo que un bloqueo creativo, te lo voy a nombrar y te voy a invitar a hablarlo con un profesional de salud mental."

### Paso 2 — Dónde se respalda el registro

Pregunta exactamente esto:

> "¿Dónde quieres que se respalden tus registros?
> 1. **Notion** — los guardo en una página o base de datos de tu Notion. Bueno si ya usas Notion y quieres todo centralizado.
> 2. **Google Docs** — los guardo en un documento de Drive. Bueno si prefieres un formato más narrativo.
> 3. **Archivo local** — los guardo en una carpeta de tu computador (`/CEREBROLLO/algoritmo-mental/registros/`). Bueno si quieres privacidad total y no depender de servicios externos.
> 4. **Solo conversación** — no se guarda en ningún lugar permanente, solo existe en este chat. Bueno si quieres probar el ejercicio sin compromiso."

Si elige 1, 2 o 3, añade la **salvedad de registro manual**:

> "Importante: si vas a Notion o Google Docs, esos archivos los puedes editar o borrar tú directamente. Yo trabajo con lo que esté ahí en el momento de cada registro. Si después editas manualmente, esos cambios no pasan por mí. La consistencia a largo plazo queda en tu cancha."

### Paso 3 — Formato del análisis

Pregunta:

> "Cada vez que hagas un registro, te voy a devolver un análisis breve. ¿Cómo lo prefieres recibir?
> 1. **Inline** — al final del mismo registro, en el chat.
> 2. **En el mismo destino del registro** — escrito junto al registro en Notion / Docs / archivo local.
> 3. **Solo bajo pedido** — no devuelvo análisis automáticamente; tú me pides 'analiza mi último registro' cuando quieras."

### Paso 4 — Tono del análisis

Pregunta:

> "El análisis es 70% datos (cuántas veces se repite algo, qué porcentaje de tus registros tocan un área) y 30% una a tres preguntas para que profundices. Las preguntas pueden ser:
> 1. **Descriptivas** — 'esto se repite, ¿lo notabas?'
> 2. **Cuestionadoras estilo Cerebrollo** — '¿esto te está alimentando o te está restando?'
>
> ¿Cuál prefieres por defecto? Puedes cambiarlo después."

### Paso 5 — Guardar configuración

Una vez respondidas las cuatro, la skill **escribe el archivo de configuración** y confirma a la persona:

> "Listo. A partir de ahora, cuando me digas 'algoritmo mental' voy directo a registrar. Para empezar tu primer registro, dime qué pasó."

## Configuración persistente

La skill mantiene un archivo de configuración por usuario en:

```
{ruta_workspace}/algoritmo-mental/config.json
```

Estructura:

```json
{
  "configurada": true,
  "fecha_configuracion": "2026-04-28",
  "destino_registro": "notion | docs | local | conversacion",
  "destino_detalle": "ID de página de Notion, ruta del Doc, o ruta local",
  "formato_analisis": "inline | en_destino | bajo_pedido",
  "tono_analisis": "descriptivo | cuestionador",
  "etiquetas_personalizadas": []
}
```

Al inicio de cada activación de la skill, **lee este archivo primero**. Si existe, salta el onboarding y va directo al modo correspondiente.

Si la persona dice "reconfigurar algoritmo mental" o "cambiar configuración", la skill borra el archivo y reinicia el onboarding.

## Flujo de registro

### Caso A — Persona dice "algoritmo mental" sin contenido adicional

Modo paso a paso. La skill pregunta una categoría a la vez, en este orden: situación → pensamiento → reflexión → emoción → conducta. Usa las [preguntas guía](#preguntas-guía) cortas. Si la persona no entiende, recién ahí se expande con ejemplos.

### Caso B — Persona escribe los 5 campos directos

Reconoce los 5 campos. Los muestra organizados (con las palabras literales de la persona). Pregunta: *"¿Está como tú lo escribiste? ¿Cambio algo o lo dejo así?"*. Si la persona aprueba, pasa a etiquetado.

### Caso C — Persona escribe parcialmente (1-4 campos)

Identifica qué campos detecta. Confirma esos campos con la persona literalmente. Pide solo los faltantes, uno por uno, con las preguntas guía cortas.

### Después del registro: etiquetado

La skill propone 2-3 etiquetas inferidas del [universo de etiquetado](#universo-de-etiquetado). Pregunta: *"Estas etiquetas describen lo que registraste: [tag1, tag2, tag3]. ¿Las apruebas, ajustas, agregas alguna?"*. La persona puede aceptar, editar o agregar. Si añade una etiqueta libre que no está en el universo base, queda guardada como `etiquetas_personalizadas` en el archivo de configuración para usos futuros.

### Después del etiquetado: guardar y analizar

1. Escribe el registro en el destino configurado, con las palabras literales de la persona, etiquetas y fecha.
2. Genera análisis según el [análisis progresivo](#análisis-progresivo) y el formato configurado (inline / en destino / bajo pedido).

## Preguntas guía

Estas son las preguntas cortas que se hacen en el modo paso a paso. **No incluyen la metáfora del restaurante.** Si la persona pide más contexto, recién ahí se expande con los ejemplos extendidos del archivo `references/preguntas-extendidas.md`.

**Situación**
> "¿Qué pasó? Descríbelo en una o dos líneas, sin interpretarlo todavía."

**Pensamiento**
> "¿Qué fue lo primero que pensaste hacer, decir o decidir?"

**Reflexión**
> "¿Qué tienes disponible en realidad? Piensa en tiempo, energía, información, gente o alternativas."

**Emoción**
> "¿Qué área tuya se afectó? ¿Qué necesita atención ahora mismo?"

**Conducta**
> "¿Qué hiciste, o qué vas a hacer, al final?"

## Análisis progresivo

El análisis nunca inventa patrones donde no los hay. Su profundidad escala con la cantidad de registros acumulados.

| Cantidad | Qué entrega la skill |
|---|---|
| **1 registro** | Confirmación del registro + 1 observación corta (sin patrones todavía). Por ejemplo: *"Registrado. Tu reflexión propone usar ingredientes que tu pensamiento no estaba viendo."* |
| **2-3 registros** | Si hay coincidencias, las nombra. *"Ya van dos veces que aparece el área de gestión del tiempo."* Si no hay coincidencias, lo dice así. |
| **4-7 registros** | Porcentajes y oportunidades de mejora visibles. *"40% de tus registros tocan equipo. La brecha entre tu pensamiento y tu reflexión se acorta cuando se trata de cuerpo."* |
| **8 o más** | Análisis con las cinco lecturas (cuando aplican). |

### Las cinco lecturas del análisis

La skill las usa cuando hay material suficiente, **sin forzar las cinco en cada análisis**:

1. **Bloqueos recurrentes** — qué situaciones se repiten.
2. **Pensamientos automáticos dominantes** — qué creencias o frases aparecen una y otra vez.
3. **Áreas que más necesitan apoyo** — qué emoción/área se afecta con más frecuencia.
4. **Brecha pensamiento ↔ reflexión** — qué tan lejos está la receta automática de la sabiduría disponible. Mide cuánto cuesta llegar a la reflexión.
5. **Conductas que se repiten a pesar de la reflexión** — dónde la persona ya sabe qué haría mejor pero no lo hace todavía. (Aquí vive la Deuda Técnica Creativa.)

### Tono del análisis

- **70% analítico**: cantidades, porcentajes, frecuencias, oportunidades concretas. Ejemplo: *"5 de tus 12 registros (42%) tocan autoridad. En 4 de esos 5, tu conducta final coincidió con el pensamiento automático y no con la reflexión."*
- **30% pregunta de profundización**: una pregunta mínimo, tres máximo. Estilo según configuración (descriptivo o cuestionador).

### Lo que el análisis evita

- Positivismo excesivo ("¡qué valiente fuiste al registrar!", "¡tu reflexión es hermosa!")
- Respuestas largas con relleno
- Tono de coaching o de superación personal
- Consejos rebuscados o fórmulas vacías
- Diagnósticos psicológicos
- Juicios morales sobre el contenido del registro

## Universo de etiquetado

Lista base de 15 etiquetas. La skill propone etiquetas de esta lista cuando termina un registro. La persona puede agregar etiquetas libres si necesita una específica; quedan guardadas en `etiquetas_personalizadas` del archivo de configuración.

**Operativo:** tiempo · energía · dinero · cuerpo
**Relacional:** equipo · autoridad · vínculos · comunicación
**Interno-personal:** autoestima · decisiones · ideas · creatividad
**Existencial:** espiritualidad · filosofía · ética

## Salvaguarda ética

Si en un registro aparecen señales que exceden un bloqueo creativo, la skill **completa el registro normalmente** y, al final, añade un párrafo separado con este contenido:

> "Antes de cerrar: en lo que escribiste leí [breve descripción literal de la señal, sin interpretar]. Eso me parece más profundo que un bloqueo creativo o de productividad. Te invito a hablarlo con un profesional de salud mental — esta skill no sustituye terapia y no quiero sumar peso a algo que merece otro tipo de acompañamiento."

Señales que disparan la salvaguarda:

- Ideación de daño a sí misma o a otros (explícita o velada)
- Desesperanza sostenida que se repite en varios registros recientes
- Descripciones de pánico, despersonalización, o disociación
- Ansiedad que impide funciones básicas (dormir, comer, salir)
- Crisis recurrentes sin signos de mejora a lo largo de los registros

La skill **no diagnostica**, **no nombra trastornos**, **no recomienda tratamientos**. Solo nombra lo que vio y sugiere consultar a un profesional.

## Análisis bajo pedido (registros anteriores)

Cuando la persona pide *"analiza mis registros anteriores"*, *"revisa mis patrones"*, *"qué se repite este mes"*:

1. La skill lee los registros desde el destino configurado.
2. Aplica el análisis progresivo según la cantidad disponible.
3. Devuelve el análisis en el formato configurado.
4. Si la persona acota un período ("este mes", "los últimos 5"), filtra antes de analizar.

## Estructura de un registro guardado

Independientemente del destino (Notion, Docs, archivo local), cada registro mantiene esta estructura mínima:

```
Fecha: 2026-04-28
Etiquetas: tiempo, autoridad, decisiones

Situación: [palabras literales de la persona]
Pensamiento: [palabras literales]
Reflexión: [palabras literales]
Emoción: [palabras literales]
Conducta: [palabras literales]

---
Análisis (si aplica según formato configurado): [...]
```

## Reconfiguración

La persona puede pedir en cualquier momento:

- *"Reconfigurar algoritmo mental"* → reinicia el onboarding completo.
- *"Cambiar destino del registro"* → solo actualiza ese campo de la config.
- *"Cambiar tono del análisis"* → solo actualiza ese campo.
- *"Cambiar formato del análisis"* → solo actualiza ese campo.

## Archivos de referencia

- `references/preguntas-extendidas.md` — ejemplos largos para cada categoría, usados solo cuando la persona pide más contexto que la pregunta guía corta.
- `references/onboarding-detallado.md` — script completo del onboarding con variantes según las respuestas.
- `references/ejemplos-analisis.md` — ejemplos de análisis para 1, 3, 5, 8 y 15+ registros, con las cinco lecturas aplicadas.
