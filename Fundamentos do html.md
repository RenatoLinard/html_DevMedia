## O que é HTML?

O HTML (Hypertext Markup Language) é uma linguagem de marcação utilizada para estruturar páginas web. Todo o conteúdo que desejamos que o navegador exiba para o usuário é contido entre tags, sinalizando para o navegador o que cada componente representa. O texto entre os sinais de `<` e `>` é chamado de elemento e, na maioria das vezes, é composto por tags de abertura e fechamento, como por exemplo `<p></p>`. O que será exibido pelo navegador é o conteúdo entre as tags de abertura e fechamento.

## Uma linguagem de tags e atributos
- As tags descrevem para o navegador o que cada elemento representa.
- Os atributos são compostos por um par de chaves e valores, e os valores são sempre escritos entre aspas duplas.

## Criando um arquivo html
- A criação de um arquivo é html precisa da extensao .html
- Quando lido corretamente pelo navegador dá origem a uma pagina web, com o qual o usuario pode interagir

# Por dentro da estrutura HTML

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
### ```<DOCTYPE>```
  - Tratra-se da instrução de qual versão do html que será renderizado, no caso ```<!DOCTYPE html>``` representa a versão 5

### html
  - É a tag raiz de toda estrutura, todas as tags precisam está contidas dentro de ```<html> </html>``` com excessão o DOCTYPE

### head
- Tag responsável por receber informações importantes referente ao documento, tais como título, metadados, entre outras.

### meta 
  - Informa o navegador qual codificação de caracteres utilizamos quando o documento foi escrito

### title
  - Fica contido da tag head e informa o título da pagina localizada na aba superior do navegador

### bod



