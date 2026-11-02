# Colophon — Landing page

Landing page statica per **Colophon**, l'editor EPUB nel browser di Little Elsewhere.
Un unico file `index.html`: zero build, zero dipendenze (solo il font Fraunces da Google Fonts).
Bilingue IT/EN con toggle in alto a destra; identità editoriale: carta, inchiostro, Fraunces, capitoli e note a margine.

- **App**: https://colophon-editor.pages.dev/
- **Landing (target)**: https://colophon-home.pages.dev/

## Deploy su Cloudflare Pages

1. Cloudflare Dashboard → **Workers & Pages** → **Create** → **Pages** → **Connect to Git**
2. Seleziona il repository `Colophon-landing` e il branch `main`
3. **Project name**: `colophon-home` → URL finale `https://colophon-home.pages.dev`
4. Framework preset: **None** · Build command: (vuoto) · Build output directory: `/`
5. **Save and Deploy**

Da quel momento ogni push su `main` pubblica automaticamente la nuova versione.

## Anteprima locale

Apri `index.html` nel browser. Fine.

## Struttura

```
index.html   ← l'intero sito: CSS, JS, SVG e favicon inline
README.md    ← questo file
```
