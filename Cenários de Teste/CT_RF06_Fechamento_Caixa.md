# CT_RF16_ Fechamento Caixa

## Objetivo
Garantir a integridade do fechamento financeiro diário, conciliando movimentos financeiros e saldo contábil.

## Pré-requisitos
- Sistema com módulo de caixa ativo.
- Caixas configurados e operacionais.

## Cenários de Teste

### CT_RF16_01_ Simular operações em 3 caixas simultâneas
**Descrição:** Realizar operações simultâneas em 3 caixas diferentes.

**Passos:**
1. Abrir 3 sessões de caixa simultâneas.
2. Realizar vendas e movimentações em cada caixa.

**Resultado Esperado:**
- Operações registradas corretamente em cada caixa.

---

### CT_RF16_02_ Gerar vendas com diferentes tipos de documentos
**Descrição:** Registrar vendas utilizando diferentes tipos de documentos fiscais.

**Passos:**
1. Realizar vendas em cada caixa com tipos variados de documentos (ex: nota fiscal, cupom fiscal).
2. Confirmar registro dos documentos.

**Resultado Esperado:**
- Vendas registradas com os tipos de documentos corretos.

---

### CT_RF16_03_ Realizar retiradas de valores
**Descrição:** Efetuar retiradas de valores dos caixas.

**Passos:**
1. Realizar retiradas de valores em cada caixa.
2. Registrar motivo e valor da retirada.

**Resultado Esperado:**
- Retiradas registradas corretamente.

---

### CT_RF16_04_ Fechar o caixa e conferir tipos de documentos
**Descrição:** Fechar cada caixa e validar os tipos de documentos registrados.

**Passos:**
1. Acessar módulo de fechamento de caixa.
2. Fechar cada caixa.
3. Conferir os tipos de documentos registrados.

**Resultado Esperado:**
- Fechamento realizado com sucesso.
- Tipos de documentos conferidos e corretos.

---

### CT_RF16_05_ Conciliar totais com relatório de vendas
**Descrição:** Conciliar os totais do fechamento com o relatório de vendas.

**Passos:**
1. Gerar relatório de vendas.
2. Comparar totais do relatório com os totais do fechamento de caixa.

**Resultado Esperado:**
- Totais conciliados e consistentes.

---

### Validação BD
- Verificar equilíbrio entre movimentos financeiros e saldo contábil no banco de dados.