# Casos de Teste: Cadastro de Especialidades

**Funcionalidade:** Cadastro de Especialidades  
**Campo Principal em Teste:** Nome da Especialidade (Regra: Mínimo 3, Máximo 30 caracteres)

---

## 1. Particionamento por Equivalência (3 Casos)

Divisão das entradas em classes válidas e inválidas para garantir o tratamento correto dos dados.

| ID | Cenário / Entrada | Classe de Equivalência | Técnica Utilizada | Resultado Esperado |
| :--- | :--- | :--- | :--- | :--- |
| **CT-PE01** | `Cardiologia` (11 caracteres) | Classe Válida (Texto com tamanho permitido) | Particionamento por Equivalência | Registro salvo com sucesso e mensagem de confirmação exibida. |
| **CT-PE02** | `Ped` (3 caracteres + espaço + números: `Ped 123`) | Classe Inválida (Caracteres especiais/números) | Particionamento por Equivalência | Sistema bloqueia o envio e exibe alerta: "O nome deve conter apenas letras". |
| **CT-PE03** | Campo em branco / Vazio (`""`) | Classe Inválida (Campo obrigatório ausente) | Particionamento por Equivalência | Sistema impede o cadastro e destaca o campo com aviso: "Campo obrigatório". |

---

## 2. Análise de Valor Limite - AVL (3 Casos)

Testes focados nas fronteiras das regras de tamanho do campo (Mínimo: 3 / Máximo: 30).

| ID | Cenário / Entrada | Limite Testado | Técnica Utilizada | Resultado Esperado |
| :--- | :--- | :--- | :--- | :--- |
| **CT-VL01** | `UT` (2 caracteres) | Limite Inferior Inválido (Mínimo - 1) | Análise de Valor Limite | Cadastro rejeitado com aviso: "O nome deve ter no mínimo 3 caracteres". |
| **CT-VL02** | `Ortopedia e Traumatologia Med` (30 caracteres) | Limite Superior Válido (Máximo exato) | Análise de Valor Limite | Registro salvo com sucesso. |
| **CT-VL03** | `Ortopedia e Traumatologia Medic` (31 caracteres) | Limite Superior Inválido (Máximo + 1) | Análise de Valor Limite | Campo limita a digitação em 30 caracteres ou exibe erro de limite excedido. |

---

## 3. Transição de Estados (3 Estados e Transições)

Mapeamento dos estados do cadastro durante o ciclo de vida da funcionalidade.

### Estados Identificados:
1. **Em Preenchimento (Rascunho):** Formulário aberto com dados sendo inseridos.
2. **Ativo (Cadastrado):** Especialidade salva com sucesso no banco de dados.
3. **Inativo (Desativado):** Especialidade desativada temporariamente sem remoção do histórico.

### Tabela de Transições de Estado:

| ID | Estado Inicial | Ação / Evento (Entrada) | Estado Final | Resultado Esperado |
| :--- | :--- | :--- | :--- | :--- |
| **CT-TE01** | Em Preenchimento | Clicar em "Salvar" com dados válidos | **Ativo** | Dados gravados no banco e especialidade listada na busca de ativos. |
| **CT-TE02** | Ativo | Clicar no botão "Desativar" | **Inativo** | Status alterado para "Inativo"; especialidade deixa de aparecer no cadastro de novos médicos. |
| **CT-TE03** | Inativo | Clicar no botão "Reativar" | **Ativo** | Status alterado para "Ativo"; especialidade volta a ficar disponível no sistema. |
