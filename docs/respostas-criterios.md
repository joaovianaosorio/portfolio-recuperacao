# Respostas aos Critérios Metodológicos da Atividade

Este documento consolida as respostas teóricas e práticas exigidas para a entrega da recuperação do projeto existente, detalhando o uso da ferramenta Impeccable e os conceitos de qualidade de software aplicados ao portfólio.

---

## 1. Finalidade dos Comandos e Ações do Impeccable

O ecossistema do Impeccable opera através de um fluxo estruturado que separa planejamento, refinamento e auditoria para evitar alterações precipitadas no código-fonte:

* **Comandos Core de Governança:**
  - **`/impeccable shape`**: Realiza o planejamento inicial e gera a documentação de produto (`PRODUCT.md` e `DESIGN.md`), estabelecendo a fundação visual e os objetivos antes de mexer no código.
  - **`/impeccable polish`**: Aplica as diretrizes visuais estabelecidas no design system diretamente nos arquivos de estilo (`style.css`), padronizando cores, espaçamentos e componentes.
  - **`/impeccable audit`**: Inspeciona a aplicação em múltiplos *breakpoints*, avaliando acessibilidade, semântica e conformidade sem modificar os arquivos.
* **Ações Granulares e Subcomandos de Correção (Identificados no relatório):**
  - **`/impeccable optimize`**: Focado em melhorias de performance (como lazy-loading de imagens e limitação de propriedades pesadas como `will-change`).
  - **`/impeccable harden`**: Direcionado à correção de marcações literais ou vulnerabilidades semânticas no texto da interface.
  - **`/impeccable typeset`**: Ajusta a escala tipográfica, espaçamentos de títulos (*kickers*) e hierarquia de fontes.

---

## 2. Identificação de Problemas Visuais, Funcionais e Técnicos

Durante a auditoria do portfólio, os problemas encontrados foram classificados em três frentes distintas:

1. **Problemas Visuais (UI):** Inconsistências de layout, alinhamentos incorretos ou hierarquias de cores mal aplicadas que afetam a primeira impressão do recrutador.
2. **Problemas Funcionais (UX/Comportamento):** Falhas de comportamento interativo na interface, tais como links de e-mail (`mailto:`) divergentes do texto visível ou menus de navegação móvel que não alternam corretamente seus estados.
3. **Problemas Técnicos e de Acessibilidade (A11y/Code Quality):** Questões de conformidade com normas web (como razões de contraste de cores abaixo do padrão WCAG AA, ausência de atributos ARIA dinâmicos como `aria-expanded`, e falta de suporte a `prefers-reduced-motion`).

---

## 3. Diferenciação: Avaliação Estética vs. Auditoria Técnica vs. Refinamento Visual

| Categoria | Definição e Foco | Exemplo Prático no Projeto |
| :--- | :--- | :--- |
| **Avaliação Estética** | Análise qualitativa e subjetiva do tom visual, da identidade e da mensagem que o produto passa ao público-alvo. | Avaliar se a paleta azul/violeta e a metáfora de "Laboratório de Projetos" transmitem confiança e objetividade para recrutadores de TI. |
| **Auditoria Técnica** | Inspeção rigorosa, matemática e normativa do código-fonte, focando em padrões de acessibilidade, semântica e desempenho. | Constatar por meio de testes automatizados que um texto secundário possui contraste de `3.07:1` (abaixo da meta de `4.5:1`) ou que faltam tags ARIA. |
| **Refinamento Visual** | Ação prática de modificação e ajuste nos arquivos de estilo e marcação com base nas diretrizes estabelecidas. | Executar o comando `/impeccable polish` para atualizar variáveis de cores, espaçamentos e estados de *hover* no `style.css`. |