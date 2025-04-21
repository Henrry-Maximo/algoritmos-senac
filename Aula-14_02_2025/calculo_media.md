# Calcula Média:
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

# Calcula Área do Triângulo:
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