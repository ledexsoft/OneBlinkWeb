# OneBlink Web

Sitio web oficial de **OneBlink** — el marketplace de Cuba.

## Estructura
- `index.html` — **Landing page** de OneBlink (hero, features, CTA)
- `privacidad.html` — **Política de Privacidad** completa (ES / EN / PT)
- `business.html` — fallback público de enlaces a negocios de LedexSoft; solo
  procesa el identificador de negocio, no consulta ni revela datos privados.
- `.well-known/apple-app-site-association` — asociación fuente para Universal
  Links de LedexSoft en `/business.html`.

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

## Enlace a negocios de LedexSoft

La URL pública acordada es `https://cumashop.app/business.html?id=<id>`. Antes
de considerar Universal/App Links publicados, configurar el dominio `cumashop.app`
para servir este repo por HTTPS, comprobar el AASA en `/.well-known/` y habilitar
Associated Domains en el App ID iOS. Android requiere `/.well-known/assetlinks.json`
con la huella SHA-256 del certificado de Play que firma LedexSoft; no debe
rellenarse con la clave de upload si Play App Signing usa otra firma.
