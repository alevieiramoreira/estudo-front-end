# Front-end Roadmap

A trilha de estudos documentados a seguir serão baseados na [roadmap front-end](https://roadmap.sh/frontend).  

Todas as anotações presentes neste documento são resultados do meu *próprio entendimento* sobre o conteúdo estudado, para facilidade de absorção e anotações para futuras consultas. 

 Todos os conteúdos acessados e utilizados neste estudo, estarão referênciados ao final deste documento.  

<!-- vscode-markdown-toc -->
* 1. [ CSS](#CSS)
	* 1.1. [ Learn the basics](#Learnthebasics)
		* 1.1.1. [Estilos (Inline, Externos e Internos)](#EstilosInlineExternoseInternos)
		* 1.1.2. [Regra de Sintaxe CSS](#RegradeSintaxeCSS)
		* 1.1.3. [ID's e Classes](#IDseClasses)
	* 1.2. [Making Layouts](#MakingLayouts)
	* 1.3. [Referências](#Referncias)

<!-- vscode-markdown-toc-config
	numbering=true
	autoSave=true
	/vscode-markdown-toc-config -->
<!-- /vscode-markdown-toc -->

##  1. <a name='CSS'></a> CSS

###  1.1. <a name='Learnthebasics'></a> Learn the basics

O que é o CSS? 

####  1.1.1. <a name='EstilosInlineExternoseInternos'></a>Estilos (Inline, Externos e Internos)

**Interno:** É diretamente inserido no documento html, especificamente na seção do `<head>`. O CSS interno só funciona para a página em específico onde ele foi inserido, e é declarado pela tag `<style>`:

``` html 
<head>
<style type="text/css">
body {
    background-color: blue; 
} 
h1 { 
    color: red; 
    padding: 60px; 
}
</style>
</head>
```

Vantagens:
- Apenas uma página é afetada pela pagina de estilos.
- Classes e IDs podem ser usados ​​por stylesheet interno.
- Não há necessidade de carregar vários arquivos. HTML e CSS podem estar no mesmo arquivo.


Desvantagens:
- Aumento do tempo de carregamento da página.
- Ela afeta apenas uma página – não é útil se você quiser usar o mesmo CSS em vários documentos.


**Externo**: O css é inserido em um arquivo externo, onde é vinculado a um ou mais documentos HTML. Por conseguir vincular múltiplos documentos, o CSS externo pode impactar um site como todo. 

O CSS externo é vinculado no HTML da seguinte maneira:

``` html
<head>
<link rel="stylesheet" type="text/css" href="style.css" />
</head>
```


Vantagens:

- Tamanho menor de páginas HTML e estrutura mais limpa.
- Velocidade de carregamento mais rápida.
- O mesmo arquivo .css pode ser usado em várias páginas.


Desvantagens:

- Até que o CSS externo seja carregado, a página pode não ser processada corretamente.

**Inline**: É o CSS utilizado apenas para uma tag específica através do atributo `style`. É a forma menos recomendada para se utilizar, pois cada tag teria que ser alterada uma por uma, o que geraria um trabalho enorme.

Útil apenas para aplicar estilo em um único elemento. Exemplo de utilização inline:

``` html
<!DOCTYPE html>
<html>
<body style="background-color:black;">

<h1 style="color:white;padding:30px;">Hostinger Tutorials</h1>
<p style="color:white;">Something usefull here.</p>

</body>
</html>

```

Vantagens:
- Útil se você quiser testar e visualizar alterações.
- Útil para correções rápidas.
- Reduzir solicitações HTTP.

Desvantagens:
- CSS Inline deve ser aplicado a cada elemento.

####  1.1.2. <a name='RegradeSintaxeCSS'></a>Regra de Sintaxe CSS 

> "*Uma regra CSS segue uma sintaxe própria que define como será aplicado estilo a um ou mais elementos da marcação HTML de uma página. Um conjunto de regras CSS formam uma folha de estilos.*" 

Uma regra CSS, na sua forma mais elementar, compõe-se de três partes: um seletor, uma propriedade e um valor.

``` css
    seletor { propriedade: valor; }
```
**Seletores**
Seletores são responsáveis por permitir que seja possível selecionar qualquer elemento na página HTML para modificação, seleção essa que é identificada através do nome do elemento, por exemplo:

``` html 
    <!--Elementos HTML-->
    <h1>Título</h1>
    <p>Flamingos felizes fazendo festa<p>
```
``` css
/*Os mesmos elementos do HTML, estilizados no CSS */ 

h1{
    color: blue;
}

p{
    color: red;
}
```
No exemplo acima, todos os elementos `<h1>` e `<p>` no HTML vinculado ao CSS sofrerão alterações.

**Propriedade**


**Valor**


**Declaração**


####  1.1.3. <a name='IDseClasses'></a>ID's e Classes

###  1.2. <a name='MakingLayouts'></a>Making Layouts
---
###  1.3. <a name='Referncias'></a>Referências
- [Hostinger - Diferenças entre estilos CSS](https://www.hostinger.com.br/tutoriais/diferenca-entre-estilos-css/)

- [Maujor - Regra CSS e sua sintaxe](https://www.maujor.com/tutorial/sintaxetut.php)