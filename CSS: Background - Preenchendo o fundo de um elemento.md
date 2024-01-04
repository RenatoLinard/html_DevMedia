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

## Background-image

Anteriormente, abordamos a possibilidade de utilizar uma imagem como fundo para 
estilizar um elemento.

### Como Implementar

```css
div {
    background-image: url('img/img-fundo.jpg');
}
```

Para aplicar essa técnica, utilizamos a propriedade `background-image` 
seguida por dois pontos. Em seguida, inserimos a URL da imagem entre parênteses 
e aspas, lembrando de incluir a extensão do arquivo no caminho.

### Localização das Imagens

A organização é fundamental. Recomenda-se criar uma pasta específica 
para armazenar as imagens do site. Dessa forma, ao inserir o caminho da 
imagem utilizando a propriedade `background-image`, referenciamos a pasta do projeto.

É válido ressaltar que, além de utilizar imagens salvas localmente, 
também podemos empregar URLs de sites para incorporar imagens.

A propriedade `background-image` pode ser empregada em qualquer seletor CSS, 
proporcionando flexibilidade na aplicação da estilização desejada.

## Estilizando a Imagem de Fundo

Quando preenchemos um elemento com uma imagem, por padrão, ela se repete para ocupar todo o espaço disponível. Para evitar a repetição, utilizamos a propriedade `background-repeat` com o valor `no-repeat`.

```css
div {
    background-repeat: no-repeat;
}
```

Também é possível controlar a repetição vertical (`repeat-y`) ou horizontal (`repeat-x`) da imagem. Em casos onde a imagem não preenche completamente o espaço, podemos utilizar `background-color` para preencher o restante com uma cor desejada.

### Posicionando a Imagem de Fundo

Após inserir a imagem, podemos posicionar utilizando a propriedade `background-position`.

```css
div {
    background-position: center;
    background-position: left;
    background-position: right;
    background-position: top;
    background-position: bottom;
}
```

Misturar posições também é viável.

```css
div {
    background-position: center top;
    background-position: right bottom;
}
```

### Ajustando o Tamanho da Imagem de Fundo

Para modificar o tamanho da imagem de fundo, utilizamos a propriedade `background-size`.

#### Valores Possíveis

- `cover`: Preenche todo o espaço do elemento, exibindo apenas parte da imagem.
- `contain`: Estica a imagem para que caiba no elemento, mantendo a proporção.
- `50% 50%`: Define a porcentagem do tamanho do elemento que a imagem ocupará (largura e altura).
- `500px 500px`: Utiliza valores em pixels para definir largura e altura.

### Fixando a Imagem de Fundo

Ao rolar a página, a imagem de fundo normalmente acompanha o movimento. Para mantê-la estática, utilizamos `background-attachment` com o valor `fixed`, criando o efeito conhecido como `parallax`. Isso gera uma ilusão de profundidade, tornando a imagem estática enquanto o conteúdo rola.

## Escrita Reduzida

Podemos simplificar a escrita utilizando uma forma reduzida para a propriedade `background`.

```css
background: top right no-repeat #0f0 fixed url('img/fundo-floresta.jpg');
```

Apesar de não haver uma ordem específica, é recomendável manter os valores separados para facilitar a manutenção durante a fase de desenvolvimento.
