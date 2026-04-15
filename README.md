# 💼 Portfólio — Lendro Campelo

Primeira versão do portfólio pessoal desenvolvido como atividade prática do curso de **Tecnologia em Sistemas para Internet** — AUPI, polo de Lagoa do Sítio, Piauí.

---

## 📋 Sobre o Projeto

O projeto consiste em uma página web de portfólio profissional que apresenta informações pessoais, habilidades técnicas e projetos desenvolvidos. Os projetos são renderizados dinamicamente via JavaScript a partir de um array de objetos.

---

## ✅ Requisitos Atendidos

| Requisito | Implementação |
|---|---|
| Estrutura Semântica HTML5 | `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>` |
| Cabeçalho com menu | `<header>` com `<nav>` e links de navegação |
| Seção Sobre Mim | `<section id="sobre">` com texto e tecnologias |
| Seção Meus Projetos | `<section id="projetos">` preenchida via JS |
| Rodapé | `<footer>` com contato e redes sociais |
| Flexbox | Navbar, hero, footer, cards internos |
| CSS Grid | Seção "Sobre" (2 colunas) e grid de projetos |
| Responsividade | Media queries para mobile (≤900px e ≤520px) |
| Array de objetos JS | `const projetos = [...]` com 3 projetos |
| Renderização dinâmica | `forEach` + `createElement` + `appendChild` |

---

## 🗂️ Estrutura de Arquivos

├── index.html      # Estrutura semântica da página
├── style.css       # Estilização com Flexbox, Grid e responsividade
├── script.js       # Array de projetos e renderização dinâmica
├── perfil.jpeg     # Foto de perfil
└── README.md       # Documentação do projeto
```

---

## 🛠️ Tecnologias Utilizadas

- **HTML5** — estrutura semântica
- **CSS3** — Flexbox, Grid, variáveis CSS, media queries, animações
- **JavaScript** — manipulação do DOM, array de objetos, renderização dinâmica
- **Google Fonts** — fonte Poppins
- **Font Awesome 6** — ícones

---

## 📐 Estrutura HTML Semântica

```
<header>          ← Cabeçalho com menu de navegação
  <nav>
    <ul>
      <li> Ver Projetos
      <li> Sobre Mim
    </ul>
  </nav>
</header>

<main>
  <section #home>         ← Apresentação / Hero
  <section #sobre>        ← Seção 1: Sobre Mim
  <section #projetos>     ← Seção 2: Meus Projetos (renderizada via JS)
</main>

<footer>          ← Rodapé com contato e redes sociais
```

---

## ⚙️ Como os Projetos são Renderizados

No arquivo `script.js`, um array de objetos contém os dados de cada projeto:

```js
const projetos = [
  {
    tag: 'Web',
    nome: 'Site Profissional',
    desc: 'Descrição do projeto...',
    tecnologias: ['HTML5', 'CSS3', 'JavaScript'],
    img: 'url-da-imagem',
    link: '#'
  },
  // ...
];
```

O JavaScript percorre o array com `forEach`, cria um `<article>` para cada projeto e o insere no `<div id="Projetos">` do HTML:

```js
projetos.forEach(projeto => {
  const card = document.createElement('article');
  card.className = 'project-card';
  card.innerHTML = `...`;
  grid.appendChild(card);
});
```

---

## 📱 Responsividade

| Breakpoint | Comportamento |
|---|---|
| > 900px | Layout em duas colunas (hero + foto lado a lado) |
| ≤ 900px | Layout empilhado, menu hamburguer ativado |
| ≤ 520px | Cards de projetos em coluna única, footer empilhado |

---

## ▶️ Como Executar

1. Clone ou baixe o repositório
2. Abra o arquivo `index.html` diretamente no navegador

Não é necessário instalar dependências ou servidor — o projeto roda totalmente no frontend.

---

## 👤 Autor

**Leandro Campelo**  
Estudante de Tecnologia em Sistemas para Internet — AUPI  
Polo: Lagoa do Sítio, Piauí  

