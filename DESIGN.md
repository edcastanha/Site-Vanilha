---
name: ITS3
description: Site institucional da ITS3, hardware de simulação para eSport SimRacing
colors:
  primary: "#e2231a"
  primary-hover: "#ff4436"
  accent-confetti: "#ff8a3d"
  bg-base: "#0b0c0f"
  surface: "#15171c"
  surface-card: "#1c1f26"
  ink: "#eef0f3"
  ink-body: "#c7c9d1"
  ink-muted: "#9a9da6"
typography:
  display:
    fontFamily: "Raleway, sans-serif"
    fontSize: "52px"
    fontWeight: 800
    lineHeight: 1.15
    letterSpacing: "1px"
  headline:
    fontFamily: "Poppins, sans-serif"
    fontSize: "36px"
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: "normal"
  label:
    fontFamily: "Poppins, sans-serif"
    fontSize: "14px"
    fontWeight: 700
    lineHeight: 1.3
    letterSpacing: "2px"
  body:
    fontFamily: "Titillium Web, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: "normal"
rounded:
  sm: "4px"
  md: "8px"
  lg: "10px"
  pill: "50px"
  circle: "50%"
spacing:
  sm: "12px"
  md: "20px"
  lg: "30px"
  xl: "60px"
  xxl: "80px"
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "#ffffff"
    rounded: "{rounded.sm}"
    padding: "14px 34px 14px 26px"
  button-primary-hover:
    backgroundColor: "#ffffff"
    textColor: "{colors.primary}"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.primary}"
    rounded: "{rounded.sm}"
    padding: "12px 32px"
  nav-link:
    backgroundColor: "transparent"
    textColor: "#ffffff"
    rounded: "{rounded.pill}"
    padding: "5px 15px 7px 15px"
  nav-link-active:
    backgroundColor: "{colors.primary}"
    textColor: "#ffffff"
    rounded: "{rounded.pill}"
  card-surface:
    backgroundColor: "{colors.surface-card}"
    textColor: "{colors.ink}"
    rounded: "{rounded.lg}"
    padding: "30px"
  logo-badge:
    backgroundColor: "{colors.primary}"
    textColor: "#ffffff"
    rounded: "6px"
    size: "26px"
---

# Design System: ITS3

## 1. Overview

**Creative North Star: "O Box de Corrida"**

O sistema visual da ITS3 é o box de uma equipe de corrida à noite: escuro, funcional, sem enfeite — e um único vermelho de alta visibilidade que marca onde a ação acontece (o CTA, o estado ativo, o alerta). Nada aqui tenta parecer acolhedor ou "amigável"; a marca vende hardware de precisão (volantes, aros, bases F4R) para simracers e pilotos, então a interface deve comunicar seriedade técnica antes de qualquer coisa. O laranja/coral do confete do logo aparece raramente, como uma luz secundária de painel — nunca como protagonista.

Este sistema rejeita explicitamente a estética de "landing page de agência": fundo branco, botões pill em tom pastel, sombras azuladas suaves, tipografia genérica de SaaS (Open Sans/Inter). Era exatamente isso que o site tinha antes do reskin, e é o anti-padrão que este documento existe para evitar que volte.

**Key Characteristics:**
- Fundo quase preto (`#0b0c0f`) em toda a página; nunca branco.
- Vermelho (`#e2231a`) como único acento de ação; usado com moderação deliberada.
- Cards angulares e diretos — cantos majoritariamente retos, com corte diagonal (`clip-path`) reservado aos CTAs principais.
- Tipografia técnica (Titillium Web no corpo) em vez de fontes de SaaS genérico.
- Profundidade via glow vermelho sutil no hover, não sombra tradicional.

## 2. Colors

Paleta de alto contraste: um único acento quente (vermelho) sobre uma base neutra quase preta, com um segundo acento (coral) reservado para toques raros de personalidade.

### Primary
- **Vermelho ITS3** (`#e2231a`): extraído do badge do "3" no logo real da marca (@its3.br). Usado em CTAs, links, estados ativos/hover de navegação, bordas de destaque e ícones em foco. É o único acento que carrega peso de ação na interface.
- **Vermelho Aceso** (`#ff4436`): variante mais clara do primário. Duplo papel: feedback de `:hover` sobre o próprio vermelho (back-to-top), e **cor de texto** sempre que vermelho aparece como texto direto sobre o fundo escuro (links, kicker de seção, itens de navegação) — `#e2231a` puro só atinge 4.2:1 de contraste sobre `#0b0c0f` (abaixo do mínimo AA de 4.5:1 para texto normal); `#ff4436` atinge 5.7:1. `#e2231a` continua sendo o vermelho de fundo/badge (texto branco sobre ele já passa em AA).

