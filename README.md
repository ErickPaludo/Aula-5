# Capítulo 1: Introdução ao CSS

## Objetivo
**Apresentar o que é CSS, sua importância e como ele se integra ao HTML.**

## Conteúdo
- *O que é CSS*: Definição e história.
- *Estrutura básica de um arquivo CSS*.
- *Inserindo CSS em HTML*: Inline, interno (internal) e externo (external).
- *Selectores básicos*: Elemento, classe e ID.
- *Propriedades e valores*.

## Prática

HTML
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Exemplo CSS Básico</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        .titulo {
            color: blue;
            text-align: center;
        }
        #paragrafo {
            font-size: 16px;
        }
    </style>
</head>
<body>
    <h1 class="titulo">Olá, CSS!</h1>
    <p id="paragrafo">Este é um exemplo de CSS inline.</p>
</body>
</html>

# Capítulo 2: Selectores e Especificidade

## Objetivo
**Explorar a lógica dos selectores e a hierarquia de estilos.**

## Conteúdo
- Revisão dos selectores básicos.
- Selectores avançados: Agrupamento, descendente, filho, adjacente e general sibling.
- Especificidade: Como CSS decide qual estilo aplicar.
- Herança de propriedades.

## Prática

HTML
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Especificidade CSS</title>
    <style>
        p {
            color: green;
        }
        .especial {
            color: red;
        }
        #unico {
            color: blue;
        }
    </style>
</head>
<body>
    <p>Parágrafo 1</p>
    <p class="especial">Parágrafo 2</p>
    <p id="unico">Parágrafo 3</p>
</body>
</html>

# Capítulo 3: Cores e Unidades

## Objetivo
**Aplicar cores e diferentes unidades de medida no CSS.**

## Conteúdo
  -   Unidades de medida: Absolutas (px, cm) vs. relativas (em, rem, %, vw, vh).
  -   Cores em CSS: Nomeadas, HEX, RGB, RGBA, HSL e HSLA.
  -   Transparência e opacidade.
  -   Gradientes lineares e radiais.

## Prática

HTML

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Paleta de Cores</title>
    <style>
        body {
            background: linear-gradient(to right, #ff7e5f, #feb47b);
            color: rgba(255, 255, 255, 0.8);
        }
    </style>
</head>
<body>
    <h1>Bem-vindo</h1>
    <p>Esta é uma paleta de cores com gradiente e opacidade.</p>
</body>
</html>

# Capítulo 4: Tipografia
## Objetivo
**Explorar como estilizar texto e escolher fontes adequadas.**

## Conteúdo
- Fontes web: Font-family, fallback fonts.
- Google Fonts e fontes personalizadas.
- Propriedades tipográficas: Tamanho, altura da linha (line-height), espaçamento entre letras (letter-spacing) e entre palavras (word-spacing).
- Estilização de texto: Negrito, itálico, sublinhado, - alinhamento, decoração e transformação.

## Prática

HTML

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Estilização de Texto</title>
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            line-height: 1.6;
        }
        h1 {
            font-size: 2em;
            text-align: center;
        }
        p {
            margin: 20px 0;
        }
        .negrito {
            font-weight: bold;
        }
        .italico {
            font-style: italic;
        }
    </style>
</head>
<body>
    <h1>Artigo de Exemplo</h1>
    <p class="negrito">Este parágrafo está em negrito.</p>
    <p class="italico">Este parágrafo está em itálico.</p>
</body>
</html>

# Capítulo 5: Box Model e Layout
## Objetivo
**Apresentar o Box Model e como ele influencia o layout de uma página.**

## Conteúdo
- Box Model: Margem (margin), borda (border), padding, conteúdo.
- Box-sizing: Content-box vs. border-box.
- Display: Block, inline, inline-block.
- Manipulação de largura e altura.

## Prática

HTML

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Box Model</title>
    <style>
        .caixa {
            width: 200px;
            height: 100px;
            margin: 20px;
            padding: 10px;
            border: 2px solid black;
            box-sizing: border-box;
        }
    </style>
</head>
<body>
    <div class="caixa">Conteúdo da Caixa</div>
</body>
</html>

# Capítulo 6: Flexbox
## Objetivo
**Utilizar o Flexbox para criar layouts flexíveis e responsivos.**

## Conteúdo
- Conceito de Flexbox.
- Container flex e itens flex.
- Propriedades do container: flex-direction, justify-content, align-items, flex-wrap.
- Propriedades dos itens: flex-grow, flex-shrink, flex-basis, align-self.

## Prática

HTML

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Galeria Flexbox</title>
    <style>
        .galeria {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }
        .item {
            flex: 1 1 calc(33.333% - 10px);
            background-color: #ccc;
            height: 100px;
        }
    </style>
</head>
<body>
    <div class="galeria">
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
    </div>
</body>
</html>

