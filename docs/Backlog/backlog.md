# Backlog do Projeto

Este documento contém as histórias de usuário derivadas da modelagem do sistema de gestão de filiais e estoque.

---

## História #01

**Título:** Cadastro de Filial  

> **Como** proprietário, **desejo** cadastrar uma nova filial no sistema, informando nome, endereço e gerente responsável, **para** expandir o controle para todas as unidades da rede.  

**Critérios de Aceitação:**  
- Deve ser possível registrar nome, endereço e gerente responsável.  
- A filial cadastrada deve aparecer na listagem geral de filiais.  

**Status:** A Fazer  
**Tipo:** Funcionalidade  

---

## História #02

**Título:** Gerenciar Filiais  

> **Como** proprietário, **desejo** visualizar uma lista de todas as filiais cadastradas e poder editar ou remover uma filial existente, **para** manter as informações da rede sempre atualizadas.  

**Critérios de Aceitação:**  
- Deve exibir lista de filiais com dados principais.  
- Deve permitir edição de informações de uma filial.  
- Deve permitir exclusão de filiais.  

**Status:** A Fazer  
**Tipo:** Funcionalidade  

---

## História #03

**Título:** Cadastro de Produto no Catálogo Central  

> **Como** proprietário, **desejo** adicionar um novo produto ao catálogo central, informando nome, descrição, código de barras e categoria, **para** disponibilizá-lo para gestão em qualquer filial.  

**Critérios de Aceitação:**  
- Deve permitir o registro de nome, descrição, código de barras e categoria.  
- Produto cadastrado deve ficar disponível para ativação em filiais.  

**Status:** A Fazer  
**Tipo:** Funcionalidade  

---

## História #04

**Título:** Gerenciar Produtos do Catálogo  

> **Como** proprietário, **desejo** visualizar, editar ou remover produtos do catálogo central, **para** corrigir informações ou descontinuar itens.  

**Critérios de Aceitação:**  
- Deve listar produtos do catálogo.  
- Deve permitir edição de dados do produto.  
- Deve permitir exclusão de produtos.  

**Status:** A Fazer  
**Tipo:** Funcionalidade  

---

## História #05

**Título:** Atribuir Produto a Filial  

> **Como** proprietário, **desejo** ativar um produto do catálogo em uma filial específica, definindo preço de compra, preço de venda e estoque mínimo, **para** começar a controlar o estoque do item naquela unidade.  

**Critérios de Aceitação:**  
- Deve permitir selecionar filial e produto.  
- Deve registrar preço de compra, preço de venda e estoque mínimo.  
- Produto deve aparecer no inventário da filial após ativação.  

**Status:** A Fazer  
**Tipo:** Funcionalidade  

---

## História #06

**Título:** Registrar Entrada de Estoque  

> **Como** proprietário, **desejo** registrar a entrada de uma quantidade de produto em uma filial, **para** refletir o recebimento de mercadorias de fornecedor.  

**Critérios de Aceitação:**  
- Deve ser possível selecionar filial e produto.  
- Deve permitir informar quantidade adicionada.  
- Estoque deve ser atualizado corretamente.  

**Status:** A Fazer  
**Tipo:** Funcionalidade  

---

## História #07

**Título:** Registrar Saída de Estoque  

> **Como** proprietário, **desejo** registrar a saída de uma quantidade de produto em uma filial (por venda ou perda), **para** manter o inventário preciso.  

**Critérios de Aceitação:**  
- Deve permitir registrar motivo da saída (ex.: venda, perda).  
- Estoque deve ser decrementado corretamente.  
- Caso estoque fique negativo, deve exibir alerta/erro.  

**Status:** A Fazer  
**Tipo:** Funcionalidade  

---

## História #08

**Título:** Transferência de Estoque entre Filiais  

> **Como** proprietário, **desejo** registrar a transferência de produtos entre duas filiais, **para** remanejar estoque conforme a demanda.  

**Critérios de Aceitação:**  
- Deve permitir selecionar filial de origem e de destino.  
- Quantidade deve ser removida do estoque da origem e adicionada à de destino.  
- Deve gerar registro histórico da transferência.  

**Status:** A Fazer  
**Tipo:** Funcionalidade  

---

## História #09

**Título:** Visualizar Estoque de Filial  

> **Como** proprietário, **desejo** selecionar uma filial e visualizar a lista de produtos com quantidades em estoque, **para** analisar o inventário da unidade.  

**Critérios de Aceitação:**  
- Deve exibir lista de produtos e respectivas quantidades.  
- Deve indicar estoque mínimo e se o produto está abaixo dele.  

**Status:** A Fazer  
**Tipo:** Funcionalidade  

---

## História #10

**Título:** Buscar Produto em Todas as Filiais  

> **Como** proprietário, **desejo** buscar um produto pelo nome ou código de barras e ver sua quantidade em todas as filiais, **para** ter visão global da disponibilidade.  

**Critérios de Aceitação:**  
- Deve permitir busca por nome e código de barras.  
- Deve retornar lista com todas as filiais e respectivos estoques.  

**Status:** A Fazer  
**Tipo:** Funcionalidade  

---

## História #11

**Título:** Relatório de Estoque Baixo  

> **Como** proprietário, **desejo** gerar relatório listando produtos de todas as filiais que estão abaixo do estoque mínimo, **para** planejar ordens de compra.  

**Critérios de Aceitação:**  
- Deve listar apenas produtos abaixo do estoque mínimo.  
- Deve permitir visualização por filial e consolidado da rede.  

**Status:** A Fazer  
**Tipo:** Funcionalidade  

---

## História #12

**Título:** Calcular Valor Total do Estoque  

> **Como** proprietário, **desejo** visualizar o valor total do inventário, calculado com base no preço de compra, tanto por filial quanto pela rede inteira, **para** entender o valor do ativo imobilizado.  

**Critérios de Aceitação:**  
- Deve calcular valor total por filial.  
- Deve calcular valor total consolidado da rede.  
- Deve considerar preço de compra x quantidade em estoque.  

**Status:** A Fazer  
**Tipo:** Funcionalidade  
