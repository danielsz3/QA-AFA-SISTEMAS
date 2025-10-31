# CT_RF12_ Processamento de Venda (PDV)

## Objetivo
Validar o fluxo completo de vendas e fechamento de caixa, incluindo descontos e pagamento misto.

## Pré-requisitos
- Sistema com módulo PDV ativo.
- Produtos cadastrados para venda.
- Caixa aberto para registro das vendas.

## Cenários de Teste

### CT_RF12_01_ Iniciar nova venda com 5 itens
**Descrição:** Registrar uma venda com 5 itens no PDV.

**Passos:**
1. Acessar o módulo PDV.
2. Iniciar nova venda.
3. Adicionar 5 itens ao carrinho.
4. Confirmar os itens adicionados.

**Dados de Entrada:**
- 5 produtos diferentes com quantidades definidas.

**Resultado Esperado:**
- Itens adicionados corretamente ao carrinho.
- Total da venda calculado corretamente.

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/1F1bvwLGbqAiAmATXZs5m6MkNcAFYhlTc/view?usp=sharing) |

---

### CT_RF12_02_ Aplicar desconto promocional em 1 item
**Descrição:** Aplicar desconto em um dos itens da venda.

**Passos:**
1. Selecionar um item no carrinho.
2. Aplicar desconto promocional (ex: 10%).
3. Confirmar o desconto aplicado.

**Resultado Esperado:**
- Desconto aplicado corretamente no item.
- Total da venda atualizado com desconto.

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/1X37sq-iUuB7aUV5Bf3HErGDwMRERPuWk/view?usp=sharing) |

---

### CT_RF12_03_ Finalizar venda com pagamento misto
**Descrição:** Finalizar a venda com pagamento misto: 70% cartão e 30% dinheiro.

**Passos:**
1. Selecionar forma de pagamento cartão para 70% do valor.
2. Selecionar forma de pagamento dinheiro para 30% do valor.
3. Confirmar pagamento e finalizar venda.

**Resultado Esperado:**
- Pagamento registrado corretamente nas duas formas.
- Venda finalizada com sucesso.

---

### CT_RF12_04_ Fechamento de caixa e validação por tipo de documento
**Descrição:** Fechar o caixa e validar os totais por tipo de documento.

**Passos:**
1. Acessar o módulo de fechamento de caixa.
2. Realizar fechamento do caixa.
3. Validar os totais por tipo de documento (dinheiro, cartão).

**Resultado Esperado:**
- Fechamento realizado com sucesso.
- Totais por tipo de documento conferidos e corretos.

---

### Validação BD
- Checar integridade dos cálculos e registros financeiros no banco de dados.
