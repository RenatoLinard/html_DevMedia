## Introdução

### Neste arquivo, aprenderemos a utilizar as tags básicas do HTML:

- ```<title></title>``` - Exibe o título de uma página web.
    
- ```<h1></h1> ... <h6></h6>``` - Cria títulos.
    
- ```<p></p>``` - Cria parágrafos.
    
- ```<a></a>``` - Cria um link.
    
- ```<img>``` - Exibe uma imagem.
    
- ```<div></div>``` - Agrupa elementos.

## Conceitos

### Tag ```<title>```

- Permite que o usuário identifique o tipo de conteúdo que pode esperar dentro daquela página e tem sua importância para os mecanismos de busca, como o Google. Portanto, precisa ser relevante e relacionado ao conteúdo da página.

- Deve ser utilizada dentro da tag ```<head>```.

- Caso a tag title não seja definida no arquivo HTML, o título que aparecerá na aba da página será o nome do arquivo.

- Exemplo de uso:
    ```html
    <head>
      <title>Tags básicas do HTML - Tag Title</title>
    </head>
    ```

### Tag ```<h1...h6>```

- Os títulos ou cabeçalhos são utilizados para identificar os assuntos de uma página.

- Hierarquia:
    - Os títulos possuem uma hierarquia, sendo o h1 o mais importante, enquanto o h6 o menos importante.

- Deve ser utilizada entre as tags de abertura e fechamento ```<body> ... </body>```.

- Exemplo de uso:
    ```html
    <body>
      <h1> Título nível 1 </h1>
        <h2> Título nível 2 </h2>
          <h3> Título nível 3 </h3>
          ...
            <h6> Título nível 6 </h6>
    </body>
    ```

### Tag ```<p>```

- Parágrafo é utilizado para separar ou agrupar conteúdos relacionados.

- Assim como ```<h1>```, a tag ```<p>``` deve ser utilizada entre as tags de abertura e fechamento ```<body> ... </body>```.

- Lembrando que dentro da tag ```<p>``` podemos usar tags para tornar o parágrafo mais interativo.

- Exemplo de uso:
    ```html
    <body>
      <p>
        Isso é um parágrafo.
      </p>
    </body>
    ```

### Tag ```<a>```

- Serve para criar uma ligação entre uma página e outra quando é clicado sobre o link.

- A tag ```<a>``` possui algumas propriedades relacionadas ao link:
    - **href**:
      - A URL para onde a página será redirecionada: ```<a href="https://github.com/RenatoLinard"> GitHub </a>```.
        
      - Um número de telefone: ```<a href="tel:+5567998811748"> +55 67 998811748 </a>```.
        
      - Um endereço de e-mail: ```<a href="mailto:renatolinardjr@gmail.com"> Enviar e-mail </a>```.

    - **target**: Por padrão, ao clicar em um link, a nova página será aberta na mesma aba, substituindo a página atual. Esta propriedade permite alterar esse comportamento:
      - **_self**: Abre a URL na mesma aba do navegador.
        ```<a href="https://github.com/RenatoLinard" target="_self"> GitHub </a>```.
        
      - **_blank**: Abre a URL em uma nova aba do navegador.
        ```<a href="https://github.com/RenatoLinard" target="_blank"> GitHub </a>```.
 
- Exemplo de uso:
    ```html
    <a href="https://github.com/RenatoLinard">
      Github
    </a>
    ```

### Tag ```<img>```

- Serve basicamente para exibir uma imagem na página.

- Sua estrutura de elemento é composta por uma tag única.

- Propriedades:
    - **src**: Caminho da imagem que será exibido.    
      - ```<img src="desktop.jpg">``` - Imagem no mesmo diretório do projeto.
      - ```<img src="https://github.com/RenatoLinard/wallpaper/blob/main/screen_bash.png">``` - Imagem de uma URL externa.
     
    - **alt**: Texto que descreve a imagem.
      - ```<img src="desktop.jpg" alt="Computador desktop completo">``` - Caso ocorra um erro ao carregar a imagem, o valor do atributo alt será exibido para o usuário.

### Tag ```<div>```

- Usada para agrupar elementos na página.

- Não possui nenhuma aparência visual.

- Utilizamos a tag de abertura, os elementos a serem agrupados e a tag de fechamento.

- Realizamos o agrupamento para juntar informações relacionadas, deixando o código mais organizado.

- Exemplo de uso:
    ```html
    <div>
      <img src="computador.jpg" alt="Notebook Lenovo Ideapad S145"
        title="Notebook Lenovo">
      <a href="pagina2.html">
        Abrir descrição do produto
      </a>
    </div>
    ```

### Tag ```<span>```

- Utilizado para marcar palavras que mereçam algum tipo de destaque.

- Não possui nenhuma aparência visual, porém pode ser adicionado estilos através do CSS.

- Ao marcar palavras, podemos organizar nosso código.

- Exemplo de uso:
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

### Tag ```<iframe>```

- Serve para incorporar o conteúdo de uma página externa para dentro do nosso site.

- É útil para trazer informações de alguma página externa sem a necessidade do usuário sair do nosso site.

- A estrutura da tag é composta por tag de abertura e fechamento.

- Existem alguns sites que não permitem a utilização da URL para utilizar com a tag ```<iframe>```, impedindo o carregamento no nosso site.

- Out

ros sites possuem URL específica para utilização da tag, exemplo disso é o Google Maps.

- Propriedades:
    - **src**: É a URL da página externa.

    - **width e length**: Definem, respectivamente, a largura e a altura do iframe.
    
- Exemplo de uso:
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

### Tag ```<!-- -->```
- Tag Utilizada para criar comentários dentro do código fonte 

- Não aparece dentro da pagina web

- Comentários são essenciais para documentar e explicar o código fonte.

- Exemplo de uso:
    ```html
      <!-- Isso é um comentário -->
    ```
