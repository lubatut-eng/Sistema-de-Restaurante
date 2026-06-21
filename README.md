# Sistema-de-Restaurante
Projeto desenvolvido para os Módulos 3 e 4 (Listas, Dicionários, Tratamento de Erros e Programação Orientada a Objetos), simulando o gerenciamento básico de um restaurante via console.

## Funcionalidades

- Funcionários: cadastrar, listar e remover
- Cardápio (Pratos): cadastrar (com ingredientes), listar e remover
- Mesas: cadastrar e listar, com controle de ocupada/livre
- Pedidos: abrir pedido em uma mesa, adicionar itens, listar e fechar conta
- Relatório Geral: totais e faturamento

## Como executar:
Depois de iniciar, digite o nome do restaurante e use o menu numerado para navegar entre as opções.

## Estrutura do código

| Classe | Responsabilidade |
|---|---|
| `Ingrediente` | dados de um ingrediente (nome, quantidade, unidade) |
| `Prato` | item do cardápio, com sua lista de ingredientes |
| `Funcionario` | dados de um funcionário (nome, cargo, salário) |
| `Mesa` | número, capacidade e status (ocupada/livre) |
| `Pedido` | itens pedidos em uma mesa e cálculo do total |
| `Restaurante` | classe central que guarda tudo em dicionários e oferece os métodos de cadastro/busca |

Erros de regra de negócio (ex.: mesa já ocupada, ID inexistente, entrada inválida) são tratados com exceções próprias, derivadas de `RestauranteError`, então o programa nunca trava — sempre mostra uma mensagem de erro e volta ao menu.



## Possíveis melhorias futuras:
- Salvar e carregar dados em arquivo (JSON)
- Abater ingredientes do estoque automaticamente ao fechar um pedido
- Criar uma classe `Gerente` que herda de `Funcionario`
