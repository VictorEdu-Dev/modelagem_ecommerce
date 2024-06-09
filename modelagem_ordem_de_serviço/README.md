# Modelagem de Controle e Gerenciamento de Execução de Ordens de Serviço em Oficina Mecânica

## Descrição

Esta modelagem consiste em um sistema de controle e gerenciamento de execução de ordens de serviço (OS) em uma oficina mecânica. Os clientes levam seus veículos à oficina para reparos ou revisões periódicas. Cada veículo é atribuído a uma equipe de mecânicos, que identifica os serviços necessários e preenche uma OS com a data de entrega prevista. A partir da OS, o sistema calcula o valor de cada serviço, consultando uma tabela de referência de mão-de-obra. O valor das peças também é incluído na OS, e o cliente deve autorizar a execução dos serviços. A mesma equipe de mecânicos avalia e executa os serviços. Cada mecânico possui um código único, nome, endereço e especialidade. Cada OS é identificada por um número único, contém a data de emissão, um valor total, um status e uma data para a conclusão dos trabalhos.

## Modelagem Conceitual

### Entidades e Atributos

#### CLIENTE
- **id_cliente** (PK): Identificador único do cliente.
- **nome**: Nome do cliente.
- **endereco**: Endereço do cliente.

#### VEÍCULO
- **id_veiculo** (PK): Identificador único do veículo.
- **id_cliente** (FK): Identificador do cliente proprietário do veículo.
- **modelo**: Modelo do veículo.
- **placa**: Placa do veículo.

#### EQUIPE
- **id_equipe** (PK): Identificador único da equipe de mecânicos.
- **nome**: Nome da equipe.

#### MECÂNICO
- **id_mecanico** (PK): Identificador único do mecânico.
- **codigo**: Código do mecânico.
- **nome**: Nome do mecânico.
- **endereco**: Endereço do mecânico.
- **especialidade**: Especialidade do mecânico.

#### ORDEM_DE_SERVICO
- **id_os** (PK): Identificador único da ordem de serviço.
- **id_veiculo** (FK): Identificador do veículo associado à OS.
- **id_equipe** (FK): Identificador da equipe responsável pela execução dos serviços.
- **data_emissao**: Data de emissão da OS.
- **valor_total**: Valor total da OS.
- **status**: Status da OS.
- **data_conclusao**: Data prevista para a conclusão dos trabalhos.

#### SERVICO
- **id_servico** (PK): Identificador único do serviço.
- **descricao**: Descrição do serviço.
- **valor**: Valor do serviço.

#### ITEM_OS
- **id_item_os** (PK): Identificador único do item da OS.
- **id_os** (FK): Identificador da OS.
- **id_servico** (FK): Identificador do serviço realizado.
- **quantidade**: Quantidade do serviço realizado.
- **valor_unitario**: Valor unitário do serviço.

### Relacionamentos

- **CLIENTE (1) <--> (N) VEÍCULO**
- **EQUIPE (1) <--> (N) MECÂNICO**
- **ORDEM_DE_SERVICO (1) <--> (N) ITEM_OS <--> (N) SERVICO**

### Observações

- A entidade **CLIENTE** representa os clientes da oficina mecânica.
- A entidade **VEÍCULO** representa os veículos dos clientes.
- A entidade **EQUIPE** representa as equipes de mecânicos.
- A entidade **MECÂNICO** representa os mecânicos da oficina.
- A entidade **ORDEM_DE_SERVICO** representa as ordens de serviço emitidas para os veículos.
- A entidade **SERVICO** representa os serviços disponíveis na oficina.
- A entidade **ITEM_OS** é uma tabela associativa que relaciona os serviços realizados em cada ordem de serviço.

Este esquema conceitual proporciona uma visão abrangente do sistema de controle e gerenciamento de execução de ordens de serviço em uma oficina mecânica, capturando as entidades, atributos e relacionamentos essenciais para o funcionamento do sistema.
