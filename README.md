# Algoritmo Mental

Skill de Claude para registrar bloqueos de tiempo, energía o ideas usando una estructura de cinco categorías y detectar patrones a lo largo del tiempo.

> Esta skill toma como base estructural el registro de pensamientos clásico de la **Terapia Cognitivo-Conductual** (Aaron Beck) y lo adapta al universo Cerebrollo. **No es una herramienta terapéutica ni sustituye psicoterapia.** Es un ejercicio de reflexión personal sobre gestión de tiempo, energía e ideas.

---

## Qué hace

Cuando le dices a Claude "algoritmo mental" o "quiero registrar un bloqueo", la skill se activa y:

1. **Te guía paso a paso** por las cinco categorías: situación, pensamiento, reflexión, emoción, conducta.
2. **Respeta tus palabras literales** — cero parafraseo, cero "mejorar la redacción".
3. **Te propone 2-3 etiquetas** de un universo de 15 (operativo, relacional, interno-personal, existencial).
4. **Guarda el registro** donde tú elijas: Notion, Google Docs, archivo local o solo conversación.
5. **Te devuelve análisis** que escala con la cantidad de registros: a partir de 8, aplica las cinco lecturas (bloqueos recurrentes, pensamientos automáticos, áreas que necesitan apoyo, brecha pensamiento↔reflexión, deuda técnica creativa).

---

## A quién está pensada

- Personas creativas, emprendedoras, dueñas de negocios de servicios.
- Quien tiene pendiente eso de "registrar más" pero la fricción de la página en blanco la frena.
- Quien quiere ver patrones reales en sus bloqueos sin tener que releer todo lo que escribió.

No es para crisis de salud mental. Si estás en crisis, busca a un profesional — la skill incluye una salvaguarda ética que te lo va a recordar si aparecen señales que exceden un bloqueo creativo, pero no espera a eso para que lo sepas.

---

## Instalación

Esta skill funciona en tres lugares distintos:

- **Claude.ai web, escritorio o app móvil** (planes Free, Pro y Max).
- **Claude Cowork** (escritorio para no-developers).
- **Claude Code** (CLI para developers).

Identifica cuál estás usando y sigue solo la sección que corresponde.

### Antes de empezar — descarga el archivo

Sea cual sea tu caso, vas a necesitar el archivo `.skill`:

1. Entra a la pestaña **Releases** de este repositorio (lateral derecho de la página).
2. Baja al último release y descarga `algoritmo-mental.skill`.
3. Guárdalo en una carpeta que recuerdes (por ejemplo, Descargas).

> Alternativa para developers: `git clone https://github.com/Marlinello/algoritmo-mental.git`.

---

### Caso 1 — Claude.ai (Free, Pro, Max) en web, escritorio o móvil

Esta es la ruta más simple. Funciona igual en plan Free que en Pro o Max.

**Paso 1 — Activa code execution**

Las skills necesitan que esté habilitado el code execution de Claude.

1. Abre Claude.ai e inicia sesión.
2. Click en tu nombre/avatar (esquina inferior izquierda) → **Settings**.
3. Ve a **Capabilities**.
4. Activa **Code execution and file creation**.

Si ya lo tenías activo, sigue al paso 2.

**Paso 2 — Sube la skill**

1. En Claude.ai, ve a **Settings → Customize → Skills**.
2. Click en **Upload skill**.
3. Selecciona el archivo `algoritmo-mental.skill` que descargaste.
4. Espera a que aparezca en la lista de skills disponibles.

**Paso 3 — Pruébala**

1. Abre una **conversación nueva** (no una existente).
2. Escribe: *"Activa la skill algoritmo-mental"* o directamente *"algoritmo mental"*.
3. Si funciona, Claude inicia el onboarding (4 preguntas rápidas, una sola vez).

Si Claude dice que no encuentra la skill, vuelve a Settings → Customize → Skills y verifica que esté listada y activa.

---

### Caso 2 — Claude Cowork

Cowork no tiene interfaz de upload todavía: las skills se instalan moviendo la carpeta al directorio correcto. Es un poco más manual.

**Paso 1 — Encuentra la carpeta de skills de Cowork**

Cowork guarda las skills en una ruta como esta (Windows):

```
C:\Users\[TU-USUARIO]\AppData\Roaming\Claude\local-agent-mode-sessions\skills-plugin\[ID-LARGO-1]\[ID-LARGO-2]\skills\
```

Para llegar:

1. Abre el Explorador de archivos.
2. Pega esto en la barra de direcciones y presiona Enter: `%APPDATA%\Claude\local-agent-mode-sessions\skills-plugin`
3. Vas a ver una o dos carpetas con nombres largos (IDs). Entra en cada una hasta llegar a una que tenga una carpeta `skills` adentro.
4. Esa es la carpeta donde van las skills.

> En Mac la ruta equivalente es `~/Library/Application Support/Claude/local-agent-mode-sessions/skills-plugin/`. El resto del flujo es igual.

**Paso 2 — Copia la carpeta `algoritmo-mental`**

Tienes dos formas de generar la carpeta:

