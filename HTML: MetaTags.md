# Criação de Arquivo HTML: Tags de Cabeçalho e Seções

## Introdução

Ao iniciar a criação de um arquivo HTML, uma das primeiras etapas é estabelecer o conteúdo do cabeçalho, incluindo títulos e meta tags.

### Tags de Cabeçalho

As tags de cabeçalho estão localizadas na seção de cabeçalho da página, contendo todo o seu conteúdo entre as tags `<head></head>`. Um exemplo de tag de cabeçalho é a `<title>`, usada para definir o título de uma página. Outro exemplo é a tag `<link>`, que permite adicionar um arquivo CSS externo à página.

Exemplo:

```html
<head>
    <title>Título do Documento</title>
    <link rel="stylesheet" type="text/css" href="style.css"/>
</head>
```

### Tags Abordadas

Na sequência, abordaremos as seguintes tags de cabeçalho:

- `title`
- `meta` (description, charset, viewport, robots)
- `link`
- `style`

### Tag `<title>`

A tag `<title>` é usada para definir o título de uma página exibida no topo do navegador (aba). Seu uso é obrigatório para validar o documento.

```html
<head>
    <title> Título da Página </title>
</head>
```

### Tag `<meta name="description">`

A `<meta name="description">` é utilizada para definir a descrição de uma página, sendo útil para buscadores e outros serviços web.

```html
<head>
    <meta name="description" content="Esse é um resumo pessoal seguindo o cronograma do curso de HTML da plataforma DevMedia">
</head>
```

### Tag `<meta charset="">`

A `<meta charset="">` informa ao navegador o conjunto de caracteres utilizados na página. O conjunto de caracteres utf-8 é recomendado pela especificação do HTML 5 por ser completo e possuir símbolos do mundo todo.

```html
<head>
    <meta charset="utf-8">
</head>
```

### Tags `<meta name="robots">`

#### `<meta name="robots" content="noindex">`

Utilizada quando não desejamos que a página apareça nos resultados de buscas, sendo útil para páginas de relatórios, sistemas administrativos e páginas com dados pessoais.

Exemplo de uso:

```html
<meta name="robots" content="noindex">
```

#### `<meta name="robots" content="nofollow">`

Além do `noindex`, existe outro tipo de uso para a tag `robots`, o `nofollow`. Os buscadores acessam o conteúdo de páginas em busca de informação. Sem a meta tag `nofollow`, o buscador vai navegar pelos links internos e associá-los à nossa página. Se não desejamos associar links externos, como os provenientes de uma página de comentários, podemos adicionar a meta tag para evitar a vinculação desses links externos à nossa página.

Exemplo de uso:

```html
<meta name="robots" content="nofollow">
```

#### `<meta name="robots" content="noindex, nofollow">`

Em resumo, ao utilizar a tag `noindex`, instruímos o mecanismo de busca a não exibir nossa página nos resultados de pesquisa. Isso não impede a associação de links. Ao empregar a tag `nofollow`, indicamos ao mecanismo de busca que não associe os links à nossa página. Se desejarmos utilizar ambos simultaneamente, basta separar os dois com uma vírgula. Isso é útil para post de fórum.

Exemplo de uso:

```html
<meta name="robots" content="noindex, nofollow">
```

### Tag `<meta name="viewport">`

A tag `<meta name="viewport">` serve para ajustar o conteúdo de uma página independentemente do tamanho do dispositivo utilizado pelo usuário.

Exemplo de uso:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Entendendo a meta tag:
- `<content="width=device-width">` - Ajusta a largura do conteúdo para a mesma largura da tela do dispositivo.
- `<content="initial-scale=1.0">` - Define o zoom inicial da página (1.0 - sem zoom).

### Adicionando Estilos CSS Externos

Primeiramente, é importante compreender o que é o CSS.

- CSS é uma linguagem que possibilita a estilização de elementos em uma página HTML.
- Podemos modificar a cor do texto, cor de fundo, tamanho da fonte e muitos outros aspectos utilizando CSS.

### HTML e CSS

A integração dos estilos CSS com o HTML é realizada de três maneiras: externa, interna e inline. Neste contexto, aprenderemos a realizar a integração de forma externa, utilizando a tag `<link>`.

### Tag `<link rel="stylesheet">`

A tag `<link>` quando utilizada junto do atributo `rel="stylesheet"` serve para adicionar um arquivo CSS a uma página HTML.

Exemplo de uso:

```html
<link rel="stylesheet" href="style.css">
```

Entendendo a tag:
- `<rel="stylesheet">` - Informa que estamos carregando um arquivo de estilos.
- `<href="style.css">` - Determina o caminho do arquivo a ser carregado.

Além das propriedades `rel` e `href`, temos a propriedade opcional `type` que indica o tipo de arquivo a ser importado.

```html
<link rel="stylesheet" href="style.css" type="text/css">
```

Quando não inserimos o `type`, o navegador vai identificar o tipo através da propriedade `rel`.

### Tag `<style>`

Através dessa tag, adicionamos o estilo CSS diretamente na página HTML.

Exemplo de uso:

```html
<style>
    h1 {
        color:#02af3b;
    }
    h3 {
        color: #ff7300;
    }
    div {
        background: #6694eb;
    }
</style>
```