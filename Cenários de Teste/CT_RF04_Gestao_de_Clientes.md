# **Cenário RF04: Gestão de Clientes**

## **Caso de Teste CT_RF04_01: Cadastrar 6 clientes (PJ e PF)**

| ID | Descrição |
| :-- | :-- |
| CT_RF04_01 | Cadastrar 6 clientes, sendo 3 pessoas jurídicas e 3 pessoas físicas. |

| **Pré-condições** |
| :-- |
| - O sistema deve ter o módulo de clientes ativo. |
| - O usuário deve possuir permissão para cadastrar clientes. |
| - O cadastro de clientes PJ e PF deve estar disponível. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o módulo de clientes |
| **E** preenche os dados para cadastrar 3 clientes PJ e 3 PF |
| **QUANDO** salvar os cadastros |
| **ENTÃO** os 6 clientes devem ser cadastrados corretamente no sistema. |

| **Critérios de aceitação** |
| :-- |
| - Os 6 clientes devem constar na lista de clientes. |
| - Os dados devem ser armazenados corretamente no banco de dados. |
| - O sistema deve exibir mensagem de sucesso após cada cadastro. |

| **Evidência(s)** |
| :--: |
| [Vídeo]("") |

---

## **Caso de Teste CT_RF04_02: Habilitar limite de crédito para 2 clientes**

| ID | Descrição |
| :-- | :-- |
| CT_RF04_02 | Configurar limite de crédito para 2 clientes cadastrados. |

| **Pré-condições** |
| :-- |
| - Os clientes devem estar previamente cadastrados. |
| - O usuário deve possuir permissão para editar informações financeiras dos clientes. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o cadastro de clientes |
| **E** seleciona 2 clientes |
| **QUANDO** definir e salvar o limite de crédito para cada um |
| **ENTÃO** o limite deve ser habilitado e registrado corretamente. |

| **Critérios de aceitação** |
| :-- |
| - O limite de crédito deve ser exibido no cadastro do cliente. |
| - As informações devem ser gravadas corretamente no banco de dados. |

| **Evidência(s)** |
| :--: |
| [Vídeo]("") |

---

## **Caso de Teste CT_RF04_03: Acrescentar dependentes para 2 clientes**

| ID | Descrição |
| :-- | :-- |
| CT_RF04_03 | Vincular dependentes a 2 clientes. |

| **Pré-condições** |
| :-- |
| - Os clientes devem estar previamente cadastrados. |
| - O módulo de dependentes deve estar ativo. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o cadastro de clientes |
| **E** seleciona 2 clientes |
| **QUANDO** cadastrar e salvar os dependentes vinculados |
| **ENTÃO** os dependentes devem ser associados corretamente aos respectivos clientes. |

| **Critérios de aceitação** |
| :-- |
| - Cada cliente deve exibir seus dependentes na listagem. |
| - O banco de dados deve refletir corretamente os vínculos entre clientes e dependentes. |

| **Evidência(s)** |
| :--: |
| [Vídeo]("") |

---

## **Caso de Teste CT_RF04_04: Registrar compras para os 6 clientes**

| ID | Descrição |
| :-- | :-- |
| CT_RF04_04 | Registrar compras para os 6 clientes, incluindo compras em nome dos dependentes. |

| **Pré-condições** |
| :-- |
| - Os clientes e dependentes devem estar cadastrados. |
| - O módulo de compras deve estar ativo. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o módulo de compras |
| **QUANDO** registrar compras para os 4 clientes sem dependentes |
| **E** registrar compras para os 2 clientes com dependentes (incluindo compras dos dependentes) |
| **ENTÃO** todas as compras devem ser registradas corretamente. |

| **Critérios de aceitação** |
| :-- |
| - As compras devem aparecer no histórico do cliente ou dependente correspondente. |
| - Todas as transações devem ser registradas corretamente no banco de dados. |

| **Evidência(s)** |
| :--: |
| [Vídeo]("") |

---

## **Caso de Teste CT_RF04_05: Realizar compra dentro e fora do limite de crédito**

| ID | Descrição |
| :-- | :-- |
| CT_RF04_05 | Validar compras dentro e fora do limite de crédito. |

| **Pré-condições** |
| :-- |
| - Os 2 clientes devem possuir limite de crédito configurado. |
| - O módulo de compras deve estar ativo. |

| **Passos** |
| :-- |
| **DADO** que o usuário registra uma compra para o Cliente 1 |
| **QUANDO** o valor estiver dentro do limite |
| **ENTÃO** a compra deve ser aprovada. |
| **DADO** que o usuário registra uma compra para o Cliente 2 |
| **QUANDO** o valor ultrapassar o limite |
| **ENTÃO** a compra deve ser bloqueada ou sinalizada pelo sistema. |

| **Critérios de aceitação** |
| :-- |
| - A compra dentro do limite deve ser registrada com sucesso. |
| - A compra que ultrapassa o limite deve ser impedida ou alertada ao usuário. |
| - O comportamento deve ser consistente com as regras de negócio. |

| **Evidência(s)** |
| :--: |
| [Vídeo]("") |

