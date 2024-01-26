# Elementos Fixos na Tela

Nesta seção, abordaremos a possibilidade de manter um elemento de forma fixa 
na tela, mesmo quando o usuário realiza a rolagem da barra.

## Fixando Elementos na Tela

A fixação de um elemento na tela torna-se útil quando desejamos mantê-lo 
sempre em destaque, facilitando a navegação do usuário na página.

Um exemplo prático é fixar o topo (menu superior) no alto da tela, garantindo 
sua visibilidade constante, mesmo durante a utilização da barra de rolagem pelo usuário.

# Fixando Elementos na Prática

Nesta seção, aprenderemos na prática como é possível manter um elemento fixo na página.

## Position Fixed

Para fixar um elemento na página, utilizamos a propriedade `position` com o valor `fixed`.

```css
div {
    position: fixed;
}
```

# Movendo Elementos

Nesta sessão, veremos como alterar a posição de um elemento na página.

Para modificar a posição de um elemento, utilizamos as propriedades:

- `top`
- `bottom`
- `right`
- `left`

```css
.div_fixa {
    position: fixed;
    border: 2px solid red;
    right: 0;
}
```

A propriedade `right` posicionou o elemento `.div_fixa` na parte direita da 
página. Ao atribuir o valor `0` para `right`, o elemento ficou colado na borda direita.

Caso utilizássemos outro valor para a propriedade `right`, como por exemplo, 
`100px`, o elemento ficaria a essa distância da borda direita.

# Movendo Elementos na Parte Inferior da Página

Para posicionar um elemento na parte inferior da tela, utilizaremos a 
propriedade **bottom**.

```css
div {
    position: fixed;
    border: 1px solid black;
    right: 100px;
    bottom: 35px;
}
```

Dessa forma, a `div` está fixada a **100px** da borda **direita** e **35px** 
da borda inferior da página. Mesmo utilizando o scroll da página, a `div` 
permanece fixa na mesma posição.

# Conhecendo as Propriedades Top e Left

As propriedades **top** e **left** também são utilizadas para mover 
elementos com **position**.

```css
div {
    position: fixed;
    top: 450px;
    left: 300px;
    border: 1px solid black;
}
```

Agora, a `div` está posicionada a **450px** do topo e **300px** da borda esquerda.

## Funcionamento das Propriedades

Nesta sessão, faremos um resumo das propriedades **top, right, bottom, left**.

As propriedades **top** e **bottom** são responsáveis por mover o elemento 
com **position** na vertical. Enquanto as propriedades **right** e **left** 
são responsáveis por movê-lo na horizontal.
