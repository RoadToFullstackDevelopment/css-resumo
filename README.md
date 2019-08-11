# CSS - Resumo

## Explique três formas de aplicar os estilos CSS a uma página *web*

Podemos aplicar os estilos CSS a uma página *web* de três formas:

**Exemplo 1**: Usar o atributo ***style*** diretamente no elemento.

```
<h1 style=”color: red; font-family: Arial; font-size: 70px”>Título da página</h1>
```

**Exemplo 2**: Incluindo o marcador ***style*** dentro do ***head***.

```
<!DOCTYPE html>
    <head>
        <title>Minha primeira página</title>
        <style>
            h1 {
                color: red;
                font-family: Arial;
                font-size: 70px;
            }
        </style>
    </head>
    <body>
        <h1>Título da página</h1>
    </body>
</html>
```

**Exemplo 3**: Incluindo o marcador ***link*** dentro do ***head*** e ali anexar um arquivo css externo.

#### Arquivo HTML

```
<!DOCTYPE html>
   <head>
	<title>Minha primeira página</title>
	<link rel=”stylesheet” href=”style.css”>
   </head>
   <body>
	<h1>Título da página</h1>
   </body>
</html>
```

#### Arquivo CSS

```
h1 {
   color: red;
   font-family: Arial;
   font-size: 70px;
}
```

## O que é CSS?

**CSS** significa ***Cascading Style Sheets***. É usado para definir estilos nas páginas *web*, incluindo *design*, *layout* e variações para dispositivos e tamanhos de tela diferentes. O objetivo do CSS é permitir aos desenvolvedores a separação do conteúdo e estrutura do código do *design* visual do *site*.

## Como utilizar variáveis no Sass?

Pense em variáveis como um modo de armazenar a informação quer reutilizar por toda a sua folha de estilos. Você pode armazenar elementos como cores, fontes ou qualquer valor CSS que queira reutilizar. O Sass usa o símbolo **$** para transformar algo em uma variável.

```
$font-stack:    Helvetica, sans-serif;
$primary-color: #333;

body {
  font: 100% $font-stack;
  color: $primary-color;
}
```

## Explique o *box model* do CSS e seus componentes de *layout*

O ***box model*** do CSS é um paradigma de *layout* retangular para elementos HMTL que compõe-se dos items a seguir:

* ***Content*** **(Conteúdo)**: é o conteúdo da caixa, no qual aparecem textos e imagens.
* ***Padding*** **(Recuo)**: é uma área transparente que rodeia o conteúdo (ou seja, a quantidade de espaço entre a borda e o conteúdo).
* ***Border*** **(Borda)**: uma borda que rodeia o *padding* (se houver) e o conteúdo.
* ***Margin*** **(Margem)**: uma área transparente que rodeia a borda (ou seja, a quantidade de espaço entre a borda e qualquer elemento vizinho). 

## O que é uma *regra CSS*?

Navegadores *web* aplicam regras CSS em um documento para modificar a forma como é exibido. Uma regra compõe-se de:

* Um ***conjunto de propriedades***, que possuem valores configurados para atualizar o modo como o conteúdo HTML é exibido.
* Um ***seletor***, que escolhe o(s) elemento(s) no(s) qual(is) você deseja aplicar os valores de propriedade atualizados.

Um conjunto de regras CSS dentro de uma folha de estilos determina a aparência de uma página *web*.

## O que é DOM *(Document Object Model)* e como podemos vinculá-lo ao CSS?

O *Document Object Model* (DOM) é uma interface de programação de aplicação de plataforma cruzada e independente de linguagem que trata um documento HTML, XHTML ou XML como uma estrutura de árvore na qual cada nó é um objeto que corresponde a uma parte do documento.
Com o *Document Object Model*, programadores podem criar e construir documentos, navegar por sua estrutura, além de adicionar, modificar ou eliminar elementos e conteúdos. O DOM especifica interfaces que devem ser usadas para manipular documentos XML ou HTML. Quando um navegador exibe um documento, deve combinar o conteúdo do documento com seu estilo. O navegador converte HTML e CSS em DOM (*Document Object Model*). O DOM representa o documento na memória do computador, combinando seu conteúdo com o estilo.

## O que é Sass?

