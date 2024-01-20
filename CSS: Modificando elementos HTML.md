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

# Exibindo e Ocultando Elementos

Nesta seção, aprenderemos como lidar e manipular a exibição de elementos no HTML.

## Elementos de Bloco e de Linha

Todo elemento HTML, por padrão, possui um tipo de exibição: **block (bloco)** 
ou **inline (linha)**.

- Um elemento do tipo **block** é criado sempre após o elemento anterior. 
Por exemplo, se criarmos dois **títulos**, eles aparecem **um abaixo do outro**. 
Do mesmo modo, se criarmos duas **divs** com cores diferentes, elas aparecem 
uma **abaixo da outra**. Além disso, elementos do tipo **block** ocupam toda a 
largura disponível para eles. Alguns elementos comuns do tipo **block** são as 
**divs**, os **parágrafos (p)** e os **títulos (h1-h6)**.

- No tipo **inline**, os elementos, por padrão, são criados ao lado de 
outros elementos. Por exemplo, se criarmos duas **spans**, elas aparecem 
**lado a lado**. Além disso, elementos do tipo **inline** ocupam apenas a 
**largura necessária** para exibir seu conteúdo. Alguns elementos comuns do tipo 
**inline** são o **span**, o **link (a)** e a **imagem (img)**.

Agora que entendemos as diferenças entre os elementos do tipo **block** e 
**inline**, veja como podemos manipular o tipo de exibição através do **CSS**.

## Contextualizando

```html
<div>
    <img src="foto.jpg">
    <p>Renato</p>
</div>
```

No exemplo acima, o nome do usuário aparece abaixo da foto por se tratar 
de um **parágrafo**, um elemento do tipo **block**.

Podemos alterar esse comportamento através da propriedade **display**, 
usando o valor **inline**.

```css
div {
    display: inline;
}
```

A propriedade **display** é capaz de transformar elementos **block** em 
**inline** e vice-versa.

Agora que fomos contextualizados no assunto, vamos entender como funciona 
a propriedade **display**.

## Display

Podemos utilizar a propriedade **display** no **CSS** para modificar o 
**modo de exibição** de um elemento.

A propriedade **display** possui diversos valores, alguns deles são: 
**inline**, **block**, **none**.

Como comentado anteriormente, o valor **inline** transforma um elemento 
do tipo block em **inline**.

E o valor **block** transforma um elemento do tipo inline em **block**.

Por fim, temos o valor **none**, que oculta a exibição de um elemento.

O elemento continua existindo, mas não é exibido para o usuário no navegador.

```css
div {
 display: inline;
}

span {
 display: block;
}

img {
 display: none;
}
```

## Visibility

**Visibility** é uma **propriedade** do **CSS** que controla a 
**visibilidade** de um elemento na tela.

A **visibility** possui dois valores mais usados: **visible** e **hidden**.

**Visible** indica que o elemento está **visível**, sendo esse o 
**valor padrão** de todo elemento.

```css
div {
    visibility: visible;
}
```

**Hidden**, por sua vez, deixa o elemento **invisível** na tela.

```css
div {
    visibility: hidden;
}
```

Apesar da semelhança com a propriedade e valor **display: none**, **visibility** 
não remove o espaço do elemento da tela; ele apenas o deixa **invisível**.

### Visibility - Sintaxe

A sintaxe é composta pelo nome da **propriedade** e seu **valor**.

```CSS
div {
    visibility: visible;
}
```

Deixa o elemento visível, e como é o padrão, não é obrigatório utilizá-lo.

```css
div {
    visibility: hidden;
}
```

Esconde o elemento, mas não remove o espaço na página.

## Opacity

Através do **CSS**, também é possível alterar a opacidade de um elemento HTML, 
ou seja, seu nível de **transparência**.

Sua sintaxe segue o padrão das demais propriedades citadas anteriormente, com 
o nome da propriedade e seu valor.

Nesse caso, podemos usar o valor em **porcentagem** ou **escala decimal**.

- `porcentagem` - De 0% a 100%. Quanto menor o valor, mais **transparente** o elemento.

- `escala decimal` - De 0 a 1.0. Quanto maior o valor, menos transparente o elemento.

# Box-Sizing

Nesta sessão, vamos entender como o **CSS** calcula o tamanho de um elemento.

## Contextualizando

Considere que temos uma página com uma imagem de capa que utiliza **toda a 
largura** da tela.

Entretanto, precisamos adicionar um **padding** de 20px e um 
**background-color** nessa imagem.

