# CT_RF11_ Inventário de Estoque

## Objetivo
Testar a precisão na reconciliação do estoque físico com o sistema após importação, contagem e lançamento do inventário.

## Pré-requisitos
- Sistema com módulo de inventário ativo.
- Arquivo XML com produtos fictícios para importação.
- Acesso ao banco de dados para validação.

## Cenários de Teste

### CT_RF11_01_ Importação de produtos via XML
**Descrição:** Importar produtos fictícios via arquivo XML e validar cadastro no sistema.

**Passos:**
1. Acessar o módulo de inventário.
2. Selecionar a opção de importação de produtos.
3. Importar o arquivo XML com produtos fictícios.
4. Confirmar a importação.

**Dados de Entrada:**
- Arquivo XML com 10 produtos fictícios.

**Resultado Esperado:**
- Produtos cadastrados corretamente no sistema.
- Mensagem de sucesso na importação.

**Validação:**
- Verificar no banco de dados se os produtos foram inseridos com os dados corretos.

---

### CT_RF11_02_ Contagem física simulada
**Descrição:** Realizar contagem física simulada e registrar no sistema.

**Passos:**
1. Acessar o módulo de inventário.
2. Selecionar os produtos cadastrados.
3. Inserir quantidades simuladas para contagem física.
4. Salvar a contagem.

**Dados de Entrada:**
- Quantidades simuladas para cada produto.

**Resultado Esperado:**
- Contagem registrada corretamente no sistema.

**Validação:**
- Conferir no banco de dados os registros da contagem física.

---

### CT_RF11_03_ Lançamento do inventário e geração de relatório de ajustes
**Descrição:** Lançar o inventário no sistema e gerar relatório de ajustes.

**Passos:**
1. Acessar o módulo de inventário.
2. Realizar o lançamento do inventário com base na contagem física.
3. Gerar o relatório de ajustes.

**Resultado Esperado:**
- Saldos ajustados conforme contagem física.
- Relatório de ajustes gerado com as diferenças entre saldo contabilizado e ajustado.

**Validação:**
- Verificar no banco de dados a consistência entre saldo contabilizado e saldo ajustado.
- Conferir o relatório gerado.