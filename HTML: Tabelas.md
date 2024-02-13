# Introdução

Ao organizar elementos em linhas e colunas na página **HTML**, a opção mais 
eficiente é o uso de **tabelas**.

## O que são?

Tabelas são elementos frequentemente utilizados para exibir dados de forma 
organizada em linhas e colunas.

## Estrutura básica de uma tabela 

```html
<table>
    <tr>
        <td>Jogo</td>
        <td>Ano</td>
    </tr>
    <tr>
        <td>Quantum Break</td>
        <td>2016</td>
    </tr>
    <tr>
        <td>Gear 5</td>
        <td>2019</td>
    </tr>
</table>
```

- `<table>...</table>` - Tag que define o início e o fim de uma tabela.
- `<tr>...</tr>` - Tag que cria uma linha na tabela.
- `<td>...</td>` - Tag que cria uma coluna na tabela.

## Porque são úteis

Além de exibir os dados organizados na tela, o uso das tabelas organiza nossos
dados semanticamente.

Isso faz com que os navegadores, buscadores e leitores de tela interpretem o 
conteudo da página adequadamente.

Os leitores de telas respeitam ordens das linhas e colunas estabelicidos. Por isso, 
é importante saber construir uma tabela corretamente.

## Quando não devemos usar?

Como mencionado anteriormente, as tabelas são úteis para organizar dados. 
No entanto, há casos em que seu uso não é indicado.

Um exemplo disso é quando os dados consistem em apenas uma coluna, sendo 
mais apropriado organizá-los em formato de listas.

## Estilizando tabelas 

As tabelas podem ser estilizadas por meio do **CSS**, assim como outros 
elementos **HTML**, proporcionando uma apresentação mais atraente na página.

# Table, tr, td, th 

Para criar uma tabela em HTML, são necessárias pelo menos 4 tags.

- `<table>` - Cria a tabela 
- `<tr>` - Cria uma linha na tabela 
- `<th>` - Cria uma coluna de cabeçalho 
- `<td>` - Cria uma coluna de conteúdo

```html
<table>
    <tr>
        <th>Música</th>
        <th>Artista</th>
    </tr>

    <tr>
        <td>First Date</td>
        <td>Blink-182</td>
    </tr>
    <tr>
        <td>Famous last words</td>
        <td>My Chemical Romance</td>
    </tr>
</table>
```

As tags **<th>** e **<td>** não diferem apenas visualmente, mas também em 
termos de semântica, indicando conteúdo de cabeçalho e conteúdo, respectivamente.

# THEAD, TBODY, TFOOT

Nesta seção, abordaremos como dividir nossa tabela em diferentes partes, como 
o **thead**, **tbody**, **tfoot**.

Ao criar uma tabela em **HTML**, é possível definir cada área da tabela usando 
uma tag específica.

- `<thead>` - Delimita o conteúdo do cabeçalho 
- `<tbody>` - Delimita o corpo da tabela 
- `<tfoot>` - Delimita o conteúdo de rodapé 

Para uma melhor organização, é importante que a estrutura da tabela siga 
sempre a ordem: **thead**, **tbody**, **tfoot**.

As tags são renderizadas nas suas respectivas posições, independentemente 
da ordem em que são escritas. No entanto, para uma melhor organização semântica 
e facilidade de leitura do código, é recomendável escrevê-las sempre nessa ordem.

```html
<table>
    <thead>
        <tr>
            <th>Música</th>
            <th>Artista</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>First Date</td>
            <td>Blink-182</td>
        </tr>
        <tr>
            <td>American Idiot</td>
            <td>Green Day</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td>Rock</td>
            <td>Estados Unidos</td>
        </tr>
    </tfoot>
</table>
```
