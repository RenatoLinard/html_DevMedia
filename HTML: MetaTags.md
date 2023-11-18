## Introdução

Ao iniciar a criação de um arquivo HTML, uma das primeiras etapas consiste em estabelecer o conteúdo do cabeçalho, incluindo títulos e meta tags.

### Nesta seção, abordaremos as seguintes tags:

- `title`
- `meta` (description, charset, viewport, robots)
- `link`
- `style`

### Tags de cabeçalho

- As tags de cabeçalho são localizadas na seção de cabeçalho da página.
- Todo o conteúdo está contido entre as tags `<head></head>`.
- Um exemplo de tag de cabeçalho é a `<title>`, que é usada para definir o título de uma página.
- Outro exemplo é a tag `<link>`, que permite adicionar um arquivo CSS externo à página.
  
Exemplo:

```html
<head>
    <title>Título do Documento</title>
    <link rel="stylesheet" type="text/css" href="style.css"/>
</head>
```

### ```<title>```

- Utilizada para definir o título de uma página exibida no topo do navegador (aba)
- Seu uso é obrigatório para que o documento seja validado
```html
<head>
    <title> Título da Página </title>
</head>
```

### ```<meta name="description">```

- Utilizada para definir a descrição de uma página
- Apesar de não ser visível para o usuário será útil para buscadores e outros serviços web
- Exemplo de uso:
- O texto localizado dentro do atributo content é a descrição da página, que será lida pelos buscadores 
```html
<head>
    <meta name="description" content="Esse é uma resumo pessoal seguindo o cronograma do curso de html da plataforma devmedia">
</head>
```

### ```<meta charset="">```

- É utilizada para informar ao navegador o conjunto de caracteres utilizados na página
- Esse conjunto de caracter é o responsável por exibir acentos e caracteres especiais
- A especificação do html 5 recomenda o uso de conjunto de caracteres utf-8, por ser completo e possuir símbolos do mundo todo
- Exemplo de uso:
```html
<head>
    <meta charset="utf-8">
</head>
```

### ```<meta name="robots" content="noindex">```

- Utilizada para quando queremos que a página não apareça nos resultados de buscas
- È útil para páginas de relátorios, sistemas administrativos e páginas com dados pessoais
- Exemplo de uso:
```html
<meta name="robots" content="noindex">
``` 
 


















