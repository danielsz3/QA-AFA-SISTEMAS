# **Cenário RF06: Fechamento de Caixa**

## **Caso de Teste CT_RF06_01: Simular operações em 3 caixas simultâneas**

| ID | Descrição |
| :-- | :-- |
| CT_RF06_01 | Realizar operações simultâneas em 3 caixas diferentes e validar o registro correto em cada um. |

| **Pré-condições** |
| :-- |
| - Sistema com **módulo de caixa ativo**. |
| - **3 caixas** configurados e operacionais. |
| - O usuário deve possuir permissão para realizar operações de venda. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o módulo de caixa |
| **QUANDO** abrir **3 sessões de caixa simultâneas** e realizar vendas e movimentações em cada caixa |
| **ENTÃO** as operações devem ser registradas corretamente em cada caixa. |

| **Critérios de aceitação** |
| :-- |
| - As operações (vendas, sangrias/suprimentos) devem ser registradas sem conflitos entre os caixas. |
| - O saldo de cada caixa deve refletir as movimentações realizadas. |
| - Os dados devem ser gravados corretamente no banco de dados. |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/1Rba9LtcVJhEWZUmQLbOlwbQiXN4vA3VM/view?usp=drive_link) |

---

## **Caso de Teste CT_RF06_02: Gerar vendas com diferentes tipos de documentos**

| ID | Descrição |
| :-- | :-- |
| CT_RF06_02 | Registrar vendas utilizando diferentes tipos de documentos fiscais e validar o registro. |

| **Pré-condições** |
| :-- |
| - O módulo de caixa deve estar ativo e operacional. |
| - Devem haver **diferentes tipos de documentos fiscais** configurados no sistema (ex: NF, Cupom). |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o módulo de caixa |
| **E** realiza vendas em cada caixa |
| **QUANDO** registrar as vendas com **tipos variados de documentos fiscais** e confirmar a operação |
| **ENTÃO** as vendas devem ser registradas com os tipos de documentos corretos e o sistema deve confirmar o registro. |

| **Critérios de aceitação** |
| :-- |
| - As vendas devem estar associadas ao tipo de documento fiscal selecionado. |
| - A contabilidade da venda deve ser consistente, independentemente do tipo de documento. |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/1e-4sZOta-VzJ3mOnAgdObuf2aAIyfGn0/view?usp=drive_link) |

---

## **Caso de Teste CT_RF06_03: Realizar retiradas de valores**

| ID | Descrição |
| :-- | :-- |
| CT_RF06_03 | Efetuar retiradas (sangrias) de valores dos caixas e verificar o registro correto da movimentação. |

| **Pré-condições** |
| :-- |
| - O caixa deve ter saldo positivo. |
| - O usuário deve possuir permissão para realizar retiradas. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o módulo de caixa |
| **E** realiza uma retirada de valor (sangria) em cada caixa |
| **QUANDO** registrar o **motivo** e o **valor da retirada** e salvar |
| **ENTÃO** as retiradas devem ser registradas corretamente, e o saldo do caixa deve ser ajustado. |

| **Critérios de aceitação** |
| :-- |
| - O valor da retirada deve ser descontado corretamente do saldo do caixa. |
| - O **motivo** e o **valor** da retirada devem ser registrados no histórico de movimentações. |
| - O registro deve ser consistente no banco de dados. |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/1oxuCH2pq-pj4Wd8d1eb6tPrEr_iaYVPl/view?usp=drive_link) |

---

## **Caso de Teste CT_RF06_04: Fechar o caixa e conferir tipos de documentos**

| ID | Descrição |
| :-- | :-- |
| CT_RF06_04 | Fechar cada caixa e validar os totais e tipos de documentos registrados no fechamento. |

| **Pré-condições** |
| :-- |
| - Operações de venda e retiradas devem ter sido realizadas nos caixas. |
| - O usuário deve possuir permissão para realizar o fechamento de caixa. |

| **Passos** |
| :-- |
| **DADO** que os caixas possuem movimentação |
| **E** o usuário acessa o módulo de fechamento de caixa |
| **QUANDO** fechar cada caixa e conferir os tipos de documentos registrados |
| **ENTÃO** o fechamento deve ser realizado com sucesso, e os tipos de documentos conferidos devem ser corretos. |

