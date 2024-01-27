# Reposicionando Elementos na Tela

Nesta sessão, veremos como retirar um elemento do fluxo padrão do HTML e 
posicioná-lo em outro lugar em nossa página web.

## Reposicionando Elementos

Muitas vezes, ao construir páginas, é necessário posicionar um elemento 
livremente na página, fora do fluxo padrão do HTML.

No fluxo padrão do HTML, os elementos são exibidos na tela na ordem em 
que foram escritos no código.

Para reposicionar, por exemplo, uma imagem, é necessário permitir que ela 
se mova livremente na página, independentemente da ordem em que foi escrita no código.

Isso é útil quando desejamos personalizar nossas páginas, como colocar a 
imagem sobre outro elemento, por exemplo.

# Movendo Elementos Livremente na Página

Para movimentar um elemento livremente na página, utilizamos a propriedade 
**position** com o valor **absolute**.

```css
h2 {
    position: absolute;
}
```

Ao utilizar **position: absolute**, juntamente com as propriedades **top**, 
**bottom**, **left** e **right**, podemos posicionar um elemento de forma independente na página.

```css
h2 {
    color: red;
    position: absolute;
    top: 125px;
    left: 110px;
}
```

A propriedade **position** com o valor **absolute**, ao contrário do valor 
**fixed**, não mantém o elemento fixo na tela quando o usuário utiliza a 
barra de rolagem. Isso permite que o elemento se mova livremente na página.

# Position Absolute Resolve Tudo?

Como vimos até aqui, podemos utilizar a propriedade **position** com o 
valor **absolute** para remover elementos do fluxo padrão do HTML e 
reposicioná-los em qualquer local da página. No entanto, se utilizarmos 
somente o **position: absolute** para posicionar um elemento, qualquer 
alteração no código poderá comprometer o layout da página.
