# CT_RF14_ Gestão de Clientes

## Objetivo
Validar o controle de relacionamento com clientes, regras de crédito, dependentes e geração de relatórios.

## Pré-requisitos
- Sistema com módulo de clientes ativo.
- Cadastro de clientes PJ e PF disponível.

## Cenários de Teste

### CT_RF14_01_ Cadastrar 6 clientes (PJ e PF)
**Descrição:** Cadastrar 6 clientes, sendo pessoas jurídicas e físicas.

**Passos:**
1. Acessar módulo de clientes.
2. Cadastrar 6 clientes, incluindo 3 PJ e 3 PF.
3. Salvar os cadastros.

**Resultado Esperado:**
- Clientes cadastrados corretamente no sistema.

---

### CT_RF14_02_ Habilitar limite de crédito para 2 clientes
**Descrição:** Configurar limite de crédito para 2 clientes.

**Passos:**
1. Selecionar 2 clientes cadastrados.
2. Definir limite de crédito para cada um.
3. Salvar alterações.

**Resultado Esperado:**
- Limite de crédito habilitado e salvo para os clientes.

---

### CT_RF14_03_ Acrescentar dependente para 2 clientes
**Descrição:** Adicionar dependentes para 2 clientes.

**Passos:**
1. Selecionar 2 clientes.
2. Cadastrar dependentes vinculados a esses clientes.
3. Salvar os cadastros.

**Resultado Esperado:**
- Dependentes vinculados corretamente aos clientes.

---

### CT_RF14_04_ Registrar compras para os 6 clientes
**Descrição:** Registrar compras para os 6 clientes, incluindo compras em nome dos dependentes para os 2 clientes com dependentes.

**Passos:**
1. Registrar compras para os 4 clientes sem dependentes.
2. Registrar compras para os 2 clientes com dependentes, tanto para o cliente quanto para os dependentes.

**Resultado Esperado:**
- Compras registradas corretamente para todos os clientes e dependentes.

---

### CT_RF14_05_ Realizar compra dentro e fora do limite de crédito
**Descrição:** Para os 2 clientes com limite de crédito, realizar uma compra dentro do limite para um e fora do limite para o outro.

**Passos:**
1. Realizar compra dentro do limite para o cliente 1.
2. Realizar compra que ultrapasse o limite para o cliente 2.

**Resultado Esperado:**
- Compra dentro do limite aprovada.
- Compra fora do limite bloqueada ou sinalizada.

---

### CT_RF14_06_ Atualizar limite de crédito
**Descrição:** Atualizar o limite de crédito de um cliente.

**Passos:**
1. Selecionar cliente com limite de crédito.
2. Alterar o valor do limite.
3. Salvar alteração.

**Resultado Esperado:**
- Limite atualizado corretamente.

---

### CT_RF14_07_ Gerar relatório de contas a receber
**Descrição:** Gerar relatório com as contas a receber dos clientes.

**Passos:**
1. Acessar módulo de relatórios.
2. Selecionar relatório de contas a receber.
3. Gerar relatório.

**Resultado Esperado:**
- Relatório gerado com dados corretos de contas a receber.

---

### Validação BD
- Verificar histórico de compras e bloqueios por crédito no banco de dados.