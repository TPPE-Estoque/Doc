# Minicenário

## Contexto

**Gustavo** é o proprietário de uma pequena rede de supermercados e precisa de um sistema centralizado para gerenciar o estoque de suas múltiplas filiais de forma eficiente. Ele quer ter uma visão consolidada do seu negócio, mas também poder analisar cada filial individualmente para tomar decisões mais estratégicas sobre compras e transferências de produtos.

## Funcionalidades Propostas

### 1. Gestão de Entidades Principais (CRUD)

-   **CRUD de Filiais:**
    -   Permitir que Gustavo cadastre, visualize, edite e remova as filiais da sua rede, registrando informações como nome, endereço e gerente responsável.

-   **Catálogo Central de Produtos (CRUD):**
    -   Manter um **catálogo único de produtos** para toda a rede. Ao adicionar um produto, informa-se dados-mestre como:
        -   Nome do produto
        -   Descrição
        -   Código de barras
        -   Categoria
    -   Esta funcionalidade **não controla a quantidade**, apenas define os produtos que a rede comercializa.

### 2. Gerenciamento de Estoque por Filial

-   **Atribuir Produto a uma Filial:**
    -   Permitir que um produto do catálogo central seja "ativado" em uma filial, definindo informações específicas para aquela localidade, como:
        -   Preço de compra
        -   Preço de venda
        -   Estoque mínimo desejado

-   **Movimentação de Estoque:**
    -   **Registrar Entrada:** Aumentar a quantidade de um produto em uma filial específica (ex: ao receber um pedido de um fornecedor).
    -   **Registrar Saída:** Diminuir a quantidade de um produto em uma filial (ex: por venda, perda ou vencimento).
    -   **Transferência entre Filiais:** Criar uma operação para mover uma quantidade `X` de um produto da `Filial A` para a `Filial B`.

### 3. Consultas e Relatórios Centralizados

-   **Visão de Estoque por Filial:**
    -   Exibir todos os produtos de uma filial selecionada, mostrando a quantidade disponível, preços e outros dados relevantes.

-   **Busca Global de Produto:**
    -   Localizar um produto por nome ou código de barras e ver sua quantidade disponível em **cada uma das filiais**.

-   **Relatórios Gerenciais:**
    -   Permitir que Gustavo filtre os relatórios por uma filial específica ou veja os dados consolidados da rede.
    -   **Curva ABC de Produtos:** Listar os produtos mais importantes com base no seu valor de estoque.
    -   **Alerta de Estoque Baixo:** Gerar um relatório de todos os produtos, em todas as filiais, que estão abaixo do nível de estoque mínimo definido.
    -   **Produtos Sem Estoque:** Listar rapidamente os produtos que estão com estoque zerado em uma ou mais filiais.
    -   **Valor Total de Estoque:** Calcular o valor total do inventário (baseado no preço de compra) por filial e para a rede inteira.