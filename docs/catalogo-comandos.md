# Catálogo Oficial de Comandos do Impeccable

Este catálogo documenta os 23 comandos da ferramenta Impeccable, detalhando suas categorias, finalidades, momentos de uso, exemplos, riscos e evidências de sucesso.

---

## 1. Comandos de Criação e Planejamento
1. **`init`**
   - **Categoria:** Criar
   - **Finalidade:** Inicializar a estrutura base de governança e metadados de design no repositório.
   - **Momento de uso:** No início absoluto de um projeto ou recuperação de interface.
   - **Exemplo:** `@workspace /impeccable init`
   - **Riscos:** Sobrescrever configurações existentes caso não haja cautela.
   - **Evidência:** Arquivos de configuração de design criados na raiz.
2. **`document`**
   - **Categoria:** Criar
   - **Finalidade:** Gerar documentação técnica detalhada do produto e especificações.
   - **Momento de uso:** Após a inicialização, para estruturar o `PRODUCT.md`.
   - **Exemplo:** `@workspace /impeccable document`
   - **Riscos:** Gerar documentação genérica desalinhada com o código real.
   - **Evidência:** Presença do arquivo `PRODUCT.md` validado.
3. **`shape`**
   - **Categoria:** Criar
   - **Finalidade:** Modelar a arquitetura visual e a metáfora do sistema de design.
   - **Momento de uso:** Na definição conceitual do layout (`DESIGN.md`).
   - **Exemplo:** `@workspace /impeccable shape`
   - **Riscos:** Definir metáforas incompatíveis com o público-alvo.
   - **Evidência:** Arquivo `DESIGN.md` estruturado com paleta e tipografia.
4. **`extract`**
   - **Categoria:** Criar
   - **Finalidade:** Extrair tokens de design e variáveis diretamente de códigos legados.
   - **Momento de uso:** Na análise de projetos pré-existentes.
   - **Exemplo:** `@workspace /impeccable extract`
   - **Riscos:** Capturar valores de cores inconsistentes ou hardcoded.
   - **Evidência:** Mapeamento completo de cores e fontes legadas.

## 2. Comandos de Avaliação e Diagnóstico
5. **`critique`**
   - **Categoria:** Avaliar
   - **Finalidade:** Realizar uma avaliação crítica qualitativa do design e da hierarquia visual.
   - **Momento de uso:** Logo após modelar a interface, antes do refinamento.
   - **Exemplo:** `@workspace /impeccable critique`
   - **Riscos:** Feedback muito subjetivo se o contexto não for bem fornecido.
   - **Evidência:** Relatório de pontos de melhoria visual.
6. **`audit`**
   - **Categoria:** Avaliar
   - **Finalidade:** Inspecionar acessibilidade (WCAG), semântica e responsividade de forma automatizada.
   - **Momento de uso:** Na fase de validação técnica do código.
   - **Exemplo:** `@workspace /impeccable audit`
   - **Riscos:** Apontar falsos positivos dependendo da renderização do ambiente.
   - **Evidência:** Relatório detalhado de contraste e conformidade a11y.
7. **`contrast`**
   - **Categoria:** Avaliar
   - **Finalidade:** Verificar especificamente as taxas de contraste de cores entre texto e fundo.
   - **Momento de uso:** Na auditoria de temas claro e escuro.
   - **Exemplo:** `@workspace /impeccable contrast`
   - **Riscos:** Ignorar estados de hover ou elementos desativados.
   - **Evidência:** Razões matemáticas de contraste atestando acima de 4.5:1.
8. **`responsive`**
   - **Categoria:** Avaliar
   - **Finalidade:** Testar o comportamento da interface em múltiplos breakpoints e detectar overflow.
   - **Momento de uso:** Durante a validação mobile-first.
   - **Exemplo:** `@workspace /impeccable responsive`
   - **Riscos:** Não simular adequadamente toques em dispositivos físicos reais.
   - **Evidência:** Layout estável sem quebras horizontais em 375px e 768px.
9. **`accessibility`**
   - **Categoria:** Avaliar
   - **Finalidade:** Checar o uso correto de tags ARIA, atributos alt e navegação por teclado.
   - **Momento de uso:** Na revisão final de código HTML/JS.
   - **Exemplo:** `@workspace /impeccable accessibility`
   - **Riscos:** Focar apenas em atributos estáticos sem testar o fluxo interativo.
   - **Evidência:** Relatório de conformidade com leitores de tela.

## 3. Comandos de Refinamento
10. **`polish`**
    - **Categoria:** Refinare
    - **Finalidade:** Aplicar ajustes finos de design system e variáveis no CSS.
    - **Momento de uso:** Após definir o `DESIGN.md`.
    - **Exemplo:** `@workspace /impeccable polish`
    - **Riscos:** Alterar acidentalmente regras de layout estrutural.
    - **Evidência:** Código CSS padronizado com as variáveis de cores corretas.
11. **`typeset`**
    - **Categoria:** Refinar
    - **Finalidade:** Ajustar a escala tipográfica, entrelinhas e espaçamentos de títulos.
    - **Momento de uso:** Na revisão de legibilidade dos textos.
    - **Exemplo:** `@workspace /impeccable typeset`
    - **Riscos:** Desalinhar a hierarquia visual caso o tamanho base mude abruptamente.
    - **Evidência:** Tipografia consistente (ex: Outfit + Inter).
