# Exclusão em Massa de Produtos nos Pedidos – ERP Sankhya

Este projeto contém um código Java desenvolvido para ser utilizado como **botão de ação** no **ERP Sankhya**, vinculado à tabela **TGFCAB**, na **tela do Portal de Vendas**. A funcionalidade permite que o usuário selecione um ou mais pedidos e realize a **exclusão em massa de produtos**.

## 📌 Funcionalidade

- Ação disponível na tela **Portal de Vendas**.
- Permite ao usuário selecionar múltiplos pedidos.
- Realiza a inclusão de um ou mais produtos nos pedidos selecionados de forma automatizada.
- Automatiza e agiliza processos operacionais, reduzindo erros manuais.

## 🛠️ Como configurar no ERP Sankhya

### 1. Criar Módulo Java

1. Acesse a tela **Módulo Java**.
2. Crie um novo **módulo adicional**:
   - **Descrição**: Informe a descrição do módulo.
   - **Identificador**: Caminho da classe Java.
3. Na aba **Arquivo Módulo (Jar)**:
   - Carregue o arquivo `.jar` contendo o código compilado.
4. Salve o registro e prossiga para o próximo passo.

### 2. Adicionar o Botão de Ação

1. Acesse a tela **Dicionário de Dados**.
2. Localize a tabela desejada, por exemplo: **TGFCAB** (CabecalhoNota).
3. Na aba **Ações**, crie um novo registro:
   - **Descrição**: Nome do botão (ex: "Excluir Produtos em Massa").
   - **Tipo**: Rotina Java.
4. No campo **Módulo**:
   - Selecione o módulo criado no passo anterior.
   - Informe a **Classe Java** contida no módulo.
   - Marque a opção **"Depois de executar, recarregar os registros selecionados"**, se necessário.

## 🧩 Estrutura do Código

O código Java está estruturado para:

- Capturar os registros selecionados.
- Se o produto não existir em um pedido selecionado, esse pedido será ignorado e os outros terão o produto excluido.
- Se o produto existir mas a quantidade a remover for superior no pedido, esse produto será removido.
- Se o valor digitado pelo usuário for 0 o produto será excluído por completo, diferente de 0 será proporcional.
- Executar a exclusão de produtos nos pedidos utilizando os objetos da API Sankhya (`DynamicVO`, etc.).
- Tratar possíveis erros e exibir mensagens amigáveis ao usuário final.

## ✅ Pré-requisitos

- Permissões adequadas no ERP para criar botões de ação e rotinas Java.

## 🧪 Testes Recomendados

- Criar pedidos de teste e simular a seleção de múltiplos registros.
- Executar o botão de ação e verificar a exclusão correta dos produtos.
- Testar com diferentes tipos de pedidos e usuários para garantir a robustez da lógica.

---

Desenvolvido por Helem Almeida, visando facilitar e otimizar processos da empresa no ERP Sankhya, garantindo agilidade na exclusão de itens em pedidos.
