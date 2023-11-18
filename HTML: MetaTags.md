# Criação de Arquivo HTML: Tags de Cabeçalho e Seções

## Introdução

Ao iniciar a criação de um arquivo HTML, uma das primeiras etapas é estabelecer o conteúdo do cabeçalho, incluindo títulos e meta tags.

### Nesta seção, abordaremos as seguintes tags:

- `title`
- `meta` (description, charset, viewport, robots)
- `link`
- `style`

### Tags de Cabeçalho

- As tags de cabeçalho estão localizadas na seção de cabeçalho da página.
- Todo o conteúdo está contido entre as tags `<head></head>`.
- Um exemplo de tag de cabeçalho é a `<title>`, usada para definir o título de uma página.
- Outro exemplo é a tag `<link>`, que permite adicionar um arquivo CSS externo à página.
  
Exemplo:

```html
<head>
    <title>Título do Documento</title>
    <link rel="stylesheet" type="text/css" href="style.css"/>
</head>
```

### Tag `<title>`

- Usada para definir o título de uma página exibida no topo do navegador (aba).
- Seu uso é obrigatório para validar o documento.

```html
<head>
    <title> Título da Página </title>
</head>
```

### Tag `<meta name="description">`

- Utilizada para definir a descrição de uma página.
- Apesar de não ser visível para o usuário, é útil para buscadores e outros serviços web.
- Exemplo de uso:

```html
<head>
    <meta name="description" content="Esse é um resumo pessoal seguindo o cronograma do curso de HTML da plataforma DevMedia">
</head>
```

### Tag `<meta charset="">`

- Informa ao navegador o conjunto de caracteres utilizados na página.
- O conjunto de caracteres utf-8 é recomendado pela especificação do HTML 5 por ser completo e possuir símbolos do mundo todo.
- Exemplo de uso:

```html
<head>
    <meta charset="utf-8">
</head>
```

### Tag `<meta name="robots" content="noindex">`

- Utilizada quando não desejamos que a página apareça nos resultados de buscas.
- Útil para páginas de relatórios, sistemas administrativos e páginas com dados pessoais.
- Exemplo de uso:

```html
<meta name="robots" content="noindex">
```

### Tag `<meta name="robots" content="nofollow">`

- Além do noindex existe outro tipo de uso para a tag robots, o nofollow
- Os bucadores acessam o conteúdo de páginas em busca de informação
- Sem a meta tag nofollow , o buscador vai navegar pelos links internos e associá-los a nossa página
- Se não desejamos associar links externos, como os provenientes de uma página de comentários, podemos adicionar a meta tag para evitar a vinculação desses links externos à nossa página.
- Exemplo de uso:

```html
<meta name="robots" content="nofollow">
```

### Tag noindex e nofollow

- Em resumo, ao utilizar a tag noindex, instruímos o mecanismo de busca a não exibir nossa página nos resultados de pesquisa. No entanto, isso não impede a associação de links. Por outro lado, ao empregar a tag nofollow, indicamos ao mecanismo de busca que não associe os links à nossa página.
- E se desejarmos utilizar ambos simultaneamente? A resposta é simples: basta separar os dois com uma vírgula.
- Isso é útil para post de fórum
- Exemplo de uso:

```html
<meta name="robots" content="noindex, nofollow">
```

### Tag `<meta name="viewport">`

- Serve para ajustar o conteudo de uma página independente do tamanho do disposito utilizado pelo usuario
- Exemplo de uso:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

- Entendo a meta tag:
    - `<content="width=device-width">` - Ajusta a largura do conteúdo para a mesma largura da tela do dispositivo 
    - `<content="initial-scale=1.0">` - Defini o zoom inicial da página (1.0 - sem zoom) 

### Tag `<link rel="stylesheet" href="style.css">`
















