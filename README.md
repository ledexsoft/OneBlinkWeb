# OneBlink Web

Sitio web oficial de **OneBlink** — el marketplace de Cuba.

## Estructura
- `index.html` — **Landing page** de OneBlink (hero, features, CTA)
- `privacidad.html` — **Política de Privacidad** completa (ES / EN / PT)

## Multi-idioma
- Detección automática por idioma del navegador (`navigator.language`)
- Selector manual ES / EN / PT (persiste en `localStorage`)
- El idioma viaja entre páginas vía `?lang=es|en|pt`

## Cómo publicar en GitHub Pages
1. GitHub → repo `ledexsoft/OneBlinkWeb` → **Settings** → **Pages**
2. *Build and deployment* → *Source*: **Deploy from a branch**
3. Branch: `main` → carpeta `/ (root)`
4. Save → esperá 1-2 min → la web queda en:
   `https://ledexsoft.github.io/OneBlinkWeb/`

## Futuro
Este repo crecerá para alojar la web completa de OneBlink
(catálogo, propiedades, blog, etc.). La política de privacidad queda en
`/privacidad.html` (con idioma: `/privacidad.html?lang=en`).
