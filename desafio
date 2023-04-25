menu = """
[d] depositar
[s] sacar
[e] extrato
[q] sair

==> """

saldo = 0
limite = 500
extrato = ""
numero_saques = 0
LIMITE_SAQUES = 3

while True:

    opcao = input(menu)

    if opcao == "d":

        valor_deposito = int(input("Informe o Valor R$ a Ser Depositado: "))

        if valor_deposito <= 0:
            print("Valor Inválido! Volte ao Menu Principal para realizar um novo Deposito!")
        else:
            saldo += valor_deposito
            extrato += f"Valor Depositado R$ {str(valor_deposito)} \n"
            print(f"Valor Depositado com Sucesso, seu Saldo é R$: {str(saldo)}")

    elif opcao == "s":
        if numero_saques == LIMITE_SAQUES:
            print(f"Caro Cliente, você já efetuou a quantidade de Saques [{str(LIMITE_SAQUES)}] Limites para o Dia!")
        else:
            valor_saque = int(input("Informe o Valor R$ do Saque: "))

            if valor_saque <= 0:
                print("Valor Inválido! Volte ao Menu Principal para realizar um novo Saque!")
            elif valor_saque > limite:
                print(f"Valor Inválido! Você possui um Limite de até R$: {str(limite)} por saque. Tente Novamente!")
            elif valor_saque > saldo:
                print(f"Saldo Insuficiente! Você possui um Saldo restante de R$: {str(saldo)}. Tente Novamente!")
            else:
                saldo -= valor_saque
                extrato += f"Valor Sacado R$ {str(valor_saque)} \n"
                print(f"Saque no valor de {str(valor_saque)} realizado com sucesso! \n")
                print(f"Seu novo Saldo é de R$: {str(saldo)}!")

    elif opcao == "e":
        print(extrato, end=f"Saldo Total R$ {str(saldo)} \n")
    elif opcao == "q":
        break
    else:
        print("Opção Inválida!")