---

## **Caso de Teste CT_RF04_06: Atualizar limite de crédito**

| ID | Descrição |
| :-- | :-- |
| CT_RF04_06 | Atualizar o limite de crédito de um cliente. |

| **Pré-condições** |
| :-- |
| - O cliente deve possuir limite de crédito ativo. |
| - O usuário deve possuir permissão para alteração de limite. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o cadastro do cliente |
| **E** altera o valor do limite de crédito |
| **QUANDO** salvar a alteração |
| **ENTÃO** o novo limite deve ser atualizado corretamente. |

| **Critérios de aceitação** |
| :-- |
| - O novo limite deve aparecer atualizado no cadastro do cliente. |
| - O banco de dados deve refletir a nova configuração. |

| **Evidência(s)** |
| :--: |
| [Vídeo]("") |

---

## **Caso de Teste CT_RF04_07: Gerar relatório de contas a receber**

| ID | Descrição |
| :-- | :-- |
| CT_RF04_07 | Gerar relatório com os valores a receber dos clientes. |

| **Pré-condições** |
| :-- |
| - Compras devem ter sido registradas anteriormente. |
| - O módulo de relatórios deve estar ativo. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o módulo de relatórios |
| **E** seleciona o relatório de contas a receber |
| **QUANDO** gerar o relatório |
| **ENTÃO** o sistema deve apresentar os valores corretos de contas a receber. |

| **Critérios de aceitação** |
| :-- |
| - O relatório deve apresentar os valores pendentes por cliente. |
| - Os dados devem estar consistentes com o banco de dados. |

| **Evidência(s)** |
| :--: |
| [Vídeo]("") |

---

## **Caso de Teste CT_RF04_08: Validação no Banco de Dados**

| ID | Descrição |
| :-- | :-- |
| CT_RF04_08 | Verificar histórico de compras e bloqueios por crédito diretamente no banco de dados. |

| **Pré-condições** |
| :-- |
| - Compras e bloqueios devem ter sido registrados previamente. |
| - O usuário deve ter permissão de consulta ao banco (perfil analista). |

| **Passos** |
| :-- |
| **DADO** que existem compras e tentativas de compra bloqueadas |
| **QUANDO** o analista consultar o banco de dados |
| **ENTÃO** o histórico deve refletir corretamente compras aprovadas, compras em nome de dependentes e tentativas bloqueadas. |

| **Critérios de aceitação** |
| :-- |
| - Todas as compras devem estar registradas corretamente. |
| - Os bloqueios devem estar gravados conforme as regras de crédito. |
| - Não devem existir inconsistências ou registros duplicados. |

| **Evidência(s)** |
| :--: |
| [Vídeo]("") |

---

# **Caso de Teste Negativo**

## **Caso de Teste CT_RF04_NEG_01: Falha ao cadastrar clientes (campos obrigatórios ausentes)**

| ID | Descrição |
| :-- | :-- |
| CT_RF04_NEG_01 | Tentar cadastrar clientes sem preencher campos obrigatórios. |

| **Pré-condições** |
| :-- |
| - Módulo de clientes ativo. |
| - Usuário com permissão para cadastrar clientes. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o módulo de clientes |
| **E** tenta cadastrar um cliente sem preencher campos obrigatórios (CPF/CNPJ, nome, endereço, etc.) |
| **QUANDO** tentar salvar o cadastro |
| **ENTÃO** o sistema deve impedir o salvamento e exibir mensagens de validação. |

| **Critérios de aceitação** |
| :-- |
| - O cliente **não** deve ser salvo. |
| - Mensagens de erro devem ser exibidas informando os campos faltantes. |
| - Banco de dados não deve registrar nenhum cadastro incompleto. |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/1hyuAuvOwG1dmciZPC0LtICbgHDnJSRap/view?usp=drive_link) |

---

## **Caso de Teste CT_RF04_NEG_02: Falha ao habilitar limite de crédito (valor inválido)**

| ID | Descrição |
| :-- | :-- |
| CT_RF04_NEG_02 | Tentar configurar limite de crédito com valor inválido. |

| **Pré-condições** |
| :-- |
| - Cliente cadastrado. |
| - Usuário com permissão financeira. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o cadastro de um cliente |
| **QUANDO** informar um limite de crédito com valor negativo ou nulo |
| **ENTÃO** o sistema deve impedir a operação e exibir aviso de valor inválido. |

| **Critérios de aceitação** |
| :-- |
| - O limite não deve ser atualizado. |
| - O sistema deve exibir mensagem clara de erro. |
| - Banco de dados não deve registrar valores inválidos. |

| **Evidência(s)** |
| :--: |
| [Vídeo]("") |

---

## **Caso de Teste CT_RF04_NEG_03: Falha ao cadastrar dependentes (cliente inexistente)**

| ID | Descrição |
| :-- | :-- |
| CT_RF04_NEG_03 | Tentar cadastrar dependente para cliente inexistente ou removido. |

| **Pré-condições** |
| :-- |
| - Cadastro de dependentes ativo. |

