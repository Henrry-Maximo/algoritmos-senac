## Aula – 16/05/2025
### Questão 01

Escreva a expressão relacional (condição) para cada situação, usando os operadores lógicos adequados.

1. **O valor da variável `pontos` estar no intervalo 15–25.**

```pseudocode
// Opção 1: usando E
pontos ≥ 15 E pontos ≤ 25

// Opção 2: usando NÃO e OU
NÃO (pontos < 15 OU pontos > 25)
```

2. **O valor da variável `pontos` não esta no intervalo 2000–5000.**

```pseudocode
// Opção 1: usando OU
salario < 2000 OU salario > 5000

// Opção 2: usando NÃO e E
NÃO (salario ≥ 2000 E salario ≤ 5000)
```

### Questão 02

Considere o seguinte trecho de um algoritmo, por meio do qual o usuário é 
solicitado a digitar 100 números inteiros, que ficam armazenados em um array. 
Complete ou reescreva o algoritmo de forma que, após a entrada dos 100 números inteiros, o usuário seja solicitado a digitar um número para ser pesquisado 
no array. Depois disso, o algoritmo deverá exibir a quantidade de vezes que o 
número informado para pesquisa foi encontrado no array.

```pseudocode
progrma Prova
variáveis
	lista[100], i, numero, quantidade: inteiro
início
	para i de 1 até 100
		leia lista[i]
	fim para
	
	leia numero
	quantidade = 0
	para i de 1 até 100
		se numero == lista[i]
			quantidade = quantidade + 1
		fim se
	fim para
	
	escreva quantidade
fim
```

```pseudocode
// exibir apenas que encontrou
progrma Prova
variáveis
	lista[100], i, numero, quantidade: inteiro
início
	para i de 1 até 100
		leia lista[i]
	fim para
	
	leia numero
	quantidade = 0
	para i de 1 até 100
		se numero == lista[i]
			quantidade = quantidade + 1
		fim se
	fim para
	
	se quantidade > 0
		escreva "ACHOU"
	senão
		escreva "NÃO ACHOU"
	fim se
fim
```

```pseudocode
progrma Prova
variáveis
	lista[100], i, numero, achou: inteiro
início
	para i de 1 até 100
		leia lista[i]
	fim para
	
	leia numero
	achou = 0
	
	para i de 1 até 100
		se numero == lista[i]
			achou = 1
		fim se
	fim para
	
	se achou == 1
		escreva "ACHOU"
	senão
		escreva "NÃO ACHOU"
	fim se
fim

achou = 0
i = 1
enquanto i <= 100 E achou == 0
	se numero == lista[i]
		achou = 1
	fim se
	i = i + 1
fim enquanto

```