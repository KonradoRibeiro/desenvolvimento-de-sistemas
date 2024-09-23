Contexto para o Diagrama de Uso de um sistema de e-commerce
Atores:
-Cliente: O cliente representa o usuário comum do sistema, aquele que faz compras e interage com o carrinho de compras.
-Administrador: O administrador é responsável pela manutenção e gerenciamento dos produtos e pedidos.
Funcionalidades:
Funcionalidades do Cliente:
-BuscarProdutos: O cliente pode procurar produtos disponíveis no sistema.
-AdicionarAoCarrinho: O cliente pode adicionar produtos ao carrinho de compras.
-VisualizarHistórico: O cliente pode acessar o histórico de suas compras anteriores.
-FazerCheckout: O cliente finaliza sua compra, realizando o pagamento e confirmando o pedido.
Funcionalidades do Administrador:
-AdicionarProduto: O administrador pode adicionar novos produtos ao catálogo do sistema.
-RemoverProduto: O administrador pode remover produtos do catálogo.
-GerenciarPedidos: O administrador pode gerenciar os pedidos feitos pelos clientes, verificando, atualizando ou cancelando pedidos conforme necessário.



1. Nome do Caso de Uso: FazerCheckout
2. Ator Principal: Cliente
3. Objetivo Principal: Permitir que o cliente finalize a compra dos produtos adicionados ao carrinho, realizando o pagamento e confirmando o pedido.
4. Ator Secundário: SistemaDePagamento
5. Pré-condições: O cliente deve estar autenticado no sistema.O cliente deve ter pelo menos um produto adicionado ao carrinho.
O SistemaDePagamento deve estar disponível e funcional.
6. Fluxo de Eventos Principal (Caminho Feliz)
O cliente acessa o sistema e faz login.
O cliente adiciona produtos ao carrinho usando a funcionalidade AdicionarAoCarrinho.
O cliente clica na opção FazerCheckout para iniciar o processo de pagamento.
O sistema exibe uma página de confirmação, com o resumo dos produtos no carrinho, valor total, impostos e opções de frete.
O cliente revisa o pedido e escolhe o método de pagamento.
O cliente insere as informações de pagamento (cartão de crédito, débito ou outra forma aceita).
O sistema se comunica com o SistemaDePagamento para processar a transação.
O SistemaDePagamento confirma a aprovação ou rejeição da transação.
O sistema exibe uma mensagem de sucesso se o pagamento for aprovado e gera um número de pedido.
O cliente é redirecionado para uma página de confirmação de pedido, onde pode visualizar o número do pedido e detalhes do envio.
7. Fluxos Alternativos (Caminhos com Exceções)
Falha no pagamento:
O cliente insere as informações de pagamento incorretamente ou a transação é rejeitada pelo SistemaDePagamento.
O sistema exibe uma mensagem informando a falha no pagamento e sugere tentar novamente ou escolher outra forma de pagamento.
O cliente revisa ou altera os dados de pagamento e tenta novamente.
Carrinho vazio:
O cliente tenta fazer o checkout, mas o carrinho está vazio.
O sistema exibe uma mensagem de erro informando que é necessário adicionar produtos ao carrinho antes de continuar.
SistemaDePagamento indisponível:
Durante o processo de pagamento, o sistema detecta que o SistemaDePagamento está fora do ar.
O sistema exibe uma mensagem informando que não é possível processar o pagamento no momento e sugere tentar novamente mais tarde.
8. Pós-condições
Se o pagamento for aprovado, o pedido do cliente é confirmado no sistema.
O estoque dos produtos comprados é atualizado.
Um número de pedido é gerado e exibido ao cliente.
O sistema de pagamento registra a transação com sucesso.
9. Regras de Negócio
O cliente deve poder revisar seu carrinho e alterar a quantidade ou remover produtos antes de concluir o pagamento.
O sistema só permite que o cliente faça o checkout se houver produtos no carrinho.
O pedido só é confirmado após a aprovação do pagamento pelo SistemaDePagamento.
O sistema deve oferecer diferentes métodos de pagamento, conforme política da loja (ex: cartão de crédito, débito, boleto, etc.).
10. Requisitos Não Funcionais
O processo de checkout deve ser concluído em menos de 5 segundos, excluindo o tempo de processamento do pagamento.
O sistema deve ser capaz de lidar com múltiplas transações simultâneas, garantindo segurança e confiabilidade nos dados financeiros.
O sistema deve criptografar as informações de pagamento do cliente, garantindo a segurança dos dados pessoais e bancários.
