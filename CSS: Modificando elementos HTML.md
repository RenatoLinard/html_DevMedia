# Introdução

Neste arquivo, utilizaremos o CSS para modificar os elementos HTML, mas 
para isso, é essencial compreender o significado da modificação dos elementos HTML.

## O Que Significa?

Modificar um elemento implica em alterar suas dimensões e espaçamentos 
por meio das propriedades a seguir:

- Largura (width)
- Altura (height)
- Espaçamento interno (padding)
- Margem (margin)
- Borda (border)

Já discutimos anteriormente como utilizar essas propriedades.

Nesta seção, abordaremos a definição de altura, largura mínima e máxima 
de um elemento. Além disso, aprenderemos a trabalhar com altura e largura 
relativas, e entenderemos como alterar a **visibilidade** de um elemento.

## Por que é útil?

A customização de elementos por meio do CSS é amplamente útil para atender 
às necessidades específicas de uma página. Por exemplo, ao exibir uma 
imagem com uma largura fixa de 1400px em uma tela pequena, a página pode 
quebrar e apresentar uma barra de rolagem horizontal.

Uma solução para esse problema é a utilização de largura relativa, como, por 
exemplo, 50%. Dessa forma, a imagem sempre terá metade da largura 
da tela, evitando que a página quebre.

Outra abordagem para lidar com essa situação é o uso de largura 
mínima e máxima, ou até mesmo cálculos de tamanho. Há diversas maneiras de 
resolver um mesmo problema, e a escolha da abordagem dependerá das 
necessidades específicas de cada caso.

## Valores Relativos

Como mencionado anteriormente, um valor relativo é aquele que define 
o seu valor com base em outro elemento.

Esse valor é expresso em porcentagem e faz com que o elemento filho ocupe a 
proporção definida em relação ao elemento pai.

### Porcentagem - Sintaxe

A porcentagem pode ser utilizada em qualquer propriedade que aceite valores 
em pixels, tais como: **width, height, margin, padding**.

Para aplicar a porcentagem, basta adicionar o valor seguido de `%` na 
propriedade desejada.

```css
img {
    width: 100%;
    height: 80%;
}
```

### VW e VH

- `VW` - é uma medida de valor relativo que se refere à largura da tela. 
Cada 1vw corresponde a 1% da largura da tela.
- `VH` - Funciona da mesma maneira que o `vw`, mas o `vh` faz referência à 
altura da tela.
