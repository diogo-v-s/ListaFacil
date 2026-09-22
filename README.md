# Lista Fácil — Lista de Compras Inteligente

> **Acesse agora:** https://diogo-v-s.github.io/ListaFacil/
>
> PWA simples, rápida e gratuita para organizar compras, com cálculo automático do total (qtd × preço unitário), controle de peso e histórico.

## 💡 Ideia
Lista minimalista que funciona no celular (no mercado) e no desktop (planejando em casa), sem cadastro ou hospedagem paga. Você adiciona itens pelo nome, informa quantidade/peso (`0,600` kg) e preço unitário durante as compras. Ao marcar o checkbox, o app calcula `quantidade × preço` e soma ao total fixo.

Tudo offline via `localStorage` e compartilhável por export/import JSON.

## 🎯 Objetivo
Simplicidade, controle financeiro em tempo real, leveza (zero deps) e custo zero (GitHub Pages). Histórico transforma listas finalizadas em “viagens ao mercado” reabrí­veis.

## ✨ Funcionalidades
- Input fixo no topo + `Enter` → item entra na base com `qtd=1`
- **Qtd** entre checkbox e nome, aceita `2` ou `0,600` (vírgula/ponto, até 3 casas)
- **Preço unitário** `R$ --` editável inline, `inputmode="decimal"`
- **Checkbox** só soma ao total quando marcado
- **Total pílula** sticky mobile, `0 4px 12px rgba(0,0,0,0.08)`
- Clique no **nome** para editar inline (Enter salva, Esc cancela)
- Lixeira, **Nova Lista** (arquiva no histórico), **Histórico** modal, **Compartilhar via link** + **Exportar PDF** (Print), **Modo escuro**

## 🛠️ Tecnologias
HTML5 + CSS3 Custom Properties (paleta `#D85012`/`#F5EBE1`/`#D7B18A`/`#1E2A38`) + JS vanilla + `localStorage` (`lista-facil-data`) + PWA (`manifest.json` + `sw.js` `v6`) + GitHub Pages + Print-to-PDF nativo. Ícones SVG inline, fonte `Inter`.

## 📦 Estrutura
```
index.html  manifest.json  sw.js  icon-192.svg  icon-512.svg
```

## 🔗 Acesso (GitHub Pages)
**Link oficial:** https://diogo-v-s.github.io/ListaFacil/

## 📤 Exportação
- **Link compartilhável** — botão 🔗 Compartilhar gera `?share=` (base64 url-safe). Quem abrir o link importa no dispositivo com 1 clique, sem arquivo
- **PDF via Impressão** — botão 🖨️ Imprimir/PDF gera PDF nativo do navegador (`window.print()`, sem libs, visual apenas)

## 🚀 Rodar local
```bash
npx serve .
```

## 🌐 Deploy GitHub Pages
Publicado em `https://diogo-v-s.github.io/ListaFacil/` via `main` → Settings → Pages → `main / root`
