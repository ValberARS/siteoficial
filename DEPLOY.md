# Start BIAI · site estático

Pasta pronta para deploy na Vercel (ou qualquer host estático). Não há build: é HTML, CSS e JS puros.

## Conteúdo

- `index.html`: página única, bilíngue PT/EN (detecção automática + toggle).
- `assets/`: prints dos dashboards (case1 a case8) e imagem de compartilhamento (og-image).
- `favicon.svg`, `robots.txt`, `sitemap.xml`, `vercel.json` (cache de assets e headers de segurança).

## Deploy na Vercel

Opção 1, pelo painel: New Project > Import > arraste esta pasta. Framework Preset: Other. Build Command vazio. Output Directory: `.`

Opção 2, pela CLI:

    npm i -g vercel
    cd start-biai-deploy
    vercel --prod

Depois aponte o domínio startbiai.com no projeto (Settings > Domains). As meta tags, canonical e sitemap já usam https://startbiai.com/.

## Manutenção

- Trocar um case: substitua `assets/caseN.png` e edite o card correspondente em `index.html` (título, descrição, alt e href do Power BI).
- Número de WhatsApp: constante `WA_BASE` no script no fim do `index.html`. O texto pré-preenchido está em `WA_MSG`.
- Ao criar páginas por serviço, adicione as URLs no `sitemap.xml` (há um exemplo comentado).
