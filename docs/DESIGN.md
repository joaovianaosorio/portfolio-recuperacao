---
name: Portfólio Pessoal e Acadêmico — João
description: Laboratório de projetos que apresenta competências, formação e evidências práticas para recrutadores de tecnologia.
colors:
  primary-blue: "#3b82f6"
  blue-hover: "#2563eb"
  accent-violet: "#8b5cf6"
  accent-gradient: "linear-gradient(135deg, #3b82f6 0%, #8b5cf6 100%)"
  dark-bg-primary: "#0f172a"
  dark-bg-secondary: "#1e293b"
  dark-bg-card-hover: "#334155"
  dark-nav: "rgba(15, 23, 42, 0.85)"
  dark-text-primary: "#f8fafc"
  dark-text-secondary: "#94a3b8"
  dark-text-muted: "#64748b"
  dark-border: "#334155"
  dark-border-subtle: "rgba(255, 255, 255, 0.08)"
  light-bg-primary: "#f8fafc"
  light-bg-secondary: "#ffffff"
  light-bg-card-hover: "#f1f5f9"
  light-nav: "rgba(248, 250, 252, 0.85)"
  light-text-primary: "#0f172a"
  light-text-secondary: "#475569"
  light-text-muted: "#94a3b8"
  light-border: "#e2e8f0"
  light-border-subtle: "rgba(0, 0, 0, 0.06)"
  success: "#10b981"
  warning: "#f59e0b"
  whatsapp: "#25d366"
  whatsapp-hover: "#1eb956"
  document-red: "#ef4444"
typography:
  display:
    fontFamily: "Outfit, sans-serif"
    fontSize: "3.25rem"
    fontWeight: 800
    lineHeight: 1.2
    letterSpacing: "-0.5px"
  headline:
    fontFamily: "Outfit, sans-serif"
    fontSize: "2.25rem"
    fontWeight: 800
    lineHeight: 1.2
  title:
    fontFamily: "Outfit, sans-serif"
    fontSize: "1.35rem"
    fontWeight: 700
    lineHeight: 1.2
  body:
    fontFamily: "Inter, -apple-system, BlinkMacSystemFont, sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.6
  label:
    fontFamily: "Inter, -apple-system, BlinkMacSystemFont, sans-serif"
    fontSize: "0.85rem"
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: "2px"
rounded:
  sm: "6px"
  md: "12px"
  lg: "20px"
  full: "9999px"
spacing:
  xs: "0.5rem"
  sm: "1rem"
  md: "1.5rem"
  lg: "2rem"
  xl: "3rem"
  section-desktop: "6rem"
  section-mobile: "4rem"
  container-max: "1200px"
components:
  button-primary:
    backgroundColor: "{colors.accent-gradient}"
    textColor: "#ffffff"
    rounded: "{rounded.md}"
    padding: "0.85rem 1.75rem"
    typography: "{typography.body}"
  button-secondary:
    backgroundColor: "{colors.dark-bg-secondary}"
    textColor: "{colors.dark-text-primary}"
    rounded: "{rounded.md}"
    padding: "0.85rem 1.75rem"
  card:
    backgroundColor: "{colors.dark-bg-secondary}"
    textColor: "{colors.dark-text-primary}"
    rounded: "{rounded.lg}"
    padding: "2rem"
  tag:
    backgroundColor: "{colors.dark-bg-card-hover}"
    textColor: "{colors.dark-text-secondary}"
    rounded: "{rounded.sm}"
    padding: "0.25rem 0.65rem"
---

# Design System: Portfólio Pessoal e Acadêmico — João

## Overview

**Creative North Star: "Laboratório de projetos"**

O portfólio combina uma apresentação pessoal objetiva com evidências concretas de trabalho. A interface deve ajudar recrutadores a reconhecer rapidamente formação, competências e projetos, mantendo a pessoa por trás do trabalho visível. A linguagem existente é tecnológica e energética, mas sua hierarquia serve primeiro à leitura e à avaliação profissional.

O tema escuro é o padrão e há uma versão clara com os mesmos papéis de cor. Azul é o acento condutor; violeta complementa o gradiente e aparece em destaques pontuais. Cards, imagens de projetos e a foto profissional dão estrutura e contexto, enquanto sombras e movimentos curtos destacam estados interativos.

**Key Characteristics:**
- Confiança e objetividade na apresentação profissional.
- Projetos como evidência, com links para código e demonstrações quando disponíveis.
- Azul como acento principal e violeta como complemento.
- Temas escuro e claro com papéis semânticos correspondentes.
- Layout responsivo, com hierarquia preservada em telas estreitas.

## Colors

