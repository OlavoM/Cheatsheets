# C#

## Variáveis
- `string texto;`
- `char caratere;`
- `int numeroInteiro;`
- `decimal numeroDecimal = 10.9m;` => Ou 10.9M
- `bool variavel;`
- `var variavel = [valor];` => Força o compilador a inferir o tipo, precisa atribuir logo em seguida o valor

<br>

## Output
- `Console.Write("")` => Imprime a mensagem
- `Console.WriteLine("")` => Imprime a mensagem e pula linha
- Verbatim string literal:
```C#
        Console.WriteLine(@"    C:\source\repos
        (this is where your code goes)");
```
- `Console.WriteLine("\u3053\u3093\u306B\u3061\u306F World!");` => Unicode escape characters ( Kon'nichiwa World )
- `Console.WriteLine($"{greeting} {firstName}!");` => String interpolation
- `Console.WriteLine($@"C:\Output\{projectName}\Data");` => Combina string interpolation e verbatim literals

<br>

## Operadores
- `decimal decimalQuotient = 7.0m/5;` => Ao menos um operando tem de ser decimal
- `decimal quotient = (decimal)firstInt / (decimal)secondInt;`
- `System.Math.Pow(x,y);` => x^y
- `int incrementado = i++` => Atribui o valor de i e depois incrementa
- `int incrementado = ++i` => Incrementa o valor de i e depois atribui

<br>

## Strings
- Concatenar numero e string gera string

<br>

## Vetores
- `int[] vetor = new int[TAM];`
- `int[] vetor = {1,2,3};`
- `vetor.Lenght`

<br>

## Laços
```C#
foreach (int elemento in vetor){
	//bloco
}
```

<br>

## Classes
- `Random dice = new Random();`
- `int roll = dice.Next(1,7);` => Gera números aleatórios entre 1 e 6
 - static significa que o método é stateless, não necessita de uma instância do objeto (acesso à memória) para funcionar, ao contrários dos stateful