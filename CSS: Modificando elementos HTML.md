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

# Valores Relativos

Como mencionado anteriormente, um valor relativo é aquele que define 
o seu valor com base em outro elemento.

Esse valor é expresso em porcentagem e faz com que o elemento filho ocupe a 
proporção definida em relação ao elemento pai.

## Porcentagem - Sintaxe

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

## vw e vh

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

# Definindo o Tamanho dos Elementos

Anteriormente, utilizamos bastante a propriedade **width**. Agora, vamos 
explorar a definição de largura mínima e máxima.

## Definindo a Largura do Elemento

Aprenderemos a utilizar as propriedades **min-width** e **max-width** 
para estabelecer a largura mínima e máxima de um elemento.

```css
img {
    width: 100%;
    min-width: 1200px;
}
``` 

A propriedade **min-width** determina a largura mínima do elemento, ou 
seja, o menor tamanho que o elemento pode ter. No exemplo acima, a imagem 
terá 100% de largura, mas não poderá ter menos de 1200px, garantindo seu 
tamanho mínimo em telas menores que 1200px de largura.

```css
img {
    width: 100%;
    min-width: 1200px;
    max-width: 1300px;
}
```

Para definir o tamanho máximo, utilizamos **max-width**. Este representa o 
maior tamanho que o elemento pode alcançar. No exemplo, quando a tela 
for maior que 1300px, o elemento não aumentará mais. Em telas iguais ou 
 menores que 1300px, o elemento ocupará 100% da tela.

Sempre que as propriedades **min-width** e **max-width** são definidas, elas 
se sobrepõem ao tamanho especificado em **width**.

## Definindo a altura do elemento

**min** e **max-height** seguem as mesmas regras de **min** e **max-width**,
porém, controlando a altura.

### min-width e max-width - sintaxe

```css
img {
    width: 100%;
    min-width: 1200px;
    max-width: 1300px;
}
```

Adicionamos a propriedade **min-width** e/ou **max-width** no elemento que 
queremos aplicar o estilo.

As propriedade **min-width** e **max-width** suportam valores em **px**, **%**,
**vw/vh**, e atá mesmo **calc*.

### min-height e min-height - sintaxe

**min** e **max-height** seguem as mesmas regras de sintaxe de **min** e 
**max-width**, porém, controlando altura.

# Overflow

O **overflow** assegura que o conteúdo respeite as dimensões do elemento,
criando uma **barra de rolagem** que permite a leitura do texto sem ultrapassar 
o tamanho, caso o texto seja muito extenso e exceda a área do elemento.

## Overflow - Sintaxe

```css
div {
  overflow: scroll;  
}
```

Para utilizá-lo, devemos adicionar a propriedade **overflow** no elemento desejado.

Em seguida, informamos o valor que queremos aplicar ao **overflow**.

O **overflow** possui diversos valores possíveis. Vamos abordar dois deles:

- `scroll` - Exibe a barra de rolagem horizontal e vertical, garantindo que o 
conteúdo interno não ultrapasse o tamanho especificado no CSS. Com o valor 
**scroll**, as barras de rolagem serão exibidas independentemente de o 
conteúdo ultrapassar ou não a área do elemento.

- `auto` - O **overflow auto** também adiciona uma barra de rolagem ao 
elemento. No entanto, ela só é exibida se o conteúdo ultrapassar o tamanho 
determinado.

## overflow-x e overflow-y - Sintaxe

A propriedade **overflow** afeta tanto a **barra de rolagem vertical** quanto 
a **horizontal**.

No entanto, quando queremos que o overflow afete apenas uma das **barras de 
rolagem**, podemos utilizar as propriedades **overflow-x** e **overflow-y**.

O **overflow-x** controla o scroll **horizontal**, adicionando uma 
barra de rolagem horizontal.

Já o **overflow-y** controla o scroll **vertical**, adicionando uma barra 
de rolagem vertical.

Em alguns casos, ao utilizar apenas o **overflow-x** ou apenas o 
**overflow-y**, podem ser exibidas as duas barras de rolagem na tela. 
Isso ocorre porque, quando o **overflow-x** ou **overflow-y** não são 
definidos, eles têm o valor **auto**. Dependendo do tamanho do elemento, pode 
ser necessário a barra de rolagem **auto**. Para resolver esse problema, basta 
definir a medida **width** ou **height** de modo a comportar na tela sem quebrar.

### Simplificando o overflow-x e overflow-y 

As propriedades **overflow-x** e **overflow-y** podem ser simplificadas 
por meio da propriedade **overflow**.

```css
div {
    overflow-x: auto;
    overflow-y: scroll;
}
```

```css
div {
    overflow: auto scroll;
}
```

Ao simplificar, o primeiro valor refere-se ao **overflow-x** e o segundo ao 
**overflow-y**.
