# PPA Coren Goiás | Gestão Estratégica

Painel de acompanhamento do PPA 2025–2027 do Coren-GO (68 iniciativas, 11 objetivos
estratégicos). App estático — HTML, CSS e JavaScript puro, sem build, sem backend.

## Arquivos

- `index.html` — a aplicação inteira (interface + lógica)
- `data.json` — os dados das 68 iniciativas, separados da interface
- `manifest.json` — metadados de instalação como PWA
- `sw.js` — service worker (cache offline)
- `icons/` — ícones de instalação (placeholder com "PPA" — troque pela logomarca oficial do Coren-GO quando quiser)

## Publicar no GitHub Pages

1. Crie um repositório novo no GitHub (pode ser privado ou público).
2. Suba estes arquivos mantendo a mesma estrutura de pastas (não precisa de `npm install` nem build — é só HTML/CSS/JS puro):
   ```
   git init
   git add .
   git commit -m "Painel PPA Coren Goiás"
   git branch -M main
   git remote add origin https://github.com/SEU-USUARIO/SEU-REPOSITORIO.git
   git push -u origin main
   ```
3. No GitHub, vá em **Settings → Pages**, em "Source" escolha a branch `main` e a pasta `/ (root)`, salve.
4. Em alguns minutos o painel fica disponível em `https://SEU-USUARIO.github.io/SEU-REPOSITORIO/`.
5. Abra esse link pelo celular e use "Adicionar à tela inicial" (Android/Chrome) ou "Adicionar à Tela de Início" (iOS/Safari) — com HTTPS do GitHub Pages, o ícone de app e o cache offline (service worker) passam a funcionar de verdade.

## Atualizar os dados depois

Basta gerar um novo `data.json` a partir da planilha (mesma estrutura de campos) e
subir o arquivo substituindo o antigo — não precisa mexer no `index.html`.

## O que ainda não está na base

Prazos, percentual de execução física, metas/indicadores e evidências não existem
na planilha atual. Quando esses campos forem adicionados ao `data.json`, o painel
pode ser estendido para exibi-los (a estrutura do código já foi pensada para isso).
