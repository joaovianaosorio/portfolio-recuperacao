# Documentação do Projeto: Portfólio Pessoal e Acadêmico

## 1. Definição do Projeto

### 1.1 Nome do Projeto
**Portfólio Pessoal e Acadêmico — João**

### 1.2 Problema Atendido
Estudantes e desenvolvedores em início de carreira enfrentam alta fricção ao compartilhar seus projetos com recrutadores de tecnologia e avaliadores acadêmicos. Enviar repositórios avulsos do GitHub exige alta carga cognitiva do recrutador para entender o contexto, as tecnologias e a execução do projeto. O portfólio centraliza essas informações em uma interface web interativa, responsiva e de navegação rápida, apresentando demonstrações ao vivo (*deploys*) e o código-fonte organizado.

### 1.3 Objetivo Principal
Apresentar de forma clara, moderna e objetiva a trajetória acadêmica no IFSP, competências técnicas, galeria de projetos práticos e canais de contato direto. O foco principal é a **obtenção de vagas de estágio em tecnologia em grandes empresas** e a **aprovação com nota máxima na disciplina universitária**.

### 1.4 Público-Alvo
1. **Recrutadores de Tecnologia e Líderes Técnicos (Foco Principal):** Profissionais com pouco tempo de avaliação (30 a 60 segundos por perfil) buscando rapidamente validar habilidades em HTML, CSS, JavaScript, lógica e projetos práticos.
2. **Avaliadores Acadêmicos / Professores do IFSP:** Professores que buscam validar o cumprimento dos requisitos técnicos da disciplina, responsividade, organização do código e boas práticas de desenvolvimento web.

---

## 2. Proposta Visual e Diretrizes Técnicas

### 2.1 Proposta Visual
* **Identidade:** Interface moderna, limpa e futurista com tema escuro (*Dark Mode*) como padrão principal.
* **Paleta de Cores:** Fundo neutro escuro (tons de grafite, preto e cinza escuro) com destaques em azul vibrante ou roxo elétrico para chamar a atenção para botões CTA e badges de tecnologias.
* **Navegação & Animações:** Navegação suave (*Smooth Scroll*) e efeitos discretos de aparição dos elementos na tela (*Scroll Reveal*) nativos.

### 2.2 Requisitos Tecnológicos (Restrições Obrigatórias)
* **HTML5:** Estruturação 100% semântica (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`).
* **CSS3:** Estilização modular com Flexbox, CSS Grid, Custom Properties (variáveis CSS) e Keyframes para animações leves. Bootstrap 5 opcional para grid básico.
* **JavaScript:** ES6+ puro (*Vanilla JS*) para controle do Dark Mode (armazenado em `localStorage`), animação de scroll via `IntersectionObserver` nativo e interações do menu/formulário.
* **Restrição Absoluta:** **Proibido o uso de qualquer biblioteca ou framework JavaScript externo** (ex: jQuery, React, GSAP, AOS, etc.).

---

## 3. Escopo do MVP (Priorização MoSCoW)

### 3.1 Must Have (Indispensável para o MVP)
1. **Apresentação Profissional & Formação Acadêmica:** Seção "Sobre Mim" destacando o curso no IFSP, competências técnicas centrais e área de interesse para estágio, finalizando com uma subseção enxuta de Hobbies/Interesses em formato de badges/cards simples.
2. **Galeria de Projetos & Competências:** Cards visuais de projetos (concluídos e em desenvolvimento), com badges das tecnologias, descrição objetiva, link para o repositório no GitHub e link funcional para a demonstração ao vivo (*Deploy*).
3. **Disponibilização do Currículo em PDF:** Botões funcionais para download direto (`download`) e visualização em nova guia (`target="_blank"`), utilizando o arquivo armazenado localmente em `assets/pdf/curriculo-joao.pdf`.
4. **Canais de Contato Direto:** Botão destacado de CTA para WhatsApp direto (com mensagem pré-formatada) e link/formulário de contato via e-mail (`mailto:` ou serviço estático Formspree).
5. **Responsividade & Compatibilidade Multiplataforma:** Adaptação perfeita em celulares, tablets e computadores desktop via Media Queries nativas.

### 3.2 Should Have (Importante para a experiência visual)
- **Dark Mode / Light Mode Toggle:** Chave de alternância de tema no cabeçalho com persistência no `localStorage` via JavaScript nativo.
- **Scroll Reveal Nativo:** Revelação suave de elementos conforme a rolagem da página utilizando a API nativa `IntersectionObserver`.

### 3.3 Could Have (Adiado para versões futuras / v2)
- Alternador de Idioma (Português / Inglês) dinâmico via JS.
- Filtro de Alto Contraste para acessibilidade avançada.
- Botões de ajuste dinâmico de tamanho de fonte (A+ / A-).

### 3.4 Won't Have Now (Fora do Escopo Atual)
- Painel Administrativo / Backend com banco de dados.
- Seções, botões ou formulários direcionados à prospecção de serviços *freelance*.

---

## 4. Critérios de Aceite para Conclusão do MVP

1. **Requisitos de Conteúdo & Design:**
   * Todas as 5 histórias de usuário *Must Have* e as 2 *Should Have* totalmente implementadas e operacionais.
   * Layout responsivo sem barras de rolagem horizontal indesejadas em telas mobile (320px a 768px) e desktop (1024px+).
2. **Integridade de Links:**
   * 100% dos links (GitHub, Deploy, WhatsApp, E-mail e Currículo PDF) testados e sem erros 404 ou botões quebrados.
   * Projetos em desenvolvimento identificados com badge informativa clara.
3. **Qualidade do Código & Restrições:**
   * Código HTML limpo e validado sem tags depreciadas.
   * Nenhum framework JS ou biblioteca externa inclusa.
4. **Publicação:**
   * Projeto estático publicado e acessível publicamente via link público de *deploy* (GitHub Pages, Netlify ou Vercel).