A paleta combina superfícies frias de alto contraste com acentos digitais; o modo claro inverte as superfícies e o texto sem mudar o papel do azul.

### Primary
- **Azul de interface** (`primary-blue`): conduz links, foco, ícones e estados ativos; é o acento mais recorrente.
- **Azul de interação** (`blue-hover`): variação de hover para ações e links.

### Secondary
- **Violeta de destaque** (`accent-violet`): complementa o azul em metadados e no gradiente de marca, sem competir com ações primárias.
- **Gradiente azul-violeta** (`accent-gradient`): assinatura aplicada ao botão principal, ao texto destacado e a detalhes da identidade.

### Neutral
- **Ardósia noturna** (`dark-bg-primary`): fundo principal do tema escuro.
- **Superfície ardósia** (`dark-bg-secondary`): navegação e superfícies de cards no tema escuro.
- **Elevação ardósia** (`dark-bg-card-hover`): superfície de hover e elementos internos no tema escuro.
- **Texto claro** (`dark-text-primary`), **texto secundário frio** (`dark-text-secondary`) e **texto auxiliar** (`dark-text-muted`): níveis de leitura no tema escuro.
- **Borda ardósia** (`dark-border`) e **divisor translúcido** (`dark-border-subtle`): contornos e separação no tema escuro.
- **Fundo claro** (`light-bg-primary`), **superfície branca** (`light-bg-secondary`) e **superfície de hover clara** (`light-bg-card-hover`): superfícies do tema claro.
- **Texto escuro** (`light-text-primary`), **texto secundário** (`light-text-secondary`) e **texto auxiliar claro** (`light-text-muted`): níveis de leitura no tema claro.
- **Borda clara** (`light-border`) e **divisor translúcido claro** (`light-border-subtle`): contornos e separação no tema claro.
- **Verde de sucesso** (`success`) e **âmbar de andamento** (`warning`): indicam estados dos projetos concluídos e em andamento.
- **Verde de contato** (`whatsapp` e `whatsapp-hover`): identifica a ação de WhatsApp.
- **Vermelho de documento** (`document-red`): identifica visualmente o PDF do currículo.

**The Accent Hierarchy Rule.** Azul identifica ações e foco; violeta complementa a assinatura visual, sem substituir a prioridade do azul.

## Typography

**Display Font:** Outfit (com fallback sans-serif)
**Body Font:** Inter (com fallback para -apple-system, BlinkMacSystemFont e sans-serif)
**Label/Mono Font:** Inter; não há família monoespaçada definida no sistema atual.

**Character:** Outfit dá presença aos títulos sem perder legibilidade; Inter sustenta leitura contínua e controles compactos. A hierarquia usa pesos expressivos nos títulos e pesos médios no texto funcional.

### Hierarchy
- **Display** (800, 3.25rem, line-height 1.2): título principal do hero; reduz em telas menores.
- **Headline** (800, 2.25rem, line-height 1.2): títulos de seção; varia conforme o breakpoint.
- **Title** (700, 1.35rem, line-height 1.2): títulos de cards e agrupamentos.
- **Body** (400, 1rem, line-height 1.6): texto corrido; descrições de perfil e conteúdo informativo podem usar line-height 1.7.
- **Label** (700, 0.85rem, line-height 1.2, tracking 2px, maiúsculas): subtítulos de seção; metadados usam tamanhos menores e tracking mais contido.

**The Evidence-First Type Rule.** Use títulos para deixar a seção escaneável e texto de corpo para contextualizar a evidência; não transforme descrições em blocos densos.

## Layout

O conteúdo alinha-se a um container central de até 1200px, com padding lateral de 1.5rem e redução para 1rem em telas de até 480px. Seções usam 6rem de respiro vertical em desktop, 4rem abaixo de 768px e 3rem abaixo de 480px. A unidade recorrente de composição é o espaço em múltiplos de 0.5rem, com gaps maiores entre grupos e seções.

No desktop, hero, formação, currículo e contato usam grids de duas colunas; a galeria de projetos e a grade de competências acomodam colunas conforme a largura disponível. Abaixo de 992px, os principais grids passam a uma coluna e o hero centraliza seu conteúdo. Abaixo de 768px, a navegação vira menu recolhido, os botões do hero e do currículo ocupam a largura disponível e os cards de projeto empilham suas ações. Abaixo de 480px, tipografia, padding e elementos de contato são compactados; competências ficam em duas colunas.

## Elevation & Depth

O sistema combina camadas de superfície com sombras. As superfícies distinguem fundo, card e hover; sombras reservam elevação para cards, botões e elementos sobrepostos. O tema claro reduz a opacidade das sombras para manter a profundidade sem escurecer as superfícies.

