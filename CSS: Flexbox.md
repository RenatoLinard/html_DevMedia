# Introdução

Até o momento, utilizamos a propriedade **CSS** `position` para posicionar 
elementos na página. No entanto, essa abordagem se mostra limitada ao lidar 
com a estruturação de páginas que exigem layouts mais complexos, especialmente 
quando envolvem múltiplos containers.

Para superar esse desafio, adotamos uma ferramenta chamada **CSS Flexbox**, que 
se destaca como a principal abordagem para posicionar elementos com **CSS**.

## Revisando o CSS position

Até agora, temos empregado a propriedade **CSS position** como a maneira mais 
simples de posicionar elementos na página. Contudo, sua eficácia é limitada 
quando tratamos de múltiplos containers na página.

## Limitação do CSS position

Ao considerarmos a criação de uma página com diversos cards, o fluxo padrão 
resulta em uma disposição vertical, um card abaixo do outro. No entanto, caso 
desejemos alinhar os cards horizontalmente, seria necessário escrever vários 
códigos para alcançar o resultado desejado. Essa abordagem não apenas demanda 
mais código, mas também compromete a responsividade do layout, pois não se 
ajusta adequadamente ao tamanho da tela, podendo resultar na perda do layout concebido.

# CSS Flexbox

## Introdução ao Flexbox

O **CSS Flexbox** é a abordagem principal para posicionar elementos dentro de um container.

Com ele, podemos posicionar todos os elementos de uma só vez, proporcionando maior flexibilidade 
no layout.

O Flexbox permite posicionar os elementos de diversas formas.

```css
.container {
    display: flex;
    flex-direction: column, row;
}
```

Ao utilizar o Flexbox, o elemento com a classe "container" terá seus filhos dispostos em uma coluna 
ou linha, conforme definido pela propriedade `flex-direction`. Essa flexibilidade oferecida pelo Flexbox 
simplifica significativamente o posicionamento dos elementos, tornando o código mais limpo e eficiente.