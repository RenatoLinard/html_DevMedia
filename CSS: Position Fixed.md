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
