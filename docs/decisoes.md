# Registros de Decisões e Governança de IA (DECISOES.md)

## 1. Contexto e Prompts Utilizados
- **Prompt Mestre (Entrevista e Revisão):** Condução do planejamento em três fases (Analista de Produto, Revisor Crítico de Escopo e Construtor de Documentação) com foco em vaga de estágio e requisitos acadêmicos.

## 2. Análises Críticas e Histórico de Interações

### Interação 01 - Definição de Evidências e Contexto Inicial (Fase 1)
- **Pergunta da IA:** Solicitou evidências passadas de perda de oportunidades por falta de portfólio.
- **Análise Crítica:** A IA assumiu um histórico inexistente. Esclareci o momento de início de carreira.
- **Decisão:** Alinhado que o problema central é **prevenir a rejeição passiva** facilitando a avaliação rápida do recrutador.

### Interação 02 - Priorização de Público e Métrica de Sucesso (Fase 1)
- **Pergunta da IA:** Solicitou a escolha entre focar em Estágio de TI ou Captação de Freelances.
- **Análise Crítica:** Pergunta essencial para não criar uma interface genérica.
- **Decisão:** **Foco 100% em Estágio de TI**. Métricas de sucesso: chamadas para entrevistas técnicas e nota máxima na disciplina.

### Interação 03 - Fechamento da Fase 1 e Suposições
- **Análise Crítica:** A IA organizou bem as suposições de produto (tempo de atenção < 60s, deploy direto).
- **Decisão:** Aprovada a síntese, removendo formalmente o público de pequenos clientes do MVP.

### Interação 04 - Revisão Crítica do MVP e Corte de Escopo (Fase 2)
- **Propostas da IA:** Sugeriu remover Hobbies, Dark Mode, Scroll Animations e barrar projetos em desenvolvimento.
- **Análise Crítica:** 
  * *Hobbies:* A IA errou ao tentar remover; é um requisito obrigatório do professor.
  * *Dark Mode / Scroll:* A IA superestimou a complexidade. Em JS puro (com `localStorage` e `IntersectionObserver`), ambas são simples e viáveis.
  * *Projetos:* Serão mantidos sob minha inteira responsabilidade técnica de entrega.
- **Decisão Final de Escopo:** Hobbies mantidos de forma enxuta; Dark Mode e Scroll mantidos no escopo secundário; formulário de freela removido; contato ajustado para `mailto:`/Formspree.

---

## 3. Síntese do Produto e Suposições Validadas

### Problema Central
Alta fricção para recrutadores e avaliadores ao analisarem projetos dispersos no GitHub sem uma interface centralizada com demonstração ao vivo.

### Objetivo e Público
Criar um portfólio web moderno (HTML/CSS/JS) focando exclusivamente em **Recrutadores de TI** (busca por estágio) e **Avaliadores Acadêmicos** (nota da disciplina).

### Suposições do Projeto
1. **Tempo de Atenção:** Recrutadores dedicam menos de 60 segundos por perfil; cards visuais com deploy reduzem essa fricção.
2. **Projetos em Andamento:** Exibir projetos bem estruturados em desenvolvimento demonstra transparência e proatividade.
3. **Conversão de Contato:** Botão direto para WhatsApp/E-mail é o meio mais eficiente de retorno.
4. **Viabilidade:** O escopo estático com incrementos em JS puro é realizável no semestre.

---

## 4. Matriz Final de Aceites, Alterações e Rejeições da IA

| Item / Funcionalidade | Sugestão da IA | Decisão Final | Justificativa |
| :--- | :--- | :--- | :--- |
| **Público Freelance** | Incluir no MVP | **Rejeitado** | Foco exclusivo em vagas de estágio de TI. |
| **Seção de Hobbies** | Remover | **Alterado / Mantido** | Requisito obrigatório do professor. Será mantido de forma sintética. |
| **Dark Mode (JS puro)** | Adiar (Muito complexo) | **Alterado / Mantido** | Implementação simples via CSS/JS com `localStorage`. |
| **Scroll Animations** | Remover (Risco de bugs) | **Alterado / Mantido** | Viável em JS puro usando a API nativa `IntersectionObserver`. |
| **Projetos em Andamento**| Restringir | **Mantido** | Validados com garantia de ausência de links quebrados. |
| **Formulário com Backend**| Remover | **Aceito** | Substituído por `mailto:` / Formspree para manter o site estático. |

### Fechamento do Planejamento e Fase 3 (Documentação Estática)
- **Análise Crítica:** A IA compilou com precisão todas as especificações e regras de arquitetura nos arquivos `documentacao.md`, `historias-de-usuario.md` e `arquitetura-e-layout.md`.
- **Decisão:** Aprovada a estrutura oficial estática do projeto. Os arquivos foram organizados na pasta `docs/` mantendo total separação em relação ao código fonte que será programado na IDE.

### Ajuste Fino de Implementação (Fase de Código)
- **Ocorrência:** O layout inicial gerado pela IDE apresentou falhas de quebra de grid em telas mobile e a omissão do badge de Viagens.
- **Ação:** Solicitada a correção das Media Queries no CSS (`css/style.css`) e a inserção do elemento do Font Awesome (`fa-plane`) no HTML (`index.html`) para alinhar 100% o código com a US01 e US05 da documentação.