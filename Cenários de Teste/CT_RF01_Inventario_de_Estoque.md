# **Cenário RF01: Inventário de Estoque**

## **Caso de Teste CT_RF01_01: Importação de produtos via XML**

| ID | Descrição |
| :-- | :-- |
| CT_RF01_01 | Importar produtos fictícios via arquivo XML e validar o cadastro no sistema. |

| **Pré-condições** |
| :-- |
| - O sistema deve ter o módulo de inventário ativo. |
| - O arquivo XML com produtos fictícios deve estar disponível. |
| - O usuário deve possuir permissão para realizar importações. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o módulo de inventário do sistema |
| **E** seleciona a opção de importação de produtos |
| **QUANDO** importar o arquivo XML com 10 produtos fictícios |
| **ENTÃO** os produtos devem ser cadastrados corretamente e o sistema exibe uma mensagem de sucesso. |

| **Critérios de aceitação** |
| :-- |
| - Os produtos devem ser exibidos corretamente no sistema após a importação. |
| - Uma mensagem de sucesso deve confirmar o término do processo. |
| - Os dados devem ser gravados corretamente no banco de dados. |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/1wFhWy344peuCfkgM-5b3duIxO48enreC/view?usp=drive_link) |

---

## **Caso de Teste CT_RF01_02: Importação de produtos via XML inválido**

| ID | Descrição |
| :-- | :-- |
| CT_RF01_02 | Tentar importar um arquivo XML inválido ou corrompido e verificar se o sistema trata o erro corretamente, sem comprometer o banco de dados. |

| **Pré-condições** |
| :-- |
| - O sistema deve ter o módulo de inventário ativo. |
| - O arquivo XML a ser importado deve conter estrutura incorreta, campos obrigatórios ausentes ou estar corrompido. |
| - O usuário deve possuir permissão para realizar importações. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o módulo de inventário do sistema |
| **E** seleciona a opção de importação de produtos |
| **QUANDO** tentar importar um arquivo XML inválido (estrutura incorreta ou dados inconsistentes) |
| **ENTÃO** o sistema deve rejeitar o arquivo, exibir uma mensagem de erro clara e não gravar nenhuma informação no banco de dados. |

| **Critérios de aceitação** |
| :-- |
| - O sistema deve identificar e bloquear a importação do arquivo XML inválido. |
| - Nenhum produto deve ser cadastrado ou alterado no banco de dados. |
| - Uma mensagem de erro amigável deve informar o motivo da falha (ex.: “Arquivo XML inválido ou corrompido”). |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/15aa9cKuOg-NuKhPrGGPuQCmBWHlaRbje/view?usp=drive_link) |

---

## **Caso de Teste CT_RF01_03: Contagem física simulada**

| ID | Descrição |
| :-- | :-- |
| CT_RF01_03 | Realizar contagem física simulada e registrar as quantidades no sistema. |

| **Pré-condições** |
| :-- |
| - Os produtos devem estar previamente cadastrados no sistema. |
| - O módulo de inventário deve estar acessível. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o módulo de inventário |
| **E** seleciona os produtos cadastrados |
| **QUANDO** inserir as quantidades simuladas de contagem física e salvar |
| **ENTÃO** o sistema deve registrar corretamente as contagens. |

| **Critérios de aceitação** |
| :-- |
| - As contagens devem ser registradas sem erro no sistema. |
| - Os registros devem ser consistentes no banco de dados. |
| - O usuário deve possuir permissão para realizar contagens. |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/1XA7U3ognJ4O-oNXj0uhbqFVemDoYsNUd/view?usp=drive_link) |

---

## **Caso de Teste CT_RF01_04: Contagem física simulada com dados inconsistentes**

| ID | Descrição |
| :-- | :-- |
| CT_RF01_04 | Tentar realizar a contagem física com valores inválidos ou campos em branco e verificar se o sistema bloqueia o registro incorreto. |

| **Pré-condições** |
| :-- |
| - Os produtos devem estar previamente cadastrados no sistema. |
| - O módulo de inventário deve estar acessível. |
| - O usuário deve possuir permissão para realizar contagens. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o módulo de inventário |
| **E** seleciona os produtos cadastrados |
| **QUANDO** inserir valores negativos, campos vazios ou caracteres não numéricos nas quantidades e tentar salvar |
| **ENTÃO** o sistema deve rejeitar o registro da contagem e exibir uma mensagem de erro explicando a inconsistência. |

| **Critérios de aceitação** |
| :-- |
| - O sistema não deve permitir salvar contagens com valores inválidos. |
| - Nenhum dado incorreto deve ser gravado no banco de dados. |
| - Uma mensagem de erro deve informar claramente o motivo da rejeição (ex.: “Quantidade inválida ou campo obrigatório ausente”). |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/1ySbZ2tY9EktjFsmPr4C6Qt6U1TxkkmlH/view?usp=drive_link) |

