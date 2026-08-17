# LibrAI

Aplicativo web (PWA) para tradução de português para **Libras** (Língua Brasileira de Sinais), com categorias temáticas e sugestão de frases por IA.

## Funcionalidades

- **Tradução em tempo real** — Digite uma frase em português e receba a tradução em Libras via [VLibras](https://www.gov.br/governodigital/pt-br/vlibras)
- **Categorias temáticas** — Navegue por Cumprimentos, Objetos de Sala e Sentimentos com imagens ilustrativas
- **Sugestão por IA** — Botão "✨ IA sugerir frase" gera frases curtas automaticamente usando a API do Google Gemini
- **PWA** — Pode ser instalado como aplicativo no celular ou desktop

## Como usar

1. Abra `index.html` no navegador ou publique no GitHub Pages
2. Digite ou selecione um texto e clique em **Traduzir**
3. Para sugestões de frases, acesse uma categoria e clique em **✨ IA sugerir frase**

## Estrutura do projeto

```
LibrAI/
├── index.html          # App principal (HTML, CSS e JS em um único arquivo)
├── manifest.json       # Manifesto PWA
├── img/
│   ├── banners/        # Imagens de capa por categoria
│   │   ├── cumprimentos.png
│   │   ├── objetos.png
│   │   └── sentimentos.png
│   ├── cumprimentos/   # Sinais de cumprimentos
│   │   ├── ola.png
│   │   ├── oi.png
│   │   ├── bom_dia.png
│   │   ├── boa_tarde.png
│   │   ├── boa_noite.png
│   │   ├── tudo_bem.png
│   │   ├── bem_vindo.png
│   │   ├── ate_logo.png
│   │   ├── ate_mais.png
│   │   ├── tchau.png
│   │   ├── obrigado.png
│   │   └── por_favor.png
│   ├── objetos/        # Sinais de objetos de sala
│   │   ├── Cadeira.png
│   │   ├── Mesa.png
│   │   ├── Quadro.png
│   │   ├── Lapis.png
│   │   ├── Mochila.png
│   │   ├── Borracha.png
│   │   ├── Caderno.png
│   │   └── Livro.png
│   └── sentimentos/    # Sinais de sentimentos
│       ├── Feliz.png
│       ├── Triste.png
│       ├── Surpreso.png
│       ├── Bravo.png
│       ├── Pensativo.png
│       ├── Agradecido.png
│       ├── Com_medo.png
│       └── Aliviado.png
└── README.md
```

## Como funciona

O app é um **Single Page Application** com tudo em um único `index.html`:

1. **VLibras Plugin** — Inicializa o widget do VLibras para traduzir texto digitado para Libras
2. **Categorias** — Ao clicar em uma categoria, o app renderiza um grid com imagens dos sinais correspondentes
3. **IA (Gemini)** — O botão de sugestão envia um prompt à API do Google Gemini Flash, que gera uma frase curta adequada para Libras no contexto da categoria

## Publicar no GitHub Pages

1. Crie um repositório no GitHub
2. Envie os arquivos para a branch `main`
3. Vá em **Settings > Pages** e selecione a branch `main` / pasta `root`
4. O app estará disponível em `https://<usuario>.github.io/<repositorio>/`

## Tecnologias

- **HTML / CSS / JS** — App single-file sem dependências de build
- [VLibras](https://www.gov.br/governodigital/pt-br/vlibras) — Widget de tradução para Libras
- **Google Gemini API** — Sugestão de frases por IA
- **PWA** — Manifesto para instalação como app
