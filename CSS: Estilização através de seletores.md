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

### Combinando estilos de seletores