| **Critérios de aceitação** |
| :-- |
| - O sistema deve calcular corretamente o saldo final de cada caixa. |
| - O resumo do fechamento deve listar e totalizar corretamente todos os tipos de documentos (NF, Cupom, etc.). |
| - O registro do fechamento deve ser gravado com sucesso. |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/15ZYfJfhwk1-g-4Kr7jhXcm8W8NmBkaM8/view?usp=drive_link) |

---

## **Caso de Teste CT_RF06_05: Conciliar totais com relatório de vendas**

| ID | Descrição |
| :-- | :-- |
| CT_RF06_05 | Conciliar os totais registrados no fechamento de caixa com os totais apresentados no relatório de vendas. |

| **Pré-condições** |
| :-- |
| - O fechamento de caixa deve ter sido realizado com sucesso para o período. |
| - O usuário deve possuir permissão para gerar o relatório de vendas. |

| **Passos** |
| :-- |
| **DADO** que o fechamento de caixa foi concluído |
| **E** o usuário gera o relatório de vendas para o mesmo período |
| **QUANDO** comparar os **totais do relatório** com os **totais do fechamento de caixa** |
| **ENTÃO** os totais devem ser conciliados e consistentes entre os dois módulos. |

| **Critérios de aceitação** |
| :-- |
| - O total de vendas no relatório deve ser **igual** ao total de vendas no fechamento. |
| - Os valores de retiradas, depósitos e vendas por meio de pagamento devem ser idênticos em ambos. |
| - Os dados devem ser consistentes no banco de dados. |

| **Evidência(s)** |
| :--: |
| [Vídeo]("") |

---

## **Caso de Teste CT_RF06_06: Validação de integridade no banco de dados**

| ID | Descrição |
| :-- | :-- |
| CT_RF06_06 | Verificar a integridade e o equilíbrio entre os movimentos financeiros e o saldo contábil no banco de dados após o fechamento. |

| **Pré-condições** |
| :-- |
| - O ciclo de fechamento de caixa deve ter sido concluído. |
| - O analista deve possuir acesso direto ao banco de dados. |

| **Passos** |
| :-- |
| **DADO** que o fechamento de caixa foi concluído e todos os movimentos registrados |
| **QUANDO** o analista consultar as tabelas financeiras e contábeis diretamente no banco de dados |
| **ENTÃO** o saldo contábil deve estar em equilíbrio com a soma dos movimentos financeiros do caixa fechado (vendas - retiradas + suprimentos). |

| **Critérios de aceitação** |
| :-- |
| - O saldo final registrado na tabela de caixa deve ser coerente com o total de movimentos registrados. |
| - O **equilíbrio** entre movimentos financeiros e saldo contábil deve ser comprovado. |
| - As transações devem ser imutáveis após o fechamento. |

| **Evidência(s)** |
| :--: |
| [Vídeo]("") |

---

# **Cenário RF06 — Versões Negativas (Fechamento de Caixa)**

## **Caso de Teste Negativo CT_RF06_01_N: Falha ao operar 3 caixas simultâneos sem permissão**

| ID | Descrição |
| :-- | :-- |
| CT_RF06_01_N | Tentar realizar operações simultâneas em 3 caixas sem permissão adequada. |

| **Pré-condições** |
| - Sistema com módulo de caixa ativo. |
| - 3 caixas configurados e operacionais. |
| - **Usuário sem permissão** para operar vendas em múltiplos caixas. |

| **Passos** |
| - **DADO** que o usuário acessa o módulo de caixa sem permissão necessária  |
| - **QUANDO** tentar abrir **3 sessões de caixa simultâneas** e realizar vendas  |
| - **ENTÃO** o sistema deve **bloquear a operação** e exibir mensagem de permissão negada. |

| **Critérios de aceitação** |
| - O sistema deve impedir abertura de múltiplos caixas sem permissão. |
| - Nenhuma venda deve ser registrada. |
| - Uma mensagem de erro clara deve ser exibida ao usuário. |

| **Evidência(s)** |
| [Vídeo]("") |

---

## **Caso de Teste Negativo CT_RF06_02_N: Falha ao registrar venda sem documento fiscal válido**

| ID | Descrição |
| :-- | :-- |
| CT_RF06_02_N | Tentar registrar vendas com documento fiscal inválido ou não configurado. |

| **Pré-condições** |
| - Módulo de caixa ativo. |
| - **Nenhum tipo de documento fiscal válido selecionado** ou tipo inexistente. |

