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

**OPERADORES LÓGICOS**
True
False
== -> igualdade
> -> maior que
>= -> maior ou igual
< -> menor
<= -> menor ou igual
!= -> diferente
not -> NÃO
and -> E
or -> OU

<br>

**DECLARAÇÃO DE VARIÁVEL**
#é dinâmica
num = 2
num_float = 2.2
texto = "abc"

<br>

**STRING**
len(string) -> length, retorna o comprimento da string
string1 + string2 -> concatenação
"Quantidade: %d" % qtd -> %d para int, %s para string, %f para float (possui inúmeros parâmetros de formatação de saída como número de zeros e etc)
"%s tem %d anos" %("João", 22)
"{} tem {} anos".format(nome, idade) -> fromat não obriga a especificar o tipo
f"{nome} tem {idade} anos" -> f-string é a forma mais compacta e eficiente
string é uma lista de caracteres e se comporta como tal com algumas funções (escolha de posição e len())

<br>

**INPUT**
texto = input("Digite: ")
inteiro = int(input("Digite: "))
ponto_flutante = float(input("Digite: "))

<br>

**OUTPUT**
print(variavel) #printa a variavel dinâmicamente
print(variavel, end=" ") #parametrô opcional que determina outro final da saída além de \n como padrão

<br>

**CONDIÇÕES**
if <condição>:
    bloco verdadeiro
else:
    bloco falso
elif <outra condição>: #fica entre o if e o else
    bloco verdadeiro

<br>

**WHILE**
while <condição>:
    bloco
    break #interrompe a execução do while

<br>

**FOR**
#projetado para percorrer listas
for elemento in lista:
    print(elemento)
    break #interrompe a execução do for
for elem in range(10): #generator de listas -> equivalente a range (0,10)
    print(elem)
range(5,20,3) ->percorre de 5 a 19 de 3 em 3
for indice, elemento in enumerate(lista): #generator de tupla
    print(f"{indice}: {elemento}")

<br>

**LISTAS**
lista = ["a", 12, "abc", 7.8]
len(lista) -> length, retorna o comprimento da lista
lista.append(valor) -> adiciona o valor ao final da lista
lista.extend(["a",1,2.4]) -> adiciona uma lista a outra
lista + ["a",1,2.4] -> funciona como extend
del lista[posicao] -> remove o(s) elemento(s) especificados
lista.pop() -> remove o ultimo elemento da lista e o retorna
lista.pop(posicao) -> remove o elemento especificado da lista e o retorna
list(range(10)) -> cria lista
lista.sort() -> ordena rapidamente
sorted(lista) -> retorna uma nova lista, ordenada

<br>

**DICIONÁRIOS**
tabela = {chave, valor
          "Alface": 0.45}
>Parei na página 123


import nome_biblioteca_um, nome_biblioteca_dois, nome_biblioteca_etc #importa bibliotecas para serem utilizadas no  código

<br>


#*******NÃO RELACIONADO COM A SINTAXE:*******
# Python executa até arquivos que não estejam na extensão .py

#Para executar um programa no terminal do linux (estando na mesma pasta):
python3 nome_do_arquivo.py

#Para transformar um arquivo python em executavel no linux:
escrever na primeira linha do .py: #!/usr/bin/env python3
chmod +x nome_do_arquivo.py #na pasta do arquivo
./nome_do_arquivo.py #para executar, estando na pasta do arquivo
/home/pi/Downloads/nome_do_arquivo.py #para executar
#Para tornar acessível como qualquer programa:
1- copiar arquivo para /usr/local/bin (necessita permissão root)
2 - executar em qualquer diretório como nome_do_arquivo.py
3 - (opcional) renomear sem a extensão .py com o comando: sudo mv /usr/local/bin/nome_do_arquivo.py /usr/local/bin/nome_do_arquivo
4 - (opcionla) executar em qualquer diretório como nome_do_arquivo

<br>

#Instalar biblioteca no windows:
Cd C:\Users\Olavo\AppData\Local\Programs\Python\Python37\Scripts
[agora é Cd C:\Users\Desert\AppData\Local\Programs\Python\Python37\Scripts>]
pip install ...

<br>

#Instalar biblioteca no linux:
sudo pip3 install [nome da biblioteca]

<br>

#Instalar biblioteca no raspberry:
#Se o passo anterior não funcionar, basta baixar o arquivo whl no site https://www.piwheels.org/
#que tem as bibliotecas pré-compiladas para o RPI e instalar via pip
Ex: sudo pip3 install ChatterBot-1.0.2-py2.py3-none-any.whl