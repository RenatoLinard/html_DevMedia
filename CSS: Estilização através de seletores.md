# Introdução

Este documento aborda a solução para o desafio de estilização divergente em elementos semelhantes.

## Modificando a Aparência de Tags Semelhantes

Não é sempre desejável que elementos idênticos compartilhem a mesma aparência. Para lidar com essa situação, utilizamos um seletor CSS para diferenciar os estilos de tags semelhantes.

Inicialmente, aprendemos a empregar o seletor de tag da seguinte maneira:

```css
div {
    font-size: 20px;
    font-family: Arial;
}
```

Agora, exploraremos o uso do seletor de `class` para estilizar uma tag específica.

```css
.texto-vermelho {
    color: red;
    font-size: 25px;
}
```

### Conceito de Seletores CSS

Os seletores são meios pelos quais o CSS identifica os elementos a serem estilizados.

- **Seletor de Tag:** O CSS identifica o elemento através da tag associada.

```css
div {
    font-size: 20px;
    font-family: Arial;
}
```

- **Seletor de Classe:** O CSS identifica o elemento pelo nome de sua classe.

```css
.texto-vermelho {
    color: red;
    font-size: 25px;
}
```

## Seletor de Tag

Já vimos a estilização através do seletor de tag anteriormente.

```css
span {
    font-size: 25px;
    font-family: fantasy;
    font-weight: bold;
}
```

Dessa forma, o CSS identifica o elemento pela tag na página e estiliza de forma global a tag.

Seu uso basicamente envolve utilizar o nome da tag dentro do código CSS, adicionando as propriedades desejadas e, assim, alterando a aparência de qualquer elemento identificado por aquela tag.

### Quando Utilizamos

Optamos por utilizar o seletor de tag quando desejamos aplicar o mesmo estilo a tags iguais em diferentes partes do documento.

## Seletor de Classe

Permite definir estilos específicos na página.

### Conhecendo o Seletor de Classe 

Inicialmente, aprendemos que para deixar elementos iguais com a mesma aparência, utilizamos o seletor de tag.

E se quisermos alterar a aparência de uma tag específica?

Para isso, utilizamos o seletor de classe, que permite deixar elementos iguais com aparências diferentes.

### Como Usar

No código HTML:

```html
<span class="texto-destaque">estilo diferente</span>
```

Na tag de abertura, inserimos o atributo `class` seguido de um valor entre aspas duplas.

No código CSS:

```css
.texto-destaque {
    color: red;
}
```

Basta utilizar o sinal de ponto (.) junto com o nome da classe.

### Exemplo de Uso

```html
...
<p>Os <span> elementos de classe</span> no CSS permitem aplicar estilos 
<span class="texto-destaque">personalizados</span>.</p>
...
```

```css
.texto-destaque {
    font-size: 20px;
    color: red;
    font-weight: bold;
}
```

### Combinando Estilos de Seletores

Quando há estilização através do seletor de tag e outro através de uma classe, o seletor de tag irá estilizar globalmente as tags selecionadas, enquanto o seletor de classe irá estilizar a tag selecionada, combinando os efeitos dos dois seletores. Desta forma, a tag em questão terá ambos os seletores aplicados para estilização.

```html
<span class="texto-destaque">estilo diferente</span>
```

```css
span {
    font-weight: bold;
}
.texto-destaque {
    color: red;
}
```

Assim, a tag `<span>` será exibida em negrito devido ao seletor de tag e terá a cor vermelha devido ao seletor de classe.

### Sobrescrevendo Estilos com Seletores

No exemplo anterior, demonstramos a combinação de seletores. Agora, se desejarmos remover apenas o estilo de negrito da tag que também possui o seletor de classe, devemos incluir no seletor de classe a instrução para normalizar o peso da fonte.

```html
<span class="texto-destaque">estilo diferente</span>
```

```css
span {
    font-weight: bold;
}
.texto-destaque {
    color: red;
    font-weight: normal;
}
```

Dessa forma, estamos sobrescrevendo o estilo definido pelo seletor de tag, removendo o negrito especificamente para a classe em questão.

### Utilizando uma Classe em Dois Elementos

Uma abordagem alternativa para resolver o problema mencionado acima é criar duas classes distintas: uma para textos em negrito e outra para textos com a cor vermelha.

```css
.texto-negrito {
    font-weight: bold;
}
.texto-vermelho {
    color: red;
}
```

Assim, podemos selecionar os textos que desejamos em negrito com o seletor 
`.texto-negrito` e os textos que desejamos em vermelho com o seletor `.texto-vermelho`. 
Essa prática permite o uso da mesma classe em mais de um elemento, proporcionando flexibilidade e reusabilidade.

## Reaproveitando Classes

### Reaproveitando Classe em Elementos Diferentes

Anteriormente, observamos que podemos usar a mesma classe em elementos semelhantes. Agora, expandindo essa ideia, podemos aplicar classes a elementos diferentes.

### Utilizando Mais de uma Classe no Mesmo Elemento

É possível adicionar mais de um estilo a um elemento. Para isso, criamos uma nova classe.

```css
.texto-verde {
    color: green;
}
```

Em seguida, adicionamos a nova classe ao elemento.

```html
<span class="texto-negrito texto-verde">Texto exemplo</span>
```

Observe que separamos as classes com um espaço em branco.

## Agrupando Seletores

### Agrupando Seletores de Tag

Anteriormente, aprendemos a definir a mesma aparência para várias tags usando vírgulas.

```css
a, p {
    color: red;
}
```

Esse conceito é chamado de `agrupamento de seletores`.

### Agrupando Seletores de Classe

Podemos agrupar seletores de classe da mesma forma que os seletores de tag.

```css
.subtitulo, .paragrafo {
    font-family: Helvetica;
    font-size: 18px;
}
```

Semelhante ao seletor de tag, agrupamos as classes separando-as por vírgulas.

## Descendência de Elementos

Neste tópico, aprenderemos como agrupar seletores no código CSS.

### Seletores de Tags Descendentes

Se desejarmos estilizar um elemento específico dentro de outro, podemos utilizar o seletor de tag e indicar dentro de qual elemento ele se encontra.

```html
<div>
    <p>Esse é um parágrafo</p>
</div>
```

```css
div p {
    font-weight: bold;
    color: red;
}
```

Primeiro, indicamos a tag que envolve o elemento e, em seguida, utilizamos um 
espaço e especificamos o elemento que queremos estilizar.

Ao combinarmos seletores de tag, é importante ter em mente que a combinação 
será aplicada a toda a estrutura HTML. Portanto, é crucial ter cuidado ao 
realizar essas combinações para evitar estilos indesejados.

### Seletores de Classes Descendentes

Da mesma forma que fizemos anteriormente com o seletor de tag podemos combinar 
os seletores de classe para estilzar elementos especificos.

```css
.secao-conteudo .texto {
    color: #109ce3;
    border-left: 5px solid #109ce3;
    padding-left: 10px;
}
```

Primeiro, indicamos a classe que envolve o elemento e em seguida, utilzamos um 
espaço em branco e especificamos o elemento que queremos estilizar.