| **Passos** |
| - **DADO** que o usuário acessa o módulo de caixa  |
| - **QUANDO** tentar registrar uma venda com um **tipo de documento fiscal inválido**  |
| - **ENTÃO** o sistema deve impedir a operação e exibir mensagem de erro. |

| **Critérios de aceitação** |
| - A venda não deve ser concluída. |
| - O sistema deve validar obrigatoriamente o tipo de documento. |
| - Mensagem clara de erro deve ser exibida. |

| **Evidência(s)** |
| [Vídeo]("") |

---

## **Caso de Teste Negativo CT_RF06_03_N: Falha ao realizar retirada com saldo insuficiente**

| ID | Descrição |
| :-- | :-- |
| CT_RF06_03_N | Tentar efetuar retirada (sangria) maior que o saldo disponível no caixa. |

| **Pré-condições** |
| - Caixa com saldo baixo ou zerado. |
| - Usuário com permissão para retiradas. |

| **Passos** |
| - **DADO** que o caixa possui saldo menor que o valor desejado para retirada  |
| - **QUANDO** o usuário tentar registrar a retirada com valor superior  |
| - **ENTÃO** o sistema deve bloquear a operação e não registrar a movimentação. |

| **Critérios de aceitação** |
| - A retirada não deve ser registrada. |
| - O saldo do caixa deve permanecer inalterado. |
| - O sistema deve exibir mensagem notificando saldo insuficiente. |

| **Evidência(s)** |
| [Vídeo]("") |

---

## **Caso de Teste Negativo CT_RF06_04_N: Falha no fechamento de caixa com documentos inconsistentes**

| ID | Descrição |
| :-- | :-- |
| CT_RF06_04_N | Tentar fechar caixa com documentos fiscais faltando ou inconsistentes. |

| **Pré-condições** |
| - Caixas com movimentação inconsistente. |
| - Documentos fiscais ausentes ou divergentes. |

| **Passos** |
| - **DADO** que existem vendas e retiradas registradas  |
| - **E** existem divergências nos tipos de documentos  |
| - **QUANDO** o usuário tentar realizar o fechamento  |
| - **ENTÃO** o sistema deve impedir o fechamento e informar a inconsistência. |

| **Critérios de aceitação** |
| - Fechamento não deve ser concluído. |
| - Sistema deve relatar documentos faltando ou inválidos. |
| - Nenhum registro de fechamento deve ser gravado. |

| **Evidência(s)** |
| [Vídeo]("") |

---

## **Caso de Teste Negativo CT_RF06_05_N: Totais divergentes no relatório e fechamento**

| ID | Descrição |
| :-- | :-- |
| CT_RF06_05_N | Comparar relatório de vendas e fechamento com totais divergentes. |

| **Pré-condições** |
| - Fechamento de caixa concluído. |
| - Relatório de vendas gerado com divergência proposital (erro de sistema ou manipulação). |

| **Passos** |
|- **DADO** que o usuário possui fechamento finalizado  |
|- **E** gera o relatório de vendas  |
|- **QUANDO** comparar os totais  |
| - **ENTÃO** devem ser detectadas divergências e o sistema deve alertar o usuário. |

| **Critérios de aceitação** |
| - Divergências devem ser apontadas claramente. |
| - O sistema não deve considerar a conciliação válida. |
| - O usuário deve ser informado sobre os valores conflitantes. |

| **Evidência(s)** |
| [Vídeo]("") |

---

## **Caso de Teste Negativo CT_RF06_06_N: Falha na integridade entre saldo contábil e movimentos**

| ID | Descrição |
| :-- | :-- |
| CT_RF06_06_N | Detectar inconsistência entre movimentos financeiros e saldo contábil no banco. |

| **Pré-condições** |
| - Fechamento de caixa concluído. |
| - Banco de dados com registros inconsistentes ou corrompidos. |

| **Passos** |
| - **DADO** que o analista acessa o banco após fechamento  |
| - **QUANDO** consultar as tabelas financeiras e contábeis  |
| - **ENTÃO** deve encontrar divergências entre valores de movimentos e saldo final. |

| **Critérios de aceitação** |
| - Divergência deve ser detectada. |
|- O sistema deve impedir atualizações posteriores ao fechamento. |
| - Deve ser registrado um log ou alerta indicando inconsistência. |

| **Evidência(s)** |
| [Vídeo]("") |

---
