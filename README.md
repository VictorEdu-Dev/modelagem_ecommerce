# Modelagem de E-commerce

Esta modelagem de e-commerce visa criar uma pequena plataforma online para a venda de produtos, abrangendo desde o cadastro de clientes, produtos e fornecedores até a gestão de pedidos, pagamentos e entregas.

## Modelagem de Dados

A modelagem de dados é composta por seis entidades principais: CLIENTE, PRODUTO, ESTOQUE, FORNECEDOR, PEDIDO e PAGAMENTO, além das entidades ITEM_PEDIDO e ENTREGA. Cada entidade possui seus atributos específicos que permitem o armazenamento e manipulação eficiente dos dados.

### Entidades Principais

#### CLIENTE
- **Tipo**: Pessoa Física (PF) ou Pessoa Jurídica (PJ).
- **Nome**: Nome do cliente.
- **CPF**: CPF do cliente (para PF).
- **CNPJ**: CNPJ do cliente (para PJ).
- **Email**: Endereço de e-mail do cliente.
- **Telefone**: Número de telefone do cliente.
- **Endereço**: Endereço de entrega do cliente.

#### PRODUTO
- **Nome**: Nome do produto.
- **Descrição**: Descrição detalhada do produto.
- **Preço**: Preço unitário do produto.
- **Fornecedor**: Fornecedor que fornece o produto.

#### ESTOQUE
- **Quantidade**: Quantidade disponível em estoque para cada produto.

#### FORNECEDOR
- **Nome**: Nome do fornecedor.
- **CNPJ**: CNPJ do fornecedor.
- **Telefone**: Número de telefone do fornecedor.
- **Endereço**: Endereço do fornecedor.

#### PEDIDO
- **Cliente**: Cliente que fez o pedido.
- **Data**: Data em que o pedido foi realizado.
- **Endereço de Entrega**: Endereço para entrega do pedido.
- **Status**: Status do pedido.
- **Valor Total**: Valor total do pedido.

#### PAGAMENTO
- **Tipo**: Tipo de pagamento (cartão de crédito, boleto, etc.).
- **Detalhes**: Detalhes específicos do pagamento.

### Requisitos do Sistema

#### Requisitos Funcionais

1. **Cadastro de Clientes**: Permitir o cadastro de clientes PF e PJ, armazenando suas informações pessoais e de contato.
2. **Gestão de Produtos**: Possibilitar o cadastro e atualização de produtos, incluindo detalhes como nome, descrição e preço.
3. **Controle de Estoque**: Monitorar a quantidade disponível de cada produto em estoque e atualizá-la conforme as vendas.
4. **Processamento de Pedidos**: Permitir que clientes façam pedidos, acompanhem o status e possam cancelá-los se necessário.
5. **Gestão de Pagamentos**: Registrar diferentes formas de pagamento e associá-las aos pedidos.
6. **Rastreamento de Entregas**: Fornecer informações sobre o status das entregas e códigos de rastreamento para os clientes.

#### Requisitos Não Funcionais

1. **Segurança**: Garantir a segurança dos dados dos clientes e transações financeiras.
2. **Desempenho**: Garantir uma resposta rápida do sistema mesmo sob carga pesada de usuários.
3. **Usabilidade**: Oferecer uma interface intuitiva e fácil de usar para clientes e administradores.
4. **Escalabilidade**: Permitir o crescimento do número de clientes, produtos e pedidos sem comprometer o desempenho do sistema.
