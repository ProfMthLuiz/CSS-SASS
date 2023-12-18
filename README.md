<strong>dicas &amp; exemplos de css/sass</strong>

#MENU 🏁
- DEFINIÇÃO

- [Ir para seção](#CURIOSIDADE(S))



## Definição CSS

<i>O Cascading Style Sheets ou Folhas de Estilo em Cascata(CSS) é uma linguagem de estilo utilizada para descrever a apresentação de um documento escrito em HTML ou XML (incluindo vários tipos de documentos XML como SVG ou XHTML). O CSS descreve como os elementos devem ser exibidos na tela, no papel ou em outras mídias.</i>

<br>
<br>
<br>

## SINTAXE CSS

![Sintaxe CSS](https://www.w3schools.com/css/img_selector.gif)

<br>
<br>

O seletor (selector) aponta para o elemento HTML que você deseja estilizar. O bloco de declaração contém uma ou mais declarações (declaration) separadas por ponto e vírgula. Cada declaração inclui um nome de propriedade (property) CSS e um valor (value), separados por dois pontos. Múltiplas declarações CSS são separadas por ponto e vírgula e declaração os blocos são cercados por chaves.

<i>Exemplo:</i>
```
 p{ 
            color: red;
            text-align: center;
}
```
Explicação: <br>
p - é um seletor em CSS  <br>
color - é uma propriedade <br>
red - é o valor da propriedade <br>
text-align - é uma propriedade <br>
center - é o valor da propriedade

<br>
<br>
<br>

## SELETORES CSS

Os seletores são usados para selecionar/encontrar os elementos HTML que você deseja estilizar, podemos dividir os seletores em cinco categorias: simples, combinador, pseudoclasse, pseudoelementos e atributos.
> Simples: selecione elementos com base no nome, id, classe <br>
> Combinador: selecione elementos baseados em um relacionamento específico entre eles <br>
> Pseudoclasse: seleciona elementos com base em um determinado estado <br>
> Pseudoelementos: selecione e estilizar uma parte de um elemento <br>
> Atributos: selecione elementos com base em um atributo ou valor de atributo <br>

### Simples
Seletores por Nome: Selecionam elementos com base em seus nomes. <br> 
Seletores por ID: Selecionam elementos com base em seus IDs únicos. <br>
Seletores por Classe: Selecionam elementos com base em suas classes. <br>

Exemplos: 
```
/* Seletor por nome, irá selecionar todos os elementos <p> ( <p> Meu primeiro paragrafo. </p> ) */
p{
    color: red;
}

/* Seletor por ID, irá selecionar todos os elementos que contem o id="title" ( <h1 id="title"> Meu primeiro titulo. </h1> ) */
#title{
    font-size: 1.2rem;
}

/* Seletor por classe, irá selecionar todos os elementos que contem class="card" ( <div class="card"> CARD! </div> ) */
.card{
    width: 100%;
    height: 150px;
}

```

### Combinador
Seletores de descendência (espaço), filho direto, irmão adjacente, irmão geral e agrupamento.

Descendência:
```
CSS
/* Estilos aplicados a todos os elementos <p> dentro de um <div> */
div p {
    color: blue;
}

HTML
<div>
    <p>Este parágrafo é azul.</p>
    <div>
        <p>Este parágrafo também é azul.</p>
    </div>
</div>

```

Filho direto (>):
```
CSS
/* Estilos aplicados a todos os elementos <p> que são filhos diretos de uma <div> */
div > p {
    border: 1px solid gray;
}

HTML
<div>
    <p>Item 1</p> --> são afetados pela estilização
    <p>Item 2</p> --> são afetados pela estilização 
    <p>Item 3</p> --> são afetados pela estilização
        <section>
            <p>Item 4</p> --> não é afetado pela estilização
        </section>
</div>


```

Irmão Adjacente (+):
```
CSS
/* Estilos aplicados ao primeiro elemento <p> que é irmão adjacente de um <h2> */
h2 + p {
    font-weight: bold;
}

HTML
<h2>Título</h2>
<p>Este parágrafo é negrito.</p>
<p>Este parágrafo não é afetado.</p>

```

Irmão Geral (~):
```
CSS
/* Estilos aplicados a todos os elementos <p> que são irmãos de um <h2> */
h2 ~ p {
    color: green;
}

HTML
<h2>Título</h2>
<p>Este parágrafo é verde.</p>
<p>Este parágrafo também é verde.</p>

```

Agrupamento (,):
```
CSS
/* Estilos aplicados a todos os elementos <h1>, <h2>, e <h3> */
h1, h2, h3 {
    text-align: center;
}

HTML
<h1>Título 1</h1>
<h2>Título 2</h2>
<h3>Título 3</h3>
```

### Pseudoclasse

As pseudoclasses em CSS são usadas para selecionar e estilizar elementos em estados específicos. Aqui estão alguns exemplos comuns de pseudoclasses: <br>

<i>:hover</i>

```
CSS
/* Estilos aplicados quando o mouse está sobre o elemento */
h1:hover {
    color: red;
}

HTML
<h1>Titulo</h1>
```

<i>:active</i>
```
CSS
/* Estilos aplicados quando o elemento está sendo ativado (clicado) */
button:active {
    background-color: #008000; /* verde */
}

HTML
<button>BOTAO</button>
```

<i>:focus</i>
```
CSS
/* Estilos aplicados quando o elemento está em foco */
input:focus {
    border: 2px solid blue;
}

HTML
<input type="text" id="fname" name="fname">
```

<i>:first-child</i>
```
CSS
/* Estilos aplicados ao primeiro filho de um elemento pai */
li:first-child {
    font-weight: bold;
}

HTML
<ol>
  <li>Coffee</li> <-- font-weight: bold;
  <li>Tea</li>
  <li>Milk</li>
</ol>

```

<i>:last-child</i>
```
CSS
/* Estilos aplicados ao último filho de um elemento pai */
p:last-child {
    color: purple;
}

HTML
<div>
  <p>Um</p>
  <p>Dois</p>
  <p>Tres</p>
  <p>Quatro</p> <-- cor do texto roxa
</div>
```

<i>:nth-child(3)</i>
```
CSS
/* Estilos aplicados ao terceiro filho de um elemento pai */
div p:nth-child(2) {
    color: red; /* texto em vermelho */
}

HTML
<div>
  <p>CHILD 1</p>
  <p>CHILD 2</p>
  <p>CHILD 3</p> <-- TEXTO EM VERMELHO
</div>
```

<i>:nth-child(odd) e :nth-child(even)</i>
```
CSS
/* Estilos aplicados a filhos ímpares de um elemento pai */
ul li:nth-child(odd) {
    background-color: yellow;
}

/* Estilos aplicados a filhos pares de um elemento pai */
ul li:nth-child(even) {
    background-color: red;
}

HTML
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
  <li>Sugar</li>
  <li>Cup</li>
  <li>Table</li>
</ul>
```

### Pseudoelementos

Pseudoelementos são usados para estilizar partes específicas de um elemento, sem a necessidade de adicionar marcação adicional ao HTML. Eles são representados por dois pontos (::) no início do seletor. Aqui estão alguns exemplos: <br>

<i>::before</i>
```
CSS
/* Adiciona conteúdo antes do conteúdo do elemento */
p::before {
    content: ">> ";
}

HTML
<p>Titulo</p>
```

<i>::after</i>
```
CSS
/* Adiciona conteúdo após o conteúdo do elemento */
p::after {
    content: " <<";
}

HTML
<p>Titulo</p>
```

<i>::first-line</i>
```
CSS
/* Seleciona a primeira linha dentro de um elemento */
p::first-line {
    font-weight: bold;
}

HTML
<p>Titulo</p>
```

<i>::first-letter</i>
```
CSS
/* Seleciona a primeira letra dentro de um elemento */
p::first-letter {
    font-size: 150%;
}

HTML
<p>Titulo</p>
```

<i>::placeholder</i>
```
CSS
input::placeholder {
  font-weight: bold;
  opacity: 0.5;
  color: red;
}

HTML
<input id="phone" type="tel" name="phone" minlength="9" maxlength="9" placeholder="Deve ter 9 dígitos" />
```

### Atributos
A seleção por atributos em CSS permite selecionar elementos com base em seus atributos e valores. Aqui estão alguns exemplos: <br>

[attribute] - Seleciona elementos com um atributo específico.

```
CSS
input[type] {
    border: 1px solid #ccc;
}

HTML
<input type="text" id="name" name="name">
```

[attribute="value"] - Seleciona elementos com um atributo específico e um valor específico.

```
CSS
a[href="https://www.google.com/"] {
    color: pink;
}

HTML
<a href="https://www.google.com/">Visite o Google</a>
```

[attribute^="value"] - Seleciona elementos com um atributo cujo valor começa com uma string específica.

```
CSS
input[type^="text"] {
    background-color: #f0f0f0;
}

HTML
<form>
 <label for="username">Nome de usuário:</label>
 <input type="text" id="username" name="username"> <!-- Background-color: #f0f0f0; -->

 <label for="password">Senha:</label>
 <input type="password" id="password" name="password"> <!-- Não afetado -->

 <label for="email">Email:</label>
 <input type="email" id="email" name="email"> <!-- Não afetado -->
</form>
```
[attribute$="value"] - Seleciona elementos com um atributo cujo valor termina com uma string específica.

```
CSS
a[href$=".pdf"] {
    color: red;
}

HTML
<p>Links para arquivos:</p>
 <ul>
  <li><a href="documento1.pdf">Documento 1 (PDF)</a></li>   <!-- Texto vermelho e negrito -->
  <li><a href="relatorio.docx">Relatório (DOCX)</a></li>    <!-- Não afetado -->
  <li><a href="imagem.jpg">Imagem (JPG)</a></li>            <!-- Não afetado -->
  <li><a href="documento2.pdf">Documento 2 (PDF)</a></li>   <!-- Texto vermelho e negrito -->
 </ul>

```

[attribute*="value"] - Seleciona elementos com um atributo cujo valor contém uma string específica.
```
CSS
[class*="button"] {
    background-color: #008000; /* verde */
}

HTML
 <button class="primary-button">Botão Primário</button> <!-- background-color: #008000; -->
 <button class="secondary-button">Botão Secundário</button> <!-- background-color: #008000; -->
 <div class="custom-button">Botão Customizado</div> <!-- background-color: #008000; -->
 <span class="other-element">Elemento Diferente</span> <!-- Não afetado -->

```
<br>
<br>
<br>

## CSS RESET
```
*{

    margin: 0;
    padding: 0;
    box-sizing: border-box;

}
```

<b>Explicação sobre o código acima: </b>

<i>Seletor Universal (*):</i> <br>
O asterisco é um seletor universal que corresponde a todos os elementos na página. Portanto, * { ... } significa que as propriedades dentro das chaves serão aplicadas a todos os elementos HTML.

<i>Margem (margin: 0;):</i> <br>
Define a margem de todos os elementos como 0. Isso significa que não haverá espaçamento entre os elementos e as bordas da janela do navegador.

<i>Preenchimento (padding: 0;):</i> <br>
Define o preenchimento interno de todos os elementos como 0. Isso garante que não haja preenchimento adicional dentro dos elementos.

<i>Box Sizing (box-sizing: border-box;):</i> <br>
Define o modelo de caixa (box-sizing) como border-box. Isso significa que as dimensões totais (largura e altura) de um elemento incluirão a borda e o preenchimento, em vez de aumentar as dimensões totais.

<br>
Em resumo, esse código é frequentemente usado como um "reset" ou "normalização" de estilos. Ele remove as margens e preenchimentos padrão dos elementos, proporcionando um ponto de partida consistente para o layout da página, especialmente quando você está construindo uma aplicação ou site e quer começar do zero sem influências indesejadas dos estilos padrão do navegador. Essa técnica é comumente conhecida como "CSS Reset" ou "CSS Normalize".

<br>
<br>
<br>

### CURIOSIDADE(S)
Programar em HTML e CSS é uma expressão comumente utilizada por pessoas que estão iniciando no mundo do desenvolvimento web, mas tecnicamente não está correta. HTML (HyperText Markup Language) e CSS (Cascading Style Sheets) não são linguagens de programação, são linguagens de marcação e estilização, respectivamente.
O termo "programar" geralmente se refere ao ato de escrever código em uma linguagem de programação, como JavaScript, Python, Java, C++, entre outras, que têm a capacidade de realizar operações lógicas e manipulação de dados. <br>
Então, quando alguém diz que está "programando em HTML e CSS", isso pode ser impreciso. É mais apropriado dizer que estão "escrevendo HTML e CSS" para criar a estrutura e o estilo de uma página web. Se a pessoa estiver usando JavaScript para adicionar interatividade à página, aí sim ela estaria envolvida em programação.





