# Cladograma Interativo — Cynodontia

Este repositório contém um pequeno site estático com o arquivo `cladograma_refinado.html` e imagens associadas (pasta `images/`).

Objetivo
- Hospedar o cladograma interativo (HTML/CSS/JS) usando GitHub Pages.

Como ver localmente
- Abra `cladograma_refinado.html` no navegador (duplo-clique), ou execute um servidor HTTP simples no diretório do projeto e acesse `http://localhost:8000`.

No PowerShell:

```powershell
# entrar na pasta do projeto
cd "c:\Users\caetanoronan\OneDrive - UFSC\Área de Trabalho\Prova_zoo\cladograma_interativo"

# iniciar um servidor HTTP Python (se tiver Python instalado)
python -m http.server 8000
# abra http://localhost:8000/cladograma_refinado.html no navegador
```

Publicando no GitHub Pages (opções)

Opção A — usar a branch `main` (root):
1. Crie um repositório remoto no GitHub (via site ou `gh` CLI).
2. Faça push do `main` e habilite GitHub Pages para servir da branch `main` / root.

PowerShell (após criar remoto):

```powershell
git init
git add .
git commit -m "Initial commit: Add cladograma site"
git branch -M main
git remote add origin https://github.com/<SEU_USUARIO>/<REPO>.git
git push -u origin main
```

Opção B — usar branch `gh-pages` (recomendado quando não quer servir da root):

```powershell
git checkout -b gh-pages
git push -u origin gh-pages
# Em GitHub -> Settings -> Pages, selecione branch gh-pages
```

Dicas para imagens
- Se as imagens forem muitas ou muito grandes, considere usar Git LFS ou um CDN (Cloudinary, S3) e referenciá-las por URL.
- Para imagens pequenas (PNG/JPG), a pasta `images/` no repositório é simples e funciona bem.

Boas práticas
- Mantenha nomes de arquivos simples (sem espaços). Ex.: `procynosuchus.png`.
- Se for privado, habilite Pages para repositórios privados conforme sua conta/plano.

Se quiser, posso também:
- Criar e configurar o repositório remoto com a `gh` CLI (se você autorizar e tiver o `gh` instalado), ou
- Configurar Git LFS para você rastrear imagens grandes, ou
- Gerar um arquivo `index.html` simples que redirecione para `cladograma_refinado.html`.

---
Gerado automaticamente — pronto para inicializar e publicar.