- **Si descargaste el `.skill`:** cambia la extensión de `.skill` a `.zip`, descomprime, te queda una carpeta `algoritmo-mental` con `SKILL.md` y `references/` adentro.
- **Si clonaste el repo:** la carpeta `algoritmo-mental` ya la tienes.

Mueve esa carpeta completa a la ubicación que encontraste en el paso 1. La estructura final debe ser:

```
...\skills\algoritmo-mental\SKILL.md
...\skills\algoritmo-mental\README.md
...\skills\algoritmo-mental\references\...
```

**Paso 3 — Reinicia Cowork**

1. Cierra completamente Cowork.
2. Vuelve a abrirlo.
3. Empieza una **conversación nueva** (las conversaciones existentes no recargan skills, solo las nuevas).

**Paso 4 — Pruébala**

Escribe *"algoritmo mental"* y Claude debe iniciar el onboarding. Si dice que no encuentra la skill, revisa el paso 1 — lo más probable es que la carpeta esté en una ubicación distinta de la que pegaste.

---

### Caso 3 — Claude Code (CLI)

Si usas Claude Code y ya manejas skills, esto es estándar.

**Paso 1 — Copia la carpeta a `~/.claude/skills/`**

```bash
# Si clonaste el repo:
cp -r algoritmo-mental ~/.claude/skills/

# O si descargaste el .skill:
unzip algoritmo-mental.skill -d ~/.claude/skills/
```

En Windows: `%USERPROFILE%\.claude\skills\algoritmo-mental\`.

**Paso 2 — Verifica que aparece**

```bash
ls ~/.claude/skills/algoritmo-mental/
# Debe listar: SKILL.md  README.md  LICENSE  references/
```

**Paso 3 — Pruébala**

En una nueva sesión de Claude Code, escribe *"algoritmo mental"*. Claude inicia el onboarding.

---

### Si nada de esto funciona

Lo más probable: te equivocaste de carpeta (Caso 2 / Caso 3) o no activaste code execution (Caso 1). Vuelve al Paso 1 del caso que te toca y revisa.

Si sigues atascada, abre un issue en este repo describiendo qué plataforma usas, qué hiciste y qué error ves.

---

## Primer uso

Una vez que la instalación está confirmada:

1. **Onboarding (una sola vez):** Claude te hace 4 preguntas — dónde guardar registros, formato del análisis, tono del análisis. La configuración queda guardada en `algoritmo-mental/config.json` y no se vuelve a hacer.

2. **Primer registro:** Dile a Claude "algoritmo mental" o "quiero registrar un bloqueo" y empieza a contar lo que pasó. Te va a guiar categoría por categoría.

3. **Análisis:** Después del primer registro Claude te da una observación corta. Después de varios, los análisis se vuelven más completos.

---

## Comandos que puedes usar

- `algoritmo mental` — empezar un registro
- `analiza mis registros` — analizar lo que ya hay
- `revisa mis patrones` — sinónimo del anterior
- `analiza los últimos 5` / `de este mes` — análisis filtrado
- `reconfigurar algoritmo mental` — empezar el onboarding de cero
- `cambiar destino` / `cambiar formato` / `cambiar tono` — actualizar solo un campo

---

## Plantilla manual (si no quieres instalar la skill)

Si prefieres registrar a mano sin instalar nada, hay versión en Notion y Google Sheets disponible en cerebrollo.com. Misma estructura, sin asistente.

---

## Estructura del repositorio

```
algoritmo-mental/
├── SKILL.md                        # cerebro principal de la skill
├── references/
│   ├── preguntas-extendidas.md     # ejemplos largos por categoría
│   ├── onboarding-detallado.md     # script completo del onboarding
│   └── ejemplos-analisis.md        # ejemplos de análisis para 1, 3, 5, 8 y 15+ registros
├── README.md                       # este archivo
└── LICENSE                         # MIT
```

---

## Reglas no negociables

1. Las palabras de la persona se respetan literalmente.
2. La skill no diagnostica ni trata.
3. El paso a paso es la entrada por defecto.
4. Si la persona ya escribió contenido, no se obliga a repetir.

Estas reglas están detalladas en `SKILL.md`.

---

## Salvaguarda ética

Si en un registro aparecen señales que exceden un bloqueo creativo (ideación de daño, desesperanza repetida, pánico, despersonalización, ansiedad que impide funciones básicas, crisis recurrentes), la skill nombra lo que vio y te invita a hablarlo con un profesional de salud mental. **No diagnostica, no nombra trastornos, no recomienda tratamientos.**

---

## Atribución

Esta skill adapta el modelo de registro de pensamientos de la Terapia Cognitivo-Conductual desarrollado por **Aaron Beck (1960)**. La adaptación al universo Cerebrollo (metáfora del restaurante en el análisis, las cinco lecturas, el universo de etiquetado, las cuatro reglas no negociables) es propia.

---

## Licencia

MIT — ver `LICENSE`.

---

## Autora

**Cerebrollo** · [www.cerebrollo.com](https://www.cerebrollo.com)
Marlinello · Diseñadora gráfica, investigadora y consultora.
