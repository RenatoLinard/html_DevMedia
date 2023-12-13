# Introdução

Em várias situações, temos a necessidade de utilizar listas. Seja para criar listas de compras, listas de passo a passo, listas de afazeres, entre outras aplicações.

Na criação de sites, não é diferente, e neste arquivo, vamos aprender sobre:

- Listas ordenadas
- Listas não ordenadas
- Listas de definições

## O que são listas 

São tópicos de texto organizados de forma vertical, tornando melhor a exemplificação de um determinado assunto.

### Listas ordenadas

São utilizadas para indicar uma sucessão de itens ou sequência de passos.

```html
<ol>
    <li>Misture os ingredientes</li>
    <li>Unte a forma com manteiga e farinha</li>
    <li>Espalhe o recheio na forma</li>
    <li>Leve ao forno</li>
</ol>
```

### Listas não ordenadas

São usadas para listar itens que não se sucedem ou a ordem não tem relevância.

```html
<ul>
    <li>Smartphone</li>
    <li>Câmera</li>
    <li>Notebook</li>
</ul>
```

### Lista de definição

Usada para citar algum termo seguido de sua definição.

```html
<dl>
    <dt>Amor</dt>
    <dd>Forte afeição por outra pessoa</dd>
</dl>
```

### Por que são úteis

Como o principal objetivo do HTML é organizar e estruturar um documento criando uma semântica, utilizar listas tem essa mesma ideia de organização, separando as listagens em seus contextos corretos.

Outro benefício é que o Google saberá diferenciar as listas dos demais conteúdos.

Também é possível estilizar uma lista através do CSS, dando um aspecto mais bonito para as listas.

## Listas ordenadas

Como foi visto, o objetivo da lista ordenada é listar itens de maneira ordenada dentro de um documento HTML.

### Sintaxe 

O início e o fim de uma lista ordenada se dão pela abertura e fechamento da tag `<ol>...</ol>`, e um item inicia e fecha com as tags `<li>...</li>`.

Dentro de um item, podemos utilizar qualquer outro elemento como títulos, imagens, parágrafos e até mesmo fazer um aninhamento com outras listas.

### Atribuição de marcação (type)

Uma lista ordenada pode ser identificada pelo seu marcador, que por padrão vem com uma ordenação numérica. No entanto, podemos alterar a marcação para outros tipos como:

- Numerais romanos 
- Ordenação alfabética

E em ambos os casos, podemos utilizar na forma maiúscula ou minúscula.

### Alterando a marcação

Para fazer a alteração do marcador, utilizamos o atributo `type`.

- `<ol type="1">` - Ordenação numérica (padrão)
- `<ol type="A">` - Ordenação alfabética maiúscula
- `<ol type="a">` - Ordenação alfabética minúscula
- `<ol type="i">` - Numerais romanos minúscula
- `<ol type="I">` - Numerais romanos maiúscula

```html
<ol type="I">
    <li>Item</li>
    <li>Item</li>
    <li>Item</li>
</ol>
```

### Ponto de partida (start)

Podemos definir um ponto de partida usando o atributo `start`. Dessa forma, a numeração iniciará com o número especificado.

```html
<ol start="3">
    <li>Item</li>
    <li>Item</li>
    <li>Item</li>
</ol>
```

### Invertendo a ordem (reversed)

Através do atributo `reversed`, invertemos a ordem da lista.

```html
<ol reversed>
    <li>Item</li>
    <li>Item</li>
    <li>Item</li>
</ol>
```
### Exemplo prático

```html
<!DOCTYPE html>
<html>
<head>
  <title>Lista Aninhada</title>
</head>
<body>
  <!-- Cronograma de estudos -->
  <ol>
    <li>
      <h3>FRONT-END</h3>
      <ol>
        <li>HTML</li>
        <li>CSS</li>
        <li>Bootstrap</li>
      </ol>
    </li>
    <li>
      <h3>BACK-END</h3>
      <ol>
        <li>Lógica de programação com PHP</li>
        <li>Estrutura de dados com PHP</li>
        <li>Orientação a objetos com PHP</li>
      </ol>
    </li>
  </ol>
</body>
</html>
```

## Listas não ordenadas

O objetivo dessa lista é agrupar itens sem se preocupar com a sequencia delas.

### Sintaxe

Uma lista não ordenada se inicia e finaliza com as tags `<ul>...</ul>` e os itens
se iniciam e finalizam com as tags `<li>...</il>`.

Assim como as listas ordenadas podemos utilizar qualquer elemento dentro das listas
não ordenadas.

```html
<ul>
    <li>Laravel</li>
    <li>Controle de versão Git</li>
    <li>Orientação a objetos</li>
    <li>Arquitetura MVC</li>
</ul> 
```

### Atributo de marcação (type)

Nas listas não ordenadas também podemos alterar o marcador com o atributo `type` 
que por padrão são setados com o valor `disc` (círculos pretos).

- `<ul type="disc">` - marcação com bolinhas pretas
- `<ul type="square">` - marcação com quadrados
- `<ul type="circle">` - marcação com bolinhas vazias
- `<ul type="none">` - remove a marcação dos itens

### Exemplo prático

```html
<!DOCTYPE html>
<html>
<head>
    <title>Categorizando produtos</title>
</head>
<body>
<ul>
    <li>
        <h3>Eletrodomésticos</h3>
        <ul type="circle">
            <li>Torradeiras</li>
            <li>Fornos e Fogões</li>
            <li>Geladeiras</li>
        </ul>
    </li>
    <li>
        <h3>Hardware</h3>
        <ul type="circle">
            <li>Placas de vídeo</li>
            <li>Placas de Som</li>
            <li>Processadores</li>
        </ul>
    </li>
</ul>
</body>
</html>
```

## Lista de definição

Tem como objetivo exibir os termos e suas respectivas definições.

### Sintaxe

- `<dl>...</dl>` - Tags de abertura e fechamento de uma lista de definição
- `<dt>...</dt>` - Tags de abertura e fechamento de um termo
- `<dd>...</dd>` - Tags de abertura e fechamento de uma descrição

Podemos utilizar outros elementos dentro de uma lista de definição.

Uma lista de definiçao é composto por um termo e um ou mais definições.

### Exemplo prático

```html
<dl>
    <dt>HTML</dt>
    <dd>Linguagem de marcação utilizada na construção de páginas Web</dd>

    <dt>CSS</dt>
    <dd>Linguagem de estilo usada para definir a apresentação de um documento HTML</dd>

    <dt>Javascript</dt>
    <dd>Linguagem de programação utilizada em páginas web.</dd>
</dl>
```
