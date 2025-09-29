# Diagrama de Classes

Este diagrama modela um sistema de gerenciamento de estoque para uma rede de supermercados, com foco na separação de responsabilidades entre catálogo, inventário e transações de venda.

<div align="center">
  <img src="./DiagramaDeClasses/DiagramaDeClasses.png" alt="Diagrama de Classes do Sistema de Estoque" width="800px">
</div>

## Classes Principais e Suas Responsabilidades

-   **`Usuario` (Abstrata):** Molde base para usuários com autenticação.
-   **`Administrador`:** Usuário com permissões globais para gerenciar filiais e usuários.
-   **`Gerente`:** Usuário vinculado a uma filial específica, com permissões para gerenciar o estoque e as operações daquela unidade.

---

-   **`Produto` (Abstrata):** Definição central de um item no catálogo.
-   **`ProdutoUnitario`:** Especialização de `Produto` para itens vendidos por unidade.
-   **`ProdutoPesavel`:** Especialização de `Produto` para itens vendidos por peso.

---

-   **`Filial`:** Representa uma loja física da rede.
-   **`ItemEstoque`:** **Classe central do inventário.** Vincula um `Produto` a uma `Filial` e armazena os dados contextuais: `quantidadeAtual` e `precoVendaAtual`.

---

-   **`Venda`:** Registra uma única transação de venda ocorrida em uma `Filial`.
-   **`ItemVenda`:** Registra um produto específico, a `quantidadeVendida` e o `precoVendido` dentro de uma `Venda`.
-   **`FormaPagamento` (Enum):** Define os tipos de pagamento válidos (`CARTAO`, `DINHEIRO`, `PIX`).
