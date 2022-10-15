# HTML

## Arquivo HTML de Exemplo

```html
<!DOCTYPE html>
<!--Comentário-->
<html lang="pt-br">
    <head>
        <meta charset="UTF-8">
            <title >Structure</title> <!--Título, fica na aba-->
    </head>
    <body><!--Conteúdo da página-->
        Hello World!

        <h1> <!--header one (numbers between one and six)-->
            This is a level 1 heading
        </h1>
        <h2>This is a level 2 heading</h2>
        <h3>This is a level 3 heading</h3>
        <h4>This is a level 4 heading</h4>
        <h5>This is a level 5 heading</h5>
        <h6>This is a level 6 heading</h6>

        This text is before the logical divison <div>This is a logical division</div>This text is directily after the logical division, at the same line!
        <p >This is a paragraph</p>
        <hr> <!--horizon rule-->
        <ol> <!--organized list-->
            <li>This is a list item</li>
            <li>We could have many list items</li>
            <li>And here is another list item</li>
        </ol>
        <ul> <!--unordered list-->
            <li>This is list item</li>
            <li> We also could have many list items inside an unordered list</li>
            <li>And another list item</li>
        </ul>

        This text is on one line
        <br> <!--break line-->
        This text is on another line

	<a href="http://google.com">Link</a> <!--Precisa do http:// para links da web-->
	<a href="http://google.com" target="_blank">Link abre em nova guia</a>
	<a href="http://google.com" title="Visits Google's Home Page">Link Google</a> <!--title aparece quando passa o mouse em cima-->
	
	<script> console.log("script direto no html (não recomendado)"); </script>
	<script src="myapp.js"></script> <!--o script mais embaixo (body) auxilia na distribuição do tempo de carregamento da página-->
    </body>
</html>
```

## Links Úteis
- https://validator.w3.org/