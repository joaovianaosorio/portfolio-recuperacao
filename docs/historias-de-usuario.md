# Histórias de Usuário e Critérios de Aceitação

Este documento detalha todas as Histórias de Usuário (US) mapeadas para o projeto do Portfólio Pessoal e Acadêmico, divididas por seu nível de priorização no escopo.

---

## 🟢 1. Histórias de Usuário — MUST HAVE (MVP)

### US01: Apresentação Pessoal, Acadêmica e Hobbies Enxutos
* **Como** recrutador de tecnologia ou avaliador acadêmico,
* **Quero** visualizar a apresentação do autor, sua formação no IFSP e seus hobbies de forma rápida,
* **Para que** eu possa compreender o perfil pessoal, acadêmico e comportamental do desenvolvedor sem perder tempo.

#### Critérios de Aceitação:
1. Existência de uma seção inicial (*Hero/Sobre Mim*) contendo nome completo, foto de perfil profissional, título (ex: "Desenvolvedor Full-Stack em Formação") e biografia sucinta.
2. Existência de um bloco dedicado à Formação Acadêmica detalhando o curso de Análise e Desenvolvimento de Sistemas no IFSP, período atual e previsão de conclusão.
3. Existência de um bloco final enxuto de Hobbies e Interesses exibido em formato de badges visuais elegantes (ex: "Tecnologia", "Xadrez", "Leitura", "Viagens") sem poluir a leitura principal.

---

### US02: Galeria de Projetos e Competências Técnicas
* **Como** recrutador de tecnologia,
* **Quero** explorar a galeria de projetos práticos e o quadro de competências técnicas com links externos,
* **Para que** eu possa avaliar as habilidades práticas, o nível de código e ver os projetos rodando ao vivo.

#### Critérios de Aceitação:
1. Exibição de *cards* responsivos de projetos contendo imagem/mockup, nome do projeto, breve descrição, status (ex: "Concluído" ou "Em Desenvolvimento") e badges das tecnologias empregadas.
2. Cada *card* de projeto deve dispor de dois botões/links funcionais: direcionamento para a demonstração ao vivo (*Deploy*) e para o repositório público no GitHub.
3. Projetos "Em Desenvolvimento" devem ter indicação visual clara e transparência quanto ao estado atual, sem links quebrados.
4. Existência de uma seção visual com ícones/badges indicando linguagens, ferramentas e competências técnicas dominadas.

---

### US03: Visualização e Download do Currículo em PDF
* **Como** recrutador de tecnologia,
* **Quero** visualizar diretamente ou baixar o currículo do autor em formato PDF,
* **Para que** eu possa salvá-lo nos arquivos da empresa ou compartilhá-lo com a equipe de engenharia/RH.

#### Critérios de Aceitação:
1. Existência de um botão funcional identificado para realizar o download direto do currículo (`assets/pdf/curriculo-joao.pdf`).
2. Existência de um botão identificado para abrir a visualização do PDF em uma nova guia do navegador (`target="_blank"`).

---

### US04: Canais de Contato Direto (WhatsApp e E-mail)
* **Como** recrutador interessado,
* **Quero** entrar em contato rápido via WhatsApp ou e-mail com um único clique,
* **Para que** eu possa agendar uma entrevista técnica ou tirar dúvidas sobre o perfil do candidato.

#### Critérios de Aceitação:
1. Botão de CTA (*Call to Action*) em destaque que abra diretamente o aplicativo/web do WhatsApp com o número preenchido e mensagem inicial personalizada.
2. Formulário ou link de contato que permita enviar uma mensagem direta por e-mail via cliente nativo (`mailto:`) ou integração estática via Formspree.

---

### US05: Responsividade e Adaptabilidade Multiplataforma
* **Como** visitante acessando via celular, tablet ou computador,
* **Quero** visualizar o portfólio perfeitamente adaptado ao tamanho da minha tela,
* **Para que** a navegação seja fluida e sem elementos sobrepostos ou barras de rolagem quebradas.

#### Critérios de Aceitação:
1. Layout totalmente responsivo utilizando CSS Flexbox, Grid e Media Queries.
2. Menu de navegação adaptável para telas móveis (ex: menu hambúrguer simples em JS nativo).
3. Testado e funcional em navegadores modernos (Chrome, Firefox, Edge, Safari).

---

## 🟡 2. Histórias de Usuário — SHOULD HAVE (MVP+)

### US06: Alternador de Tema Claro e Escuro (Dark Mode)
* **Como** visitante,
* **Quero** alternar entre o modo escuro e o modo claro através de um botão no menu,
* **Para que** eu tenha maior conforto visual dependendo da iluminação do meu ambiente.

#### Critérios de Aceitação:
1. Botão/ícone seletor de tema visível no cabeçalho.
2. Clique altera dinamicamente a classe CSS no elemento `body`, atualizando a paleta de cores instantaneamente.
3. A preferência do usuário deve ser salva e recuperada no `localStorage` do navegador.

---

### US09-B: Animações de Rolagem (Scroll Reveal Nativo)
* **Como** visitante,
* **Quero** que os elementos da página apareçam suavemente conforme eu rolo a tela,
* **Para que** a experiência de navegação seja mais dinâmica e atraente.

#### Critérios de Aceitação:
1. Implementação nativa via API `IntersectionObserver` em JavaScript puro.
2. Efeito discreto de fade-in ou slide-up nos cards de projetos e seções principais.

---

## ⚪ 3. Histórias de Usuário — COULD HAVE (Versões Futuras / v2)

### US07: Alternador de Idioma (Português / Inglês)
* **Como** recrutador internacional,
* **Quero** alternar o idioma do site para o inglês,
* **Para que** eu possa avaliar o perfil do autor em vagas globais.

### US08: Filtro de Alto Contraste
* **Como** visitante com baixa visão ou daltonismo,
* **Quero** aplicar um modo de alto contraste no site,
* **Para que** os elementos tenham diferenciação de cor máxima.

### US09-A: Controle de Tamanho de Fonte (A+ / A-)
* **Como** visitante,
* **Quero** aumentar ou diminuir a fonte do texto diretamente pelo menu,
* **Para que** a leitura seja mais acessível.
