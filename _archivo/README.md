# Archivo de prototipos

Estos 13 HTML son borradores de la landing. El 26 de octubre de 2026 se movieron acá porque ya no se usan y, al estar en la raíz del repo, cualquiera podía abrirlos por URL en el sitio publicado. El sitio vigente sigue siendo solo `index.html`, `privacy.html` y `terms.html` (más el `README.md` de la raíz). Esos archivos no se modificaron.

Cada ruta se agregó una sola vez, con el mensaje "Add files via upload", y ningún commit posterior la editó. El historial queda en Git porque el movimiento fue un rename, no un borrado.

Los 13 `<title>` incluyen el nombre provisorio **RaízTech NEA** (13 de 13). El `index.html` publicado ya no lo usa.

## Por qué esta carpeta no sale en el sitio

GitHub Pages publica `main` desde `/` con el build legacy de Jekyll, y el repo no tiene `.nojekyll`. Jekyll no copia al sitio las carpetas cuyo nombre empieza con `_`. El nombre `_archivo` existe para eso.

Hay que confirmarlo en el sitio publicado después de cada deploy: `https://pinomh.github.io/landing/_archivo/<archivo>` y la URL vieja de la raíz tienen que responder 404.

**Advertencia.** Si se agrega `.nojekyll`, o si el modo de publicación pasa a uno que copie todo el repositorio, esta carpeta vuelve a ser pública.

## Cómo verlos en local

Desde la raíz del repo:

```bash
python3 -m http.server 8765
```

Abrir, por ejemplo, `http://127.0.0.1:8765/_archivo/v2.html`. Un servidor local sí los sirve. GitHub Pages no debería.

Para el historial de un archivo:

```bash
git log --follow -- _archivo/v2.html
```

La etiqueta `pre-archivo-prototipos` marca el último commit en el que estos archivos todavía estaban en la raíz y, por lo tanto, publicados (`fa8a144`).

## Qué es cada archivo

| archivo | alta | commit | qué es |
|---|---|---|---|
| `v2.html` | 2026-06-30 | `f48bd8d` | Primera versión corta. Título: "RaízTech NEA — Tecnología que da tranquilidad". |
| `v3.html` | 2026-06-30 | `f61308d` | Segunda versión. El título lleva el slogan "No vendemos software. Vendemos tranquilidad." |
| `v4.html` | 2026-06-30 | `3175579` | La misma línea que v3, bastante más larga, ya con animación en el CSS. |
| `v6navy.html` | 2026-07-01 | `04a12e6` | Paleta navy y coral. El título dice "Navy + Coral — V6 Hero Oscuro". No tiene canvas. |
| `v6navy-animado.html` | 2026-07-01 | `ff3ed1a` | La misma paleta, con fondo topográfico dibujado en un canvas. |
| `v6slate.html` | 2026-07-01 | `5bd4662` | Paleta slate y amarillo (`#1C2540` / `#F7E848`). No tiene canvas. |
| `v6slate-animado.html` | 2026-07-01 | `70ffc47` | Slate y amarillo con canvas topográfico. |
| `v6slate-animado2.html` | 2026-07-01 | `2ff4d2d` | Segunda iteración animada de esa paleta. Suma Google tag. |
| `v6slate-animado2-gem.html` | 2026-07-01 | `93e2c3b` | Título "Soluciones Operativas". El comentario del hero indica fotografía en lugar del canvas. |
| `v6slate-animado-fable1.html` | 2026-07-02 | `7dbc999` | Iteración slate/amarillo animada, con Google tag. |
| `v6slate-animado-fable2.html` | 2026-07-02 | `06e08f4` | La pasada siguiente de esa serie. |
| `topo-slate-yellow-timeline.html` | 2026-07-02 | `6e6f2bf` | Variante slate/amarillo. El título aclara "Timeline" e incluye canvas topográfico. |
| `index-cursor.html` | 2026-07-02 | `a2918dd` | Último prototipo completo de la serie (canvas, timeline y Google tag). No es el `index.html` publicado. |
