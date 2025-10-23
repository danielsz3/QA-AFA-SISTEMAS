# CT_RF13_ Compra com Fornecedores

## Objetivo
Testar gestão de supply chain e controle de pagamento total e parcial.

## Pré-requisitos
- Sistema com módulo de compras ativo.
- Cadastro de fornecedores disponível.

## Cenários de Teste

### CT_RF13_01_ Cadastrar novo fornecedor
**Descrição:** Cadastrar um novo fornecedor no sistema.

**Passos:**
1. Acessar módulo de fornecedores.
2. Inserir dados do novo fornecedor.
3. Salvar cadastro.

**Resultado Esperado:**
- Fornecedor cadastrado com sucesso.

---

### CT_RF13_02_ Gerar pedido de compra com 10 itens
**Descrição:** Criar pedido de compra com 10 itens.

**Passos:**
1. Acessar módulo de pedidos de compra.
2. Selecionar fornecedor cadastrado.
3. Adicionar 10 itens ao pedido.
4. Salvar pedido.

**Resultado Esperado:**
- Pedido criado com os 10 itens corretamente.

---

### CT_RF13_03_ Simular parcelamento e pagamentos
**Descrição:** Simular parcelamento em 5 vezes, pagar a primeira parcela integralmente e a segunda parcialmente.

**Passos:**
1. Parcelar contas a pagar em 5 vezes.
2. Efetuar pagamento total da primeira parcela.
3. Efetuar pagamento parcial da segunda parcela.

**Resultado Esperado:**
- Pagamentos registrados corretamente.
- Parcelas atualizadas conforme pagamentos.

---

### CT_RF13_04_ Fechamento de caixa
**Descrição:** Realizar fechamento de caixa após pagamentos.

**Passos:**
1. Acessar módulo de fechamento de caixa.
2. Fechar caixa.

**Resultado Esperado:**
- Fechamento realizado com sucesso.

---

### Validação BD
- Confirmar atualização de estoque apenas para itens recebidos.