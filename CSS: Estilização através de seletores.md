# Introdução

Este documento aborda a solução para o desafio de estilização divergente em elementos semelhantes.

## Modificando a Aparência de Tags Semelhantes

Não é sempre desejável que elementos idênticos compartilhem a mesma aparência.
Para lidar com essa situação, utilizamos um seletor CSS para diferenciar os estilos de tags semelhantes.

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

