# Guia de Treinamento para Cães em 7 Dias

Site de vendas estático (HTML + CSS + JS já compilados, com vídeo VSL incluído). Pronto para hospedar em qualquer servidor estático — funciona em qualquer subpasta.

## Hospedar no GitHub Pages (passo a passo)

1. Crie um repositório novo no GitHub (público ou privado, qualquer nome — ex: `guiadetreinamentoparacaes`).
2. Faça upload de **todos os arquivos desta pasta** (incluindo `.nojekyll`, `assets/`, `index.html`, `404.html`, `favicon.svg` e `opengraph.jpg`) na raiz do repositório.
   - Pelo navegador: botão **"Add file" → "Upload files"** → selecione tudo → **Commit changes**.
   - O vídeo da VSL tem ~20 MB; se o upload pelo navegador falhar, use o GitHub Desktop ou Git pela linha de comando.
3. No repositório, vá em **Settings → Pages**.
4. Em **Source**, escolha **"Deploy from a branch"**.
5. Em **Branch**, selecione **`main`** e a pasta **`/ (root)`** → **Save**.
6. Aguarde 1–2 minutos. O GitHub mostrará a URL pública (ex: `https://seu-usuario.github.io/guiadetreinamentoparacaes/`).
7. Ao acessar, **lembre da barra final** (`/`) na URL — `https://seu-usuario.github.io/guiadetreinamentoparacaes/`. Sem ela alguns navegadores resolvem para `/index.html` direto, o que está coberto pelo `404.html`.

Pronto. A página identifica automaticamente em qual subpasta foi hospedada.

## Conteúdo

- `index.html` — página principal (quiz + página de vendas).
- `404.html` — cópia do index para garantir SPA routing em URLs como `/foo`.
- `.nojekyll` — desativa o processamento Jekyll do GitHub Pages.
- `assets/` — JS, CSS, imagem da capa e vídeo VSL.
- `favicon.svg`, `opengraph.jpg` — ícones e imagem de compartilhamento.

## Outras opções de hospedagem

- **Netlify** — arraste a pasta em https://app.netlify.com/drop
- **Vercel** — `vercel deploy` na pasta
- **Cloudflare Pages** — upload direto no painel
- **Hospedagem comum** (Hostinger, etc.) — suba via FTP para `public_html/`

## Observações

- O botão de checkout aponta para `https://pay.cakto.com.br/5ju9gcx_834856`.
- Os botões de compra só aparecem após **10 segundos** do vídeo assistidos. Esse desbloqueio fica salvo no navegador do visitante.
- O quiz salva as respostas no navegador (localStorage). Não há banco de dados nem servidor.
- O cronômetro de 24 minutos é por dispositivo — cada visitante tem seu próprio.
- O contador de "X pessoas assistindo agora" é fictício/decorativo (varia entre ~80 e ~200).
