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

Si nunca instalaste una skill antes, esta guía está pensada para ti. Es la primera vez que muchas personas hacen esto. Va paso a paso.

### Lo que necesitas

- Una computadora con Windows (las instrucciones son para Windows; en Mac/Linux el principio es el mismo, los comandos cambian).
- **Cowork** o **Claude Code** instalado.
- 5 minutos.

### Paso 1 — Descarga los archivos

Tienes dos opciones:

**Opción A: descarga el `.skill` (más simple)**

1. Ve a la pestaña **Releases** de este repositorio.
2. Descarga `algoritmo-mental.skill`.
3. Guárdalo en una carpeta que recuerdes. Por ejemplo, `Descargas`.

**Opción B: clona el repositorio (si ya usas git)**

```powershell
git clone https://github.com/[USUARIO]/algoritmo-mental.git
```

### Paso 2 — Encuentra la carpeta de skills de Cowork

Cowork guarda las skills instaladas en una ruta como esta:

```
C:\Users\[TU-USUARIO]\AppData\Roaming\Claude\local-agent-mode-sessions\skills-plugin\[ID-LARGO-1]\[ID-LARGO-2]\skills\
```

Para encontrarla:

1. Abre el Explorador de archivos.
2. Pega esto en la barra de direcciones y presiona Enter: `%APPDATA%\Claude\local-agent-mode-sessions\skills-plugin`
3. Vas a ver una o dos carpetas con nombres largos (IDs). Entra en cada una hasta llegar a una que tenga una carpeta `skills` adentro.
4. Esa es la carpeta donde van las skills.

### Paso 3 — Copia los archivos a la carpeta de skills

**Si descargaste el `.skill` (Opción A):**

1. Cambia la extensión del archivo de `.skill` a `.zip`.
2. Descomprime el `.zip`. Te quedará una carpeta llamada `algoritmo-mental` con `SKILL.md` y `references/` dentro.
3. Mueve esa carpeta `algoritmo-mental` completa a la ubicación que encontraste en el paso 2.

**Si clonaste el repo (Opción B):**

1. Copia la carpeta `algoritmo-mental` (la que tiene `SKILL.md` adentro) a la ubicación del paso 2.
2. Asegúrate de que la estructura final sea: `...\skills\algoritmo-mental\SKILL.md`.

### Paso 4 — Reinicia Cowork

1. Cierra completamente Cowork.
2. Vuelve a abrirlo.
3. Empieza una **conversación nueva** (no una existente — las viejas no recargan skills).

### Paso 5 — Prueba que funcione

En la nueva conversación, escribe:

> "Activa la skill algoritmo-mental"

Si la skill está bien instalada, Claude te va a responder iniciando el onboarding (te va a explicar qué es y te va a hacer 4 preguntas rápidas). Si Claude dice que no encuentra ninguna skill con ese nombre, revisa el paso 3 — lo más probable es que la carpeta esté en una ubicación distinta.

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