12. **`tokens`**
    - **Categoria:** Refinar
    - **Finalidade:** Organizar e centralizar os tokens de design (cores, raios, espaçamentos).
    - **Momento de uso:** Na refatoração do arquivo de estilos.
    - **Exemplo:** `@workspace /impeccable tokens`
    - **Riscos:** Quebrar referências de classes legadas.
    - **Evidência:** Variáveis CSS centralizadas e semânticas.
13. **`theme`**
    - **Categoria:** Refinar
    - **Finalidade:** Calibrar as regras de transição entre o tema claro e o tema escuro.
    - **Momento de uso:** Ao implementar suporte a múltiplos temas.
    - **Exemplo:** `@workspace /impeccable theme`
    - **Riscos:** Conflitos de especificidade nas classes de cores.
    - **Evidência:** Alternância fluida e sem perda de contraste entre os temas.
14. **`layout`**
    - **Categoria:** Refinar
    - **Finalidade:** Otimizar o alinhamento de grids e flexboxes nos componentes.
    - **Momento de uso:** Na estruturação de cards e seções.
    - **Exemplo:** `@workspace /impeccable layout`
    - **Riscos:** Distorcer o fluxo de elementos em telas intermediárias.
    - **Evidência:** Distribuição harmônica dos elementos no container max-width.

## 4. Comandos de Simplificação
15. **`simplify`**
    - **Categoria:** Simplificar
    - **Finalidade:** Remover redundâncias e regras CSS duplicadas ou não utilizadas.
    - **Momento de uso:** Na limpeza de código pré-produção.
    - **Exemplo:** `@workspace /impeccable simplify`
    - **Riscos:** Apagar regras visuais acopladas a estados específicos.
    - **Evidência:** Redução do tamanho do arquivo CSS sem perda visual.
16. **`distill`**
    - **Categoria:** Simplificar
    - **Finalidade:** Resumir descrições textuais longas em blocos escaneáveis (Evidence-First).
    - **Momento de uso:** Na revisão de textos do portfólio.
    - **Exemplo:** `@workspace /impeccable distill`
    - **Riscos:** Omitir informações essenciais do perfil profissional.
    - **Evidência:** Textos objetivos de rápida leitura por recrutadores.
17. **`clean`**
    - **Categoria:** Simplificar
    - **Finalidade:** Limpar comentários obsoletos e lixo de código no HTML/CSS.
    - **Momento de uso:** Antes de gerar a versão final para entrega.
    - **Exemplo:** `@workspace /impeccable clean`
    - **Riscos:** Remover anotações de código úteis.
    - **Evidência:** Código limpo e padronizado.

## 5. Comandos de Preparação para Produção
18. **`optimize`**
    - **Categoria:** Preparar
    - **Finalidade:** Otimizar performance (lazy-loading, limitação de `will-change`).
    - **Momento de uso:** Na preparação final de assets e animações.
    - **Exemplo:** `@workspace /impeccable optimize`
    - **Riscos:** Afetar o tempo de carregamento de imagens críticas (LCP).
    - **Evidência:** Melhoria nos indicadores de performance e animações leves.
19. **`harden`**
    - **Categoria:** Preparar
    - **Finalidade:** Endurecer a segurança e corrigir marcações literais vulneráveis.
    - **Momento de uso:** Na revisão de formulários e links externos.
    - **Exemplo:** `@workspace /impeccable harden`
    - **Riscos:** Bloquear links legítimos se mal configurado.
    - **Evidência:** Links externos com `rel="noopener"` e sanitização aplicada.
20. **`validate`**
    - **Categoria:** Preparar
    - **Finalidade:** Validar a integridade estrutural do HTML e CSS contra erros de sintaxe.
    - **Momento de uso:** Na etapa final de controle de qualidade.
    - **Exemplo:** `@workspace /impeccable validate`
    - **Riscos:** Falsos positivos em pré-processadores.
    - **Evidência:** Zero erros de sintaxe nos validadores oficiais.

## 6. Comandos de Sistematização e Execução Final
21. **`preview`**
    - **Categoria:** Sistematizar
    - **Finalidade:** Gerar uma prévia interativa dos componentes isolados.
    - **Momento de uso:** Durante o desenvolvimento de novos blocos visuais.
    - **Exemplo:** `@workspace /impeccable preview`
    - **Riscos:** Divergência entre o ambiente de preview e o site real.
    - **Evidência:** Componentes testados individualmente.
22. **`sync`**
    - **Categoria:** Sistematizar
    - **Finalidade:** Sincronizar o design system documentado com o código implementado.
    - **Momento de uso:** Sempre que houver alteração de variáveis visuais.
    - **Exemplo:** `@workspace /impeccable sync`
    - **Riscos:** Conflitos de mesclagem em equipes colaborativas.
    - **Evidência:** Alinhamento de 100% entre `DESIGN.md` e `style.css`.
23. **`live`**
    - **Categoria:** Sistematizar
    - **Finalidade:** Validar a aplicação no ambiente de execução real ou hospedagem final.
    - **Momento de uso:** No encerramento e publicação do projeto.
    - **Exemplo:** `@workspace /impeccable live`
    - **Riscos:** Problemas de cache no navegador ou CDN.
    - **Evidência:** Aplicação rodando perfeitamente online e sem falhas de carregamento.