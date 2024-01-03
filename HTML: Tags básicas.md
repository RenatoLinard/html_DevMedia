# HTML: Utilização de Tags Básicas e Conceitos

## Introdução

Neste documento, exploraremos o uso das tags básicas do HTML, essenciais para estruturar páginas web.

- `<title></title>`: Exibe o título de uma página web.
    
- `<h1></h1> ... <h6></h6>`: Cria títulos.
    
- `<p></p>`: Cria parágrafos.
    
- `<a></a>`: Cria um link.
    
- `<img>`: Exibe uma imagem.
    
- `<div></div>`: Agrupa elementos.

## Conceitos

### Tag `<title>`

- Permite que o usuário identifique o tipo de conteúdo que pode esperar na página, sendo crucial para mecanismos de busca como o Google.

- Deve ser usada dentro da tag `<head>`.

- Se não for definida, o título na aba da página será o nome do arquivo.

- Exemplo:
    ```html
    <head>
      <title>Tags básicas do HTML - Tag Title</title>
    </head>
    ```

### Tag `<h1...h6>`

- Títulos ou cabeçalhos identificam os assuntos de uma página.

- Possuem uma hierarquia, sendo h1 o mais importante e h6 o menos.

- Deve ser utilizada entre as tags de abertura e fechamento `<body> ... </body>`.

- Exemplo:
    ```html
    <body>
      <h1> Título nível 1 </h1>
        <h2> Título nível 2 </h2>
          <h3> Título nível 3 </h3>
          ...
            <h6> Título nível 6 </h6>
    </body>
    ```

### Tag `<p>`

- Parágrafo é utilizado para separar ou agrupar conteúdos relacionados.

- Deve ser usada entre as tags de abertura e fechamento `<body> ... </body>`.

- Dentro da tag `<p>`, podemos usar outras tags para tornar o parágrafo mais interativo.

- Exemplo:
    ```html
    <body>
      <p>
        Isso é um parágrafo.
      </p>
    </body>
    ```

### Tag `<a>`

- Cria uma ligação entre páginas quando clicado sobre o link.

- Para criação de um link basta utilizar a tag de abertura, o conteúdo e a tag
de fechameto.

```html
<a>conteúdo</a>
```

O conteúdo dentro das tags será exibido para o usuário.

##### Propriedades

A tag `a` possui algumas propriedades que estão relacionadas ao link.

- `href`- Propriedade que irá redirecionar para o conteúdo desejado.

- A url para onde a página será redirecionada.

```html
<a href="https://github.com/RenatoLinard">Renato Linard</a>
```

- Um número de telefone.

```html
<a href="tel:+5567998811748"> (67) 998811748 </a>
```

- Um endereço de email

```html
<a href="mailto:renatolinardjr@gmail.com">Enviar emal</a>
```

- `target`- Por padrão quado clidado em um link a página é aberta na mesma 
aba, com essa propriedade podemos alterar esse comportamento.

`_self`- Abre a url na mesma página.

`_blank`- Abre a url em uma nova aba.



### Tag `<img>`

- Exibe uma imagem na página.

- Propriedades: `src` (caminho da imagem) e `alt` (texto que descreve a imagem).

- Exemplo:
    ```html
    <img src="desktop.jpg" alt="Computador desktop completo">
    ```

### Tag `<div>`

- Agrupa elementos na página, sem aparência visual própria.

- Utilizada para organizar o código.

- Exemplo:
    ```html
    <div>
      <img src="computador.jpg" alt="Notebook Lenovo Ideapad S145"
        title="Notebook Lenovo">
      <a href="pagina2.html">
        Abrir descrição do produto
      </a>
    </div>
    ```

### Tag `<span>`

- Marca palavras que merecem destaque.

- Não possui aparência visual própria, mas pode receber estilos via CSS.

- Exemplo:
    ```html
    <div>
      <h3>
        <span>Notebook Lenovo Ideapad</span> S145 8ª Intel Core I5 8GB 1TB HD 15,6" W10 Prata
      </h3>

      <p>
        Com o Notebook da Lenovo, você terá um notebook de <span>última geração</span>,
        prático e <span>veloz</span>, com excelente capacidade de <span>armazenamento</span>,
        design inovador e exclusivo.
      </p>
    </div>
    ```

### Tag `<iframe>`

- Incorpora o conteúdo de uma página externa em nosso site.

- Útil para trazer informações externas sem que o usuário saia do site.

- Propriedades: `src` (URL da página externa), `width` e `height` (largura e altura do iframe).

- Exemplo:
    ```html
    <div>
      <h3>Previsão do tempo</h3>

      <p>Veja como está o clima hoje.</p>

      <iframe
        src="https://www.accuweather.com/"
        width="600" height="450"
      >
      </iframe>
    </div>
    ```

### Tag `<!-- -->`

- Cria comentários dentro do código fonte, não visíveis na página web.

- Essenciais para documentar e explicar o código fonte.

- Exemplo:
    ```html
      <!-- Isso é um comentário -->
    ```
