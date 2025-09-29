# Protótipo do Gerenciador de Estoque

## Introdução

Este documento apresenta o protótipo de baixa/média fidelidade da interface do usuário (UI) para o Sistema de Gerenciamento de Estoque. O objetivo desta versão inicial é validar o fluxo de navegação e a estrutura visual das principais funcionalidades definidas no backlog e no diagrama de classes.

---

### 1. Tela de Login

A porta de entrada do sistema. É uma tela simples e direta, onde os usuários (`Administrador` ou `Gerente`) inserem suas credenciais para obter acesso à plataforma.

<div align="center">
  <img src="./Prototipo/TelaLogin.png" alt="Tela de Login do Sistema" width="800px">
</div>

---

### 2. Tela de Dashboard (Visão do Administrador)

Esta é a tela principal que o `Administrador` (Gustavo) visualiza ao fazer login. Ela oferece uma visão geral e consolidada de toda a rede de supermercados, com indicadores chave (KPIs) e acesso rápido às filiais.

<div align="center">
  <img src="./Prototipo/TelaDashboard.png" alt="Tela de Dashboard do Administrador" width="800px">
</div>

---

### 3. Tela de Gestão de Estoque

A tela operacional mais importante, onde o `Gerente` ou `Administrador` gerencia o inventário de uma filial específica. A interface é focada na visualização de dados em tabela e no acesso rápido às ações de controle de estoque.

*A imagem a seguir mostra a lista de `ItemEstoque` e as ferramentas de busca e botões de ação.*
<div align="center">
  <img src="./Prototipo/TelaEstoque1.png" alt="Tela de Gestão de Estoque - Visão Principal" width="800px">
</div>

*Esta segunda imagem mostra um resumo do estoque.*
<div align="center">
  <img src="./Prototipo/TelaEstoque2.png" alt="Tela de Gestão de Estoque - Modal de Movimentação" width="800px">
</div>

---

### 4. Tela de Produtos (Catálogo Central)

Esta tela administrativa é usada para gerenciar o catálogo central de `Produtos` da empresa. É aqui que novos produtos são definidos antes de serem atribuídos ao estoque de uma filial.

<div align="center">
  <img src="./Prototipo/TelaProduto.png" alt="Tela de Gestão do Catálogo de Produtos" width="800px">
</div>

---

### 5. Tela de Gestão de Filiais

Interface dedicada ao `Administrador` para cadastrar, visualizar, editar e remover as `Filiais` da rede de supermercados.

<div align="center">
  <img src="./Prototipo/TelaFilial.png" alt="Tela de Gestão de Filiais" width="800px">
</div>

---

### 6. Tela de Gestão de Gerentes

Tela da visão do `Gerente`. Um `Gerente` não é capaz de adicionar ou remover filiais.

<div align="center">
  <img src="./Prototipo/TelaGerente.png" alt="Tela da Visão dos Gerentes" width="800px">
</div>