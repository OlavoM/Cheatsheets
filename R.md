# R

TODO: funções básicas da linguagem

## Vetores
- ` vetor = c(1,2,3,4,5,6) ` => ` [1] 1 2 3 4 5 6 `
- ` vetor = c("a","b",1,2) ` => ` "a" "b" "1" "2" `
- ` z = scan() ` => adiciona os números um a um, até apertar a tecla enter 2 vezes

<br>

## Sequências
- ` z = seq(5,10,2.3) ` => ` [1] 5.0 7.3 9.6 `
- ` z = 1:10 ` => ` [1]  1  2  3  4  5  6  7  8  9 10 `

<br>

## Funções
- ` abs(x) ` => absoluto de x
- ` sum(vetor) ` => soma os itens do vetor
- ` length(vetor) ` => conta o número de elementos no vetor

<br>

## Distribuição Uniforme Discreta
- ` ddunif(a,𝛼, 𝛽) ` => retorna P(X=a)
- ` pdunif(a,𝛼, 𝛽) ` => retorna P(X<=a) [com lower.tail=FALSE no final retorna P(X>a)]
- ` qdunif(𝛾, 𝛼, 𝛽) ` => retorna o quantil de ordem 𝛾 da função de probabilidade 𝑈(𝛼, 𝛽)
- ` rdunif(𝑚,𝛼, 𝛽) ` => retorna uma amostra casual simples de tamanho 𝑚 da função de probabilidade 𝑈(𝛼, 𝛽)

<br>

## Função de Probabilidade Binomial
- ` dbinom(a,n,p) ` => retorna P(X=a)
- ` pbinom(a,n,p) ` => retorna P(X<=a) [com lower.tail=FALSE no final retorna P(X>a)]
- ` qbinom(𝛼,n,p) ` => retorna o quantil de ordem 𝛼 da distribuição binomial (n,p)
- ` rbinom(m,n,p) ` => retorna uma amostra casual simples de tamanho m da distribuição binomial (n,p)

<br>

## Função de Probabilidade Hipergeométrica
- k indivíduos selecionados
- população M+N com M tendo característica específica
- ` dyper(s,M,N,k) ` => retorna P(X=s)
- ` phyper(s,M,N,k) ` => retorna P(X<=s)
- ` qhyper(𝛼, M,N,k) ` => retorna o quantil de ordem 𝛼 da distribuição hipergeométrica (𝑀, 𝑁, 𝑘)
- ` rhyper(m,M,N,k) ` => retorna uma amostra casual simples de tamanho m da distribuição hipergeométrica (M,N,k)

<br>

## Função de Probabilidade Geométrica
- ` dgeom(k,p) ` => retorna P(X=k)
- ` pgeom(k,p) ` => retorna P(X<=k)
- ` qgeom(𝛼,𝑝) ` => devolve o quantil de ordem 𝛼 da distribuição geométrica (𝑝)
- ` rgeom(m,𝑝) ` => devolve uma amostra casual simples de tamanho m da distribuição geométrica (𝑝)

<br>

## Função de Probabilidade de Poisson
- ` dpois(k,𝜃) ` => retorna P(X=k)
- ` ppois(k,𝜃) ` => retorna P(X<=k)
- ` qpois(𝛼, 𝜃) ` => devolve o quantil de ordem 𝛼 da distribuição de Poisson (𝜃)
- ` rpois(m, 𝜃) ` => devolve uma amostra casual simples de tamanho m da distribuição de Poisson (𝜃)

