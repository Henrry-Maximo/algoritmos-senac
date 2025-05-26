# Laços de repetição com validação usando "faça...enquanto

## Estrutura técnica básica
````
faça 
    leia valor 
    se valor inválido 
        escreva "Mensagem de erro!" 
    fim se 
enquanto valor inválido 
````

## Sem validação
````
programa Exemplo_94
variáveis
  início, fim, x: inteiro
início
  leia início, fim

  para x de início >= fim
    escreva "Valor: ", x
  fim para
fim
````
- Se inserir um valor de nício maior do que o valor final, o programa aceitará;
- É aceitável supor que o valor inicial precise er menor do que o final.

## Com validação
````
programa Exemplo_94
variáveis
  início, fim, x: inteiro
início
  faça
    leia início, fim
    se início >= fim
      escreva "O valor inicial precisa ser menor do que o final."
    fim se
  enquanto início >= fim
  para x de início >= fim
    escreva "Valor: ", x
  fim para
fim
````
# 95. A partir do programa do exercício 1, faça a validação de cada uma das duas notas com faça...enquanto.
- Caso seja inserida uma nota inválida, deve ser mostrada uma mensagem de erro para alertar o usuário antes da nota ser novamente solicitada.

````
programa ValidaçãoNotaProva
variáveis
  nota1, nota2, media: real
início
  faça
    leia nota1
    se nota1 < 0 OU nota1 > 10
      escreva "A 1ª  nota precisa estar entre 0 e 10."
    fim se
  enquanto nota1 < 0 OU nota1 > 10

  faça
    leia nota2
    se nota2 < 0 OU nota2 > 10
      escreva "A 2ª nota precisa estar entre 0 e 10."
    fim se
  enqaunto nota2 < 0 OU nota2 > 10

  media = (nota1 + nota2) / 2
  escreva media
fim
````

# 96. A partir do programa do exercício 3, faça a validação das notas com faça...enquanto, considerando que P1 deve estar entre 0 e 10, P2 e Pi entre 0 e 5.
- Caso sejam inseridas notas inválidas, deve ser mostrada uma mensagem de erro para alertar o usuário antes da nota ser novamente solicitada.

````
programa CalculaMediaPonderada
variáveis
  p1, p2, pi, nota: real
início
  faça
    leia p1
    se p1 < 0 OU p1 > 10
      escreva "A nota precisa estar entre 0 e 10."
    fim se
  enquanto p1 < 0 OU p1 > 10

  faça
    leia p2
    se p2 < 0 OU p2 > 10
      escreva "A nota precisa estar entre 0 e 5."
    fim se
  enquanto p2 < 0 OU p2 > 5

  faça
    leia pi
    se pi < 0 OU pi > 10
      escreva "A nota precisa estar entre 0 e 3."
    fim se
  enquanto p1 < 0 OU pi > 5

  nota = (p1 + (p2 + pi)  * 2) / 3
  escreva nota
fim
````

# 98. A partir do programa do exercício 5 da ADO 3, faça a validação dos valores inseridos usando faça...enquanto.
- As condições de validade são que o sexo pode ser apenas “M” ou “F” e a idade precisa ser positiva.
Deve ser mostrada uma mensagem de erro para alertar o usuário caso um valor inválido seja inserido.

````
programa q5
variáveis
    idade, i, qmasc, qfem, sgeral, smasc, sfem: inteiro
    mmasc, mfem: real
    sexo: texto
início
    qmasc = 0
    qfem = 0
    smasc = 0
    sfem = 0
    para i de 1 até 100
        faça
            leia sexo
            se sexo != "M" E sexo != "F"
                escreva "Digite apenas M ou F."
            fim se
        enquanto sexo != "M" E sexo != "F"
        faça
            leia idade
            se idade <= 0
                escreva "A idade precisa ser positiva."
            fim se
        enquanto idade <= 0
        sgeral = sgeral + idade
        se sexo == "M"
            qmasc = qmasc + 1
            smasc = smasc + idade
        senão
            qfem = qfem + 1
            sfem = sfem + idade
        fim se
    fim para
    se qmasc == 0
        mmasc = 0
    senão
        mmasc = smasc / qmasc
    fim se
    se qfem == 0
        mfem = 0
    senão
        mfem = sfem / qfem
    fim se
    escreva qmasc, qfem, mmasc, mfem, sgeral / 100
fim
````

# 99. A partir do programa do exercício 8 da ADO 3, faça a validação dos valores inseridos usando faça...enquanto.

## As condições de validade são:
- O salário mínimo precisa ser um número positivo.
- O turno precisa ser “M”, “N” ou “V”.
- A quantidade de horas trabalhadas precisa estar entre 0 e 160.
- Devem ser mostradas mensagens de erro para alertar o usuário caso valores inválidos sejam inseridos.

````
programa q8
variáveis
    quantf: inteiro
    horas, salmin, vhora, salbase, auxilio, sbruto, totbruto, sbmedio: real
    categoria, turno: texto
início
    totbruto = 0
    quantf = 0
    sbmedio = 0
    faça
        leia salmin
        se salmin <= 0
            escreva "O salário-mínimo precisa ser positivo."
        fim se
    enquanto salmin <= 0
    leia categoria    /* FIM termina */
    enquanto categoria != "FIM"
        faça
            leia turno
            se turno != "M" E turno != "N" E turno != "V"
                escreva "Turno precisa ser M, N ou V."
            fim se
        enquanto turno != "M" E turno != "N" E turno != "V"
        faça
            leia horas
            se horas < 0 OU horas > 160
                escreva "Horas precisam estar entre 0 e 160."
            fim se
        enquanto horas < 0 OU horas > 160
        
        /* definição do valor por hora trabalhada */
        se categoria == "G"
            se turno == "N"
                vhora = salmin * 0.1
            senão
                vhora = salmin * 0.08
            fim se
        senão
            se turno == "N"
                vhora = salmin * 0.06
            senão
                vhora = salmin * 0.04
            fim se
        fim se
        salbase = horas * vhora
        /* definição do auxílio alimentação */
        se salbase <= 2500
            auxilio = salbase * 0.2
        senão
            se salbase <= 5000
                auxilio = salbase * 0.15
            senão
                auxilio = salbase * 0.1
            fim se
        fim se
        sbruto = salbase + auxilio
        totbruto = totbruto + sbruto

        escreva vhora, salbase, auxilio, sbruto
        
        quantf = quantf + 1
        leia categoria
    fim enquanto
    se quantf > 0
        sbmedio = totbruto / quantf
    fim se
    escreva quantf, totbruto, sbmedio
fim
````

# 97. A partir do programa do exercício 67, faça a validação dos valores inseridos usando faça...enquanto.
- A condição de validade é que somente deverá ser aceito um valor positivo na quantidade de compras. Deve ser mostrada uma mensagem de erro para alertar o usuário caso um valor inválido seja inserido.

````
programa Promocao
variáveis
    compras, i: inteiro
início
    para i de 1 até 5
        faça
            leia compras
            se compras <= 0
                escreva "A quantidade precisa ser positiva."
            fim se
        enquanto compras <= 0
        se compras >= 5
            escreva "TEM PROMOÇÃO"
        senão
            escreva "COMPRE MAIS"
        fim se
    fim para
fim
````

## Exercício:
→ Crie um algoritmo que leia a idade de uma pessoa:
→ Só aceite se for:
  - maior ou igual a 18
  - menor ou igual a 100
→ Se for inválido, escreva:
  - "Idade inválida, tente novamente."

Desafio extra:
→ Depois que validar, diga:
  - "Você tem idade para dirigir!"