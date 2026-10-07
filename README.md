# ABC Tools — ABC Club Landing

Mockup della landing page "Entra nell'ABC Club", pronto per lo sviluppo.

## File

| File | Contenuto |
| --- | --- |
| `index.html` | Mockup UI definitivo (HTML/CSS/JS in un unico file) — online su https://estro2026.github.io/ABC-TOOLS/ |
| `VI/img/` | Le tre foto usate nel mockup (hero, "Chi siamo", catalogo) |
| `VI/Logo/webp/` | Logo in uso nel mockup (Dark su fondi chiari, Light su fondi scuri) |
| `VI/Logo/svg` `/png` `/pdf` | Stesso logo in altri formati (vettoriale/stampa), non richiesti dal mockup |
| `VI/Font/` | Steelfish (titoli) e Arial (testo) |
| `Cartella colori ABC Tools.pdf` | Palette ufficiale del brand |

Aprire `index.html` nel browser tenendo la cartella `VI/` accanto al file: logo e foto si caricano da lì con percorso relativo.

## Visual identity

- **Colori:** blu `#001489` · arancio `#F26A2A` (vedi `Cartella colori ABC Tools.pdf`). Tutti i colori sono token CSS in `:root`.
- **Font:** Steelfish per i titoli (incorporato nel file come fallback, funziona anche senza `VI/`), Arial per il testo.
- **Logo:** `ABCToolsLogoDark.webp` su fondi chiari, `ABCToolsLogoLight.webp` su fondi scuri.

## Note per lo sviluppo

- **Foto:** `VI/img/operaio.webp` (hero), `chiaveinglese.webp` (Chi siamo), `catalogo.png` (Catalogo). Già inserite come `<img>` nel contenitore `.media`.
- **Video ABC Stories:** YouTube `2fOBAODJ2MA` (id in `data-yt` su `#player`), l'iframe si carica al click su Play. Aperto da `file://` YouTube può dare errore per via del referrer; online funziona normalmente.
- **Form:** collegato all'endpoint Pardot `https://go.marketing.abctools.it/l/1065722/2026-10-01/8mr9nc` (`POST`, `target="formTarget"`). L'invio avviene dentro un iframe nascosto: la pagina non cambia e alla risposta compare il messaggio di conferma. Il front-end gestisce validazione e stato "inviato". Da verificare lato Pardot la mappatura dei campi `nome`, `cognome`, `email`, `azienda`, `citta`, `tipo`, `privacy`, con un test di arrivo lead. Il segmento Professionista/Rivenditore è in `userType` nello script e viaggia nel POST come campo `tipo` (input hidden `#f-tipo`).
- **Link legali:** Privacy e Cookie puntano alle pagine iubenda di ABC Tools, Condizioni alle condizioni generali di vendita su abctools.it.
- **Responsive:** menu hamburger ≤1024px, card a swipe ≤720px. Hero + banda occupano sempre il 100% della viewport (misurato via JS, non solo calcolato in CSS, per restare corretto anche con lo zoom del browser o lo scaling del monitor).
