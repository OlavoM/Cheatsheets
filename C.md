# C

## Operadores
```c
x++; // Ou ++x, incrementa x
x--; // Ou --x, decrementa x
&& // AND
|| // OR
! // NOT
<< // Deslocamento binário para a esquerda (1<<30 == 2^30)
>> // Deslocamento binário para a direita
```

<br>

## Includes e Define

```c
#include <stdio.h>  // Importa a biblioteca standard in out para input e output
#include <stdlib.h> // Para usar funções system()
#include <stdbool.h> // Para usar booleanos
#include <conio.h> // Para getch e colorir
#include <time.h> // Para numeros aleatorios em conjuto com stdlib.h
#include <malloc.h> // Para trabalhar com alocação dinâmica de memória

#define TAM 5 // TAM significa 5 (sem colocar ; no final)
```

<br>

## Hello World

```c
main() { // Função principal, o compilador considera uma função para retornar inteiro
    printf("Hello, World!\n"); // Imprime na tela
}
```

<br>

## Input

```c
scanf("%f", &numero); // Input de dados
scanf(" %c", &caractere); // Contorna bug do input com enter
```

<br>

## Operadores compospostos de atribuição
```c
num +=5; // num = num + 5
num -=1; // num = num - 1
num *=5; // num = num * 5
num /=5; // num = num / 5
```

<br>

## Laços
```c
for(int i=0; i<5; i++) // (passo inicial; condição de execução; passo executado a cada iteração)
	printf("%d", i); // For de uma linha

int i =0;
while (i<5){ //enquanto a condição for atendida o laço é executado
	printf("%d", i);
	i++;
}

//laços infinitos
for(;;)
while(|)
while(1) //C não tem booleano, a condição retorna 0 ou 1
```

<br>

## Vetores
```c
int v[10]; // Vetor de tamanho 10, com valores anteriores da memória
v[x] = x; // Vetor na posição x recebe x
int a[5] = {1,2,3}; // Vetor inicializado, fica com [1,2,3,0,0], eficaz quando se tem conhecimento dos valores
vetor[10] {} // Vetor inicializado e zerado
memset(vetor,1,8) // Vetor com as 8 primeiras posições com 1
```

<br>

## Matriz
```c
int matriz[10][5]; // Cria matriz de inteiros com 10 linhas e 5 colunas
zerarMatriz(matriz) // Passa para a função pelo nome
void zerarMatriz(int matriz[][n_colunas]) // Chama especificando o numero de colunas
```

<br>

## Ponteiros e Endereços
```c 
int *ponteiro; // Ponteiro de inteiros
ponteiro = &variavel; // Ponteiro recebe o endereço da variável
```

<br>

## Números Aleatórios
```c 
srand(time(NULL)); // Zera para que o valor aleatório seja sempre novo
int numero_aleatorio =  (rand() % 100) + 1; // Inteiro aleatorio de 1 a 100 (0 a 99 + 1 depois)
```

<br>

## Alocação Dinâmica de Memória
```c
int* criaVetorInt(int tamanho){ // Retorna ponteiro
    int *vetor;
    vetor = malloc(tamanho * sizeof(int)); // em C++ adiciona-se a conversão antes de malloc '(int *)'
    return vetor;
}
```

<br>

## Struct
```c
struct nomeDaEstrutura{
    char letra;
    int numero;
};
```

<br>

## Outros

- Quebrando linhas:

    Basta colocar `\` na linha que poderá digitar na de baixo

- Separar numeros grandes pelos milhares:

    `int milhao = 1'000'000;`

<br>

## Pthread
```c
pthread_t threads[QTD]; // Declaracao de threads
pthread_create(&threads[0], NULL, depositos, &saldo); // Global, invocando thread, especificando vetor e posição, NULL para configurações default, função e parametros dela (só tem & aí pois era um ponteiro mesmo)
pthread_join(threads[0], NULL); // Reune as treads na main
pthread_mutex_t trava; // Global, declaração de mutex, uma trava para seções críticas
pthread_mutex_init(&trava, NULL); 

void *depositos(double *x){ // Função para thread tem que ter * (parametro era ponteiro)
    for(int i=0; i<21474830; i++){
        pthread_mutex_lock(&trava);
        *x += 5.0;
        pthread_mutex_unlock(&trava);
    }
    pthread_exit(0); // Sai da thread
}
```
`gcc -pthread nomeDoPrograma.c -o nomeDoPrograma` => Compila com esse comando

<br>

## OpenMP
```c
#include <omp.h>
int maxThreads = omp_get_max_threads(); //threads lógicas
IDThread = omp_get_thread_num();

#pragma omp parallel
{
	//trecho paralelo, automaticamente será executado em todas as threads disponíveis
}

#pragma omp parallel for
    for() //for paralelo automaticamente distribuído entre as threads
```
`gcc nomeDoPrograma.c -o nomeDoPrograma -fopenmp` => Compila com esse comando

`OMP_NUM_THREADS=$x` => x processadores, é uma variavel de ambiente

<br>

## Erros comuns do compilador
`initializer element is not constant` => Alguma variável não está dentro de uma função e ocorre uma confusão no global


