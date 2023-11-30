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

`height` - Define a altura do elemento.
`width` - Define a largura do elemento.

As propriedades `height` e `width` podem ser aplicadas a qualquer elemento HTML.

Quando utilizamos as propriedades `height` e `width`, podemos distorcer uma imagem caso não utilizemos valores proporcionais às dimensões originais da imagem.