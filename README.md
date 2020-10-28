# Curso HTML + CSS

Curso dedicado a duas linguagens fundamentais do desenvolvimento web: HTML e CSS.

Ferramentas necessárias:
- [Chrome](https://www.google.pt/intl/pt-PT/chrome/)
- [Visual Studio Code](https://code.visualstudio.com/)

## Conteúdos
- [Introdução ao HTML](#introducao-ao-html)
- [Sintaxe do HTML](#sintaxe-do-html)

## Introdução ao HTML

HTML (Hyper Text Markup Language) é uma linguagem de hipertexto e de marcação que descreve a estrutura de uma página web. 

- Por ser uma linguagem de hipertexto aceita links que permitem o acesso directo a outras páginas.
- Por ser uma linguagem de marcação aceita `<tags>` que permitem que os browsers consigam ler de forma correcta a estrutura de um documento.

O HTML é a linguagem base do desenvolvimento web, sendo que todas as outras como o CSS, Javascript ou PHP gravitam à sua volta.

O HTML não é considerado uma linguagem de programação pois não é capaz de instruir o computador para performar operações.

Um ficheiro HTML é identificado pela extensão `.html`.

## Sintaxe do HTML

### Tags

Um documento HTML é estruturado por tags, que são os elementos que indicam como a página deve ser renderizada pelo browser. 
As tags encontram-se dentro de um sinal de menor (<) e de maior (>) e, na sua maioria, têm uma marcação de início e outra de fim. Em alguns casos, apenas tem uma marcação que assinala o ínicio e o fim.

É a partir das tags que os browsers conseguem renderizar ou interpretar as páginas de forma correcta.

````
<nomeTag>Conteúdo</nomeTag>
<nomeTag />
````
Referências de todas as tags:
https://www.w3schools.com/TAGS/default.ASP

### Atributos

Algumas tags aceitam atributos que permitem adicionar propriedades.

````
<nomeTag atributo=”valor”>Conteúdo</nomeTag>
````

### Árvore de elementos

Uma página HTML é uma estrutura que se organiza em árvore sendo que as tags podem ter pais e filhos.

````
<tagPai>
    <tagFilho>
    </tagFilho>
</tagPai>
````

## Estrutura de um documento

Um documento HTML começa com o que chamamos de estrutura base. Esta estrutura é compostas por:
- Definição do documento (Doctype)
- Head 
- Body

````
<!DOCTYPE html><!-- definição do documento -->
 
<html>
   <head>
       <!-- No head (cabeça) estão as informações que não são para ser vistas pelo utilizador -->
   </head>
 
   <body>
       <!-- No body (corpo) estão as informações que são para ser vistas pelo utilizador -->
   </body>
</html>
````

### Definição do documento (Doctype)
Este elemento serve para informar o browser de que se trata de um documento com código HTML. É um elemento obrigatório e deve sempre estar na primeira linha. No passado era um código longo mas na versão 5 do HTML foi simplificado para `<!DOCTYPE html>`

### Head
No `<head>` estão as informações que não são para ser vistas pelo utilizador. Nele estão os metadados, links para outros arquivos e scripts. 

### Body
No `<body>`  encontram-se as informações para serem lidas pelo utilizador, que pode ser em formato de texto, imagem, vídeo, áudio ou códigos embutidos.


## Primeira página

````
<!DOCTYPE html>
 
<html>
   <head>
       <title>A  minha primeira página</title> <!-- título do documento -->
       <meta charset="utf-8"> <!-- codificação da língua -->
   </head>
 
   <body>
       Olá mundo!
   </body>
</html>
````

## Tags essenciais

### Títulos e subtítulos

Os títulos e subtítulos são identificados pelas tags `<h1>` até à `<h6>`. `<h1>` o mais importante e `<h6>` menos importante.

````
<h1>Título 1</h1>
<h2>Título 2</h2>
<h3>Título 3</h3>
<h4>Título 4</h4>
<h5>Título 5</h5>
<h6>Título 6</h6>
````

### Parágrafos
Os parágrafos são identificados pela tag `<p>`.

````
<p>Isto é um parágrafo.</p>
```` 

### Lista não ordenada
Uma lista não ordenada é identificada pela tag `<ul>` e cada item pela tag `<li>`. 
Numa lista não ordenada cada item é antecedido por um símbolo bullet.

````
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ul>
````

### Lista ordenada
Uma lista ordenada é identificada pela tag `<ol>` e cada item pela tag `<li>`. 
Numa lista ordenada cada item é numerado por ordem.

````
<ol>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ol>
````

### Blocos
Os blocos são elementos que começam sempre numa nova linha e ocupam toda a largura possível.

````
<header>Header</header>
<div>Block</div>
<footer>Footer</footer>
````

### Links
O links são criados utilizando a tag `<a>` que recebe o atributo `href=''` que contém o URL.

````
<a href='<!-- URL -->'>Texto que aparece</a>
````

### Imagens
As imagens são definidas pela tag `<img>` que recebe o atributo `src=''` que contém o URL da imagem ou o caminho relativo, caso a imagem esteja no nosso servidor.

````
<img width='500' src='<!-- URL da Imagem -->'>
<img width='500' src='<!-- caminho relativo -->'>
````

# CSS

## Introdução ao CSS
CSS (Cascading Style Sheets) é uma extensão do HTML que permite manipular os estilos de um documento ao dizer como elementos devem aparecer no browser.

Deste modo, o CSS define o design e permite que o website seja responsivo (que se adapte aos diferentes tamanhos de ecrã).

## Sintaxe do CSS
Uma regra em CSS é definida por um selector e por um bloco de declarações. Cada declaração é composta por uma propriedade e por um valor atribuído.

````
selector {
    propriedade1: valor1;
    propriedade2: valor2;
}
````

## Adicionar o CSS
Podemos adicionar o CSS de três formas diferentes:
- inline
- interno
- externo (preferencial)

### Inline
Directamente numa tag HTML através do atributo `style=""`.

Este método não é aconselhável pois, por uma questão de organização, devemos separar o código HTML do CSS.

````
<p style="color: blue">Texto azul</p>
````

### Interno
Através da tag `<style>` colocada no `<head>`, que permite que seja utilizada a sintaxe CSS dentro de um documento HTML.

````
<html>
  <head>
    <style>
      p {
        color: blue;
      }
    </style>
  </head>
  <body>
    <p>Texto azul</p>
  </body>
</html>
````

### Externo
Através de um ficheiro externo com a extensão `.css`, que permite separar o código CSS do documento HTML. 

O fichero CSS deve ser colocado na pasta do website e chamado pelo HTML através da tag `<link>` colocada no `<head>`. A tag `<link>` recebe o atributo `href=""`que recebe o caminho relativo do ficheiro CSS.

Exemplo se o ficheiro CSS (style.css) estiver na mesma pasta que o ficheiro HTML:

````
<head>
    <link rel="stylesheet" href="style.css">
<head>
````