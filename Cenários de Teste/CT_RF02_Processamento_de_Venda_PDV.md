# **Cenário RF12 — Processamento de Venda (PDV)**

---

| **Objetivo** |
| :-- |
| Validar o fluxo completo de vendas e fechamento de caixa, incluindo descontos e pagamento misto. |

| **Pré-requisitos** |
| :-- |
| - Sistema com módulo PDV ativo. |
| - Produtos cadastrados para venda. |
| - Caixa aberto para registro das vendas. |

---

## **Caso de Teste CT_RF12_01: Iniciar nova venda com 5 itens**

| ID | Descrição |
| :-- | :-- |
| CT_RF12_01 | Registrar uma venda com 5 itens no PDV. |

| **Pré-condições** |
| :-- |
| - Módulo PDV ativo. |
| - Produtos cadastrados. |
| - Caixa aberto. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o PDV |  
| **QUANDO** inicia uma nova venda e adiciona 5 itens ao carrinho |  
| **ENTÃO** os itens devem ser registrados corretamente no carrinho. |

| **Dados de Entrada** |
| :-- |
| - 5 produtos diferentes com quantidades definidas. |

| **Critérios de Aceitação** |
| :-- |
| - Itens adicionados corretamente ao carrinho. |
| - Total calculado corretamente. |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/1F1bvwLGbqAiAmATXZs5m6MkNcAFYhlTc/view?usp=sharing) |

---

## **Caso de Teste CT_RF12_02: Aplicar desconto promocional em 1 item**

| ID | Descrição |
| :-- | :-- |
| CT_RF12_02 | Aplicar desconto promocional em um item da venda. |

| **Pré-condições** |
| :-- |
| - Venda iniciada. |
| - Itens cadastrados no carrinho. |

| **Passos** |
| :-- |
| **DADO** que o usuário seleciona um item no carrinho |  
| **QUANDO** aplica um desconto promocional (ex: 10%) |  
| **ENTÃO** o item deve refletir o desconto e o total da venda deve ser recalculado. |

| **Critérios de Aceitação** |
| :-- |
| - Desconto aplicado corretamente. |
| - Total atualizado com desconto. |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/1Zq-lt9MmpESbBQYuxg43J6YVycW3Aivb/view?usp=sharing) |

---

## **Caso de Teste CT_RF12_03: Finalizar venda com pagamento misto**

| ID | Descrição |
| :-- | :-- |
| CT_RF12_03 | Finalizar venda com pagamento misto: 70% cartão e 30% dinheiro. |

| **Pré-condições** |
| :-- |
| - Venda em andamento. |
| - Itens revisados no carrinho. |

| **Passos** |
| :-- |
| **DADO** que o usuário seleciona formas de pagamento |  
| **QUANDO** define 70% do valor em cartão e 30% em dinheiro |  
| **ENTÃO** a venda deve ser finalizada com sucesso e os pagamentos registrados. |

| **Critérios de Aceitação** |
| :-- |
| - Pagamento misto registrado corretamente. |
| - Venda finalizada sem erros. |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/1X37sq-iUuB7aUV5Bf3HErGDwMRERPuWk/view?usp=sharing) |

---

## **Caso de Teste CT_RF12_04: Fechamento de caixa e validação por tipo de documento**

| ID | Descrição |
| :-- | :-- |
| CT_RF12_04 | Realizar fechamento de caixa e validar totais por tipo de documento. |

| **Pré-condições** |
| :-- |
| - Venda(s) registrada(s). |
| - Caixa aberto e operacional. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o módulo de fechamento de caixa |  
| **QUANDO** realiza o fechamento |  
| **ENTÃO** os totais por tipo de documento devem ser exibidos corretamente. |

| **Critérios de Aceitação** |
| :-- |
| - Fechamento realizado com sucesso. |
| - Totais corretos por cada tipo de documento (dinheiro, cartão). |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/1ZECSYeDLawtLU_q2cMMkHZPBA5tauhtb/view?usp=sharing) |

---

## **Validação no Banco de Dados**

| Critérios |
| :-- |
| - Validar integridade dos cálculos. |
| - Validar registros financeiros gravados corretamente no BD. |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/1FoeautySTxti4IisVl6JlDZOd1OzgNKM/view?usp=drive_link) |

---

# **Cenário RF12 — Negativos (Processamento de Venda - PDV)**

---

## **Caso de Teste Negativo CT_RF12_01_N: Falha ao iniciar venda com item inválido**

| ID | Descrição |
| :-- | :-- |
| CT_RF12_01_N | Tentar iniciar venda adicionando item inexistente ou inativo. |

