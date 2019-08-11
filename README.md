# CSS - Resumo

## Explique três formas de aplicar os estilos CSS a uma página **web**

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
