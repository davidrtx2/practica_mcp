# ⚽ PITCHLIVE — Plataforma de Streaming de Fútbol en Vivo

Interfaz web **funcional y responsive** para ver partidos de fútbol en directo, con reproductor de video, selector de servidores, chat en vivo y estadísticas en tiempo real.

Diseño original generado en **Google Stitch** y convertido en una aplicación web funcional (HTML + CSS + JavaScript, sin frameworks).

---

## 🚀 Demo

Abre el archivo `index.html` directamente en el navegador, o sírvelo con un servidor local:

```bash
# Opción 1: abrir directo
# Doble clic en index.html

# Opción 2: servidor local (Python)
python -m http.server 8080 --directory .
# Luego abre: http://localhost:8080/index.html

# Opción 3: servidor local (Node)
npx serve .
```

---

## ✨ Características

- 🎬 **Reproductor de video real** (`<video>`):
  - Play / Pausa (botón y clic en el video)
  - Barra de progreso con *seek* (avanzar/retroceder)
  - Control de volumen y silencio
  - Pantalla completa (Fullscreen API)
  - Picture-in-Picture (PiP)
- 📡 **Selector de servidores** con estado activo, overlay de "Reconectando…" y latencia dinámica.
- 🎚️ **Selector de calidad** (480p → 4K UHD) y **pista de audio** (Español / Inglés / Ambiente).
- 💬 **Chat en vivo funcional**:
  - Envía mensajes (botón o tecla **Enter**)
  - Mensajes entrantes simulados
  - Barra de reacciones rápidas (⚽🔥🏆👏🟥💚)
  - Auto-scroll al último mensaje
- 📊 **Pestañas Chat / Estadísticas** (posesión, tiros, córners, tarjetas…).
- 🔎 **Búsqueda** y **filtros por liga** (Premier, LaLiga, Libertadores, Serie A…) con contadores dinámicos.
- 🖥️ **Modo Teatro / Multi-View**: amplía el reproductor y oculta el panel lateral.
- ⏱️ **Extras en vivo**: reloj de partido, contador de espectadores, notificaciones y modal **GO PRO**.
- 🌗 Diseño *dark* premium con acentos neón, tipografías Space Grotesk + Manrope.

### ⌨️ Atajos de teclado
| Tecla | Acción |
|-------|--------|
| `Espacio` | Play / Pausa |
| `F` | Pantalla completa |
| `M` | Silenciar / activar audio |

---

## 🧱 Tecnologías

- **HTML5** semántico
- **Tailwind CSS** (vía CDN) con un tema personalizado (Design System *"Electric Pitch"*)
- **JavaScript** vanilla (sin dependencias ni build step)
- **Google Fonts**: Space Grotesk, Manrope y Material Symbols

No requiere instalación ni compilación: es un único archivo autocontenido.

---

## 📁 Estructura del proyecto

```
pitchlive/
├── index.html            # Aplicación funcional (versión final)
├── stitch-original.html  # Diseño original exportado desde Google Stitch (referencia)
└── README.md             # Este archivo
```

---

## 🎨 Origen del diseño

- **Herramienta:** Google Stitch
- **Proyecto:** *Plataforma Streaming Fútbol Vivo* (`projects/9128949567698633983`)
- **Pantalla:** *Fútbol en Vivo - Transmisión y Reproductor HD* (Desktop)
- **Design System:** *Electric Pitch* — tema oscuro, color primario `#00E676` (verde césped eléctrico), superficies `#0d1510`.

El archivo `stitch-original.html` conserva el markup original tal cual lo generó Stitch, y `index.html` es la versión mejorada con toda la interactividad.

---

## ⚠️ Notas

- **Video de demostración:** no existe un stream público de fútbol con derechos disponibles, por lo que el reproductor usa un clip de muestra con **fuentes de respaldo** (`jsDelivr` → `w3.org` → `w3schools`). Para producción, sustituye el `<source>` por tu propio stream (`HLS .m3u8` o `MP4`).
- **Requiere conexión a internet** para: el CDN de Tailwind, las fuentes de Google y el video de muestra.
- Se recomienda sustituir el CDN de Tailwind por una build propia (PostCSS/CLI) antes de producción.

---

## 🗺️ Próximos pasos (roadmap)

- [ ] Conectar un stream real (HLS `.m3u8` con `hls.js`)
- [ ] Integrar API de partidos y marcadores en vivo
- [ ] Backend para el chat en tiempo real (WebSocket)
- [ ] Build de Tailwind para producción
- [ ] Despliegue (Netlify / Vercel / GitHub Pages)

---

## 📄 Licencia

Uso educativo / demostración. Las marcas, escudos y nombres de clubes o competiciones pertenecen a sus respectivos propietarios.
