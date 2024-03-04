# Introdução

Até o momento, utilizamos a propriedade **CSS** `position` para posicionar 
elementos na página. No entanto, essa abordagem se mostra limitada ao lidar 
com a estruturação de páginas que exigem layouts mais complexos, especialmente 
quando envolvem múltiplos containers.

Para superar esse desafio, adotamos uma ferramenta chamada **CSS Flexbox**, que 
se destaca como a principal abordagem para posicionar elementos com **CSS**.

## Revisando o CSS position

Até agora, temos empregado a propriedade **CSS position** como a maneira mais 
simples de posicionar elementos na página. Contudo, sua eficácia é limitada 
quando tratamos de múltiplos containers na página.

## Limitação do CSS position

Ao considerarmos a criação de uma página com diversos cards, o fluxo padrão 
resulta em uma disposição vertical, um card abaixo do outro. No entanto, caso 
desejemos alinhar os cards horizontalmente, seria necessário escrever vários 
códigos para alcançar o resultado desejado. Essa abordagem não apenas demanda 
mais código, mas também compromete a responsividade do layout, pois não se 
ajusta adequadamente ao tamanho da tela, podendo resultar na perda do layout concebido.

# CSS Flexbox

## Introdução ao Flexbox

O **CSS Flexbox** é a abordagem principal para posicionar elementos dentro de 
um container.

Com ele, podemos posicionar todos os elementos de uma só vez, proporcionando 
maior flexibilidade no layout.

O Flexbox permite posicionar os elementos de diversas formas.

```css
.container {
    display: flex;
    flex-direction: column, row;
}
```

Ao utilizar o Flexbox, o elemento com a classe "container" terá seus filhos 
dispostos em uma coluna ou linha, conforme definido pela propriedade `flex-direction`. 
Essa flexibilidade oferecida pelo Flexbox simplifica significativamente o 
posicionamento dos elementos, tornando o código mais limpo e eficiente.

## Páginas Flexíveis

Atualmente, a construção de páginas flexíveis tornou-se comum, ou seja, 
páginas que se adaptam a diferentes tipos de telas e conteúdos.

O Flexbox oferece uma maneira fácil e eficaz de modelar esse tipo de página, 
garantindo uma experiência de usuário mais consistente em diversas plataformas 
e dispositivos. Essa capacidade de adaptação é crucial para acompanhar a 
diversidade de tamanhos de tela e garantir que o conteúdo seja apresentado de 
maneira otimizada em diferentes contextos.

## Aplicando o flexbox nos cards

A ferramenta **flexbox** pode ser utilizada para para posicionar elementos do 
container pai, quanto para os elementos filhos dentro dos cards.

# Propriedades do Flexbox

## display: flex e flex-direction

# `display: flex`: A Base do Flexbox

A propriedade **`display: flex`** é fundamental ao utilizar a ferramenta **Flexbox**.

Anteriormente, já exploramos a propriedade **`display`** em contextos mais simples:

```css
.container {
    display: block;
    display: inline;
    display: none;
}
```

Essa propriedade possibilita a alteração do **modo de exibição** padrão do elemento, 
influenciando seu comportamento no layout.

## Alinhando Elementos Lado a Lado

No exemplo a seguir, empregaremos a ferramenta **Flexbox** para posicionar os cards lado a lado:

```html
<body>
    <div class="container">
        <div class="box1">Imagem Produto 1</div>
        <div class="box2">Imagem Produto 2</div>
        <div class="box3">Imagem Produto 3</div>
    </div>
</body>
```

```css
.container {
    padding: 40px 20px 20px;
    background-color: black;
    display: flex;
}

.box1,
.box2,
.box3 {
    width: 200px;
    height: 200px;
    background-color: white;
    border: 1px solid gray;
}
```

Ao aplicarmos **`display: flex`** à classe "container", os elementos filhos (box1, box2, box3) 
serão dispostos lado a lado, formando um layout mais fluido e adequado. Essa é apenas uma das 
muitas possibilidades oferecidas pelo Flexbox para aprimorar o posicionamento de elementos em uma página.

## Ajustando a largura dos cards com **display: flex**

Um ponto importante no uso do **display: flex** é o ajuste da largura dos elementos (cards).

Por padrão os elementos são ajustados (comprimidos) automaticamente.

Se a largura total não for suficiente, os elementos por padrão serão comprimidos para caber no container.

## flex-direction






