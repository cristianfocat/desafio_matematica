import math
from random import randint#IMPORTAÇÃO DA BIBLIOTECA RANDOM
r=randint(1,1000)
l=randint(1,1000)

#DESAFIO DE RAIZ
def raiz():
    rais= math.sqrt(r)
    print(f'Qual a raiz de {l}')
    try:
        resp=int(input("De seu palpite: "))
    except:
        print('Apenas Valores Numericos')
        raiz()
    if resp == rais:
        print("Você Ganhou!!!😀😀😀")
    else:
        print("Você Perdeu!!!😥😥😥")
        print(f'A raiz é {rais:.2f}')
    continuar()

#DESAFIO DE MULTIPLICAÇÃO
def mult():
    mu=r*l
    print()
    print(f"Qual a Multiplicação de: {r} x {l}")
    try:
        resp=int(input("Dê sua resposta: "))
    except:
        print('Apenas Valores Númericos.')
        mult()
    if resp == mu:
        print("Você Ganhou!!!😀😀😀")
    else:
        print("Você Perdeu!!!😥😥😥")
        print(f'A respsota é: {mu}')
    continuar()

#DESAFIO DE SUBTRAÇÃO
def sub():
    su=r-l
    print()
    print(f'Qual a Subtração de: {r} - {l}')
    try:
        resp=int(input("Qual A Resposta: "))
    except:
        print('Apenas Valores Númericos.')
        sub()
    if resp == su:
        print("Você Ganhou!!!😀😀😀")
    else:
        print("Você Perdeu!!!😥😥😥.")
        print(f'A raiz é {su}')
    continuar()

#DESAFIO DE SOMA
def soma():
    som=r+l
    print()
    print(f'Qual a Soma de: \033[33m{r} \033[0m+ \033[33m{l}\033[0m')#QUAL A SOMA DE...
    try:
        resp=int(input("Qual a Resposta: \033[32m"))#QUAL A RESPOSTA
    except:
        print('\033[31mApenas Valores Númericos.')
        soma()
    if resp == som:
        print()
        print("\033[34mVocê Ganhou!!!😀😀😀\033[0m")
    else:
        print()
        print("\033[31mVocê Perdeu!!!😥😥😥\033[0m")
        print()
        print(f'A Soma é: \033[34m{som}\033[0m')
    continuar()

#Continuação Do Jogo
def continuar():

    print()
    continua=input("deseja continuar?: ").lower()
    if continua != 's':
        print()
        print('👋👋👋Ate a Próxima👋👋👋')
        exit()
    else:
        escolha_desafio()

#Escolha Qual Operação Será o Desafio
def escolha_desafio():
    print()
    print(15*'=','PRONTO PARA O DESAFIO?',15*'=')
    print()
    print(15*'=','ESCOLHA UMA DAS OPÇÔES',15*'=')
    print('1- Raiz \n2- Multiplicação \n3- Sub \n4- Soma')
    print()
    try:
        escolha_o_desafio=int(input('QUAL OPÇÂO ESCOLHIDA?: '))
        print()
    except:
        print()
        print('\033[31mAPENAS OS VALORES JÁ INFORMADOS!!!\033[0m')
        escolha_desafio()

    if escolha_o_desafio == 1:
        raiz()
    elif escolha_o_desafio == 2:
        mult()
    elif escolha_o_desafio == 3:
        sub()
    elif escolha_o_desafio == 4:
        soma()

escolha_desafio()
