# Protótipo do Gerenciador de Estoque

## Introdução

Este documento apresenta o **protótipo de média e alta fidelidade** da interface do usuário (UI) do **Sistema de Gerenciamento de Estoque**.  
O objetivo desta versão é **validar o fluxo de navegação, usabilidade e estrutura visual** das principais funcionalidades definidas no backlog e no diagrama de classes.

## 1. Tela de Login

A porta de entrada do sistema.  
Nesta tela, os usuários — **Administrador** ou **Gerente** — inserem suas credenciais para acessar a plataforma.

<div align="center">
  <img src="./Prototipo/TelaLogin.png" alt="Tela de Login do Sistema" width="800px">
  <p><em>Figura 1 — Tela de Login</em></p>
</div>

## 2. Dashboard (Visão do Administrador)

Após o login, o **Administrador** (exemplo: *Gustavo*) acessa o painel principal, que apresenta uma **visão consolidada da rede de supermercados**.  
A tela inclui **indicadores-chave (KPIs)**, atalhos para filiais e métricas globais de desempenho.

<div align="center">
  <img src="./Prototipo/TelaDashboard.png" alt="Tela de Dashboard do Administrador" width="800px">
  <p><em>Figura 2 — Dashboard do Administrador</em></p>
</div>

## 3. Gestão de Estoque

A tela operacional mais importante do sistema.  
Nela, **Gerentes e Administradores** podem **monitorar e ajustar o inventário** de uma filial específica.  
A interface prioriza a **clareza das informações** e o **acesso rápido às ações de controle de estoque**.

<div align="center">
  <img src="./Prototipo/TelaEstoque1.png" alt="Tela de Gestão de Estoque - Visão Principal" width="800px">
  <p><em>Figura 3 — Controle de Estoque (Visão Principal)</em></p>
</div>

<div align="center">
  <img src="./Prototipo/TelaEstoque2.png" alt="Tela de Gestão de Estoque - Resumo" width="800px">
  <p><em>Figura 4 — Resumo do Estoque</em></p>
</div>

## 4. Catálogo de Produtos (Central)

Tela utilizada pelo **Administrador** para **gerenciar o catálogo central de produtos** da empresa.  
É neste ambiente que novos produtos são cadastrados e preparados para integração com o estoque das filiais.

<div align="center">
  <img src="./Prototipo/TelaProduto.png" alt="Tela de Gestão do Catálogo de Produtos" width="800px">
  <p><em>Figura 5 — Catálogo Central de Produtos</em></p>
</div>

## 5. Gestão de Filiais

Interface exclusiva do **Administrador**, responsável por **cadastrar, visualizar, editar e remover filiais** da rede.  
O layout prioriza a clareza e a eficiência na manutenção de dados corporativos.

<div align="center">
  <img src="./Prototipo/TelaFilial.png" alt="Tela de Gestão de Filiais" width="800px">
  <p><em>Figura 6 — Gestão de Filiais</em></p>
</div>

## 6. Gestão de Gerentes

Tela dedicada à visão do **Gerente**, com funcionalidades restritas em relação ao administrador.  
Aqui o gerente pode **gerenciar produtos e estoques**, mas **não possui permissão para adicionar ou remover filiais**.

<div align="center">
  <img src="./Prototipo/TelaGerente.png" alt="Tela da Visão dos Gerentes" width="800px">
  <p><em>Figura 7 — Interface do Gerente</em></p>
</div>

## 7. Gestão de Usuários

Tela exclusiva do **Administrador**, projetada para **cadastrar, editar e apagar usuários** do sistema (administradores e gerentes).  

<div align="center">
  <img src="./Prototipo/TelaUsuarios.png" alt="Tela de Gestão de Usuários" width="800px">
  <p><em>Figura 8 — Gestão de Usuários</em></p>
</div>

## 8. Relatórios e Receita

Tela dedicada à **visualização de relatórios financeiros e operacionais**.  
Nesta seção, são exibidos **gráficos e indicadores de receita** com base nas vendas registradas por filial.

- O **Administrador** visualiza:
  - Receita total consolidada de todas as filiais;
  - Receita individual por filial (filtro ou menu dropdown).

- O **Gerente** visualiza:
  - Apenas a **receita de sua própria filial**.

<div align="center">
  <img src="./Prototipo/TelaRelatorio.png" alt="Tela de Relatórios e Receita" width="800px">
  <p><em>Figura 9 — Tela de Relatórios e Receita</em></p>
</div>

## Acesso Interativo ao Protótipo

Para explorar o protótipo de forma interativa, acesse o link abaixo:

<div align="center">

🔗 **[Acessar Protótipo Interativo](https://ecostock.vercel.app/login)**  
*(clique para abrir em nova aba)*

</div>
