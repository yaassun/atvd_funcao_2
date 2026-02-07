# atvd_funcao_2

def calculadora():
    while True:
        print("\nEscolha uma operação:")
        print("1: Soma")
        print("2: Subtração")
        print("3: Multiplicação")
        print("4: Divisão")
        print("0: Sair")

        opcao = input("Digite o número da operação: ")

        if opcao == "0":
            print("Encerrando o programa...")
            break

        elif opcao in ["1", "2", "3", "4"]:
            try:
                num1 = float(input("Digite o primeiro valor: "))
                num2 = float(input("Digite o segundo valor: "))

                if opcao == "1":
                    resultado = num1 + num2
                    print("Resultado da soma:", resultado)

                elif opcao == "2":
                    resultado = num1 - num2
                    print("Resultado da subtração:", resultado)

                elif opcao == "3":
                    resultado = num1 * num2
                    print("Resultado da multiplicação:", resultado)

                elif opcao == "4":
                    if num2 == 0:
                        print("Erro: divisão por zero não é permitida.")
                    else:
                        resultado = num1 / num2
                        print("Resultado da divisão:", resultado)

            except ValueError:
                print("Erro: digite apenas números válidos.")

        else:
            print("Essa opção não existe")


# Chamada da função
calculadora()
