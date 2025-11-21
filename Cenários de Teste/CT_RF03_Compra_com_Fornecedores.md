# **Cenário RF03: Compra com Fornecedores**

## **Caso de Teste CT_RF03_01: Cadastrar novo fornecedor**

| ID | Descrição |
| :-- | :-- |
| CT_RF03_01 | Cadastrar um novo fornecedor no sistema. |

| **Pré-condições** |
| :-- |
| - O sistema deve ter o módulo de compras ativo. |
| - O usuário deve possuir permissão para gerenciar fornecedores. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o módulo de fornecedores |
| **E** insere os dados de um novo fornecedor |
| **QUANDO** salvar o cadastro |
| **ENTÃO** o fornecedor deve ser cadastrado corretamente e o sistema deve exibir uma mensagem de sucesso. |

| **Critérios de aceitação** |
| :-- |
| - O fornecedor deve constar na lista de fornecedores cadastrados. |
| - Os dados devem ser gravados corretamente no banco de dados. |
| - Deve ser exibida uma mensagem confirmando o cadastro. |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/14OIiv51SZ8VSu75M0_wQJM5ru_4berEd/view?usp=drive_link) |

---

## **Caso de Teste CT_RF03_02: Gerar pedido de compra com 10 itens**

| ID | Descrição |
| :-- | :-- |
| CT_RF03_02 | Criar um pedido de compra contendo 10 itens. |

| **Pré-condições** |
| :-- |
| - O fornecedor deve estar previamente cadastrado no sistema. |
| - O módulo de pedidos de compra deve estar ativo. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o módulo de pedidos de compra |
| **E** seleciona um fornecedor cadastrado |
| **QUANDO** adicionar 10 itens ao pedido e salvar |
| **ENTÃO** o pedido deve ser criado com todos os 10 itens registrados corretamente. |

| **Critérios de aceitação** |
| :-- |
| - Os 10 itens devem aparecer no pedido de compra. |
| - Os valores, quantidades e descrições dos itens devem ser consistentes. |
| - O pedido deve ser salvo corretamente no banco de dados. |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/1ouqYEUeuPoePcJyk2lvWembvJUuK4415/view?usp=drive_link) |
| [Vídeo](https://drive.google.com/file/d/1pd5X7WSdvr6YKD_KHLRxh5xfBN1cvPnt/view?usp=drive_link) |

---

## **Caso de Teste CT_RF03_03: Simular parcelamento e pagamentos**

| ID | Descrição |
| :-- | :-- |
| CT_RF03_03 | Simular parcelamento em 5 vezes, pagar a primeira parcela integralmente e a segunda parcialmente. |

| **Pré-condições** |
| :-- |
| - Deve existir um pedido de compra gerando contas a pagar. |
| - O usuário deve ter permissão para registrar pagamentos. |
| - O módulo financeiro deve estar ativo. |

| **Passos** |
| :-- |
| **DADO** que o usuário parcelou o pedido em 5 parcelas |
| **E** possui as parcelas geradas no contas a pagar |
| **QUANDO** registrar o pagamento total da primeira parcela |
| **E** registrar um pagamento parcial da segunda parcela |
| **ENTÃO** o sistema deve atualizar corretamente os valores pagos e pendentes, mantendo o histórico de pagamentos. |

| **Critérios de aceitação** |
| :-- |
| - A primeira parcela deve constar como paga integralmente. |
| - A segunda parcela deve apresentar saldo pendente após pagamento parcial. |
| - O sistema deve registrar corretamente os valores no banco de dados. |
| - O histórico de pagamentos deve ser atualizado mantendo integridade e rastreabilidade. |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/1Zpq97sMWL68ZWlmvqsMO1rGB8NW8PY9z/view?usp=drive_link) |

---

## **Caso de Teste CT_RF03_04: Fechamento de caixa**

| ID | Descrição |
| :-- | :-- |
| CT_RF03_04 | Realizar fechamento de caixa após registros de pagamento. |

| **Pré-condições** |
| :-- |
| - Devem existir pagamentos registrados no período. |
| - O módulo de fechamento de caixa deve estar disponível. |
| - O usuário deve possuir permissão para fechar o caixa. |

| **Passos** |
| :-- |
| **DADO** que pagamentos foram registrados no sistema |
| **QUANDO** o usuário acessar o módulo de fechamento de caixa e executar o fechamento |
| **ENTÃO** o sistema deve concluir o fechamento e registrar os totais do período. |

