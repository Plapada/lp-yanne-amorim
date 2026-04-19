# Project Progress

## Goal
Landing page cinematográfica para Dra. Yanne Amorim — Médica Pneumologista Paliativista, com identidade visual completa da marca e fotos reais.

## Status
Done — LP v2 cinematográfica editorial completa com fotos reais.

## Completed
### V1 (arquivada)
- [x] Primeira versão cinematográfica dark com placeholders.

### V2 (atual) — Redesign completo com identidade real
- [x] Extração das 7 fotos profissionais da Dra. Yanne (`Yanne Amorim/fotos/`) para `assets/fotos/`.
- [x] Importação dos grafismos, estampas, logos e fonte Noto Serif Display da pasta de branding para `assets/brand/`.
- [x] Troca do tema: de dark cinematográfico para **Editorial Luxury Light** (fiel à paleta bege/azul/rosa/gold da marca).
- [x] Reescrita completa do `index.html` (2 versões, ~1300 linhas).
- [x] Preloader cinematográfico (logo SVG com stroke-draw, letras staggered "YANNE AMORIM", contador animado).
- [x] Custom cursor com spring physics (dot + ring, difference blend, estado hover).
- [x] Lenis smooth scroll + anchor scrolling custom.
- [x] Hero split em 2 colunas: headline 3-linhas com reveal + foto portrait em arco (referência logo).
- [x] Badge flutuante no hero com logo + manifesto "Aqui, você não está só."
- [x] Marquee full-width navy com slogans ("Cuidar é permanecer · Presença · Técnica · Humanidade").
- [x] Seção Sobre com foto lateral + lead serif italic + 3 stats count-up animados.
- [x] Seção Especialidades (tema navy): 2 cards double-bezel (Paliativos + Pneumologia) com listas detalhadas.
- [x] Galeria horizontal pinned (scroll horizontal ao rolar vertical) com 5 fotos da Dra. + captions cinematográficos.
- [x] Seção Valores: lista hover-fill com reveal de ink navy.
- [x] Timeline trajetória com linha vertical animada + itens alternando esquerda/direita + dots com glow.
- [x] FAQ accordion com sticky sidebar navy + CTA interno.
- [x] Seção Contato grande (tema navy) com botão gold WhatsApp + info grid + foto serena.
- [x] Footer editorial com "Yanne Amorim" em tipografia massiva italic serif.
- [x] Animações: reveals staggered, parallax hero+leafs, magnetic buttons, counter-up stats, hover states, marquee infinito.
- [x] Accessibility: `prefers-reduced-motion` dispara skip de animações, ARIA em accordion, alt em imagens.
- [x] Performance: só `transform`/`opacity`, `backdrop-filter` só em nav fixo, cursor desativado em touch, safety timeout 5s no preloader.
- [x] Verificação visual no browser com Playwright: 11 screenshots de todas seções — 0 erros no console.

## Pending (pré-deploy)
- [ ] Substituir `5500000000000` pelo número real do WhatsApp.
- [ ] Inserir CRM e RQE reais (buscar `CRM-XX XXXXXX`).
- [ ] Confirmar anos de experiência (hoje `data-count="10"`) e atualizar se necessário.
- [ ] Comprimir JPGs (~2-4 MB cada) e converter para WebP.
- [ ] Deploy em Vercel.

## Decisions Made

### Paleta da Marca (aplicada nas CSS custom properties)
- Bege: `#f5efe3` (background principal)
- Bege deep: `#eadfc9`
- Cream: `#faf6ec`
- Azul: `#7aa3bf` / `#5c86a4` (deep) / `#b8d0de` (mist)
- Rosa: `#f6cac4`
- Gold: `#d9a658` / `#f2d196` (light)
- Ink (navy): `#1f2d3d`

### Tipografia
- Noto Serif Display (Google Fonts) — headlines e elementos italic
- Outfit (Google Fonts) — corpo, nav, CTAs
- Peso: 300 como base (editorial), italic para ênfase

### Design System
- Radii: 14/22/32px (sm/md/lg)
- Easing: cubic-bezier custom (`--ease`, `--ease-out`, `--ease-soft`) — zero linear/ease-in-out
- Grain SVG fixo (mix-blend multiply, opacity 0.45)
- Cards double-bezel em especialidades e contato
- Todos os botões com island arrow (arrow em círculo próprio)
- Magnetic effect em todos CTAs

### Stack
- Single HTML com CSS e JS inline
- CDN: Lenis 1.1.18
- Fotos em `assets/fotos/` (7 retratos DGP*.JPG)
- Grafismos em `assets/brand/` (Grafismos, Estampas, Logos)
- Sem dependência de GSAP — tudo em JS vanilla com IntersectionObserver + Lenis events

## Known Issues / Blockers
- Placeholders de contato (WhatsApp, CRM, cidade) ainda precisam dos dados reais.
- JPGs grandes (precisam otimização antes do deploy).

## Resume From Here
LP v2 cinematográfica está completa e foi verificada visualmente (11 screenshots, 0 erros de console). Para deploy:
1. Trocar `5500000000000` pelo número real e `CRM-XX XXXXXX` pelo CRM/RQE reais.
2. Otimizar fotos: comprimir e gerar WebP (imagens hoje pesam ~2-4 MB cada).
3. Deploy via Vercel (`vercel deploy`).
