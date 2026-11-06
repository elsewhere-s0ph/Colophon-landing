# Colophon — Landing page

Landing page statica per **Colophon**, l'editor EPUB nel browser di Little Elsewhere.
Due pagine statiche: `index.html` (italiano) e `en/index.html` (inglese), collegate dalle pill EN/IT nella nav.
Identità editoriale: carta, inchiostro, Fraunces, capitoli e note a margine.
Tema chiaro/scuro: segue il sistema, con switch manuale in nav (la scelta viene ricordata e condivisa tra le due lingue).
SEO & social: og:image + twitter:card con anteprime localizzate, JSON-LD SoftwareApplication (offers price 0), hreflang incrociati, canonical.

- **App**: https://colophon-editor.pages.dev/
- **Landing (target)**: https://colophon-home.pages.dev/ · https://colophon-home.pages.dev/en/

## Deploy su Cloudflare Pages

1. Cloudflare Dashboard → **Workers & Pages** → **Create** → **Pages** → **Connect to Git**
2. Seleziona il repository `Colophon-landing` e il branch `main`
3. **Project name**: `colophon-home` → URL finale `https://colophon-home.pages.dev`
4. Framework preset: **None** · Build command: (vuoto) · Build output directory: `/`
5. **Save and Deploy**

`/en/` funziona senza configurazioni: l'hosting statico serve `en/index.html` sulla URL pulita.
Da quel momento ogni push su `main` pubblica automaticamente la nuova versione.

## Anteprima locale

Apri `index.html` nel browser. Fine.

## Struttura

```
index.html      <- versione italiana
en/index.html   <- versione inglese
og.jpg          <- anteprima social (og:image) italiana
en/og.jpg       <- anteprima social (og:image) inglese
robots.txt      <- indicizzazione
sitemap.xml     <- mappa del sito (it + en, con hreflang)
_headers        <- CSP con hash SHA-256 degli script inline, HSTS, nosniff, X-Frame-Options
README.md       <- questo file
```

## Modifiche

Le modifiche si possono iterare nei canvas "Colophon — Landing" (IT) e "Colophon — Landing (EN)",
poi si pusha qui, oppure editando direttamente il file nel repo: il deploy è automatico.
