# Diagrama de Classes

Este diagrama de classes modela a arquitetura de software para um sistema de Gerenciamento de Estoque Multi-Filial. O design foi concebido utilizando princípios de Orientação a Objetos para garantir uma estrutura flexível, manutenível e que representa fielmente as regras de negócio.

O modelo é centrado em quatro domínios de negócio claros: **Usuários e Acesso**, **Produtos (Catálogo)**, **Estoque (Inventário)** e **Transações (Vendas)**.

<div align="center">
  <img src="./DiagramaDeClasses/DiagramaDeClasses.png" alt="Diagrama de Classes do Sistema de Estoque" width="800px">
</div>


## Arquitetura do Modelo e Padrões de Design

A estrutura do diagrama se baseia em padrões de design que promovem um código limpo e robusto:

- **Herança e Polimorfismo:** As hierarquias de **`Usuario`** e **`Produto`** utilizam classes abstratas para definir um "contrato" comum. Isso permite que o sistema trate diferentes tipos de usuários e produtos de forma uniforme, enquanto cada subclasse implementa seu comportamento específico (ex: o método `validar_quantidade()` é diferente para `ProdutoUnitario` e `ProdutoPesavel`).

- **Classe Associativa:** As classes **`ItemEstoque`** e **`ItemVenda`** são cruciais. Elas resolvem relacionamentos Muitos-para-Muitos e, mais importante, armazenam atributos que pertencem à relação em si (como `quantidade` e `preco`), que não poderiam existir nem no produto nem na filial/venda sozinhos.

- **Encapsulamento e Intenção:** Métodos como `desativar_filial()` e `finalizar_venda()` foram preferidos em vez de "setters" genéricos. Isso torna a interface das classes mais clara, pois os nomes dos métodos revelam a **intenção de negócio**, e a lógica complexa fica encapsulada dentro da classe.

- **Soft Delete:** Em vez de exclusão física, o sistema utiliza um atributo `status` em entidades como `Produto` e `Filial`. Isso garante a **integridade histórica** dos dados, permitindo que relatórios e análises passadas continuem funcionando mesmo que um produto seja descontinuado.


## Classes Principais e Suas Responsabilidades

### Domínio de Usuários e Acesso
- **`Usuario` (Abstrata):** Molde base para todos os atores do sistema, contendo dados de autenticação.
- **`Administrador`:** Orquestrador do sistema. Não possui estado próprio, mas detém os métodos para realizar operações globais, como `adicionar_filial()` e `descontinuar_produto()`.
- **`Gerente`:** Ator com escopo limitado, fortemente associado a **uma** `Filial`. Seus métodos, como `solicitar_reposicao_estoque()`, refletem ações no contexto de sua própria loja.

### Domínio de Produtos (Catálogo)
-   **`Produto` (Abstrata):** Define a identidade universal de um item (nome, código de barras), servindo como entrada única no catálogo da empresa.
-   **`ProdutoUnitario` / `ProdutoPesavel`:** Especializações que implementam regras de negócio distintas, principalmente na validação de quantidades (números inteiros vs. decimais).

### Domínio de Estoque (Inventário)
-   **`Filial`:** Representa uma loja física. É a classe que gerencia ativamente seu próprio inventário através de métodos como `registrar_entrada()`, `registrar_saida()` e `atualizar_preco_venda()`.
-   **`ItemEstoque`:** **Classe central do sistema.** Representa a existência de um `Produto` em uma `Filial` específica, armazenando os dados que só fazem sentido nesse contexto: `quantidade_atual` e `preco_venda_atual`.

### Domínio de Transações (Vendas)
-   **`Venda`:** Modela uma transação de venda. Possui um ciclo de vida gerenciado por métodos como `adicionar_item()`, `finalizar_venda(forma: FormaPagamento)` e `cancelar_venda()`. O método `finalizar_venda` é o gatilho que dispara a baixa no estoque.
-   **`ItemVenda`:** Linha de uma venda. "Fotografa" a quantidade e o preço de um produto no momento exato da transação, garantindo a precisão do histórico financeiro.
-   **`FormaPagamento` (Enum):** Garante que as formas de pagamento sejam um conjunto de constantes predefinidas e seguras.