| **Passos** |
| :-- |
| **DADO** que o usuário tenta cadastrar um dependente |
| **QUANDO** selecionar um cliente que não existe ou foi excluído |
| **ENTÃO** o sistema deve bloquear a operação. |

| **Critérios de aceitação** |
| :-- |
| - O dependente não deve ser criado. |
| - O sistema deve exibir mensagem indicando que o cliente é inválido. |
| - Nenhuma relação deve ser gravada no banco de dados. |

| **Evidência(s)** |
| :--: |
| [Vídeo]("") |

---

## **Caso de Teste CT_RF04_NEG_04: Falha ao registrar compras (cliente inativo ou bloqueado)**

| ID | Descrição |
| :-- | :-- |
| CT_RF04_NEG_04 | Tentar registrar compras para cliente inativo ou bloqueado. |

| **Pré-condições** |
| :-- |
| - Cliente deve estar cadastrado, porém inativo ou bloqueado para compras. |

| **Passos** |
| :-- |
| **DADO** que o usuário tenta registrar uma compra |
| **QUANDO** o cliente estiver inativo ou bloqueado |
| **ENTÃO** o sistema deve impedir o registro. |

| **Critérios de aceitação** |
| :-- |
| - A compra não deve ser registrada. |
| - Mensagem de bloqueio deve ser exibida para o usuário. |
| - Banco de dados não deve registrar compras para clientes bloqueados. |

| **Evidência(s)** |
| :--: |
| [Vídeo]("") |

---

## **Caso de Teste CT_RF04_NEG_05: Tentativa de compra muito acima do limite (erro crítico)**

| ID | Descrição |
| :-- | :-- |
| CT_RF04_NEG_05 | Registrar compra com valor extremamente acima do limite, simulando fraude. |

| **Pré-condições** |
| :-- |
| - Cliente com limite de crédito configurado. |

| **Passos** |
| :-- |
| **DADO** que o usuário registra uma compra |
| **QUANDO** o valor for muito acima do limite (ex.: limite 1.000 → compra 50.000) |
| **ENTÃO** o sistema deve bloquear a compra e gerar alerta. |

| **Critérios de aceitação** |
| :-- |
| - A compra deve ser negada imediatamente. |
| - Logs de auditoria devem registrar a tentativa suspeita. |
| - Nenhum registro deve ser salvo no histórico de compras. |

| **Evidência(s)** |
| :--: |
| [Vídeo]("") |

---

## **Caso de Teste CT_RF04_NEG_06: Falha ao atualizar limite de crédito (usuário sem permissão)**

| ID | Descrição |
| :-- | :-- |
| CT_RF04_NEG_06 | Usuário sem permissão tenta atualizar o limite de crédito. |

| **Pré-condições** |
| :-- |
| - Cliente com limite existente. |
| - Usuário sem permissão financeira. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o cadastro do cliente |
| **QUANDO** tentar alterar o limite |
| **ENTÃO** o sistema deve impedir a alteração e exibir mensagem de permissão negada. |

| **Critérios de aceitação** |
| :-- |
| - Nada deve ser alterado no cadastro. |
| - Mensagem de permissão negada deve ser exibida. |
| - Banco de dados permanece inalterado. |

| **Evidência(s)** |
| :--: |
| [Vídeo]("") |

---

## **Caso de Teste CT_RF04_NEG_07: Falha ao gerar relatório de contas a receber (filtros inválidos)**

| ID | Descrição |
| :-- | :-- |
| CT_RF04_NEG_07 | Tentar gerar relatório com filtros inválidos ou período inexistente. |

| **Pré-condições** |
| :-- |
| - Registro de compras existente. |
| - Módulo de relatórios ativo. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o módulo de relatórios |
| **QUANDO** selecionar filtros inválidos (datas invertidas, período inexistente, etc.) |
| **ENTÃO** o sistema deve impedir a geração. |

| **Critérios de aceitação** |
| :-- |
| - O relatório não deve ser gerado. |
| - Mensagem de erro deve aparecer. |
| - Nenhum dado incorreto deve ser exibido. |

| **Evidência(s)** |
| :--: |
| [Vídeo]("") |

---

## **Caso de Teste CT_RF04_NEG_08: Inconsistências no histórico no banco de dados**

| ID | Descrição |
| :-- | :-- |
| CT_RF04_NEG_08 | Validar que o sistema não permita dados inconsistentes ou duplicados no histórico de compras. |

| **Pré-condições** |
| :-- |
| - Tentativas de compras duplicadas ou inconsistentes devem existir no log do sistema. |

| **Passos** |
| :-- |
| **DADO** que o analista consulta o banco |
| **QUANDO** identificar possíveis duplicidades geradas por falhas |
| **ENTÃO** deve ser possível evidenciar que o sistema preveniu gravações incorretas. |

| **Critérios de aceitação** |
| :-- |
| - Não devem existir compras duplicadas. |
| - Não devem existir registros de bloqueio sem justificativa. |
| - Integridade referencial deve ser mantida. |

| **Evidência(s)** |
| :--: |
| [Vídeo]("") |
