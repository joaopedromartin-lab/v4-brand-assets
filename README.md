# V4 Brand Assets

Repositório público de assets de marca da V4 Company, servidos via GitHub Pages pra qualquer projeto importar sem precisar copiar arquivos localmente.

## Como usar em um projeto

Uma linha no `<head>` do HTML:

```html
<link rel="stylesheet" href="https://joaopedromartin-lab.github.io/v4-brand-assets/fonts/morganite.css">
```

Depois usa normalmente no CSS:

```css
.headline {
  font-family: 'Morganite', sans-serif;
  font-weight: 700;
}
```

Pesos disponíveis: **500** (Medium), **600** (SemiBold), **700** (Bold).

## Stack tipográfica da V4

- **Corpo/UI:** IBM Plex Sans (Google Fonts) — `font-family: 'IBM Plex Sans', sans-serif;`
- **Impacto/títulos grandes:** Morganite (este repo) — `font-family: 'Morganite', sans-serif;`

Não usar Anton, Oswald, Bebas ou qualquer outra condensed como fallback. Se o Morganite falhar, o browser deve cair pro `sans-serif` genérico, não pra uma substituição visualmente diferente.

## Conteúdo do repo

```
v4-brand-assets/
├── README.md
└── fonts/
    ├── morganite.css              ← arquivo principal (importado pelos projetos)
    ├── Morganite-Medium.woff2     ← 26 KB
    ├── Morganite-Medium.ttf       ← fallback pra browsers antigos
    ├── Morganite-SemiBold.woff2
    ├── Morganite-SemiBold.ttf
    ├── Morganite-Bold.woff2
    └── Morganite-Bold.ttf
```

WOFF2 é o formato preferido (~25KB por peso, 4x menor que o TTF). TTF entra como fallback.

## Setup do GitHub Pages (uma vez só)

1. GitHub → repo `v4-brand-assets` → Settings → Pages
2. Source: `Deploy from a branch` → Branch: `main` → Folder: `/ (root)` → Save
3. Esperar ~1 min, URL final fica: `https://joaopedromartin-lab.github.io/v4-brand-assets/fonts/morganite.css`

## Atualizar uma fonte

1. Substituir o arquivo em `fonts/`
2. Commit + push na main
3. GitHub Pages reflete em ~1 min (use `?v=2` na URL pra forçar refresh do cache do browser durante testes)
