# Primeiro Programa
## Versão 01
programa Primeiro_Programa
  /*
    pede dois números ao usuário, soma-os e mostra o resultado na tela
  */
variáveis
  n1, n2, soma: inteiro
  /*
    n1 - o primeiro número
    n2 - o segudo número
    soma - a soma de n1 e n2
  */
início
  leia n1, n2 /* pede os dois números ao usuário */
  soma = n1 + n2 /* calcula e armazena a soma dos números */
  escreva soma /* exibe o valor da soma dos números */
fim

# Cálcula Média:
## Versão 01
programa Calcula_Media
  /*
    pede duas notas ao usuário, calcula e exibe a média dessas
    duas notas
  */
variáveis
  nota1, nota2, media: real
início
  leia nota1, nota2 /* entrada de dados */
  media = (nota1 + nota2) / 2 /* cálculo de média */
  escreva media /* exibição da média */
fim

## Versão 02
programa Calcula_Media
  /*
    pede duas notas ao usuário, calcula e exibe a média dessas
    duas notas
  */
variáveis
  nota1, nota2: real
início
  leia nota1, nota2 /* entrada de dados */
  escreva (nota1 + nota2) / 2 /* cálculo de média */
fim
- variável media não existe, o valor foi calculado para ser imediamento exibido

# Cálcula Área do Triângulo:
## Versão 01
programa Calcula_Area_Triangulo
  /*
    calcula e exibe a área de um triângulo a partir das medidas da base e da altura
  */
variáveis
  base, altura, area: real
início
  leia base, altura
  area = (base * altura) / 2
  escreva area
fim

## Versão 02
programa Calcula_Area_Triangulo
  /*
    calcula e exibe a área de um triângulo a partir das medidas da base e da altura
  */
variáveis
  base, altura: real
início
  leia base, altura
  escreva (base * altura) / 2
fim

# Cálcula Reembolso
## Versão 01
programa Calcula_Reembolso
variáveis
  quilometragem, reembolso: real
início
  leia quilometragem
  reembolso = quilometragem * 0.25478
  escreva reembolso
fim

## Versão 02
programa Calcula_Reembolso
variáveis
  quilometragem: real
início
  leia quilometragem
  escreva quilometragem * 0.25478
fim

## Versão 03
programa Calcula_Reembolso
variáveis
  quilometragem, valorkm, reembolso: real
início
  valorkm = 0.25478
  leia quilometragem
  reembolso = quilometragem * valorkm
  escreva reembolso

  /*
    Observe que foi criada a variável valorkmpara armazenar o valor por km
    percorrido. Apesar de ocupar um pouco mais de memória RAM,
    dependendo da situação isso pode ser interessante.
  */
fim