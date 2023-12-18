<strong>dicas &amp; exemplos de css/sass</strong>

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

As pseudoclasses em CSS são usadas para selecionar e estilizar elementos em estados específicos. Aqui estão alguns exemplos comuns de pseudoclasses:

### Pseudoelementos
### Atributos

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