### Secondary
- **Coral Confete** (`#ff8a3d`): extraído dos pontinhos de confete ao redor do logo. Reservado a detalhes raros — o traço sob o rótulo de seção, o subtítulo dos cargos da equipe, a hashtag da hero. Nunca disputa espaço com o vermelho no mesmo componente.

### Neutral
- **Preto Pista** (`#0b0c0f`): fundo base de toda a página (`html`, `body`).
- **Cinza-Chumbo** (`#15171c`): superfície de seção quando uma seção precisa se destacar sutilmente do fundo base (ex. `.team`, `.breadcrumbs`).
- **Cinza-Grafite** (`#1c1f26`): superfície de card — a camada mais clara da hierarquia de fundo, usada em cards de conteúdo (contato, equipe, portfolio-details, dropdown de navegação).
- **Branco-Gelo** (`#eef0f3`): texto primário/headings sobre qualquer fundo escuro.
- **Cinza-Névoa** (`#c7c9d1`): texto de corpo padrão (`body`), ligeiramente mais suave que o branco-gelo.
- **Cinza-Fumaça** (`#9a9da6`): texto secundário/legenda (subtítulos, metadados, texto muted).

### Named Rules
**A Regra do Vermelho Único.** Existe apenas um acento de ação por vez: vermelho. Se um componente já usa vermelho para o CTA, nenhum outro elemento no mesmo componente deve competir com uma segunda cor saturada — o coral fica para elementos puramente decorativos, nunca acionáveis.

## 3. Typography

**Display Font:** Raleway (com fallback `sans-serif`)
**Body Font:** Titillium Web (com fallback `sans-serif`)
**Label/Mono Font:** Poppins, para rótulos curtos e maiúsculos

**Character:** Raleway em peso alto (800) dá aos títulos grandes o ar técnico-agressivo da marca; Titillium Web no corpo mantém a leitura confortável com uma textura ligeiramente mais "de engenharia" que uma humanista genérica (Open Sans/Inter) — é a mesma família usada em HUDs de simulador de corrida.

### Hierarchy
- **Display** (800, 52px, 1.15): título principal da hero (`#hero h2`), sempre uppercase com `letter-spacing: 1px`. O nome da marca dentro do título é destacado em vermelho (`#hero h2 span`).
- **Headline** (700, 36px, 1.2): título grande de cada seção (`.section-title p`), uppercase.
- **Label** (700, 14px, 1.3, uppercase, `letter-spacing: 2px`): o "kicker" vermelho acima de cada headline de seção (`.section-title h2`) e os itens de navegação (uppercase, `letter-spacing: 0.4px`).
- **Body** (400, 16px, 1.5): parágrafos de conteúdo. Limitado a `max-width: 65ch` nos blocos de texto corrido (about, cta, faq) para não estourar a linha em telas largas.

### Named Rules
**A Regra do Peso, Não do Tamanho.** A hierarquia agressiva vem de peso (800/700) e uppercase, não de tamanhos gigantes — o `clamp` de display fica em 52px, nunca acima disso; motorsport é sobre precisão, não escala.

## 4. Elevation

Sem sombras tradicionais de "cartão flutuante". A profundidade vem de duas camadas de fundo (`bg-base` → `surface` → `surface-card`, cada uma um degrau mais clara) e, na interação, de um glow vermelho sutil — como um painel que acende quando tocado, não uma sombra física.

### Shadow Vocabulary
- **Glow de Interação** (`box-shadow: 0 2px 20px rgba(226, 35, 26, 0.3)`): usado em `:hover` de cards (`.team .member:hover`, `.services .icon-box:hover`) para sinalizar interatividade sem introduzir uma sombra escura tradicional.
- **Sombra Estrutural** (`box-shadow: 0px 2px 15px rgba(0, 0, 0, 0.35)`): usada em repouso sob cards elevados sobre o fundo (contato, equipe, portfolio-details) apenas para separá-los levemente do fundo — nunca como efeito decorativo.

### Named Rules
**A Regra do Painel Aceso.** Nada "flutua" por padrão. Estados de repouso são quase planos; o glow vermelho só aparece como resposta a hover/focus, como uma luz de painel que acende quando o piloto toca o controle.

