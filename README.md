produtos = {}
id_atual = 1

while True:
    nome = input("Digite o nome do produto (ou 'sair' para parar): ")
    if nome == 'sair':
        break
    preco = float(input("Digite o preço do produto: "))
    
    produtos[id_atual] = {"nome": nome, "preco": preco}
    id_atual += 1
    if id_atual == 6:
        break

print("\nProdutos cadastrados:")
for id, info in produtos.items():
    print(f"ID: {id} - Nome: {info['nome']} - Preço: R$ {info['preco']:.2f}")
    
total = 0

for info in produtos.values():
    total += info["preco"]

print(f"\nValor total dos produtos: R$ {total:.2f}")# produtos