| **Pré-condições** |
| :-- |
| - Módulo PDV ativo. |
| - Caixa aberto. |
| - Produto inexistente, inativo ou sem estoque. |

| **Passos** |
| :-- |
| **DADO** que o usuário inicia uma nova venda no PDV |  
| **QUANDO** tenta adicionar ao carrinho um item inexistente ou sem estoque |  
| **ENTÃO** o sistema deve impedir a adição e exibir mensagem de erro. |

| **Critérios de Aceitação** |
| :-- |
| - Item não deve ser adicionado ao carrinho. |
| - Total da venda deve permanecer inalterado. |
| - Mensagem clara deve informar que o item é inválido ou indisponível. |

| **Evidência(s)** |
| :--: |
| [Vídeo]("") |

---

## **Caso de Teste Negativo CT_RF12_02_N: Falha ao aplicar desconto inválido**

| ID | Descrição |
| :-- | :-- |
| CT_RF12_02_N | Tentar aplicar desconto superior ao permitido ou em formato inválido. |

| **Pré-condições** |
| :-- |
| - Venda iniciada com itens no carrinho. |
| - Regras de desconto configuradas no sistema. |

| **Passos** |
| :-- |
| **DADO** que o usuário seleciona um item no carrinho |  
| **QUANDO** tenta aplicar um desconto inválido (ex: 90%, negativo ou maior que o permitido) |  
| **ENTÃO** o sistema deve rejeitar o desconto e manter o valor original. |

| **Critérios de Aceitação** |
| :-- |
| - Desconto não deve ser aplicado. |
| - Totais não devem sofrer alteração. |
| - Sistema deve exibir mensagem informando o erro no desconto. |

| **Evidência(s)** |
| :--: |
| [Vídeo]("") |

---

## **Caso de Teste Negativo CT_RF12_03_N: Falha ao finalizar venda com pagamento misto inválido**

| ID | Descrição |
| :-- | :-- |
| CT_RF12_03_N | Tentar finalizar venda com soma incorreta das formas de pagamento. |

| **Pré-condições** |
| :-- |
| - Venda em andamento com itens cadastrados. |
| - Formas de pagamento habilitadas no sistema. |

| **Passos** |
| :-- |
| **DADO** que o usuário seleciona formas de pagamento |  
| **QUANDO** tenta registrar pagamento misto cuja soma não corresponde ao valor total da venda |  
| **ENTÃO** o sistema deve impedir a finalização e exibir mensagem de inconsistência. |

| **Critérios de Aceitação** |
| :-- |
| - Venda não deve ser finalizada. |
| - Nenhum pagamento deve ser registrado. |
| - Mensagem clara deve indicar que o total pago é diferente do total da venda. |

| **Evidência(s)** |
| :--: |
| [Vídeo]("") |

---

## **Caso de Teste Negativo CT_RF12_04_N: Falha no fechamento de caixa com totais incorretos**

| ID | Descrição |
| :-- | :-- |
| CT_RF12_04_N | Tentar fechar caixa com divergência nos totais por tipo de documento. |

| **Pré-condições** |
| :-- |
| - Venda(s) registradas com erro simulado ou divergências. |
| - Caixa aberto. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o módulo de fechamento de caixa |  
| **E** o sistema apresenta diferenças entre os valores por tipo de documento |  
| **QUANDO** tenta concluir o fechamento |  
| **ENTÃO** o sistema deve bloquear a operação e informar divergência. |

| **Critérios de Aceitação** |
| :-- |
| - Fechamento não deve ser concluído. |
| - Sistema deve alertar sobre documentos divergentes. |
| - Nenhum registro final deve ser gravado no banco. |

| **Evidência(s)** |
| :--: |
| [Vídeo]("") |

---

## **Caso de Teste Negativo CT_RF12_05_N: Falha na validação de integridade no banco de dados**

| ID | Descrição |
| :-- | :-- |
| CT_RF12_05_N | Detectar erros de integridade nos registros financeiros após o processo de venda. |

| **Pré-condições** |
| :-- |
| - Venda finalizada anteriormente. |
| - Banco de dados com registros inconsistentes ou manipulados. |

| **Passos** |
| :-- |
| **DADO** que o analista consulta as tabelas financeiras |  
| **QUANDO** identifica divergência entre valores de venda, pagamento e registros de caixa |  
| **ENTÃO** o sistema deve alertar o erro e impedir continuidade de operações dependentes. |

| **Critérios de Aceitação** |
| :-- |
| - Divergências devem ser identificadas corretamente. |
| - Sistema não deve permitir ações que dependem desses valores. |
| - Log ou alerta deve ser registrado. |

| **Evidência(s)** |
| :--: |
| [Vídeo]("") |

---
