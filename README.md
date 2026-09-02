# Currículo Pessoal — Kevin Muerembe

**Nome:** Kevin Muerembe
**Disciplina:** Programação e Design Web  
**Ano:** 2º Ano, 2026

---

## Descrição do Projeto

Site pessoal de currículo/portfólio desenvolvido em HTML5 e CSS3 puro, sem frameworks ou JavaScript, como trabalho prático para a disciplina de Programação de Design Web.

O site é composto por cinco páginas interligadas e apresenta informações sobre mim, os meus projetos, hobbies e um formulário de contacto com validação nativa HTML5.

Todo o layout, comportamento visual, validação de formulários e responsividade foram alcançados apenas com HTML e CSS, conforme exigido no enunciado.

---

## Como Visualizar

1. Descarrega ou clona o repositório.
2. Abre o ficheiro `https://github.com/kmuerembe/meu-curriculo` num navegador moderno (Google Chrome, Mozilla Firefox, Microsoft Edge, etc.).
3. Navega pelas páginas utilizando o menu no topo (header fixo).

---

## Páginas do Site

### Home (`index.html`)
- Apresentação pessoal com nome, foto/avatar e frase de efeito.
- Breve descrição de competências.
- Call-to-action (botão "Fala Comigo") para a página de contacto.
- Inclui elementos multimédia: áudio (apresentação em MP3) e vídeo (demonstração via YouTube no portfólio).

### Currículo (`about.html`)
- Formação académica (lista ordenada).
- Experiência / projetos (lista não ordenada).
- Imagem com legenda (certificado, usando `<figure>` e `<figcaption>`).
- Tabela de proficiência em tecnologias, com `rowspan` e `colspan`, `thead` e `tbody`.
- Link para descarregar CV em PDF.

### Portfólio (`portfolio.html`)
- Grelha de projetos em cartões, com imagem, título, descrição e tags de tecnologia.
- Layout principal com CSS Grid (`grid-template-columns: repeat(auto-fit, minmax(280px, 1fr))`).
- Vídeo de demonstração de projeto incorporado via YouTube (iframe).

### Hobbies (`hobbies.html`)
- Cartões organizados com CSS Grid (reutiliza a mesma classe do index), mas o menu e footer usam Flexbox.
- Cada cartão tem ícone (Font Awesome), título e descrição.
- Apresenta interesses pessoais fora da programação.

### Contacto (`contact.html`)
- Formulário completo com os seguintes campos:
  - Nome (`text`, `required`, `minlength`, `maxlength`)
  - Email (`email`, `required`)
  - Telefone (`tel`, `pattern` para formato moçambicano)
  - Data preferida (`date`)
  - Orçamento (`number`, `min`, `max`, `step`)
  - Assunto (`select` com `option`, `required`)
  - Forma de contacto preferida (`radio`)
  - Áreas de interesse (`checkbox`)
  - Anexar ficheiro (`file`, `accept`)
  - Mensagem (`textarea`, `required`, `minlength`, `maxlength`)
- Todos os campos estão devidamente associados a `<label>` (via `for`/`id`).
- Agrupamento com `<fieldset>` e `<legend>`.
- Validação nativa HTML5 (sem JavaScript).
- Estilização personalizada de `radio` e `checkbox`.

---

## Principais Tags e Atributos Utilizados

