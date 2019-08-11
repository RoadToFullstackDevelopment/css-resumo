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