**Sass**, ou ***Syntactically Awesome Style Sheets***, é um pré-processador que adiciona poder e elegância a uma linguagem básica, permitindo o uso de variáveis, regras aninhadas, *mixins*, importações em linha e muito mais, tudo com uma sintaxe totalmente compatível com CSS. O Sass ajuda a manter grandes folhas de estilo bem organizadas e faz com que folhas de estilo pequenas funcionem com rapidez.
Um pré-processador CSS é uma linguagem de *script* que extende o CSS, permitindo que desenvolvedores escrevam código em uma linguagem e então compilá-la em CSS.

## Quais são as principais funcionalidades do Sass?

* Compatibilidade total com CSS3.
* Extensões de linguagem como aninhamentos, variáveis e *mixins*.
* Muitas funções úteis para manipular cores e outros valores.
* Funcionalidades avançadas como diretivas de controle para bibliotecas.
* Resultado bem formatado e personalizável.

## O que é interpolação de variável no Sass?

Interpolação de variável é a conversão da variável em seu respectivo valor. Para realizar a interpolação, utilizamos os caracteres **#{}**.

```
Interpolação
#{}
```

Considere a seguinte declaração:

```
aside .side-ad {
    box-sizing: border-box;
    border-width: 2px;
}
```

Criamos as variáveis a seguir:

```
$b: "border";
$s: "side";

//"border" e "side" são cadeias de caracteres, ou seja, são strings.
```

Ao aplicar a interpolação de variável, a declaração assume a seguinte forma:

```
a#{$s} .#{$s}-ad {
    box-sizing: #{$b}-box;
    #{$b}-width: 2px;
}
```

Usando a interpolação, substituímos os seletores e as declarações (**"border"** e **"side"**)pelos seus respectivos valores (**#{$b}** e **#{$s}**).


## Quais são os tipos de dados suportados pelo Sass?

O Sass suporta sete tipos principais de dados:

* **Números**: na maioria das vezes, aparecem acompanhados de uma unidade de algum tipo, porém ainda são números. Você pode realizar operações matemáticas básicas nesses valores.

```
$size: 18;                  // A number
$px-unit: $size * 1px;      // A pixel measurement
$px-string: $size + px;     // A string
$px-number: $px-unit / 1px; // A number
```

* **Strings** (*Cadeia de caractetes*): assim como no CSS, aceita *strings* com e sem aspas, mesmo se contiver espaços.

```
$headline-typeface: Lucida Grande;  
$headline-typeface: 'Lucida Grande';  
$headline-typeface: "Lucida Grande";
```

* **Cores**: expressões de cor do CSS são representadas pelo tipo de dado ***color***. É possível referir-se a cores em notações hexadecimais, como valores **rgb**, **rgba**, **hsl** e **hsla** ou usar palavras-chave nativas como **pink**, **blue**, etc.

```
$color: yellowgreen;           // #9ACD32
color: lighten($color, 15%);    // #b8dc70
color: darken($color, 15%);     // #6c9023
color: saturate($color, 15%);   // #a1e01f
color: desaturate($color, 15%); // #93ba45
color: (green + red);           // #ff8000
```

* **Valores booleanos**: somente dois valores são possíveis: **true** (verdadeiro) e **false** (falso).

```
$i-am-true: true;

body {
  @if not $i-am-true {
    background: rgba(255, 0, 0, 0.6);
  } @else {
    background: rgba(0, 0, 255, 0.6); // expected
  }
}
```

* **Null** (***Nulo***): geralmente usado para definir um estado vazio, seja *true* (verdadeiro) ou *false* (falso). Trata-se de um valor que você quer configurar quando define uma variável sem um valor, somente para impedir que o analisador (*parser*) não quebre.

```
.foo {
  content: type-of(null); // null
  content: type-of(NULL); // string
  $bar: 'foo' + null; // invalid null operation: "foo plus null”.
}
```

* **Listas**: versão em Sass dos *arrays*. Você pode armazenar vários tipos de valores em uma lista.

```
$font-list: 'Raleway','Dosis','Lato'; // Three comma separated elements
$pad-list: 10px 8px 12px; // Three space separated elements
$multi-list: 'Roboto',15px 1.3em; // This multi-list has two lists.
```

* **Mapas**: os mapas no Sass são como *arrays* associativos. Um mapa armazena chaves e valores relacionados com aquelas chaves.

```
$styling: (
  'font-family': 'Lato',
  'font-size': 1.5em,
  'color': tomato,
  'background': black
);

h1 {
  color: map-get($styling, 'color');
  background: map-get($styling, 'background');
}
```

