# Introdução ao CSS (Cascading Style Sheets)

## Visão Geral

A alteração da aparência de uma página web envolve o uso da linguagem de estilização conhecida como CSS (Cascading Style Sheets). O CSS permite a modificação visual dos elementos presentes na página.

- `HTML`: Utilizado para estruturar a página web.
- `CSS`: Empregado para estilizar a página web.

### Exemplo de Uso:

```css
p {
    font-size: 16px;
    font-weight: bold;
    color: black;
}
```

## Sintaxe do CSS

```css
elemento {
    propriedade: valor;
}
```

- `elemento`: Representa uma tag no arquivo HTML.
- `{}`: Delimita a estrutura com um par de chaves no final. Os estilos a serem aplicados encontram-se entre essas chaves.
- `propriedade`: Refere-se à característica do elemento a ser modificada.
- `valor`: Relativo à propriedade e dependente dela para definição.

### Importância da Sintaxe

- A presença de erros na sintaxe impedirá a obtenção do resultado desejado no código.
- Erros comuns incluem:
  - Omissão do par de chaves.
  - Escrita incorreta do nome da propriedade.
  - Falta do ponto e vírgula no final de cada estilo para separá-los.
    - Existem dois casos em que o ponto e vírgula podem ser omitidos:
        1. Se houver apenas um estilo.
        2. Após o último estilo.

## Primeiro código CSS

Agora que entendemos a sintaxe do CSS e a importância de implementá-lo corretamente, veremos as formas de utilizá-lo em uma página HTML.

### Adicionando e Analisando CSS em uma Página

Neste exemplo, vamos utilizar a forma interna de implementação do CSS no HTML.

```html
<!doctype html>
<html lang="pt-br">
    <head>
        <title>Estrutura CSS</title>
        <meta charset="utf-8">

        <style>
            h1 {
                font-size: 40px;
                color: blue;
            }

            p {
                font-size: 20px;
            }
        </style>

    </head>

    <body>
        <h1>Introdução ao CSS</h1>
        <p>A alteração da aparência de uma página web envolve o uso da linguagem de estilização conhecida como CSS (Cascading Style Sheets). O CSS permite a modificação visual dos elementos presentes na página.</p>
    </body>
</html>
```

No exemplo acima, observamos o código CSS dentro da tag `style` e sua sintaxe correta para que seu funcionamento realize o que está sendo solicitado.

A propriedade `font-size` altera em pixels o tamanho das fontes, e `color` altera a cor da fonte.

## Padrões de Cores

Padrões de cores são um assunto importante devido ao seu constante uso em todo tipo de projeto.

Basicamente, utilizamos 3 padrões de cores:

- RGB
- Hexadecimal
- Nome da cor (Inglês)

### Padrão de Cor Nominal

- Utiliza o nome da cor em inglês.
- O nome da cor é definido com valor da propriedade.

### Padrão RGB

- É um sistema de cores onde são combinadas as cores `vermelha (R)`, `verde (G)`, e `azul (B)` para criar uma cor.
- Sua sintaxe segue um padrão:
    - Escrevemos `rgb`.
    - Abrimos e fechamos parênteses.
    - Inserimos respectivamente as cores vermelho, verde e azul.
    - Cada cor é inserida com a quantidade de 0 a 255.
- Normalmente, são utilizadas nas propriedades `color` e `background-color`.

### Padrão Hexadecimal

- Assim como o `rgb` o padrão `hexadecimal` utiliza a combinação de cores `vermelho`, `verde` e `azul` 
- A diferença é que invés de usar valor de 0 à 255 é utilizado caracteres hexadecimais (0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 0, A, B, C, D, E, F)
- Sua sintaxe segue o seguinte padrão:
    - Escrevemos # (hashtag)
    - E os valores referentes a cores vermelho, verde e azul respectivamente
- Pode conter 3 caracteres, sendo um para cada cor ou 6 caracteres, dois para cada cor
- Assim como a nominal e RGB normalmente são utilizadas nas propriedades `color` e `background-color`

Existem duas ótimas ferramentas seletoras de cores:
- [**Site do Mozilla**](https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_Colors/Color_picker_tool) - permite escolher uma cor e ver a forma escrita em `rgb` e `hexadecimal`
- [**Site Pick Color From Image**](https://imagecolorpicker.com/) - permite escolher cores através de imagens

## CSS em um Arquivo Externo

Anteriormente foi utilizado a tag `<style>` para adicionar o CSS interno, agora vamos aprender a usar a tag `<link>` para adicionar um arquivo CSS externo.

A adoção de arquivos externos é altamente recomendada devido à sua capacidade de proporcionar organização e facilitar a manutenção do código. Essa abordagem contribui significativamente para uma estrutura mais limpa e gerenciável.

Vamos seguir um passo a passo simples para criação e organização dos arquivos:

1. Criar um diretório para guardar o arquivo .html e .css.
2. Criar o arquivo com a extensão .html que será responsável por conter a estrutura da página.
3. Criar o arquivo com a extensão .css que será responsável por conter os estilos da página.
4. Por fim, devemos linkar o arquivo .css com .html utilizando a tag `<link rel="stylesheet" href="#">`.

Na propriedade `href`, devemos prestar atenção para descrever o caminho correto do arquivo .css, caso esteja em uma subpasta ou um diretório diferente.

## Propriedades de Fonte

É importante conhecer as diversas propriedades disponíveis para se ter opções de estilização.

### Conhecendo propriedades para estilizar textos

- `font-size`- Altera o tamanho da fonte
    - `valores`- ##px
- `font-family`- Altera a família da fonte
    - `valores`- [

**artigo de fontes padrões**](https://www.devmedia.com.br/lista-de-fontes-padrao-no-css/43215)

### Conhecendo a propriedade para a espessura da fonte

- `font-weight`- propriedade para espessura da fonte
    - `valores`- normal e bold

### Conhecendo a propriedade para o estilo da fonte

- `font-style`- Aplicamos um "efeito" na fonte 
    - `valores`- normal e italic

### Conhecendo a propriedade para aplicar linhas em textos

- `text-decoration`- Responsável por aplicar linhas em um texto
    - `valores`- underline, overline, line-through, none

É muito comum para remover os sublinhados que vem por padrões em links

### Conhecendo a propriedade para alinhar textos

- `text-align`- Define o alinhamento do texto
    - `valores`- left, center, right

### Conhecendo a propriedade que define a altura da linha de textos

- `line-height`- Define a altura das linhas de um texto
    - `valores`- ##px

### Estilizando textos dentro de uma div

Aplicar os estilos dentro de uma div tem o mesmo efeito de aplicar estilos em cada elemento por vez, porém com a vantagem de não precisar replicar o código várias vezes.
É importante ressaltar que caso seja aplicado um estilo em uma div e outro para algum elemento, a prioridade de aplicação fica para o estilo do elemento.