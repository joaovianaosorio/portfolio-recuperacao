# Arquitetura e Guia de Estilo do Projeto

Este documento especifica a estrutura de arquivos do projeto, padrões de código, identidade visual e arquitetura de scripts nativos.

---

## 1. Estrutura de Diretórios do Projeto

A aplicação é estruturada como um projeto estático em HTML5, CSS3 e Vanilla JavaScript, organizada da seguinte forma:

```text
portfolio/
├── assets/
│   ├── images/
│   │   ├── avatar-joao.png
│   │   ├── favicon.ico
│   │   └── projects/
│   │       ├── projeto-1.jpg
│   │       ├── projeto-2.jpg
│   │       └── projeto-3.jpg
│   └── pdf/
│       └── curriculo-joao.pdf
├── css/
│   └── style.css
├── script/
│   └── main.js
├── docs/
│   ├── documentacao.md
│   ├── historias-de-usuario.md
│   └── arquitetura-e-layout.md
└── index.html
```

---

## 2. Identidade Visual & Design System

### 2.1 Paleta de Cores (CSS Custom Properties)

O design adota o tema **Dark/Futurista** por padrão, utilizando variáveis CSS nativas para facilitar a alternância no Dark Mode (US06).

```css
:root {
  /* Tema Escuro (Padrão) */
  --bg-primary: #0f172a;       /* Fundo principal (Slate 900) */
  --bg-secondary: #1e293b;     /* Cards e containers (Slate 800) */
  --bg-card-hover: #334155;    /* Hover nos cards (Slate 700) */
  
  --text-primary: #f8fafc;     /* Texto principal (Slate 50) */
  --text-secondary: #94a3b8;   /* Texto secundário (Slate 400) */
  --text-muted: #64748b;       /* Legendas e detalhes (Slate 500) */
  
  --accent-primary: #3b82f6;   /* Azul vibrante (Destaques e CTAs) */
  --accent-secondary: #8b5cf6; /* Roxo futurista (Gradients e Badges) */
  --accent-hover: #2563eb;     /* Hover de botões */
  
  --border-color: #334155;     /* Bordas sutis */
  --shadow-sm: 0 4px 6px -1px rgba(0, 0, 0, 0.3);
  --shadow-lg: 0 10px 15px -3px rgba(0, 0, 0, 0.5);
  
  --radius-sm: 6px;
  --radius-md: 12px;
  --radius-lg: 20px;
  
  --transition-fast: 0.2s ease;
  --transition-normal: 0.3s ease;
}

/* Tema Claro (Invertido via classe CSS no body) */
body.light-theme {
  --bg-primary: #f8fafc;
  --bg-secondary: #ffffff;
  --bg-card-hover: #f1f5f9;
  
  --text-primary: #0f172a;
  --text-secondary: #475569;
  --text-muted: #94a3b8;
  
  --border-color: #e2e8f0;
  --shadow-sm: 0 4px 6px -1px rgba(0, 0, 0, 0.05);
  --shadow-lg: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
}
```

---

## 3. Arquitetura JavaScript (`main.js`)

Todos os scripts são escritos em **JavaScript ES6+ puro**, encapsulados em funções ou módulos simples inicializados no evento `DOMContentLoaded`.

### 3.1 Módulo 1: Alternador de Tema (Dark/Light Mode)
```javascript
// Controle de Dark/Light mode com persistência no localStorage
function initThemeToggle() {
  const themeBtn = document.getElementById('theme-toggle');
  const currentTheme = localStorage.getItem('portfolio-theme') || 'dark';

  if (currentTheme === 'light') {
    document.body.classList.add('light-theme');
  }

  themeBtn?.addEventListener('click', () => {
    document.body.classList.toggle('light-theme');
    const isLight = document.body.classList.contains('light-theme');
    localStorage.setItem('portfolio-theme', isLight ? 'light' : 'dark');
  });
}
```

### 3.2 Módulo 2: Scroll Reveal com `IntersectionObserver`
```javascript
// Revelação suave de elementos na rolagem da página sem bibliotecas
function initScrollReveal() {
  const observerOptions = {
    root: null,
    threshold: 0.15
  };

  const observer = new IntersectionObserver((entries, obs) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('reveal-active');
        obs.unobserve(entry.target);
      }
    });
  }, observerOptions);

  document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
}
```

### 3.3 Módulo 3: Navegação Suave & Menu Mobile
```javascript
// Menu responsivo e navegação suave
function initNavigation() {
  const mobileMenuBtn = document.getElementById('mobile-menu-btn');
  const navLinks = document.getElementById('nav-links');

  mobileMenuBtn?.addEventListener('click', () => {
    navLinks.classList.toggle('active');
  });
}

document.addEventListener('DOMContentLoaded', () => {
  initThemeToggle();
  initScrollReveal();
  initNavigation();
});
```

---

## 4. Boas Práticas e Regras de Desenvolvimento

1. **Semântica HTML:** Utilizar marcas apropriadas. Títulos principais devem seguir a hierarquia estrita (`<h1>` único na página, `<h2>` para seções, `<h3>` para cards).
2. **Desempenho de Imagens:** Todas as imagens de projetos e avatares devem estar otimizadas (formatos WebP/PNG compactados) e conter atributo `alt` descritivo.
3. **Acessibilidade Básica:** Elementos interativos devem ter contraste adequado e estados `:focus-visible` visíveis para navegação por teclado.
4. **Sem Arquivos Desnecessários:** Manter o repositório enxuto e sem dependências externas via CDN ou npm.
