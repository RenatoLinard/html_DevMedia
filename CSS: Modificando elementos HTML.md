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

### vw e vh

- `VW` - é uma medida de valor relativo que se refere à largura da tela. 
Cada 1vw corresponde a 1% da largura da tela.
- `VH` - Funciona da mesma maneira que o `vw`, mas o `vh` faz referência à 
altura da tela.

### vw e vh - sintaxe 

O valor `vw` e `vh` pode ser utilizada em qualquer propriedade que aceite valores 
em pixels, tais como: **width, height, margin, padding**.

```css
img {
    width: 50vw;
    height: 60vh;
    margin: 5vh 5vw;
    padding: 3vh 0;
}
```

Para utilizar basta passar o valor seguido de `vw` ou `vh` para a propriedade 
desejada.

## Calc

Em alguns casos, desejamos que uma imagem ocupe **toda a largura** da tela.

```css
img {
    width: 100vw;
}
```

No entanto, se quisermos adicionar uma **borda**, **margem** ou **padding** 
à imagem, isso pode quebrar a página devido ao aumento dos pixels da imagem.

A imagem continuará tendo os **100vw**, mas com a adição das margens, a imagem 
se afasta pela quantidade de pixels definida para margem ou padding, colocando-a fora da tela.

Para evitar esse problema, podemos utilizar o **calc**.

```css
img {
    width: calc(100vw - 60px);
    margin: 30px;
}
```

Com o uso do **calc**, podemos instruir o **CSS** a realizar cálculos 
utilizando valores **relativos (%, vw, vh) e fixos**. 
Isso permite um controle mais preciso sobre as dimensões e posicionamento 
dos elementos, evitando quebras na apresentação da página.

No exemplo acima, removemos **60px** da **largura** da imagem 
(**30px** da margem esquerda e **30px** da margem direita).

Ao contrário de **%**, **vw**, **vh**, o **calc** não é um valor 
por si só, mas sim uma ferramenta para **calcular valores** no **CSS**.

### calc - Sintaxe

Agora que compreendemos o propósito do **calc**, vamos examinar como usá-lo.

```css
img {
    width: calc(100vw - 60px);
}
```

Adicionamos o **calc** à propriedade na qual desejamos calcular um valor.

Ao lado do **calc**, abrimos e fechamos parênteses, e inserimos o cálculo dentro deles.

O **calc** também pode ser empregado em outras propriedades e para realizar cálculos mais complexos.
