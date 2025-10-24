# **Cenário RF01: Inventário de Estoque**

## **Caso de Teste CT_RF01_01: Importação de produtos via XML**

| ID | Descrição |
| :-- | :-- |
| CT_RF01_01 | Importar produtos fictícios via arquivo XML e validar o cadastro no sistema. |

| **Pré-condições** |
| :-- |
| - O sistema deve ter o módulo de inventário ativo. <br> - O arquivo XML com produtos fictícios deve estar disponível. <br> - O usuário deve possuir permissão para realizar importações. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o módulo de inventário do sistema <br> **E** seleciona a opção de importação de produtos <br> **QUANDO** importar o arquivo XML com 10 produtos fictícios <br> **ENTÃO** os produtos devem ser cadastrados corretamente e o sistema exibe uma mensagem de sucesso. |

| **Critérios de aceitação** |
| :-- |
| - Os produtos devem ser exibidos corretamente no sistema após a importação. <br> - Uma mensagem de sucesso deve confirmar o término do processo. <br> - Os dados devem ser gravados corretamente no banco de dados. |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://drive.google.com/file/d/1wFhWy344peuCfkgM-5b3duIxO48enreC/view?usp=drive_link) |

---

## **Caso de Teste CT_RF01_02: Contagem física simulada**

| ID | Descrição |
| :-- | :-- |
| CT_RF01_02 | Realizar contagem física simulada e registrar as quantidades no sistema. |

| **Pré-condições** |
| :-- |
| - Os produtos devem estar previamente cadastrados no sistema. <br> - O módulo de inventário deve estar acessível. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o módulo de inventário <br> **E** seleciona os produtos cadastrados <br> **QUANDO** inserir as quantidades simuladas de contagem física e salvar <br> **ENTÃO** o sistema deve registrar corretamente as contagens. |

| **Critérios de aceitação** |
| :-- |
| - As contagens devem ser registradas sem erro no sistema. <br> - Os registros devem ser consistentes no banco de dados. |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://www.youtube.com) |

---

## **Caso de Teste CT_RF01_03: Lançamento do inventário e geração de relatório de ajustes**

| ID | Descrição |
| :-- | :-- |
| CT_RF01_03 | Lançar o inventário no sistema e gerar o relatório de ajustes conforme contagem física. |

| **Pré-condições** |
| :-- |
| - A contagem física simulada deve ter sido concluída e salva. <br> - O usuário deve possuir permissão para lançar inventários. |

| **Passos** |
| :-- |
| **DADO** que o usuário acessa o módulo de inventário <br> **E** seleciona o inventário com contagem concluída <br> **QUANDO** realizar o lançamento do inventário e gerar o relatório de ajustes <br> **ENTÃO** o sistema deve ajustar os saldos conforme a contagem e apresentar as diferenças entre saldo contabilizado e ajustado. |

| **Critérios de aceitação** |
| :-- |
| - O relatório de ajustes deve ser gerado corretamente. <br> - Os saldos contabilizado e ajustado devem estar consistentes no banco de dados. <br> - As diferenças devem estar corretamente refletidas no sistema. |

| **Evidência(s)** |
| :--: |
| [Vídeo](https://www.youtube.com) |

---
