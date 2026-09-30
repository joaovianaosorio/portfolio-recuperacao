# Definição do MVP - Portfólio Pessoal e Acadêmico (IFSP)

## 1. Visão Geral e Fluxo Central
O MVP é uma aplicação web estática (HTML5 semântico, CSS3 e Vanilla JS ES6+) focada em apresentar a trajetória acadêmica e os projetos práticos do aluno para recrutadores de tecnologia (vagas de estágio) e professores do IFSP.

**Fluxo Central do Usuário (Recrutador/Professor):**
1. Acessar a página e visualizar o perfil profissional no Hero (Nome, ADS - IFSP, Objetivo de Estágio).
2. Explorar as competências técnicas e a seção enxuta de Hobbies/Interesses.
3. Avaliar a galeria de projetos, abrindo a demonstração ao vivo (Deploy) ou o código-fonte no GitHub.
4. Baixar/visualizar o currículo em PDF ou clicar no botão de CTA do WhatsApp/E-mail.

---

## 2. Escopo da Primeiras Versão (O que ENTRA no MVP)

* **Hero Section & Sobre Mim:** Nome, foto/avatar profissional, formação em ADS no IFSP, biografia curta e bloco de Hobbies em badges visuais.
* **Competências & Galeria de Projetos:**
  * Quadro de badges com tecnologias dominadas (C, JavaScript, HTML5, CSS3, Git).
  * Cards responsivos de projetos (concluídos e em desenvolvimento) com título, descrição, badges e links testados de Deploy e GitHub.
* **Currículo PDF:** Botões funcionais para download direto (`assets/pdf/curriculo-joao.pdf`) e abertura em nova guia (`target="_blank"`).
* **Canais de Contato:** Botão direto para WhatsApp com mensagem pré-formatada e link para e-mail via `mailto:` ou Formspree.
* **Efeitos Visuais & Interatividade:**
  * Alternador de Tema Claro e Escuro (Dark Mode) no topo com salvamento em `localStorage`.
  * Aparição suave dos cards (*Scroll Reveal*) nativa via API `IntersectionObserver`.
* **Design Responsivo:** Adaptabilidade para mobile, tablet e desktop sem quebra de layout.

---

## 3. Funcionalidades Adiadas / Removidas

* **Adiado (v2):** Alternador de idioma (PT/EN), modo de Alto Contraste e botões de ajuste de fonte (A+/A-).
* **Removido:** Formulários e botões de orçamento para serviços *freelance*, backend com banco de dados e frameworks externos (jQuery, React, GSAP, etc.).