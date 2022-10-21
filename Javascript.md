# Javascript

## Tipos de Dados
- `'string'`
- `"string"`
- `10`
- `1.1`
- `true`
- `false`
- `null`
- `undefined`
- `NaN`

<br>

## Variáveis
- `var name = "Jhon";` => Variável com tipagem dinâmica
- `var vazio;`
- `const TAM = 5;` => Constante
- `var lista = ["string", 100, ["embed", 200], {car : "ford"}, function(){return "drive";}];`
- `let letSymbol = "scoped value";` => Respect the scope

<br>

## Operadores
- `+` => Concatena string dinamicamente até com outros tipos
- `-`
- `*`
- `/` => Gera float
- `%`
- `a**n` => Ou `Math.pow(a,n)`
- `==`
- `===` => Strict equality, checka além dos valores (não tolera diferenças de tipos)
- `!=`
- `!==`
- `>; <;` => Com string verifica o lenght (se não tiver diferença de caixa alta ou baixa)
- `>=; <=;` 
- `&&` => And
- `||` => Or

<br>

## Condição
```js
if(condicao){
	//bloco
}
else if(condicao){
	//bloco
}
else{
	//bloco
}
```

<br>

## Laços
```js
for(let i=0; i<lista.lenght; i++){
	//bloco
}
for(var i in lista){
	//bloco
}
while(condicao){
	//bloco
}
```

<br>

## Output (Console)
- `console.log("Hello World!");` => Exibe uma mensagem no console do navegador

<br>

## Objetos
```js
var car = {
    color : "red",
    speed : "200",
    drive : function(){return "drive";}
};
```
- alterações profundas no objeto podem ser realizadas no console após a execução
- `window` => Highest level object
- `this` => Refere-se ao objeto do contexto
- `new objeto` => Cria uma nova instância do objeto
- `delete` => Deleta elemento, retorna booleano

```js
function Apple(color, weigth) //é recomendado letra maiúscula para construtores
{
    this.color = color;
    this.weigth = weigth;
}
Apple.prototype = {
    eat : function(){ return "eat the apple";},
    throw : function(){ return "throw the apple";}
}
var apple1 = new Apple("red", 200);
```

<br>

## Arrays
- `array.shift()` => Retorna o primeiro elemento e o remove
- `array.pop()` => Retorna o último elemento e o remove
- `array.unshift("elemento")` => Insere os elementos do parâmetro no começo, retorna o length
- `array.push("elemento")` => Insere os elementos do parâmetro no final, retorna o length
- `array.splice(posicao, n_deletar)` => Recorta do array o numero especificado a partir da posição especificada, retorna o que deletou
- `array.splice(posicao, 0, "novo elemento")` => Adiciona os elementos a partir da posicao especificada (deleta algo se o valor for maior que 0)

<br>

## Outros
 - `//comentário`
 - JS possui memory hoisting, que iça funções pra memória que ao longo do código não foram declaradas anteriormente
