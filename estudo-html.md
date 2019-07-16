# Front-end Roadmap

A trilha de estudos documentados a seguir serão baseados na [roadmap front-end](https://roadmap.sh/frontend).  

Todas as anotações presentes neste documento são resultados do meu *próprio entendimento* sobre o conteúdo estudado, para facilidade de absorção e anotações para futuras consultas. 

 Todos os conteúdos acessados e utilizados neste estudo, estarão referênciados ao final deste documento.  

<!-- vscode-markdown-toc -->
* 1. [HTML](#HTML)
	* 1.1. [Learn the basics](#Learnthebasics)
		* 1.1.1. [Tags e Elementos](#TagseElementos)
		* 1.1.2. [Caracteres Especiais](#CaracteresEspeciais)
		* 1.1.3. [Nesting (Aninhar)](#NestingAninhar)
		* 1.1.4. [Atributos](#Atributos)
	* 1.2. [Semantic HTML](#SemanticHTML)
		* 1.2.1. [Content Models](#ContentModels)
		* 1.2.2. [Ênfases](#nfases)
	* 1.3. [SEO](#SEO)
	* 1.4. [Referências](#Referncias)

<!-- vscode-markdown-toc-config
	numbering=true
	autoSave=true
	/vscode-markdown-toc-config -->
<!-- /vscode-markdown-toc -->

##  1. <a name='HTML'></a>HTML

###  1.1. <a name='Learnthebasics'></a>Learn the basics

Resumidamente, HTML (Hypertext Markup Language) é uma linguagem de marcação utilizada para o desenvolvimento de páginas web, mais precisamente para construir o *corpo* da página.

 Por ser uma linguagem de marcação, devem ser marcados elementos para marcar quais infos são exibidas na página, utilizando as *Tags e Elementos*.

####  1.1.1. <a name='TagseElementos'></a>Tags e Elementos

Procurando material de estudos na internet, encontra-se uma grande utilização dos termos *tags* e *elementos*. Em alguns lugares são tratados praticamente como se fossem iguais mas existe diferença:

**Tags:** Trata-se do conjunto de caracteres que darão forma a um elemento.

**Elementos:** Formados a partir de tags, que semanticamente se trata do conteúdo esperado dentro das tags.

A maioria das tags, por sua vez, precisam ser declaradas com um início e um fim, onde é necessário começar com os caracteres <> e fechar com os caracteres </>. 

> *As Tags servem para marcar onde começam e terminam os Elementos. Já os Elementos são uma parte conceitual/semântica que têm um começo e fim determinados.*

Seguem exemplos de algumas tags utilizadas para a construção de uma página HTML:

```html
<!-- Define que o documento é do tipo HTML -->
<!DOCTYPE html>
```

```html
<!-- Define um documento HTML -->
<html> </html>
```

```html
 <!-- Define o cabeçalho p/ infos sobre o documento -->
<head> </head>
```

```html
<!-- Geralmente utilizada para search engines, porém tem inúmeras funções p/ o documento. Mais detalhes no link abaixo. -->
<meta charset="UTF-8">
 ```
* [DevMedia- Guia sobre Meta Tags](https://www.devmedia.com.br/html-meta-tags-entendendo-o-uso-de-meta-tags/30328)

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

<!-- Por boas práticas, sempre utilizar a ordem hierárquica de 1 a 6 no documento, sem pular números -->
 ```  

* [Lista de tags HTML 5](http://testking.com/techking/wp-content/uploads/2011/02/IG-HTML5-Cheatsheet-1000px.png)

Todo o conteúdo necessário deve ficar entre a abertura e fechamento da tag, por exemplo a tag `<b>`, que deixa o texto em negrito: 

```html
 I love <b> flamingos </b>
 ```

 Apenas a palavra "flamingos" estará em negrito, já que é o único texto presente dentro da tag `<b></b>`, trazendo um resultado semelhante como:

 > I love **flamingos**

Importante ressaltar que nem todas as tags necessitam de fechamento, como a `<br>` por exemplo, utilizada para a quebra de linha. 

####  1.1.2. <a name='CaracteresEspeciais'></a>Caracteres Especiaiss

 Existem caracteres especiais que podem ser adcionados ao seu HTML. Seguem alguns exemplos mais comuns:

- `&nbsp;` -  Non breakable space. Transforma um espaço não "quebrável" na identação de um texto; 
- `&trade` - Insere o caractere especial de TradeMark ™;
- `&amp` - Insere caractere especial do E comercial (&); 

Estes são apenas alguns exemplos. Todos os caracteres estão nessa [lista de caracteres especiais](https://erikasarti.com/html/acentuacao-caracteres-especiais/).


####  1.1.3. <a name='NestingAninhar'></a>Nesting (Aninhar)
Os elementos, por sua vez, podem ser "inseridos dentro" de outros elementos, criando assim uma relação de pai-filho entre os elementos/tags, o que comumente é chamado de *nesting*.  

Por exemplo:

```html
<h2><b>Greater</b> <i>Flamingo</i></h2> 
```
Percebe-se que a tag `<b>` está abre e fecha dentro da tag `<h2>`, tornando assim, a `<h2>` pai da `<b>`, resultando:

> ## **Greater** *Flamingo*

Todo o conteúdo de texto está inserido dentro do `<h2>`, enquanto apenas a palavra "Greater" faz parte do elemento negrito e apenas "Flamingo" faz parte do elemento itálico, e tanto o itálico quanto o negrito estão dentro do `<h2>`.


Outro exemplo de nesting em uma estrutura básica em html:

![nesting-img](https://i1.wp.com/qatechhub.com/wp-content/uploads/2016/09/BasicHtmlStructure.png?resize=540%2C360 "Exemplo nesting")


####  1.1.4. <a name='Atributos'></a>Atributos

São comandos que atribuem características para as tags HTML. Existem atributos globais - que funcionam para todas as tags - e atributos específicos para determinadas tags. Todo atributo possui um nome e um valor.

Exemplo de atributo `lang`, que define a linguagem do documento html:

```html
    <html lang="pt-br">
``` 

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
----
###  1.2. <a name='SemanticHTML'></a>Semantic HTML

HTML Semântico é o uso da linguagem HTML para reforçar o significado de todas as informações inseridas no seu documento. Essa semântica, por exemplo, facilita para os leitores de tela identificarem todas as seções da página.

Por exemplo, um código repleto de `<div>` no cabeçalho do site:

```html
<div>
	<div>Meu Blog</div>
	<div>
		<div>Página inicial</div>
		<div>Categorias</div>
		<div>Contato</div>
		<div>Sobre mim</div>
	</div>
</div>
```

Por exemplo, este HTML não semântico impossibilitaria o leitor de tela identificar que trata-se de um cabeçalho.

Agora o mesmo cabeçalho refatorado para ser semântico:
```html
<header>
	<h1>Meu Blog</h1>
	<nav>
		<ul>
			<li><a href="/">Página inicial</a></li>
			<li><a href="/categorias">Categorias</a></li>
			<li><a href="/contato">Contato</a></li>
			<li><a href="/sobre-mim">Sobre mim</a></li>
		</ul>
	</nav>
</header>
```
- Incluindo a tag `<header>`, já é possível identificar que o elemento presente trata-se de um cabeçalho;

- A tag `<h1>` identifica o título principal; 

- A tag `<nav>` identifica que é um elemento de navegação do site;

- Dentro da nav, foi inserida uma lista não ordenada através da tag `<ul>`;

- Esta lista não ordenada possui itens, elementos caracterizados pela tag `<li>`;

Agora é possível que um leitor de dela identifique todos os elementos daquele cabeçalho (além do próprio).

####  1.2.1. <a name='ContentModels'></a>Content Models

Modelos de conteúdo são formas de dar significado aos elementos HTML, definidos por regras que dizem que modelo de conteúdo cada elemento trabalha.

Os elementos HTML são divididos em categorias para atribuição desse significado: 

![modelos-conteudo](https://developer.mozilla.org/@api/deki/files/6244/=Content_categories_venn.png?size=webview "Modelos de conteúdo")

* Metadata content

Os elementos pertencentes a categoria conteúdo de metadados modificam a apresentação ou o comportamento do resto do documento, define ligações para outros documentos ou transmitem outras informações. 

*Alguns* Exemplos: `<meta>`, `<style>` e `<title>`.

* Flow content:

> Elementos pertencentes a categoria de conteúdo de fluxo tipicamente contém texto ou conteúdo embutido. A maioria dos elementos utilizados no body e aplicações são categorizados como Flow Content. 

*Alguns* Exemplos: `<a>`, `<div>`, `<button>`, `<embed>` e `<img>`.

* Sectioning content:

> Os elementos pertencentes ao modelo de conteúdo de sectioning criam uma seção no esboço atual que define o escopo dos elementos `<header>`, elementos `<footer>` e no conteúdo do cabeçalho.

Exemplos: `<article>`, `<aside>`, `<nav>` e `<section>`.

* Heading content:

> O conteúdo do cabeçalho define o título de uma seção.

Exemplos: `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>` e `<hgroup>`. 

* Phrasing content:

>O conteúdo fraseado define o texto e a marcação que ele contém. Séries de conteúdos fraseados compõem parágrafos.

*Alguns* Exemplos: `<b>`, `<input>`, `<i>` e `<label>`.

* Embedded content:

> O conteúdo embutido importa outro recurso ou insere conteúdo de uma outra linguagem de marcação no documento.

Exemplos:  `<audio>`, `<canvas>`, `<embed>`, `<iframe>`, `<img>`, `<math>`, `<object>` e `<video>`.

* Interactive content:

> O conteúdo interativo inclui elementos que são especificamente desenvolvidos para a interação do usuário. Alguns elementos pertencem a essa categoria somente sob condições específicas.

Exemplos:  `<a>`, `<button>`, `<details>`, `<embed>`, `<iframe>`, `<label>`, `<select>`, e `<textarea>`.

- [Lista com todas e seus modelos de conteúdo](https://developer.mozilla.org/pt-BR/docs/Web/Guide/HTML/Categorias_de_conteudo)

####  1.2.2. <a name='nfases'></a>Ênfases

A semântica também está presente nas tags HTML que dão ênfase ao conteúdo fraseado. Como assim? Os leitores de tela alteram o tom de voz da própria leitura, dependendo da utilizada. Seguem algumas comparações:

- A tag `<b>` por exemplo é responsável por deixar o texto em negrito, porém um leitor de tela não dará ênfase alguma ao ler o elemento. A tag `<strong>` também deixará o texto em negrito, entretanto dará uma ênfase  vocal de **importância** pelo leitor de tela.

- A tag `<em>` é visualmente semelhante a `<i>`, que deixará o texto em itálico. Porém, ao utilizar `<em>`, o leitor de tela dará ênfase vocal. Esta tag é comumente utilizada em textos de outras línguas ou citações. 

Mais detalhes sobre modelos de conteúdo em: [Mozilla org - Modelos de conteúdo](https://developer.mozilla.org/pt-BR/docs/Web/Guide/HTML/Categorias_de_conteudo) e [Tableless - Modelos de conteúdo no HTML5](https://tableless.com.br/modelos-de-conteudo-no-html5/)

###  1.3. <a name='SEO'></a>SEO


________________

###  1.4. <a name='Referncias'></a>Referências 

-[Maujor - Escrevendo HTML Semântico](https://www.maujor.com/tutorial/escrevendo-html-semantico.php)

- [Tableless - O que são Tags, elementos e atributos](https://tableless.github.io/iniciantes/manual/html/oquetags.html)

- [Qatechclub - HTML Page structure and nesting](https://qatechhub.com/html-page-structure-nesting/)

- [Medium - O meu HTML é semântico e o seu?](https://medium.com/collabcode/meu-html-%C3%A9-sem%C3%A2ntico-e-o-seu-4e97c81c0c49)

- [Mozilla org - HTML Attributes](https://developer.mozilla.org/pt-BR/docs/HTML/Attributes)

- [Udemy - Curso Aprenda HTML](https://www.udemy.com/aprendahtml/)

- [DevMedia - Códigos HTML](https://www.devmedia.com.br/html-basico-codigos-html/16596)

- [Cheatsheet - HTML 5](http://testking.com/techking/wp-content/uploads/2011/02/IG-HTML5-Cheatsheet-1000px.png)

- [Tableless - Diferenças sutis na semântica](https://tableless.com.br/diferencas-sutis-na-semantica/)