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

El fallback actualmente publicado es
`https://ledexsoft.github.io/OneBlinkWeb/business.html?id=<id>`. La página solo
procesa el ID y ofrece abrir LedexSoft mediante su esquema registrado; no
consulta ni revela datos privados del negocio. El enlace `cumashop.app` no se
usa mientras el dominio no resuelva públicamente.

El archivo `.well-known/apple-app-site-association` de este repo es solo una
fuente preparada: GitHub Pages sirve este proyecto bajo `/OneBlinkWeb/`, no en
la raíz del host. Por eso no constituye una asociación Universal Link activa.
Para enlaces verificados hace falta un host raíz resoluble, servir allí AASA y
`assetlinks.json`, habilitar Associated Domains en el App ID iOS, y publicar en
Digital Asset Links la SHA-256 exacta del certificado de distribución Android
(el certificado de Play App Signing, no necesariamente el de upload).
