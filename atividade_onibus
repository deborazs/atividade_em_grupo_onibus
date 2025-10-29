# Sistema para monitorar a demanda das linhas de ônibus
#Desenvolvido por: Debora Beatriz,Jaqueline Fanton e Maria Clara.

LIMITE_MAXIMO = 50  # máximo de passageiros permitido

total_linhas = 0
total_sobrecarregadas = 0
relatorio = []

print("=== Sistema de Controle de Linhas de Ônibus 🛣  ===\n")

continuar = "S"

while continuar.upper() == "S":
    numero_linha = input("Digite o número da linha: ")
    nome_linha = input("Digite o nome da linha: ")
    qtd_passageiros = int(input("Digite a quantidade de passageiros na hora de pico: "))

    if qtd_passageiros > LIMITE_MAXIMO:
        status = "SOBRECARREGADA"
        print("Atenção! Essa linha está sobrecarregada, precisa de mais ônibus.\n")
        total_sobrecarregadas += 1
    else:
        status = "Normal"
        print("Demanda normal nessa linha.\n")

    # Armazena as informações da linha
    linha = {
        "numero": numero_linha,
        "nome": nome_linha,
        "passageiros": qtd_passageiros,
        "status": status
    }

    relatorio.append(linha)
    total_linhas += 1

    continuar = input("Deseja cadastrar outra linha? (S/N): ")
    if continuar == "S":
        print()
        continuar = input("Deseja cadastrar outra linha? (S/N): ").strip()
continuar = continuar.upper()

if continuar == "S":
    print("Você escolheu continuar.\n")

elif continuar == "N":
    print("Você escolheu encerrar.\n")

else:
    print("Opção inválida! Digite apenas S ou N.\n")


# Exibição do relatório final
print("===== RELATÓRIO FINAL =====")
print("Total de linhas analisadas:", total_linhas)
print("Total de linhas sobrecarregadas:", total_sobrecarregadas)
print("------------------------------------")
print("LISTAGEM DETALHADA DAS LINHAS:")
for linha in relatorio:
    print("------------------------------------")
    print("Número da linha:", linha["numero"])
    print("Nome da linha:", linha["nome"])
    print("Passageiros na hora de pico:", linha["passageiros"])
    print("Status:", linha["status"])

print("------------------------------------")
print("Fim do relatório.")
