# C++

## Comentário
- `//comentário`
- `/* comentário */`

<br>

## Using Namespace
`using namespace std;` => Para não precisar digitar std:cout o tempo todo, mas deve ser usado com cuidado, esse recurso pode comprometer o funcionamento de bibliotecas

<br>

## Input/Output
```c++
#include <iostream> // Necessário para input e output
cout<<"Hello World!"; // Output
cin>>variavel // Input 
```

<br>

## Operador Condicional
```c++
// Escrever:
if (condicao) {
	a = 10;
} else {
	b = 20;
}
// É o mesmo que escrever:
(condicao) ? a = 10 : b = 20;
```

<br>

## Converter String
```c++
varInt = stoi(varString);
varFloat = stof(varString);
```

<br>

## Const
```c++
// Const indica que o vlaor da variável não deve ser alterado ao longo do código
int const pi_arredondado = 3.14;
```

<br>

## Auto
```c++
// auto indica ao compilador que deve substituir pelo tipo de variável que está sendo atribuída
auto iter = map.begin(); // É igual a: std::map<std::string,std::string>::iterator iter = map.begin();
```

<br>

## Switch Case
```c++
#include <stdlib.h>
int opc;
cin>>opc
switch (opc){
	case 1:{
		// Conteúdo
	}break;
}
```
