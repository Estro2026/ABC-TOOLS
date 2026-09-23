# ABC Tools — ABC Club Landing

Mockup della landing page "Entra nell'ABC Club", pronto per lo sviluppo.

## File

| File | Contenuto |
| --- | --- |
| `ABC Club Landing - Mockup.html` | Mockup UI definitivo (HTML/CSS/JS in un unico file) |
| `ABC Club Landing (standalone).html` | Wireframe di partenza |
| `VI/` | Visual identity: logo (SVG, PNG, PDF, WebP), font, cartella colori |

Aprire il mockup nel browser tenendo la cartella `VI/` accanto al file: i loghi WebP vengono caricati da `VI/Logo/webp/`.

## Visual identity

- **Colori:** blu `#001489` · arancio `#F26A2A` (vedi `Cartella colori ABC Tools.pdf`). Tutti i colori sono token CSS in `:root`.
- **Font:** Steelfish per i titoli (anche incorporato nel file come fallback), Arial per il testo.
- **Logo:** `ABCToolsLogoDark.webp` su fondi chiari, `ABCToolsLogoLight.webp` su fondi scuri.

## Note per lo sviluppo

- Le foto sono placeholder (`.media`): sostituire con `<img>` mantenendo il contenitore.
- Video ABC Stories: YouTube `2fOBAODJ2MA`, l'iframe si carica al click su Play (da `file://` YouTube può dare errore, online funziona).
- Responsive: menu hamburger ≤1024px, card a swipe ≤720px. Hero + banda occupano esattamente la viewport.