## 5. Components

### Buttons
- **Shape:** cantos majoritariamente retos com um corte diagonal sutil (`clip-path: polygon(0 0, 100% 0, 100% 70%, 92% 100%, 0 100%)`) nos CTAs principais (`.btn-get-started`, `.cta-btn`) — o único lugar do sistema com um ângulo não-retangular, reservado à ação mais importante da tela.
- **Primary:** fundo vermelho (`#e2231a`), texto branco, uppercase, `letter-spacing: 1.5px`, padding `14px 34px 14px 26px`.
- **Hover:** inversão para fundo branco / texto vermelho (`.cta .cta-btn:hover`) — nunca escurece, inverte.
- **Ghost/Outline (`.btn-learn-more`):** borda vermelha de 2px, fundo transparente, preenche de vermelho sólido no hover.
- **Nav pill (`.nav-menu a`):** formato pílula (`border-radius: 50px`), fundo transparente, uppercase, vermelho sólido só no hover/ativo — esta é a única família de botão que mantém o pill herdado do template original, por ser navegação e não CTA.

### Cards / Containers
- **Corner Style:** retos a levemente arredondados (`8px`–`10px`); nunca o pill usado nos botões de navegação.
- **Background:** `#1c1f26` (surface-card) sobre `#0b0c0f`/`#15171c`.
- **Shadow Strategy:** ver Elevation — sombra estrutural em repouso, glow vermelho no hover.
- **Border:** quando presente, sempre um traço fino vermelho translúcido (`rgba(226, 35, 26, 0.15–0.35)`), nunca cinza neutro.
- **Internal Padding:** `20px`–`30px`.

### Inputs / Fields
- Não há um formulário real ativo no site hoje (o formulário de contato do template está comentado; o contato usa cards de info + mapa incorporado). Se reativado, deve seguir `surface-card` como fundo e borda vermelha translúcida no foco, mantendo a mesma linguagem dos cards.

### Navigation
- Header fixo, fundo quase preto translúcido (`rgba(11, 12, 15, 0.92)`) que fecha para opaco (`0.97`) ao rolar, com uma linha inferior vermelha translúcida que intensifica no scroll.
- Logo é um wordmark HTML/CSS: "ITS" em branco (Raleway 800) + badge quadrado vermelho com o "3" (`.its3-logo-badge`), recriando o logo real da marca sem depender de imagem.
- Menu mobile (`.mobile-nav`) usa a mesma superfície de card escura com borda vermelha translúcida, nunca fundo branco.

### Hero Tag (componente de assinatura)
Um chip com borda vermelha translúcida e texto coral (`.hero-tag`) carrega a hashtag real da marca (`#JuntosSomosMaisFortes`) acima do título da hero — o único lugar onde a voz literal da marca (Instagram) aparece verbatim na interface.

## 6. Do's and Don'ts

### Do:
- **Do** usar `#0b0c0f` como fundo de página em toda seção nova; nunca introduzir branco como fundo de bloco de conteúdo.
- **Do** reservar o vermelho (`#e2231a`) para exatamente um elemento de ação por componente (link, CTA, estado ativo).
- **Do** usar o corte diagonal (`clip-path`) apenas nos CTAs primários da hero e da seção CTA — não espalhar esse tratamento para outros botões.
- **Do** manter parágrafos de corpo a `max-width: 65ch`.
- **Do** manter contraste WCAG AA (`≥4.5:1` texto normal, `≥3:1` texto grande) em qualquer novo par de cor sobre os fundos escuros do sistema — validar com `npx impeccable detect` antes de finalizar.

### Don't:
- **Don't** usar fundo branco ou cinza-claro (`#fff`, `#f8f8f8`) em blocos de conteúdo — é exatamente a estética de "template SaaS genérico" que este redesign existe para eliminar.
- **Don't** usar laranja/coral (`#ff8a3d`) em elementos clicáveis ou de ação — ele é decorativo, o vermelho é quem age.
- **Don't** usar Open Sans, Inter, Roboto ou qualquer fonte "de SaaS genérico" como fonte de corpo — o corpo é Titillium Web.
- **Don't** usar sombras azuladas suaves (`rgba(68, 88, 144, ...)`) como estratégia de elevação — a estratégia é glow vermelho no hover, sombra estrutural neutra em repouso.
- **Don't** aplicar `border-radius: 50px` (pill) em CTAs de ação — pill é reservado à navegação; CTAs usam o corte diagonal ou cantos retos.
