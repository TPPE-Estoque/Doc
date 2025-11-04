# Modelo Físico (ERD)

Abaixo está o Modelo Físico, também conhecido como Diagrama Entidade-Relacionamento (ERD), que representa a estrutura final do banco de dados do projeto.

Este diagrama foi gerado automaticamente pela ferramenta DBeaver, conectando-se diretamente ao banco de dados PostgreSQL que está rodando no contêiner Docker. Ele mostra as tabelas reais, suas colunas, tipos de dados e os relacionamentos de chave estrangeira (foreign keys).

É importante notar a convenção de nomenclatura do Django ORM: as tabelas são nomeadas no formato `nome_do_app_nome_do_modelo` (ex: `produto_produto`, `filial_filial`, `estoque_itemestoque`), que é a representação física exata do nosso Diagrama de Classes lógico.

<div align="center">
  <img src="./ModeloFisico/ModeloFisico.png" alt="Modelo Físico (ERD) do Banco de Dados" width="900px">
</div>