# Projeto
projeto

print('BEM VINDO AO CADASTRO DE PESSOAS DE BAIXA RENDA URBANA E RURAL')
print('DIGITE UM NUMERO:')
while True:
    p = int(input('1- Cadastro     2- Analise      3- outros'))
    if p == 1:
        def caduser():
            per = input('Digite seu nome e sobrenome')
            perg = int(input('Digite o cep da sua rua ou cidade de sua residencia'))
            pergun = int(input('digite seu CPF'))
            pergunt = float(input('Digite sua renda'))
            pergunta = int(input('Data do cadastro'))

        per = input('Digite seu nome e sobrenome')
        perg = int(input('Digite o cep da sua rua ou cidade de sua residencia'))
        pergun = int(input('digite seu CPF'))
        pergunt = float(input('Digite sua renda'))
        pergunta=int(input('Data do cadastro'))
        arquivo = open('usuarios txt', 'a')
        arquivo.write(per + '#')
        arquivo.write(str(perg) + '#')
        arquivo.write(str(pergunt) + '#')
        arquivo.write(str(pergun) + '\n')
        arquivo.write(str(perg) + '#')
        print('----------------------------------------')
        arquivo.close()
        print('Cadastro realizado com sucesso')
        print('OBRIGADO POR  USAR O SISTEMA DE CADASTRO DE PESSOAS DE BAIXA RENDA URBANA E RURAL')
    elif p == 2:
        arquivo = open("usuarios txt", "r")
        for linha in arquivo:
            valores = linha.split()
            print(linha)
        arquivo.close()
    elif p == 3:
        a = int(input('1- Calculadora  2- Telenofe'))
        if a == 1:
            a = int(input('1- Adição   2- Subtração    3-Multiplicação     4-Divisão       5-Fatorial   6- Numero primo ou não primo'))
            if a == 1:
                soma = 0
                b1=0
                while True:
                    b1 = float(input('Digite um numero (DIGITE 000 PARA SAIR)'))
                    if b1 == 000:
                        break
                    soma += b1
                    print('A adição dos valores foi :{}'.format(soma))
                p3 = str(input('Quer continuar ? s / n'))
                if p3 == 's':
                    print('OK')
                elif p3 == 'n':
                    print('OBRIGADO POR USAR O NOSSO SISTEMA')
                    break
                else:
                    print('Você não digitou uma opção aceitavel. Tente novamente')
            elif a == 2:
                while True:
                    f1 = float(input('Digite um numero'))
                    f2 = float(input('Digite outro numero'))
                    f3 = f1 - f2
                    print('O primeiro numero que voce digitou foi: {} e o segundo é: {}, a soma dos dois é {}'.format(f1, f2, f3))
                    f4 = str(input('Quer continuar ? s / n'))
                    if f4 == 's':
                        print('OK')
                    elif f4 == 'n':
                        print('OBRIGADO POR USAR O NOSSO SISTEMA')
                        break
                    else:
                        print('Você não digitou uma opção aceitavel. Tente novamente')
            elif a == 3:
                multiplicador = 1
                while True:
                    b1 = float(input('Digite um numero (DIGITE 000 PARA SAIR)'))
                    if b1 == 000:
                        break
                    multiplicador *= b1
                    print('A multpiplicação dos valores foi :{}'.format(multiplicador))
                b4 = str(input('Quer continuar ? s / n'))
                if b4 == 's':
                    print('OK')
                elif b4 == 'n':
                    print('OBRIGADO POR USAR O NOSSO SISTEMA')
                    break
                else:
                    print('Você não digitou uma opção aceitavel. Tente novamente')

            elif a == 4:
                while True:
                    c1 = float(input('Digite um numero'))
                    c2 = float(input('Digite outro numero'))
                    c3 = c1 / c2
                    print('O primeiro numero que voce digitou foi: {} e o segundo é: {}, a divisão dos dois é {}'.format(c1, c2, c3))
                    c4 = str(input('Quer continuar ? s / n'))
                    if c4 == 's':
                        print('OK')
                    elif c4 == 'n':
                        print('OBRIGADO POR USAR O NOSSO SISTEMA')
                        break
                    else:
                        print('VOÇÊ NÃO DIGITOU UM COMANDO ACEITAVEL. TENTE NOVAMENTE')
            elif a == 5:
                n=1
                while (n>0):
                    p = int(input('Digite um numero'))
                    n = 1
                    for i in range(p, 0, -1):
                        n = n * i
                        print('{}!={}'.format(p, n))
                        m=input('DESEJA CONTINUAR ? s / n')
                        if m=='s':
                            print('OK')
                        else:
                            print('OBRIGADO POR USAR A NOSSA CALCULADORA')
                            break
            elif a==6:
                p = int(input('Digite um numero'))
                for i in range(2, p):
                    if (p % i == 0):
                        print('Numero não primo:{}'.format(p))
                        break
                    else:
                        print('Numero primo'.format(p))
                        break
        elif a == 2:
            print('Supervisor:(XX)XXXXX-XXXX')
            print('Ouvidoria:(XX)XXXXX-XXXX')
            print('Atendimento (XX)XXXXX-XXXX')
    else:
        print('COMANDO INVALIDO')
