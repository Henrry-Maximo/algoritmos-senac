# 🧮 Primeiro Programa – Cálculo da Média Ponderada

Este exercício solicita a criação de um programa que leia três notas (P1, P2 e PI) e calcule a média ponderada com os seguintes critérios:

- A nota **P1** possui peso **1**.
- As notas **P2** e **PI** possuem peso **2** cada.
- A média final deve ser calculada com a fórmula:

## Versão 01
programa CalculaMediaPonderada
variáveis
  p1, p2, pi, nota: real
início
  /* entrada de dados */
  leia p1, p2, pi

  /* cálculo da nota final */
  nota = (p1 + (p2 + pi) * 2) / 3

  /* exibição da nota final */
  escreva nota
fim

## Versão 02
programa CalculaMediaPonderada
variáveis
  p1, p2, pi: real
início
  /* entrada de dados */
  leia p1, p2, pi

  /* cálculo e exibição da nota final */
  escreva (p1 + (p2 + p1) * 2) / 3
fim

# 🧮 Programa – Cálculo de Cotação Moeda

Uma das tarefas rotineiras em um banco é a troca de 
moeda, sendo que o cliente chega com uma 
determinada quantidade de reais e o funcionário do 
caixa, após consultar a cotação da moeda estrangeira 
no dia, devolve-lhe o equivalente nessa moeda. Crie um 
programa que permita saber qual a quantidade de 
moeda estrangeira que deve ser paga a um cliente a 
partir da quantidade de reais que ele apresenta no 
caixa.

## Versão 01
programa TrocaMoeda
variáveis
  reais, cotacao, quantidade: real
início
  /* entrada de dados */
  leia reais, cotacao

  /* cálculo da quantidaade de moeda estrangeira */
  quantiadade = reais / cotacao

  /* escreva quantidade */
fim

## Versão 02
programa TrocaMoeda
variáveis
  reais, cotacao: real
início
  /* entrada de dados */
  leia reais, cotacao

  /* cálculo e exibição da quantidade de moeda estrangeira */
  escreva reais / cotacao
fim

# 🧮 Programa – Cálculo de Venda Produto
Em um determinado estado, o preço de venda para o 
consumidor final de um automóvel é calculado a partir do preço de 
fabricação, dos impostos e da margem do revendedor, sendo que 
essas partes são assim calculadas:
- a) O preço de fabricação é dado pelo fabricante.
- b) Os impostos correspondem a 35% do preço de fabricação.
- c) A margem do revendedor corresponde a 10% da soma do preço 
de fabricação e dos impostos.
- d) O preço de venda para o consumidor final é a soma dos itens “a”, 
“b” e “c”.
Crie um programa que peça ao usuário os dados necessários, 
calcule e exiba as seguintes informações: o valor dos impostos, o 
valor da margem do revendedor e o preço de venda para o 
consumidor final.

## Versão 01:
programa Calcula_Venda
variáveis
  preco_fab, imposto, margem, preco_venda: real
início
  leia preco_fab

  imposto = preco_fab * 0.35
  margem = (preco_fab + imposto) * 0.1
  preco_venda = preco_fab + imposto + margem
  escreva imposto, margem, preco_venda
fim

## Versão 02:
programa Calcula_Venda
variáveis
  preco_fab: real
início
  leia preco_fab
  escreva preco_fab * 0.35 /* exibe o imposto */
  escreva (preco_fab + preco_fab * 0.35) * 0.1 /* exibe a margem */
  escreva preco_fab + preco_Fab * 0.35 + (preco_fab + preco_fab * 0.35) * 0.1 /* exibe o preço de venda */
fim

# 🧮 Programa – Cálculo de Pontos
Sabe-se que em um campeonato de futebol cada 
equipe soma três pontos por vitória, um por empate e 
zero por derrota. Crie um programa que permita saber 
qual o total de pontos de uma equipe a partir da 
quantidade de vitórias e empates que tenha.

## Versão 01:
programa CalculaPontos
variáveis
  vitorias, empates, pontos: inteiro
início
  leia vitorias, empates
  pontos = vitorias * 3 + empates
  escreva pontos
fim