# Snitap Patins

![Logo Snitap](/assets/Thumbnail.png)

## 📋 Sobre o Projeto

Snitap Patins é um site moderno para uma marca fictícia de patins, desenvolvido durante o curso Fullstack da Rocketseat. O projeto destaca-se pelo uso de tecnologias web modernas e técnicas avançadas de CSS, especialmente com foco em animações e efeitos visuais que proporcionam uma experiência interativa e dinâmica aos usuários.

## 🚀 Tecnologias Utilizadas

- **HTML5**: Estruturação semântica do conteúdo
- **CSS3**: Estilização avançada com foco em:
  - CSS Moderno (importação de módulos CSS)
  - Variáveis CSS para consistência visual
  - Layout com Flexbox e Grid
  - Seletores avançados e pseudo-elementos
  - Animações e transições
  - View Timeline API (animações baseadas em scroll)

## 💻 Estrutura do Projeto

O projeto está estruturado de forma modular, com arquivos CSS separados por componentes:

```
📁 assets/
📁 styles/
  ├── index.css       # Importa todos os módulos CSS
  ├── global.css      # Resets e variáveis globais
  ├── header.css      # Estilos do cabeçalho
  ├── hero.css        # Seção principal com animações
  ├── banner.css      # Banner animado
  ├── gallery.css     # Galeria de fotos
  └── footer.css      # Rodapé
📄 index.html         # Estrutura HTML principal
```

## ✨ Destaques de Implementação

### 🎭 Animações e Efeitos CSS

O projeto apresenta uma variedade de técnicas avançadas de animação em CSS:

#### Animação de Texto Rotativo

Na seção hero, as palavras "radical", "divertida", "saudável" alternam-se automaticamente com uma animação de deslizamento vertical:

```css
h1 span {
  display: block;
  animation: slideUp 5s 2s infinite ease;
}

@keyframes slideUp {
  /* Controle preciso da animação com percentuais */
  0%,
  22% {
    transform: translateY(0);
  }
  /* ... outros keyframes ... */
  100% {
    transform: translateY(-15rem);
  }
}
```

#### Animação de Entrada dos Elementos

O patins e elementos decorativos na seção hero entram na tela com um efeito de deslizamento suave:

```css
img[src*='patins'] {
  z-index: 1;
  transform: translateX(200%);
  animation: slideIn 3s 200ms ease forwards;
}

@keyframes slideIn {
  50% {
    transform: translateX(-20px);
  }
  100% {
    transform: translateX(0);
  }
}
```

#### Banner com Rolagem Infinita

Banner utilizando animação contínua para criar um efeito de rolagem infinita:

```css
.rolling {
  display: flex;
  gap: 1.5rem;
  animation: rolling 2s linear infinite;
}

@keyframes rolling {
  to {
    transform: translateX(-132px);
  }
}
```

#### Gradiente Animado

Fundo com gradiente que muda de posição animadamente:

```css
.bg-gradient-animate {
  background: linear-gradient(45deg, var(--snitap-sky-light), var(--snitap-joy-light));
  background-size: 400%;
  background-position: 0 50%;
  animation: bg-gradient 20s ease infinite;
}

@keyframes bg-gradient {
  50% {
    background-position: 100% 50%;
  }
}
```

#### Animações baseadas em Scroll (View Timeline API)

As imagens da galeria aparecem conforme o usuário rola a página:

```css
figure {
  animation: image-appear linear backwards;
  animation-timeline: view();
  animation-range: 100px 300px;
}

@keyframes image-appear {
  from {
    opacity: 0;
    transform: translateY(100%);
  }
}
```

#### Interações em Hover

Elementos interativos como botões, links e imagens possuem transições suaves quando o usuário passa o mouse sobre eles:

```css
.button {
  transition: scale 350ms;
}

.button:hover {
  scale: 1.1;
}
```

### 📊 Layout Responsivo

Layout construído com Flexbox e Grid para garantir boa experiência em diferentes dispositivos:

```css
.content {
  display: grid;
  grid-template-areas:
    'A B B'
    'C C D';
  gap: 2.5rem;
}
```

### 🎨 Sistema de Design Consistente

Uso de variáveis CSS para garantir consistência visual:

```css
:root {
  --snitap-sun: #ffcd1e;
  --snitap-sky-mid: #06b6d4;
  --snitap-sky-light: #67e8f9;
  --snitap-joy-mid: #db2777;
  --snitap-joy-light: #f472b6;
  --snitap-leaf-mid: #16a34a;

  /* ... outras variáveis ... */
}
```

## 🌟 Recursos Técnicos Avançados

### Nesting em CSS

Uso de seletores aninhados para melhorar organização e legibilidade:

```css
section.hero {
  & h1 {
    max-width: 40rem;
  }

  & .buttons {
    display: flex;
    gap: 2rem;
  }
}
```

### Pseudo-elementos

Uso criativo de pseudo-elementos para efeitos visuais:

```css
a::after {
  content: '';
  width: 100%;
  height: 2px;
  background-color: var(--snitap-sky-mid);
  /* ... outras propriedades ... */
}
```

### Efeitos de Sobreposição

Técnicas de posicionamento absoluto e z-index para criar efeitos de sobreposição:

```css
figcaption {
  position: absolute;
  bottom: 0;
  width: 100%;
  background: linear-gradient(to top, rgb(0 0 0 / 0.64), rgb(0 0 0 / 0));
}
```

## 📝 Aprendizados do Projeto

Este projeto demonstra várias técnicas modernas de desenvolvimento front-end:

1. **Organização modular** de código CSS
2. **Animações complexas** para melhorar a experiência do usuário
3. **Design system** com variáveis CSS
4. **Layout responsivo** com Grid e Flexbox
5. **Interatividade** sem depender de JavaScript
6. **Performance** com animações otimizadas

## 🎓 Projeto Desenvolvido Durante o Curso Fullstack da Rocketseat

Este projeto foi desenvolvido como parte do aprendizado no curso Fullstack da Rocketseat, aplicando conceitos avançados de HTML e CSS.

## 🧠 Conceitos Explorados

- CSS modular
- Animações customizadas
- Timelines de animação
- Pseudo-elementos e pseudo-classes
- Gradientes e efeitos visuais
- Layouts avançados com Grid e Flexbox
- Timeline View
