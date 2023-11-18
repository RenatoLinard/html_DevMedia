# HTML: Linguagem de Marcação para Estruturação de Páginas Web

O HTML (Hypertext Markup Language) é uma linguagem de marcação amplamente utilizada para estruturar páginas web. O conteúdo destinado à exibição no navegador é delimitado por tags, indicando ao navegador a função de cada componente. Elementos, representados pelo texto entre os sinais `<` e `>`, geralmente consistem em tags de abertura e fechamento, como `<p></p>`. O que é renderizado pelo navegador é o conteúdo entre essas tags.

## Uma Linguagem de Tags e Atributos
- Tags descrevem a função de cada elemento para o navegador.
- Atributos são compostos por pares de chave e valor, sendo que os valores são sempre inseridos entre aspas duplas.

## Criação de um Arquivo HTML
- Um arquivo HTML deve ter a extensão .html.
- Quando interpretado corretamente pelo navegador, resulta em uma página web interativa para o usuário.

## Estrutura HTML Essencial

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <h1></h1>
    <p></p>
  </body>
</html>
```

### `<!DOCTYPE>`
- Instrução que especifica a versão do HTML a ser renderizada; por exemplo, `<!DOCTYPE html>` representa a versão 5.

### `<html></html>`
- Tag raiz que engloba toda a estrutura; todas as outras tags devem estar contidas entre `<html> </html>`, exceto o DOCTYPE.

### `<head></head>`
- Responsável por conter informações essenciais sobre o documento, como título, metadados, entre outros.

### `<meta charset="utf-8">`
- Indica ao navegador a codificação de caracteres utilizada no documento.

### `<title></title>`
- Localizado dentro da tag head, define o título da página exibido na aba do navegador.

### `<body></body>`
- Contém todo o conteúdo interativo disponibilizado para o usuário.

### `<p></p>`
- Representa um parágrafo de texto.


