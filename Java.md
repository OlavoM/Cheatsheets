# Java

## Hello World
```java
public class Main { //comentário
    public static void main(String[] args){
        System.out.println("Hello World!"); //detecta a tipagem dinamicamente
    }
}
```

<br>

## Variáveis
- `String name = "João";`
- `byte` => Números de -128 a 127 (1 byte)
- `short` => Números de -32,768 a 32,767 (2 bytes)
- `int` => Números de -2,147,483,648 a 2,147,483,647 (4 bytes)
- `long myNum = 15000000000L;` => Números de -9,223,372,036,854,775,808 a 9,223,372,036,854,775,807 (8 bytes)
- `float var = 10.23f;` => Números com 6 a 7 dígitos decimais (4 bytes)
- `float f1 = 10e3f;` => Número científico, com "e" indicando potência de 10 (10000.0)
- `double myNum = 19.99d;` => Números com 15 dígitos decimais (8 bytes)
- `double d1 = 5*10e2d;` => Número científico, com "e" indicando potência de 10 (5000.0)
- `char var = 'a';`
- `boolean var = true;` => Ou `false`
- `final int TAM = 5;` => Constante

<br>

## Operadores
- `x++;` => Ou `++x`, incrementa x
- `x--;` => Ou `--x`, decrementa x
- `&&` => AND
- `||` => OR
- `!` => NOT

<br>

## IF & ELSE
```java
if (condicao) {
    //bloco
}
else if (condicao){
    //bloco
}
else {
    //bloco
}
```

```java
String resultado = (hora<18) ? "Bom Dia" : "Boa Noite"; //ternary operator, if e else de uma linha
switch(expression) {
  case x:
    // code block
    break;
  case y:
    // code block
    break;
  default:
    // code block if there is no case match
}
```

<br>

## Laços
```java
while(condicao) {
    //bloco
}
```

```java
do {
    //bloco
}
while(condicao);
```

```java
for (int i = 0; i < 5; i++) {
    //bloco
}
```

```java
for (type elemento : vetor) { //for-each
    //bloco
}
```

```java
break; //sai do laço
continue; //interrompe a iteração e continua no laço
```

<br>

## String
- `texto.length()`
- `texto.indexOf("string")` => Procura a string dentro da string e retorna o índice da primeira ocorrência
- `texto.concat(textoDois)` => Concatena assim como o uso do operador `+`
- `"\"aspas\""` => O `\` ignora o carectere especial que o segue
- Concatenar número e string gera string

<br>

## Vetores
```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"}; //ou String cars[]
int[] myNum = {10, 20, 30, 40};
vetor.length // Propriedade que retorna o length
int matriz[][] = {{1,2,3,4},{5,6,7}};
```

<br>

## Listas
```java
ArrayList<String> listaDeStrings = new ArrayList<String>();
listaDeStrings.add("Item");
listaDeStrings.get(0);
listaDeStrings.remove(0);
```

<br>

## Maps
```java
HashMap<String, Integer> mapa = new HashMap<String, Integer>(); // Chave String para valor int
// Os elementos não são ordenados
// Rápida a busca/inserção de dados

mapa.put(name, phone); // Permite inserir valore e chaves nulas
mapa.get(name); // Retorna null, se não tiver um valor com essa chave
```
<br>

## HashSet
```java
HashSet<String> set = new HashSet<String>(); // Coleção de dados, não possui valores repetidos
// Os elementos não são ordenados
// Rápida a busca/inserção de dados

set.add("Valor"); // Se esse valor já está no set, ele simplesmente não adiciona

set.size(); // Retorna o número de itens
```

<br>

## Métodos
```java
static void myMethod(tipo parametro, tipo parametroDois){ // Precisa ser declarado dentro de uma classe
    // Bloco
    // Static significa que o método pertence à classe e não é um objeto, ou seja, pode ser acessado sem instanciar um objeto
    // Void pois não retorna nada
}
```

<br>

## Classes
```java
public class Main { // Sempre com letra maiúscula e filename igual (Main.java)
  int x = 5; // Atributos
  int y;
  public Main(){ // Construtor
      y = 3;
  }
}
```

```java
class Ponto{ // Declarada assim para ser acessada no mesmo arquivo, declara-se com public para acessar em outro arquivo
}
```

```java
final class Vehicle{ // Com "final" a classe não pode ser herdada
    // Bloco
}
```

```java
abstract class Animal { // Classe abstrata, não cria objetos e não pode ser acessada, apenas pode ser herdada
    public abstract void animalSound(); // Método abstrato, usável somente em classes abstratas, não tem corpo, é preenchido na herança  
}
```

```java
class Pig extends Animal{
    public void animalSound(){
        // Bloco
    }
}
```

```java
interface Animal { // Interface, uma classe totalmente abstrata, só agrupa métodos vazios
    public void animalSound(); 
    int x = 10; // Atributo public, static e final
}
```

```java
class Pig implements Animal{ // A classe implementa a interface, pode implementar várias interfaces ao mesmo tempo
    public void animalSound(){
        // Bloco
    }
}
```

```java
enum Turno { // Grupo de constantes, enum = "enumerations"
    MANHA("manhã"), // Valor para o turno
    TARDE("tarde"),
    NOITE("noite");
    private String valor; // Atributo
    Turno(String valor){ // Construtor
        this.valor = valor;
    }
    public String getValor(){ // Getter
        return valor;
    }
}
String turnoAtual = Turno.MANHA.getValor(); // Acesso ao valor
```

<br>

## Input
```java
Scanner scan = new Scanner(System.in);
System.out.println("Enter username");
String userName = scan.nextLine(); //nextLine é para strings
System.out.println("Username is: " + userName);
scan.close();
```
```java
inteiro = scan.nextInt();
```

<br>

## Math
```java
Math.max(5, 10);
Math.min(5, 10);
Math.sqrt(64); // Raiz quadrada
Math.abs(-4.7);
Math.random(); // Entre 0.0 e 1.0
int randomNum = (int)(Math.random() * 101);  // 0 a 100
```

<br>

## Try-Catch
```java
try {
    // Bloco de código
}
catch(Exception e) {
    // Tratamento do erro (output amigável por exemplo)
}
finally {
    // Código a executar independente do resultado do try catch
}
```

<br>

## Executar por linha de comando
- `javac Server.java` -> Gera o arquivo Server.class
- `start java Server` -> Start, no Windows, força a execução em uma segunda janela (no Linux, use java Server &)
- `javac Principal.java Classe.java` -> Para dependência de classes no mesmo diretório

<br>

## Comandos
- `jps` - Lista todos os processos que estão rodando na JVM
- `jshell` - Shell de Java, boa para testar trechos de código