### Shadow Vocabulary
- **Baixa (`shadow-sm`):** `0 4px 6px -1px rgba(0, 0, 0, 0.3)` no tema escuro; separação discreta em cards. No tema claro, usa a mesma geometria com opacidade baixa.
- **Média (`shadow-md`):** `0 10px 15px -3px rgba(0, 0, 0, 0.4)` no tema escuro; botão primário e elevação intermediária.
- **Alta (`shadow-lg`):** `0 20px 25px -5px rgba(0, 0, 0, 0.5)` no tema escuro; imagem de perfil, cartão sobreposto e menu móvel.
- **Brilho azul (`glow-shadow`):** `0 0 25px rgba(59, 130, 246, 0.35)` no tema escuro; realce do botão principal e da imagem de perfil.

**The Stateful Elevation Rule.** Sombras e brilho reforçam a hierarquia ou uma interação; a distinção entre superfícies continua visível por cor e borda.

## Shapes

Os cantos variam conforme a função: controles compactos usam 6px, botões e cards menores 12px, e cards de destaque 20px. Pílulas são reservadas a badges e tags arredondadas. Bordas finas acompanham cards e controles; imagens de projeto são recortadas dentro do card, e o avatar recebe moldura em gradiente.

## Components

### Buttons
- **Caráter:** ações claramente diferenciadas por prioridade e contexto.
- **Shape:** cantos médios de 12px; ícone e rótulo ficam alinhados horizontalmente.
- **Primary:** gradiente azul-violeta, texto branco, padding de `0.85rem 1.75rem`, peso 600 e sombra média; no hover sobe 2px e recebe brilho azul.
- **Secondary:** superfície de card, borda e texto primários; no hover clareia a superfície, colore a borda de azul e sobe 2px.
- **WhatsApp:** verde dedicado à ação de contato, com sombra verde própria e variação de fundo no hover.
- **Focus:** contorno visível de 2px na cor primária com offset de 4px.
- **Mobile:** ações do hero e do currículo se expandem à largura do container; ações dos projetos empilham verticalmente.

### Chips
- **Style:** badges de hobby e competência usam superfície elevada, borda sutil, texto principal e formato pílula; tags de tecnologia usam formato compacto, raio de 6px e texto secundário.
- **State:** hover de hobby destaca borda e texto em azul; tags de status distinguem projetos concluídos em verde e em andamento em âmbar.

### Cards / Containers
- **Corner Style:** 12px para competências e 20px para projetos, perfil e contato.
- **Background:** superfície de card correspondente ao tema ativo, com borda de contraste sutil.
- **Shadow Strategy:** sombra baixa em repouso nos cards de perfil e projeto; cards de competências elevam no hover.
- **Border:** borda semântica que recebe destaque azul no hover.
- **Internal Padding:** 2rem em cards de perfil; 1.5rem em conteúdo de projeto; ajustes compactos em telas pequenas.
- **Project card:** imagem de 200px de altura, status sobreposto no canto superior, descrição, tags de tecnologia e ações de repositório/demonstração.

### Navigation
- **Desktop:** cabeçalho fixo com fundo translúcido e blur; links em texto secundário, com texto primário e linha de gradiente no hover e no item ativo.
- **Theme control:** botão circular de 42px para alternar tema.
- **Mobile:** botão de menu revela links em coluna sob o cabeçalho, com superfície secundária e sombra alta.

### Hero Profile
- A foto profissional é enquadrada em bloco de 320px, com padding de 8px, raio amplo, moldura em gradiente e sombra alta com brilho azul. O cartão de formação sobrepõe a imagem; em telas estreitas, a imagem reduz e o cartão volta ao fluxo do conteúdo.

## Do's and Don'ts

### Do:
- **Do** manter azul como cor de ação, link, foco e estado ativo.
- **Do** conservar o tema claro e o escuro com contraste semântico entre fundo, superfície e texto.
- **Do** apresentar tecnologias, projetos e status com tags e estados de cor já estabelecidos.
- **Do** manter foco de teclado visível e layouts funcionais em celular, tablet e desktop.
- **Do** usar Outfit em títulos e Inter em conteúdo e controles.

### Don't:
- **Don't** dar ao violeta mais prioridade que ao azul em ações primárias.
- **Don't** usar a cor de sucesso ou de andamento como decoração sem significado de status.
- **Don't** remover bordas, estados de hover ou foco que ajudam a identificar controles interativos.
- **Don't** apresentar métricas, depoimentos ou resultados profissionais sem evidência real.
- **Don't** introduzir uma terceira tipografia ou uma paleta alheia ao sistema existente sem uma decisão explícita de identidade.