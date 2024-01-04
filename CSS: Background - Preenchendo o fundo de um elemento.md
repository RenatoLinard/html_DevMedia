# Introdução 

Ao desenvolver uma página, é comum buscarmos maneiras de realçar a presença de um elemento, seja através da escolha de uma cor de fundo ou da utilização de uma imagem.

## Valorizando a Estética dos Elementos

No tópico anterior, exploramos como modificar a cor de fundo de um elemento 
usando a propriedade `background-color`.

No entanto, em determinadas situações, é mais atrativo utilizar uma 
imagem para estilizar o fundo do elemento. Essa personalização é 
possível através da propriedade `background-image`.

```css
div {
    background-image: url('img/img-fundo.jpg');
    background-repeat: repeat;
    background-position: 10px;
    background-size: 100px;
    background-attachment: fixed;
}
```

Essa abordagem é frequentemente aplicada em caixas (boxes), cartões (cards) 
e seções de uma página, proporcionando um visual mais dinâmico.

## Conceito de Background

O termo "background" refere-se ao espaço que podemos preencher dentro de um elemento HTML.

## Relembrando a Propriedade `background-color`

Para alterar a cor de fundo de um elemento, utilizamos a propriedade `background-color`.

```css
div {
    background-color: #fff;
}
```

Basta escrever o nome da propriedade seguido por dois pontos e a cor desejada. 
Vale ressaltar que é possível utilizar diferentes formatos de cor, 
como o nome nominal, o código hexadecimal ou o formato RGB.

