# Python

## Operadores Matemáticos
- `+` => Adição
- `-` => Subtração
- `*` => Multiplicação
- `/` => divisão
- `//` => divisão inteira
- `%` => mod
- `**` => exponenciação

<br>

## Operadores Lógicos
- `True`
- `False`
- `==` => Igualdade
- `>` => Maior que
- `>=` => Maior ou igual
- `<` => Menor
- `<=` => Menor ou igual
- `!=` => Diferente
- `not`=> NÃO
- `and`=> E
- `or`=> OU

<br>

## Declaração de variável
- A declaração de variável é dinâmica
- `num = 2`
- `num_float = 2.2`
- `texto = "abc"`

<br>

## String
- `len(string)` => Length, retorna o comprimento da string
- `string1 + string2` => Concatenação
- `"Quantidade: %d" % qtd` => %d para int, %s para string, %f para float (possui inúmeros parâmetros de formatação de saída como número de zeros e etc)
- `"%s tem %d anos" %("João", 22)`
- `"{} tem {} anos".format(nome, idade)` => format não obriga a especificar o tipo
- `f"{nome} tem {idade} anos"` =>  f-string é a forma mais compacta e eficiente
- string é uma lista de caracteres e se comporta como tal com algumas funções (escolha de posição e len())

<br>

## Input
```python
texto = input("Digite: ")
inteiro = int(input("Digite: "))
ponto_flutante = float(input("Digite: "))
```

<br>

## Output
```python
print(variavel) # Printa a variavel dinâmicamente
print(variavel, end=" ") # Parametrô opcional que determina outro final da saída além de \n como padrão
```

<br>

## Condições
```python
if <condição>:
    bloco verdadeiro
else:
    bloco falso
elif <outra condição>: # Fica entre o if e o else
    bloco verdadeiro
```

<br>

## While
```python
while <condição>:
    bloco
    break # Interrompe a execução do while
```

<br>

## For
```python
# Projetado para percorrer listas
for elemento in lista:
    print(elemento)
    break # Interrompe a execução do for

for elem in range(10): # Generator de listas -> equivalente a range (0,10)
    print(elem)

range(5,20,3) # Percorre de 5 a 19 de 3 em 3

for indice, elemento in enumerate(lista): #  Generator de tupla
    print(f"{indice}: {elemento}")
```

<br>

## Listas
- `lista = ["a", 12, "abc", 7.8]`
- `len(lista)` => Length, retorna o comprimento da lista
- `lista.append(valor)` => Adiciona o valor ao final da lista
- `lista.extend(["a",1,2.4])` => Adiciona uma lista a outra
- `lista + ["a",1,2.4]` => Funciona como extend
- `del lista[posicao]` => Remove o(s) elemento(s) especificados
- `lista.pop()` => Remove o ultimo elemento da lista e o retorna
- `lista.pop(posicao)` => Remove o elemento especificado da lista e o retorna
- `list(range(10))` => Cria lista
- `lista.sort()` => Ordena rapidamente
- `sorted(lista)` => Retorna uma nova lista, ordenada

<br>

## Dicionários
```python
tabela = {chave, valor
          "Alface": 0.45}
```

<br>

## Import
- `import nome_biblioteca_um, nome_biblioteca_dois, nome_biblioteca_etc` => Importa bibliotecas para serem utilizadas no  código

<br>

## Outros


- Python executa até arquivos que não estejam na extensão .py

- Para executar um programa no terminal do linux (estando na mesma pasta): `python3 nome_do_arquivo.py`

- Para transformar um arquivo python em executavel no linux:
    - Escrever na primeira linha do .py: `#!/usr/bin/env python3`
    - `chmod +x nome_do_arquivo.py` => Na pasta do arquivo
    - `./nome_do_arquivo.py` => Para executar, estando na pasta do arquivo
    - `/home/pi/Downloads/nome_do_arquivo.py` => Para executar de outro diretório

- Para tornar acessível como qualquer programa:
    - copiar arquivo para /usr/local/bin (necessita permissão root)
    - executar em qualquer diretório como nome_do_arquivo.py
    - (opcional) renomear sem a extensão .py com o comando: `sudo mv /usr/local/bin/nome_do_arquivo.py /usr/local/bin/nome_do_arquivo`
    - (opcional) executar em qualquer diretório como nome_do_arquivo

- Instalar biblioteca no windows:
    - `cd [python_dir]`
    - `pip install [lib_name]`


- Instalar biblioteca no linux:
    - `sudo pip3 install` [nome da biblioteca]

- Instalar biblioteca no raspberry:
    - Se o passo anterior não funcionar, basta baixar o arquivo whl no site https://www.piwheels.org/
    - Ele tem as bibliotecas pré-compiladas para o RPI e instalar via pip
    - Ex: `sudo pip3 install ChatterBot-1.0.2-py2.py3-none-any.whl`