| Tag / Atributo | Explicação |
|----------------|------------|
| `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>` | Estrutura semântica HTML5, melhorando acessibilidade e SEO. |
| `<figure>` + `<figcaption>` | Agrupa imagens com legendas descritivas (certificados, projetos). |
| `<table>` com `thead`/`tbody`, `colspan`/`rowspan` | Organiza dados da tabela de competências com células que se estendem por várias linhas/colunas. |
| `<video>` com `controls`, `poster`, `<source>` (e `type`) | Reprodução nativa de vídeo com interface de controlo e imagem de pré-visualização (se usado). |
| `<audio>` com `controls`, `<source>` (e `type="audio/mpeg"`) | Reprodução nativa de áudio MP3. |
| `<form>` com `action="#" method="get"` | Formulário de contacto com validação nativa (sem JavaScript). |
| `required`, `minlength`, `maxlength`, `pattern`, `min`, `max`, `accept` | Atributos de validação nativos para cada tipo de campo. |
| `<fieldset>` + `<legend>` | Agrupa campos relacionados no formulário. |
| `<label for="...">` e `id` correspondente | Associação explícita entre rótulo e campo, essencial para acessibilidade. |
| `aria-label`, `aria-current`, `aria-hidden`, `role`, `aria-labelledby` | Atributos de acessibilidade para leitores de ecrã. |

---

## Principais Recursos CSS Utilizados

| Recurso | Explicação |
|---------|------------|
| `:root` com variáveis CSS | Centraliza cores, fontes e espaçamentos para fácil manutenção. |
| `box-sizing: border-box` | Garante que padding e border não aumentem o tamanho dos elementos. |
| `position: sticky` no header | Header fixo no topo ao rolar (com comentário explicativo no CSS sobre os tipos de posicionamento). |
| Flexbox no menu e footer | Layout flexível e responsivo para navegação e redes sociais. |
| CSS Grid no portfólio | Grelha responsiva de cartões de projetos (`grid-template-columns: repeat(auto-fit, minmax(280px, 1fr))`). |
| Pseudo‑classes (`:hover`, `:focus`, `:nth-child(even)`) | Efeitos visuais em links, botões, cards, e estilização de linhas pares na tabela. |
| Pseudo‑elementos (`::before` e `::after`) | Decoração no menu (linha animada) e ícones em checkboxes estilizados. |
| `@keyframes` e `transition` | Animações suaves de entrada (`fadeInUp`) e transições em hover. |
| `linear-gradient` e `box-shadow` | Efeitos decorativos (faixa capulana) e profundidade visual (sombras). |
| Media queries (mobile‑first) | Adaptação do layout para tablet (≥768px) e desktop (≥1024px), com ajustes para telemóvel (≤480px). |
| Unidades relativas (`rem`, `em`, `%`, `vw/vh`) | Utilizadas em conjunto com unidades fixas (px) de forma justificada para garantir flexibilidade. |

---

## Estrutura de Pastas
/
├── index.html
├── about.html
├── portfolio.html
├── hobbies.html
├── contact.html
├── css/
│ ├── estilo.css
│ └── responsivo.css
├── assets/
│ ├── img/
│ │ ├── avatar.jpg
│ │ ├── certificado.jpg
│ │ ├── projeto1.jpg
│ │ ├── projeto2.jpg
│ │ ├── projeto3.jpg
│ │ └── projeto4.jpg
│ ├── video/
│ │ └── apresentacao.mp4 (ou apenas iframe do YouTube)
│ ├── audio/
│ │ └── apresentacao.mp3
│ └── ficheiros/
│ └── cv-kevin.pdf
└── README.md

---

## Multimédia

- **Imagens**: todas as imagens têm `alt` descritivo e, quando com legenda, estão envolvidas em `<figure>` com `<figcaption>`.
- **Áudio**: ficheiro `apresentacao.mp3` em `assets/audio/`, com player nativo `<audio>` e `controls`.
- **Vídeo**: demonstração de projeto incorporada via YouTube (`<iframe>`) na página `portfolio.html`, cumprindo o requisito de pelo menos uma forma de vídeo.


## Repositório e Commits

Este projeto foi desenvolvido com commits progressivos, refletindo a evolução do trabalho:
- Estrutura HTML das páginas
- CSS base com variáveis e layout
- Responsividade e media queries
- README e ajustes finais

---

## Autoria

Desenvolvido por **Kevin Muerembe** – Universidade Licungo, Moçambique, 2026.

---

*Trabalho prático realizado para a disciplina de Programação de Design Web, 2º Ano de Licenciatura em Informática.*