# Capítulo 7: Grid Layout
## Objetivo
**Apresentar o CSS Grid e suas capacidades para criação de layouts complexos.**

## Conteúdo
- Introdução ao CSS Grid.
- Containers e itens de grid.
- Definindo colunas e linhas: grid-template-columns, grid-template-rows.
- Áreas de grid e alinhamento de itens.
- 
## Prática

HTML

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Layout Grid</title>
    <style>
        .container {
            display: grid;
            grid-template-areas:
                'header'
                'main'
                'footer';
            grid-gap: 10px;
            color:black;
        }
        .header {
            grid-area: header;
            background-color: #ccc;
        }
        .main {
            grid-area: main;
            background-color: #eee;
        }
        .footer {
            grid-area: footer;
            background-color: #ccc;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">Cabeçalho</div>
        <div class="main">Conteúdo Principal</div>
        <div class="footer">Rodapé</div>
    </div>
</body>
</html>

# Capítulo 8: Estilização Avançada e Animações
## Objetivo
**Explorar técnicas avançadas de estilização e introduzir animações em CSS.**

## Conteúdo
- Pseudo-classes e pseudo-elementos.
- Animações básicas: @keyframes, animation, transition.
- Efeitos de hover e foco.
- Transições suaves e animações personalizadas.
- 
## Prática

HTML

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Menu de Navegação Animado</title>
    <style>
        nav ul {
            list-style-type: none;
            padding: 0;
            display: flex;
            justify-content: center;
        }
        nav ul li {
            margin: 0 15px;
            position: relative;
        }
        nav ul li a {
            text-decoration: none;
            color: black;
            padding: 10px 15px;
            font-size: 15px;
            transition: color 0.3s;
        }
        nav ul li a:hover {
            color: blue;
        }
        nav ul li::after {
            content: '';
            display: block;
            height: 2px;
            background: blue;
            transition: width 0.3s;
            width: 0;
            position: absolute;
            bottom: -5px;
            left: 0;
        }
        nav ul li:hover::after {
            width: 100%;
        }
    </style>
</head>
<body>
    <nav>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">Sobre</a></li>
            <li><a href="#">Serviços</a></li>
            <li><a href="#">Contato</a></li>
        </ul>
    </nav>
</body>
</html>

# Capítulo 9: Responsividade e Media Queries
## Objetivo
**Criar layouts responsivos que se adaptam a diferentes dispositivos.**

## Conteúdo
- Conceito de design responsivo.
- Media queries: Sintaxe e uso.
- Layouts fluidos e imagens responsivas.
- Unidades relativas para responsividade.
- 
## Prática

HTML

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Layout Responsivo</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        .header, .footer {
            background: #333;
            color: white;
            text-align: center;
            padding: 10px 0;
        }
        .main {
            display: flex;
            flex-wrap: wrap;
        }
        .main > div {
            flex: 1;
            padding: 10px;
            box-sizing: border-box;
        }
        @media (max-width: 768px) {
            .main {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">Cabeçalho</div>
        <div class="main">
            <div>Coluna 1</div>
            <div>Coluna 2</div>
            <div>Coluna 3</div>
        </div>
        <div class="footer">Rodapé</div>
    </div>
</body>
</html>

# Capítulo 10: Boas Práticas e Otimização
## Objetivo
**Consolidar os conceitos aprendidos e introduzir boas práticas e técnicas de otimização.**

## Conteúdo
- Estruturação e organização de CSS: Módulos, BEM (Block Element Modifier).
- Minificação e compressão de arquivos CSS.
- Ferramentas de desenvolvimento: DevTools, linting, pré-processadores (Sass).
- Acessibilidade em CSS.
- 
## Prática

HTML

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Projeto CSS Otimizado</title>
    <link rel="stylesheet" href="styles.min.css">
</head>
<body>
    <style>
      .header{
        background: black;
        color: #fff;
        padding: 20px;
        text-align: center;
      }
      .header_title{
        font-size: 2em;
      }
      .main-content{
        padding: 20px;
      }
      .module{
        margin-bottom: 20px;
      }
      .module_title{
        font-size: 1.5em;
        color: black;
      }
      .module_text{
        font-size: 1em;
        color: black;
      }
      .footer{
        background: black;
        padding: 10px;
        text-align: center;
      }
      .footer_text{
        font-size: 1em;
        color: white;
      }
    </style>
    <header class="header">
        <h1 class="header_title">Projeto CSS Otimizado</h1>
    </header>
    <main class="main-content">
        <section class="module">
            <h2 class="module_title">Seção de Exemplo</h2>
            <p class="module_text">Exemplo estrutura e organização em CSS usando BEM.</p>
        </section>
    </main>
    <footer class="footer">
        <p class="footer_text">© 2024 Projeto CSS Otimizado</p>
    </footer>
</body>
</html>
