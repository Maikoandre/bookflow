# Bookflow - Projeto de Banco de Dados

Este projeto implementa um esquema de banco de dados para um sistema de gerenciamento de livraria chamado "Bookflow". Ele inclui tabelas para gerenciar livros, clientes, pedidos e muito mais. O projeto também apresenta views, stored procedures, funções e triggers para dar suporte a várias funcionalidades do aplicativo.

## Esquema do Banco de Dados

O banco de dados é chamado `Bookflow` e usa o conjunto de caracteres `utf8mb4`.

### Tabelas

* **Categorias**: Armazena as categorias dos livros.
* **Livros**: Contém informações sobre os livros, incluindo título, autor, ISBN, preço e quantidade em estoque.
* **Autores**: Armazena informações sobre os autores.
* **Editoras**: Contém os nomes das editoras.
* **Clientes**: Gerencia os dados dos clientes, como nome, e-mail e endereço.
* **Pedidos**: Armazena os pedidos dos clientes, incluindo a data e o status do pedido.
* **Itens_Pedido**: Contém os itens individuais de cada pedido.
* **Carrinho**: Gerencia os itens no carrinho de compras de cada cliente.

## Funcionalidades

### Views

* `vw_livros_mais_vendidos`: Uma view que lista os livros mais vendidos.
* `vw_estoque_baixo`: Mostra livros com estoque baixo (menos de 10 unidades).
* `vw_clientes_ativos`: Lista os clientes que fizeram um pedido nos últimos 6 meses.
* `vw_relatorio_vendas`: Um relatório de vendas agrupado por categoria e autor.

### Stored Procedures

* `cadastrar_cliente`: Cadastra um novo cliente.
* `atualizar_cliente`: Atualiza as informações de um cliente.
* `excluir_cliente`: Exclui um cliente.
* `criar_pedido`: Cria um novo pedido para um cliente.
* `adicionar_item_pedido`: Adiciona um livro a um pedido e atualiza o estoque.
* `atualizar_status_pedido`: Atualiza o status de um pedido.

### Funções

* `login_cliente`: Valida as credenciais de login de um cliente.
* `recuperar_senha`: Recupera a senha de um cliente.
* `calcular_total_pedido`: Calcula o custo total de um pedido, incluindo frete e taxas.

### Triggers

* `verificar_estoque`: Um trigger que verifica se há estoque suficiente antes de adicionar um livro a um pedido.

### Índices

O banco de dados inclui vários índices nas tabelas para melhorar o desempenho das consultas, especialmente em chaves estrangeiras e colunas frequentemente filtradas.

## Como Usar

1.  **Configuração do Banco de Dados**: Execute o script `Database/Tables.sql` para criar o banco de dados e as tabelas, e para inserir os dados iniciais.
2.  **Instalação de Funcionalidades Adicionais**: Execute os scripts na pasta `Database` para criar as views, procedures, funções, triggers e índices.

## Consultas de Exemplo

O arquivo `Database/Tables.sql` também contém várias consultas `SELECT` de exemplo que demonstram como recuperar informações do banco de dados, tais como:

* Selecionar livros com preço acima de um determinado valor.
* Listar livros de uma categoria específica.
* Encontrar pedidos com um status específico.
* Calcular o valor total de um pedido.
