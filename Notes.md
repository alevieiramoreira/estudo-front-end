# Front-end Roadmap

A trilha de estudos documentados a seguir serão baseados na [roadmap front-end](https://roadmap.sh/frontend).  

Todas as anotações presentes neste documento são resultados do meu *próprio entendimento* sobre o conteúdo estudado, para facilidade de absorção e anotações para futuras consultas. 

 Todos os conteúdos acessados e utilizados neste estudo, estarão referênciados ao final deste documento.  

<!-- vscode-markdown-toc -->
* 1. [HTML](#HTML)
		* 1.1. [Learn the basics](#Learnthebasics)
		* 1.2. [Semantic HTML](#SemanticHTML)
* 2. [Referências](#Referncias)

<!-- vscode-markdown-toc-config
	numbering=true
	autoSave=true
	/vscode-markdown-toc-config -->
<!-- /vscode-markdown-toc -->

##  1. <a name='HTML'></a>HTML

####  1.1. <a name='Learnthebasics'></a>Learn the basics

Resumidamente, HTML (Hypertext Markup Language) é uma linguagem de marcação utilizada para o desenvolvimento de páginas web, mais precisamente para construir o *corpo* da página.

 Por ser uma linguagem de marcação, devem ser marcados elementos para marcar quais infos são exibidas na página, utilizando as *Tags e Elementos*.

##### Tags e Elementos

Procurando material de estudos na internet, encontra-se uma grande utilização dos termos *tags* e *elementos*. Em alguns lugares são tratados praticamente como se fossem iguais mas existe diferença:

**Tags:** Trata-se do conjunto de caracteres que darão forma a um elemento.

**Elementos:** Formados a partir de tags, que semanticamente se trata do conteúdo esperado dentro das tags.

A maioria das tags, por sua vez, precisam ser declaradas com um início e um fim, onde é necessário começar com os caracteres <> e fechar com os caracteres </>. 

> *As Tags servem para marcar onde começam e terminam os Elementos. Já os Elementos são uma parte conceitual/semântica que têm um começo e fim determinados.*

Seguem exemplos de algumas tags utilizadas para a construção de uma página HTML:

```html
<!-- Define um documento HTML -->
<html> </html>
 ```

 ```html
 <!-- Define infos sobre o documento -->
<head> </head>
 ```
```html
<!-- Define o título do documento -->
<title> </title>
 ```
```html
<!-- Define o elemento do corpo do documento -->
<body> </body>
 ```

```html
<!-- Define uma seção no documento -->
<div> </div>
 ```

```html
<!-- Define um parágrafo -->
<p> </p>
 ```

 ```html
 <!-- Heading tag para destacar títulos. Vai de h1 até h6. -->
<h1> </h1>
 ```  

* [Lista de tags HTML 5](http://testking.com/techking/wp-content/uploads/2011/02/IG-HTML5-Cheatsheet-1000px.png)

Todo o conteúdo necessário deve ficar entre a abertura e fechamento da tag, por exemplo a tag `<b>`, que deixa o texto em negrito: 

```html
 I love <b> flamingos </b>
 ```

 Apenas a palavra "flamingos" estará em negrito, já que é o único texto presente dentro da tag `<b></b>`, trazendo um resultado semelhante como:

 > I love **flamingos**

Importante ressaltar que nem todas as tags necessitam de fechamento, como a `<br>` por exemplo, utilizada para a quebra de linha. 

 ##### Nesting (Aninhar)
Os elementos, por sua vez, podem ser "inseridos dentro" de outros elementos, criando assim uma relação de pai-filho entre os elementos/tags, o que comumente é chamado de *nesting*.  

Por exemplo:

```html
<h2><b>Greater</b> <i>Flamingo</i></h2> 
```
Percebe-se que a tag `<b>` está abre e fecha dentro da tag `<h2>`, tornando assim, a `<h2>` pai da `<b>`, resultando:

> ## **Greater** *Flamingo*

Todo o conteúdo de texto está inserido dentro do `<h2>`, enquanto apenas a palavra "Greater" faz parte do elemento negrito e apenas "Flamingo" faz parte do elemento itálico, e tanto o itálico quanto o negrito estão dentro do `<h2>`.


Outro exemplo de nesting em uma estrutura html:

![nesting-img](https://i1.wp.com/qatechhub.com/wp-content/uploads/2016/09/BasicHtmlStructure.png?resize=540%2C360 "Exemplo nesting")


##### Atributos

São comandos que atribuem características para as tags HTML. Existem atributos globais - que funcionam para todas as tags - e atributos específicos para determinadas tags. Todo atributo possui um nome e um valor.

Exemplo utilzando o atributo global `style`, com o valor `text-align:center;`:

```html
    <h1 style="text-align:center;"> texto </h1>
```    

Exemplo de atributo privado `src` que se aplica apenas para elementos que utilizem uma URL incorporável, como por exemplo `<img>`, `<script>`, `<video>` entre outros: 

```html
    <img src="flamingo.png"/>
```  

*   [Lista de atributos (globais e não globais)](https://developer.mozilla.org/pt-BR/docs/HTML/Attributes)

- Por boas práticas, sempre atribuir o valor do atributo entre aspas duplas.

####  1.2. <a name='SemanticHTML'></a>Semantic HTML

________________

### 2. <a name='Referncias'></a>Referências 

[Tableless - O que são Tags, elementos e atributos](https://tableless.github.io/iniciantes/manual/html/oquetags.html)

[Qatechclub - HTML Page structure and nesting](https://qatechhub.com/html-page-structure-nesting/)

[Mozilla org - HTML Attributes](https://developer.mozilla.org/pt-BR/docs/HTML/Attributes)

[Udemy - Curso Aprenda HTML](https://www.udemy.com/aprendahtml/)

[Cheatsheet - HTML 5](http://testking.com/techking/wp-content/uploads/2011/02/IG-HTML5-Cheatsheet-1000px.png)