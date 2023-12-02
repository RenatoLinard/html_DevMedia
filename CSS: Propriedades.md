# Conceito de Propriedades CSS

Neste artigo, exploraremos de maneira mais detalhada as principais propriedades do CSS e como elas influenciam a aparência de um elemento em uma página web.

## Resumo do Artigo Anterior

As propriedades representam características dos elementos da página web.

Exemplo de HTML:

```html
<a href="#contato">Contato</a>
```

Exemplo de CSS:

```css
a {
    font-size: 24px;
    color: white;
    background-color: black;
}
```

A aparência da tag de link está sendo modificada por meio das propriedades `font-size`, `color` e `background-color`. Cada uma desempenha uma função específica para alterar o estilo do link.

- 1. `font-size` - Altera o tamanho da fonte.
- 2. `color` - Altera a cor da fonte.
- 3. `background-color` - Altera a cor de fundo.

## Cor

Uma das alterações mais comuns na hora de estilizar é a mudança de cor. Para isso, temos duas propriedades muito comuns para esse propósito: `color` e `background-color`.

No artigo anterior, discutimos os padrões utilizados no CSS para alterar a cor.

- 1. `Nominal` - Utiliza o nome da cor em inglês.
- 2. `Hexadecimal` - Utiliza caracteres hexadecimais.
- 3. `RGB` - Utiliza a combinação vermelho (`RED`), verde (`Green`) e azul (`Blue`) com uma escala de intensidade de 0 a 255.

Exemplos de utilização:

```css
a {
    color: white;
}
```

```css
a {
    background-color: #FFFFFF;
}
```

```css
a {
    background-color: rgb(255, 255, 255);
}
```

No exemplo acima, representamos a mesma cor utilizando os padrões mencionados.

## Fonte

Outra alteração importante para o programador conhecer são as propriedades de alteração de fontes. Para isso, temos: `font-size`, `font-family`, `font-weight`, `text-decoration`, `text-align`, `line-height`.

- 1. `font-size` - Tamanho da fonte.
- 2. `font-family` - Família da fonte.
- 3. `font-weight` - Espessura da fonte.
- 4. `text-decoration` - Tracejado da fonte.
- 5. `text-align` - Alinhamento do texto.
- 6. `line-height` - Altura da linha do texto.

```css
p {
    font-size: 24px;
    font-family: Verdana;
    font-weight: bold;
    text-decoration: underline;
    text-align: center;
    line-height: 20px;
}
```

## Altura e Largura

Duas propriedades essenciais que determinam a área que um elemento ocupa na tela são altura (`height`) e largura (`width`).

```css
div {
    height: 100px;
    width: 100px;
    background-color: green;
}
```

- `height` - Define a altura do elemento.
- `width` - Define a largura do elemento.

As propriedades `height` e `width` podem ser aplicadas a qualquer elemento HTML.

Quando utilizamos as propriedades `height` e `width`, podemos distorcer uma imagem caso não utilizemos valores proporcionais às dimensões originais da imagem.

## Margem

Essas propriedades são úteis para a estilização de uma página, pois criam um espaçamento entre os elementos, evitando que fiquem "colados" entre si.

Alguns elementos já possuem a margem padrão, porém podemos alterá-las para deixá-los mais ou menos espaçados.

```css
h1 {
    margin: 60px;
}
```

Quando definimos apenas um valor de `margin`, como no exemplo acima, estamos definindo um valor para cima, direita, baixo e esquerda.

Podemos ser mais específicos em qual lado queremos alterar usando:

- 1. `margin-top` - espaçamento de cima
- 2. `margin-right` - espaçamento da direita
- 3. `margin-bottom` - espaçamento de baixo
- 4. `margin-left` - espaçamento da esquerda

### Propriedades específicas de margem

Dessa forma, especificamos exatamente o lado que queremos alterar a margem.

```css
p {
    margin-top: 10px;
    margin-bottom: 5px;
    margin-left: 15px;
    margin-right: 15px;
}
```

### Formas compactas de propriedade

Também podemos usar uma forma mais compacta para definir os quatro lados usando apenas uma linha de código.

```css
div {
    margin: 70px 20px 10px 60px;
}
```

Dessa forma, estamos definindo, respectivamente, o lado de cima (top), direita (right), baixo (bottom), esquerda (left).

Temos também uma segunda forma compacta para definir o espaçamento dos elementos.

```css
div {
    margin: 20px 15px;
}


```

Dessa forma, definimos da seguinte forma:

- `margin-top e margin-bottom` - 20px
- `margin-right e margin-left` - 15px

### Centralizando elementos na tela

Podemos usar a propriedade `margin` para centralizar

 um elemento da tela.

```css
div {
    margin: 10px auto 
}
```

Dessa forma, definimos da seguinte forma:

- `margin-top e margin-bottom` - 10px
- `margin-right e margin-left` - auto

Dessa forma, o valor `auto` faz com que as margens laterais fiquem do mesmo tamanho se ajustando à tela, independente do tamanho da tela o elemento vai se ajustar lateralmente ficando sempre centralizado.

### Removendo as margens de um elemento

Como citado anteriormente alguns elementos possuem margens pré-definidas e se quisermos remover essas margens por algum motivo utilizamos o "0" como valor.

```css
div {
    margin: 0;
}
```

## Borda

A propriedade "border" é utilizada para criar linhas ao redor dos elementos.

Para criar essas bordas ao redor dos elementos, usamos as seguintes propriedades:

1. `border-width` - Largura da borda.
2. `border-style` - Estilo da borda.
3. `border-color` - Cor da borda.

```css
div {
    border-width: 2px;
    border-style: solid;
    border-color: #454545;
}
```

O estilo da borda (`border-style`) é a única característica obrigatória para aplicar a borda em um elemento. As outras características são opcionais.

### Como Usar as Propriedades nos Elementos

- `border-width` - Representa a largura da borda de um elemento, definindo a espessura da borda. Seu valor é representado por números de pixels.
- `border-style` - Representa o estilo de uma borda do elemento, definindo a aparência da borda. Seus valores são variados e podem ser acessados na lista de sugestões do IDE.
- `border-color` - Representa a cor da borda de um elemento. Com isso, podemos colorir a borda. Seu valor é definido por um dos três padrões de cores (nominal, hexadecimal, RGB).

### Usando a Propriedade `border`

A propriedade `border` oferece uma maneira compacta de definir todas as características da borda em uma única linha de código. Por exemplo:

```css
div {
    border: 2px solid #454545;
}
```

Dessa forma, podemos especificar a largura, o estilo e a cor da borda em uma única declaração.

Podemos omitir as características de cor e espessura, porém o estilo continua sendo obrigatório no código.

A ordem na qual são declaradas as características não afeta no código, porém é interessante seguir o padrão `border: 2px solid #454545` espessura, estilo e cor.

### Usando propriedades especificas para os lados do elemento

Podemos aplicar bordas em um lado especifico do elemento. Temos quatro propriedades que representam as bordas nos lados dos elementos.

- `border-top`- Cria borda na parte superior 
- `border-right`- Cria borda no lado direto
- `border-bottom`- Cria borda na parte inferior
- `border-left`-  Cria borda no lado esquerdo

Podemos combinar as propriedades de borda:

```css
div {
    border-top: 2px dotted #454545;
    border-bottom: dashed;
    border-left: 10px #454545;
    border-right: 5px dotted green;
}
```

Caso todas as bordas tenham o mesmo valor é recomendado utilizar apenas a propriedade `border`.