Isso poderia quebrar a página, pois a **largura** da tela seria 
ultrapassada, criando uma barra de rolagem horizontal.

Esse problema pode ser resolvido com o **calc**, mas existe uma maneira 
mais simples: o **box-sizing**.

## O Que é?

Por padrão, o **tamanho do elemento** leva em conta sua **altura**, 
**largura**, **padding** e **border**.

```css
div {
    width: 350px;
    padding: 20px;
}
```

Repare que, mesmo tendo definido a largura como 350px, o elemento cresceu e 
ficou com um total de 390px.

Para impedir que o elemento **cresça**, utilizamos o **box-sizing**, fazendo 
com que o **padding** seja incluído na largura total.

Internamente, o **CSS** vai **subtrair** o **padding** do width.

O mesmo vale para a **altura**.

Com o **box-sizing: border-box**, as medidas do elemento passam a ser 
respeitadas, e os valores do **padding** e **border** passam a ser 
**incluídos** no valor da largura.

## Sintaxe 

O **box-sizing** é uma propriedade do **CSS** e sua **sintaxe** segue o mesmo 
padrão das demais, com o **nome** e **valor**.

```css
div {
    box-sizing: border-box;
}
```

O valor mais utilizado é o **border-box**, que faz com que as medidas do 
elemento sejam respeitadas.

Existe também o **content-box**, que é o **valor padrão**, por isso seu 
uso não é necessário.

# Box-shadow

O **box-shadow** é uma propriedade **CSS** que permite adicionar **sombra** em 
volta dos elementos.

A **sombra** pode ser aplicada a qualquer elemento **HTML**, como **divs**, 
**spans** e até mesmo em **img**.

## Deslocamento

Para o **box-shadow** funcionar, ele precisa receber dois valores, o 
**deslocamento x** e o **deslocamento y**.

```css
img {
    width: 250px;
    height: 250px;
    box-shadow: 20px 0;
}
```

O primeiro valor refere-se ao **deslocamento x (horizontal)**, enquanto o 
segundo se refere ao **deslocamento y (vertical)**.

**Deslocamento** é o **valor** que define a **posição** em que a sombra vai aparecer.

O **valor padrão** dos eixos **x** e **y** é **0**, o que significa que a 
sombra está **atrás** do elemento.

Quando **deslocamos** a sombra, sua **posição** é ajustada a partir 
da **posição do elemento**.

No eixo **x**, o **valor positivo** move a sombra para a **direita**.

Já um valor **negativo** no **eixo x** move a sombra para a **esquerda**.

No **eixo y**, um **valor positivo** move a sombra para **baixo**.

Já um **valor negativo** no **eixo y** move a sombra para **cima**.

## Desfoque

É possível aplicar um efeito de **desfoque** à sombra adicionando um terceiro 
valor ao **box-shadow**.

```css
img {
    width: 250px;
    height: 250px;
    box-shadow: 20px 20px 10px;
}
```

Quanto maior o **valor**, maior o **desfoque**.

## Expansão 

Por padrão, a sombra tem o **mesmo tamanho** do elemento.

É possível **expandir** a sombra em todas as direções, adicionando um quarto 
valor ao **box-shadow**.

```css
img {
    width: 250px;
    height: 250px;
    box-shadow: 0 0 0 30px;
}
```

Quando adicionamos uma expansão, a sombra aumenta de **tamanho** em 
**todas as direções**.

O uso da expansão é opcional, mas quando for utilizado, é necessário informar 
o valor do desfoque, mesmo que seja **0**.

## Cor 

Por padrão, a sombra tem a **cor preta**.

É possível alterar a **cor da sombra** preenchendo um **quinto** valor com 
a **cor desejada**.

```css
img {
    width: 250px;
    height: 250px;
    box-shadow: 20px 20px 0 0 blue;
}
```

Já vimos como adicionar sombras externas em elementos; agora, vamos ver 
como utilizar sombras internas.

## Inset 

Por padrão, o **box-shadow** cria uma sombra com o tamanho do elemento atrás dele.

O **valor inset** modifica isso, criando a sombra na **frente** do elemento 
com a **expansão** informada.

```css
div {
    width: 450px;
    text-align: center;
    background-color: green;
    padding: 10px;
    box-shadow: 0 0 30px 20px black inset;
}
```

Se **expandirmos** uma **sombra inset** em 20px, ela contará esse tamanho 
**a partir das bordas** do elemento.

O valor **inset** funciona com **divs**, **spans** e outros elementos, **mas não com img**.

O valor **inset** pode ser colocado no **início** ou no **final** do **box-shadow**.
