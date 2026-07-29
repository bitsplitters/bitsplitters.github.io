# bitsplitters.github.io

Landing page dell'apex **[bitsplitters.app](https://bitsplitters.app)** — sito statico servito da GitHub Pages (org pages).

## Struttura

- `index.html` — pagina unica, self-contained (CSS e JS inline, nessuna dipendenza esterna).
- `CNAME` — dominio custom (`bitsplitters.app`).
- `.nojekyll` — disattiva l'elaborazione Jekyll (sito statico puro).

## Modificare il link alla documentazione

L'URL della documentazione è centralizzato in **una sola riga** in fondo a `index.html`:

```js
const DOCS_URL = "https://tasks.bitsplitters.app";
```

Punta al sito di documentazione di **Team Tasks Manager** (`tasks.bitsplitters.app`).
Se lo si riporta a `"#"`, il pulsante *Documentation* torna a mostrare "coming soon"
ed è disabilitato.

## Aggiungere un prodotto

Duplica il blocco `<article class="card">` dentro `.grid` in `index.html`: la griglia è
già responsive e accoglie più card senza modifiche al CSS.

## Deploy

Push su `main` → GitHub Pages pubblica in automatico. DNS su Cloudflare: record per l'apex
verso GitHub Pages in modalità **DNS only** (grey cloud), altrimenti GitHub non emette il
certificato TLS per il dominio `.app`.
