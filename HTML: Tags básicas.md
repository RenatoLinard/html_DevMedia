# Introdução

### Nesse arquivo vamos aprender a usar as tags básicas do html:

  - ```<title></title>``` - Exibe o título de uma página web
    
  - ```<h1></h1> ... <h6></h6>``` - criar títulos
    
  - ```<p></p>``` - criar parágrafos
    
  - ```<a></a>``` - criar um link
    
  - ```<img>``` - exibir uma imagem
    
  - ```<div></div>``` - agrupar elementos

## Conceitos

- Tag ```<title></title>```:
  
  - Permite que o usuário identifique o tipo de conteúdo que ele pode esperar dentro daquela página e tem sua importância para os mecanismos de busca, como o Google. Portando precisa ser relevante e relacionado ao conteúdo da pagina.
  
  - Deve ser utilizada dentro da tag ```<head>```.
    
  - Caso a tag title não seja definida no arquivo html, o título que aparecerá na aba da página será o nome do arquivo.
    
  - Exemplo de uso:
    ```html
    <head>
      <title>Tags básicas do HTML - Tag Title</title>
    </head>
    ```

- Tag ```<h1...h6></<h1...h6>```:
  - Os títulos ou cabeçalhos são utilizados para identificar os assuntos de uma página

  - Hierarquia:
      - Os títulos possuem uma hierarquia, o h1 é o mais importante enquanto o h6 o menos importante.

  - Deve ser utilizada entre as tags de abertura e fechamento ```<body> ... </body>```.

  - Exemplo de uso:
    ```html
    <body>
      <h1> Título nivel 1 </h1>
        <h2> Título nivel 2 </h2>
          <h3> Título nivel 3 </h3>
          ...
            <h6> Título nivel 6 </h6>
    </body>
    ```

- Tag ```<p></p>```:
  - Parágrafo é utilizado para separar ou agrupar conteúdos que estão relacionados
    
  - Assim como ```<h1>``` a tag ```<p>``` deve ser utilizado entre as tags de abertura e fechamento ```<body> ... </body>```
    
  - Lembrando que dentro da tag ```<p>``` podemos usar tags para tornar o parágrafo mais interativo
    
  - Exemplo de uso:
    ```html
    <body>
      <p>
        Isso é um parágrafo
      </p>
    </body>
    ```

- Tag ```<a></a>```:
  - Serve para criar uma ligação entre uma pagina e outra quando é clicado sobre o link
 
  - A tag ```<a>``` possui algumas propriedades que estão relacionados ao link:
    - href:
      - A url para onde a página será redirecionada ```<a href="https://github.com/RenatoLinard"> Github </a>```
        
      - Um número de telefone ```<a href="tel:+5567998811748"> +55 67 998811748 </a>```
        
      - Um endereço de email ```<a href="mailto: renatolinardjr@gmail.com"> Enviar email </a>```

    - target: Por padrão ao clicar em um link a nova pagina será aberta na mesma aba substituindo a página atual. Essa propriedade nos permite alterar esse comportamento:
      - _self: Abre a URL na mesma aba do navegador
        ```<a href="https://github.com/RenatoLinard" target="_self"> Github </a>```
        
      - _blank: Abre a URL em uma nova aba do navegador
        ```<a href="https://github.com/RenatoLinard" target="_blank"> Github </a>```
 
  - Exemplo de uso:
    ```html
      <a href="https://github.com/RenatoLinard">
        Github
      </a>
    ```

- Tag ```<img>```:
  - Serve basicamente para exibir uma imagem na página
    
  - Sua estrutura de elemento é composta por uma tag única
    
  - Propriedades:
    -src: Caminho da imagem que será exibido
      ```<img src="desktop.jpg" >``` - Imagem no mesmo diretório do projeto
      ```<img src="https://github.com/RenatoLinard/wallpaper/blob/main/screen_bash.png" >``` - Imagem de uma URL externa
    
 















    
