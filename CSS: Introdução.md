# Introdução ao CSS (Cascading Style Sheets)

## Visão Geral

A alteração da aparência de uma página web envolve o uso de uma linguagem de estilização conhecida como CSS (Cascading Style Sheets). O CSS permite a modificação visual dos elementos presentes na página.

- `HTML`: Utilizado para estruturar a página web.
- `CSS`: Empregado para estilizar a página web.

### Exemplo de Uso:

```html
p {
    font-size: 16px;
    font-weight: bold;
    color: black;
}
```

## Sintaxe do CSS

```html
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
