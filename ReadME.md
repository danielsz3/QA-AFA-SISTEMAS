# 📘 Extensão QA — Vídeos de Rotinas e Cenários de Teste

### Daniel Mesquita (RA 14044)
---
### Gustavo Passos (RA 14262)  
---
### Projeto de Extensão • AFA Sistemas
---

## 👤 Integrantes do Projeto

| Foto | Nome | RA | GitHub |
|------|------|------|--------|
| ![Daniel Mesquita](https://github.com/danielsz3.png) | **Daniel Mesquita Oliveira** | 14044 | https://github.com/danielsz3 |
| ![Gustavo Passos](https://github.com/GustavoPS18.png) | **Gustavo Passos** | 14262 | https://github.com/GustavoPS18 |

---

## 🎥 Acesso aos Vídeos

📁 **Drive com todos os cenários gravados:**  
🔗 https:\
/drive.google.com/drive/folders/1i6tMjC4LuEJl6lndNjfbM_hAgrXuQUZs?usp=drive_link

---

## 🧪 Sobre o Projeto

Este repositório apresenta os **vídeos das rotinas e cenários de teste** desenvolvidos para a disciplina de **Extensão de Qualidade de Software**, aplicados no sistema **AFA Sistemas**.

O objetivo foi **planejar, executar e evidenciar testes reais** dos módulos:

- Vendas (PDV)
- Compras
- Estoque
- Clientes
- Financeiro

Cada rotina também foi validada diretamente no **banco de dados**, assegurando integridade, cálculos corretos e consistência.

---

# 📂 Rotinas e Cenários Testados

## 🔹 1. Inventário de Estoque

### Fluxo Testado
- Importação de produtos via XML  
- Contagem física  
- Lançamento do inventário  
- Emissão de relatório de ajustes  

### Validações no Banco
- Comparação saldo físico × contabilizado  
- Verificação da reconciliação automática  

📌 **Objetivo:** Garantir consistência do estoque após o inventário.

---

## 🔹 2. Processamento de Venda (PDV)

### Fluxo Testado
- Venda com 5 itens  
- Desconto promocional  
- Pagamento misto (dinheiro + cartão)  
- Fechamento de caixa  

### Validações no Banco
- Cálculos financeiros  
- Geração correta dos documentos  

📌 **Objetivo:** Validar o processo completo de venda e caixa.

---

## 🔹 3. Compra com Fornecedores

### Fluxo Testado
- Cadastro de fornecedor  
- Pedido de compra com 10 itens  
- Geração de contas a pagar em 5 parcelas  
- Pagamento total da 1ª e parcial da 2ª parcela  
- Fechamento de caixa  

### Validações no Banco
- Atualização de estoque somente dos itens recebidos  

📌 **Objetivo:** Confirmar integridade do fluxo de compras e pagamentos.

---

## 🔹 4. Gestão de Clientes

### Fluxo Testado
- Cadastro de clientes PF/PJ  
- Configuração de limite de crédito  
- Inclusão de dependentes  
- Registro de compras por cliente e dependentes  
- Testes dentro e fora do limite  
- Bloqueios automáticos  
- Relatório de contas a receber  

### Validações no Banco
- Histórico de compras  
- Controle de crédito e bloqueios  

📌 **Objetivo:** Garantir gestão correta do relacionamento e crédito.

---

## 🔹 5. Fechamento de Caixa

### Fluxo Testado
- Operações simultâneas em 3 caixas  
- Tipos variados de documentos  
- Retiradas e sangrias  
- Fechamento  
- Conciliação com relatório diário  

### Validações no Banco
- Conferência saldo contábil × movimentação  

📌 **Objetivo:** Validar integridade financeira diária.

---

# 👥 Autores

| Nome | RA | GitHub |
|------|------|--------|
| Daniel Mesquita Oliveira | 14044 | https://github.com/danielsz3 |
| Gustavo Passos | 14262 | https://github.com/GustavoPS18 |

---

## 📄 Documento Base

**ROTINAS AFA SISTEMAS.pdf** — utilizado como referência para criação dos cenários.

---

## 🏁 Finalidade

Este repositório organiza todos os **vídeos, cenários e validações** desenvolvidos no projeto, demonstrando:

- ✔ Construção de cenários  
- ✔ Execução prática  
- ✔ Evidências gravadas  
- ✔ Validação técnica via banco  
- ✔ Documentação estruturada  

---
