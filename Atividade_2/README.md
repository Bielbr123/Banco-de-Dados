# Sistema de Gestão de Vendas e Estoque - AquiCarro

## 📋 Descrição do Projeto
Sistema para gerenciamento de vendas de peças automotivas, controle de estoque e relacionamento com fornecedores da loja fictícia AquiCarro.

## 🎯 Minimundo
Modelagem completa do fluxo de vendas de peças para clientes, requisições da loja para estoque, retirada e reposição de peças.

## 📊 Entidades Principais
- **Cliente** (CPF, dados pessoais, contatos multivalorados)
- **Venda** (Valor, descrição, horário, lucro derivado)
- **Vendedor** (CPF, nome, comissão derivada)
- **Peça** (ID, nome, preço, atributos não estruturados)
- **Estoque** (Fabricante, quantidade, localização, datas)
- **Compra** (ID, fornecedor, preço)
- **Fornecedor** (CNPJ, nome)

## 🔗 Relacionamentos
- Cliente **Realiza** Venda (1:N)
- Vendedor **Faz** Venda (0:N - 1:1)
- Peça **Comercializa** Venda (0:1 - 1:N)
- Estoque **Contém** Peça (0:1 - 0:1)
- Estoque **Irá** Compra (0:1 - 1:1)
- Peça **Irá Repor** Compra (1:1 - 1:N)
- Fornecedor **Irá Fornecer** Compra (0:N - 1:1)

## 📁 Entregáveis
- Diagrama Entidade-Relacionamento (DER) completo
- Imagens do modelo com e sem zoom
- Detalhamento de elementos e cardinalidades

## ⚠️ Considerações
- Atributos não estruturados incluídos no modelo
- Entidades Venda e Compra tratadas como fortes
- Desafios na classificação de atributos não convencionais

---

**Disciplina:** Banco de Dados  
**Projeto:** Modelagem DER - Sistema AquiCarro
