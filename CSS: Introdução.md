# Introdução ao CSS (Cascading Style Sheets)

## Visão Geral

A alteração da aparência de uma página web envolve o uso de uma linguagem de estilização conhecida como CSS (Cascading Style Sheets). O CSS permite a modificação visual dos elementos presentes na página.

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
    - Existem dois casos em que o ponto e vírgula pode ser omitido:
        1. Se houver apenas um estilo.
        2. Após o último estilo.

## Primeiro código CSS

Agora que entendemos a sintaxe do CSS e a importância de implementá-lo corretamente, veremos as formas de utilizá-lo em uma página HTML.

### Adicionando e analisando CSS em uma página

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
        <p>A alteração da aparência de uma página web envolve o uso de uma linguagem de estilização conhecida como CSS (Cascading Style Sheets). O CSS permite a modificação visual dos elementos presentes na página.</p>
    </body>
</html>
```

No exemplo acima, observamos o código CSS dentro da tag `style` e sua sintaxe correta para que seu funcionamento realize o que está sendo solicitado.

A propriedade `font-size` altera em pixels o tamanho das fontes e `color` altera a cor da fonte.

## Padrões de cores

Padrões de cores é um assunto importante para ser abordado devido seu constante uso uso em todo tipo de projeto.

Basicamente utilizamos 3 padrões de cores:

- RGB
- Hexadecimal
- Nome da cor (Inglês)

### Padrão de cor nominal

- Utiliza o nome da cor em inglês
- O nome da cor é definido com valor da propriedade

### Padrão RGB

- É um sistema de cores onde é combinado as cores `vermelha (R)`, `verde (G)` e `azul (B)` para criar uma cor
- Sua sintaxe segue um padão:
    - Escrevemos rgb
    - abrimos e fechamos parênteses 
    - e inserimos respectivamente as cores vermelho, verde e azul
    - cada cor é inserida com a quantidade de 0 à 255
- Normalemente são utilizadas nas propriedade color e background-color

### Padrão hexadecimal