| **Critérios de aceitação** |
| :-- |
| - O fechamento deve ser concluído sem erros. |
| - Os valores do caixa devem refletir corretamente os pagamentos efetuados. |
| - As informações devem ser gravadas no banco de dados com data, hora e usuário. |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/1yMBkOC0QMc0GntV6M1_68X4Jazq5KhKp/view?usp=drive_link) |
| [Foto](https://drive.google.com/file/d/1sKjIsLfYLo_buSPzpWCa4Hjs2vL7BBvk/view?usp=drive_link) |

---

## **Caso de Teste CT_RF03_05: Validação no Banco de Dados**

| ID | Descrição |
| :-- | :-- |
| CT_RF03_05 | Validar no banco de dados se o estoque foi atualizado apenas para itens recebidos. |

| **Pré-condições** |
| :-- |
| - Deve existir um pedido de compra com itens recebidos e não recebidos. |
| - O usuário deve possuir acesso de consulta ao banco de dados (perfil de analista). |

| **Passos** |
| :-- |
| **DADO** que o pedido de compra possui itens com status recebidos e pendentes |
| **QUANDO** o analista consultar diretamente o banco de dados |
| **ENTÃO** apenas os itens recebidos devem ter registrado movimentação de entrada no estoque. |

| **Critérios de aceitação** |
| :-- |
| - Nenhuma movimentação de estoque deve existir para itens não recebidos. |
| - Os itens recebidos devem apresentar movimentações consistentes com o pedido. |
| - Não deve haver registros duplicados ou inconsistentes. |

| **Evidência(s)** |
| :--: |
| [Foto](https://drive.google.com/file/d/1wtV6sE5YnbH91oBMVFp_K8KtGnS5ckRQ/view?usp=drive_link) |
| [Foto](https://drive.google.com/file/d/1GAlUps7whoUgTE813mTmeOmnjesKOzN-/view?usp=drive_link) |

---

# **Cenários Negativos – RF03: Compra com Fornecedores**

---

## **Caso de Teste CT_RF03_01_NEG: Falha ao cadastrar novo fornecedor**

| ID | Descrição |
| :-- | :-- |
| CT_RF03_01_NEG | Tentar cadastrar fornecedor com dados inválidos ou incompletos. |

| **Pré-condições** |
| :-- |
| - O módulo de compras deve estar ativo. |
| - O usuário deve possuir permissão para gerenciar fornecedores. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o módulo de fornecedores |
| **E** tenta inserir dados inválidos (ex.: CNPJ inválido, campos obrigatórios vazios) |
| **QUANDO** tentar salvar o cadastro |
| **ENTÃO** o sistema deve bloquear a operação e exibir mensagens de erro. |

| **Critérios de aceitação** |
| :-- |
| - O sistema não deve permitir salvar o fornecedor. |
| - Devem ser exibidas mensagens indicando os campos incorretos. |
| - Nenhum registro deve ser criado no banco de dados. |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/1yFvozV63m8yH5oT1iYPBRtOUMCFzIJqy/view?usp=drive_link) |

---

## **Caso de Teste CT_RF03_02_NEG: Falha ao gerar pedido de compra com 10 itens**

| ID | Descrição |
| :-- | :-- |
| CT_RF03_02_NEG | Tentar gerar um pedido com itens inválidos ou fornecedor inexistente. |

| **Pré-condições** |
| :-- |
| - Deve existir pelo menos um fornecedor cadastrado. |
| - O módulo de pedidos de compra deve estar ativo. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o módulo de pedidos de compra |
| **E** seleciona um fornecedor inexistente ou remove-o antes de salvar |
| **OU** insere itens com valores ou quantidades inválidas |
| **QUANDO** tentar salvar o pedido |
| **ENTÃO** o sistema deve impedir a criação do pedido e exibir mensagens de erro. |

| **Critérios de aceitação** |
| :-- |
| - O sistema deve impedir salvar itens inválidos. |
| - Nenhum pedido deve ser registrado no banco de dados. |
| - Mensagens claras devem indicar o motivo da falha. |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/1NOTNhJgOgHT-C-tTbFSAYA9-OkXlPqh6/view?usp=drive_link) |

---

## **Caso de Teste CT_RF03_03_NEG: Falha ao simular parcelamento e pagamentos**

| ID | Descrição |
| :-- | :-- |
| CT_RF03_03_NEG | Tentar registrar pagamento em parcela inexistente ou valores superiores ao permitido. |

| **Pré-condições** |
| :-- |
| - Deve existir um pedido parcelado no contas a pagar. |
| - O usuário deve ter permissão para registrar pagamentos. |

| **Passos** |
| :-- |
| **DADO** que o usuário tenta pagar uma parcela inexistente |
| **OU** tenta registrar pagamento maior que o valor da parcela |
| **QUANDO** tentar confirmar o pagamento |
| **ENTÃO** o sistema deve impedir o registro e exibir mensagens de erro. |

| **Critérios de aceitação** |
| :-- |
| - O sistema não deve aceitar valores inconsistentes. |
| - Nenhum pagamento inválido deve ser registrado. |
| - O histórico de pagamentos deve permanecer íntegro. |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/1TImG60Trbx9qvmXbDwIbB8SE4FLM6WZq/view?usp=drive_link) |

---

## **Caso de Teste CT_RF03_04_NEG: Falha no fechamento de caixa**

| ID | Descrição |
| :-- | :-- |
| CT_RF03_04_NEG | Tentar realizar fechamento de caixa com pendências ou dados inconsistentes. |

| **Pré-condições** |
| :-- |
| - Deve haver pagamentos no período. |
| - O módulo de fechamento de caixa deve estar disponível. |

| **Passos** |
| :-- |
| **DADO** que existem inconsistências nos registros de pagamentos (ex.: valores negativos ou duplicados) |
| **OU** o usuário não tem permissão para fechar o caixa |
| **QUANDO** tentar realizar o fechamento |
| **ENTÃO** o sistema deve impedir o fechamento e exibir mensagens de erro. |

| **Critérios de aceitação** |
| :-- |
| - O fechamento não deve ser concluído. |
| - Deve ser exibida uma mensagem indicando a inconsistência ou falta de permissão. |
| - Nenhum dado incorreto deve ser gravado no banco. |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/1ArhqY3J5M45JtUG4SRovaE2aax4QKOms/view?usp=drive_link) |

---
