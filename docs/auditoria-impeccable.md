# Relatório de Auditoria Impeccable (auditoria-impeccable.md)

## 1. Visão Geral da Auditoria
- **Ferramenta Utilizada:** Módulo de Auditoria do Impeccable (`/impeccable audit`).
- **Escopo Analisado:** Estrutura semântica, responsividade, acessibilidade (a11y), contrastes de cores, interatividade por teclado/toque e conformidade com o design system estabelecido (`DESIGN.md`).
- **Objetivo:** Mapear de forma transparente os pontos fortes da implementação atual e identificar melhorias técnicas prioritárias para garantir a excelência do portfólio voltado a recrutadores de tecnologia.

---

## 2. Pontos Fortes Validados (O que está em conformidade)
Durante a inspeção automatizada e os testes visuais em múltiplos *breakpoints* (375px, 768px e 1440px), os seguintes itens obtiveram sucesso:
- **Responsividade e Layout:** O projeto passou com sucesso nos testes de *overflow*, mantendo a estabilidade visual em telas de dispositivos móveis, tablets e desktops.
- **Alternância de Tema:** O modo escuro e o modo claro funcionam de forma persistente e correta, preservando a semântica visual.
- **Navegação e Foco:** A base semântica HTML está bem estruturada, contando com suporte adequado a foco visível por teclado e elementos de navegação organizados.

---

## 3. Achados Priorizados (Pontos de Atenção e Correção)

A auditoria identificou pontos específicos que exigem ajustes finos para elevar o rigor técnico e a acessibilidade do portfólio:

### A. Contraste de Cores (Acessibilidade / WCAG)
- **Descrição:** Determinados elementos textuais e secundários apresentaram taxas de contraste abaixo da recomendação ideal para leitura normal (limiar de 4.5:1):
  - Texto secundário (`#64748b`) em superfície escura obteve razão de `3.07:1`.
  - Texto auxiliar claro registrou `2.56:1`.
  - Link padrão no tema claro (`primary-blue`) obteve `3.52:1`.
  - O botão de WhatsApp registrou `1.98:1`.
- **Ação Recomendada:** Ajustar a opacidade ou o tom das cores no `DESIGN.md` e no `style.css` para garantir conformidade total com os critérios de contraste de acessibilidade.

### B. Inconsistência no Link de Contato por E-mail
- **Descrição:** O atributo `href="mailto:..."` no código HTML aponta para um endereço de correio eletrónico divergente daquele exibido de forma visual no texto da interface.
- **Ação Recomendada:** Sincronizar o endereço de e-mail do link funcional com o texto visível ao recrutador.

### C. Acessibilidade do Menu Mobile
- **Descrição:** O botão de menu para dispositivos móveis inicia sem os atributos dinâmicos essenciais para leitores de tela (`aria-expanded` e `aria-controls`), e o rótulo de texto permanece estático ("Abrir Menu") mesmo quando o menu já se encontra aberto.
- **Ação Recomendada:** Atualizar os seletores em JavaScript para alternar o estado de `aria-expanded` e o texto descritivo conforme a abertura ou fecho do menu.

### D. Textos Alternativos (`alt`) nas Imagens de Projetos
- **Descrição:** Os atributos `alt` das imagens associadas aos cards de projetos contêm descrições genéricas que diferem dos títulos reais apresentados nos cartões.
- **Ação Recomendada:** Revisar os textos alternativos para refletirem com precisão o conteúdo visual de cada projeto, melhorando a indexação e a acessibilidade para leitores de tela.

### E. Otimização de Animações e Movimento Reduzido
- **Descrição:** A propriedade `will-change` está aplicada de forma global aos elementos de animação de entrada (*reveal*), e falta uma regra de suporte para `prefers-reduced-motion`.
- **Ação Recomendada:** Restringir o uso de `will-change` para evitar consumo desnecessário de memória e adicionar a diretiva `@media (prefers-reduced-motion: reduce)` para desativar animações em usuários com sensibilidade a movimento.

---

## 4. Conclusão da Auditoria
O projeto apresenta uma base técnica sólida e funcional, perfeitamente alinhada com as premissas de um portfólio de estágio. Os achados listados neste relatório servem como roteiro para as melhorias incrementais de qualidade de código (Code Quality) e acessibilidade (A11y).