---

## **Caso de Teste CT_RF01_05: Lançamento do inventário e geração de relatório de ajustes**

| ID | Descrição |
| :-- | :-- |
| CT_RF01_05 | Lançar o inventário no sistema e gerar o relatório de ajustes conforme contagem física. |

| **Pré-condições** |
| :-- |
| - O usuário deve possuir permissão para lançar inventários. |
| - A contagem física simulada deve ter sido concluída e salva. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o módulo de inventário |
| **E** seleciona o inventário com contagem concluída |
| **QUANDO** realizar o lançamento do inventário e gerar o relatório de ajustes |
| **ENTÃO** o sistema deve ajustar os saldos conforme a contagem e apresentar as diferenças entre saldo contabilizado e ajustado. |

| **Critérios de aceitação** |
| :-- |
| - O relatório de ajustes deve ser gerado corretamente. |
| - Os saldos contabilizado e ajustado devem estar consistentes no banco de dados. |
| - As diferenças devem estar corretamente refletidas no sistema. |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/1Awok59jo3gfCkZ8LFbnSNeTJp0qdS6W4/view?usp=drive_link) |

---

## **Caso de Teste CT_RF01_06: Lançamento do inventário sem contagem concluída**

| ID | Descrição |
| :-- | :-- |
| CT_RF01_06 | Tentar lançar o inventário sem que a contagem física tenha sido concluída e verificar o comportamento do sistema. |

| **Pré-condições** |
| :-- |
| - O usuário deve possuir permissão para lançar inventários. |
| - Deve existir um inventário cadastrado, porém com contagem física não finalizada. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o módulo de inventário |
| **E** seleciona um inventário cuja contagem ainda não foi concluída |
| **QUANDO** tentar realizar o lançamento e gerar o relatório de ajustes |
| **ENTÃO** o sistema deve impedir o lançamento, exibir mensagem de erro e não gerar o relatório. |

| **Critérios de aceitação** |
| :-- |
| - O sistema não deve permitir o lançamento de inventário com contagem pendente. |
| - Nenhum dado deve ser alterado no banco de dados. |
| - Uma mensagem clara deve informar o motivo da rejeição (ex.: “Não é possível lançar inventário sem contagem concluída”). |
| - O sistema deve manter a integridade dos dados existentes. |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/1WDRbBf871T0NiIn5HVYX3-Hz_dSF7K31/view?usp=drive_link) |

---

## **Caso de Teste CT_RF01_07: Exclusão de produto cadastrado**

| ID | Descrição |
| :-- | :-- |
| CT_RF01_07 | Excluir um produto cadastrado e validar se ele é removido corretamente do sistema e do banco de dados. |

| **Pré-condições** |
| :-- |
| - Deve existir ao menos um produto cadastrado no sistema. |
| - O usuário deve possuir permissão para exclusão. |
| - O produto não deve estar vinculado a inventário ativo. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o módulo de inventário |
| **E** visualiza a lista de produtos cadastrados |
| **QUANDO** aciona a opção “Excluir produto” para um item existente |
| **ENTÃO** o sistema deve remover o registro, exibir mensagem de confirmação e atualizar a lista de produtos. |

| **Critérios de aceitação** |
| :-- |
| - O produto é removido corretamente do banco de dados. |
| - Uma mensagem de sucesso é exibida confirmando a exclusão. |
| - O sistema impede exclusão de produtos vinculados a inventários ativos, exibindo mensagem explicativa. |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/1dAYEUtW7Dz9VOxucKaGdKb-Rs72E0Oii/view?usp=drive_link) |
| [Vídeo](https://drive.google.com/file/d/1cvoZ7S2zUmI5tZNiVSEjtHzBGTZY27z2/view?usp=drive_link) |

---

## **Caso de Teste CT_RF01_08: Consulta e filtragem de inventário**

| ID | Descrição |
| :-- | :-- |
| CT_RF01_08 | Consultar produtos e inventários aplicando filtros e visualizar detalhes das contagens. |

| **Pré-condições** |
| :-- |
| - Devem existir produtos e inventários cadastrados. |
| - O usuário deve possuir permissão de consulta. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o módulo de inventário |
| **E** utiliza os filtros disponíveis (por descrição, código, data ou status) |
| **QUANDO** aplicar um filtro específico e selecionar um inventário |
| **ENTÃO** o sistema deve listar apenas os registros correspondentes e permitir visualização detalhada. |

| **Critérios de aceitação** |
| :-- |
| - O sistema deve exibir corretamente os resultados filtrados. |
| - A visualização de detalhes deve exibir as informações completas (saldo contabilizado, contagem física, diferenças). |
| - O tempo de resposta deve ser adequado e os dados devem estar consistentes com o banco de dados. |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/1GW0_NTKbw-aBwaCEb9WZjNsBK2aQgu1J/view?usp=drive_link) |

---
