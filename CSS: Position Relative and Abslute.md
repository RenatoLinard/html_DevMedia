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

# Position Relative

Nesta sessão, vamos conhecer o **position: relative** e entender como ele é 
útil para posicionar um elemento com o **position: absolute**.

Anteriormente, mencionamos que se utilizarmos apenas o **position: absolute** 
para posicionar um elemento, qualquer alteração no código pode quebrar o 
layout da página.

Mesmo dentro de uma **div**, o elemento não respeitará os limites 
estabelecidos quando utilizado apenas o **position: absolute**, pois ele 
sempre se posicionará de acordo com as bordas da página.

É aqui que entra o **position: relative**.

## Usando o **Relative** para Limitar o **Absolute**

A propriedade **position** com o valor **relative** também permite que um 
elemento seja reposicionado na página, mas, diferentemente dos valores 
**fixed** e **absolute**, não remove o elemento do fluxo padrão do HTML.

```css
div {
    position: relative;
    margin-top: 30px;
    border: 1px solid black;
    background-color: white;
    width: 320px;
    height: 400px;
    padding: 10px;
}

img {
    position: absolute;
    width: 100px;
    top: -25px;
    right: -25px;
}
```

Neste exemplo, estamos fazendo com que a **img** seja sempre posicionada de 
acordo com os limites da **div**. Ou seja, a **img** passa a estar 
posicionada em relação à **div** em que está contida, e não em relação à página.

## Position Relative Resolveu o Problema?

Com o **absolute**, podemos posicionar um elemento em qualquer lugar da 
página, tendo as bordas da página como referência. Quando utilizamos o 
**relative** no elemento pai, o elemento com **absolute** passa a ser 
posicionado a partir das bordas do pai.

Podemos dizer que usar o **relative** no elemento pai é como definir um 
**mapa** pelo qual o elemento com **absolute** se moverá. Se o elemento 
pai não estiver com **relative**, o mapa para o elemento com **absolute** 
passa a ser a página inteira.
