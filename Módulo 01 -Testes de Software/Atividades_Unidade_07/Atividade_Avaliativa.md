# Plano de Testes: Módulo de Especialidades

## 1. Análise do Valor Limite (AVL)
Testes focados nos limites de caracteres (Min: 3, Max: 50).

| ID | Entrada (Campo Especialidade) | Técnica | Resultado Esperado |
| :--- | :--- | :--- | :--- |
| **AVL-01** | "Od" (2 caracteres) | Limite Mínimo - 1 | Sistema deve bloquear e exibir erro de tamanho mínimo. |
| **AVL-02** | 50 caracteres válidos | Limite Máximo | Sistema deve aceitar o cadastro. |
| **AVL-03** | 51 caracteres | Limite Máximo + 1 | Sistema deve bloquear e exibir erro de limite excedido. |

## 2. Particionamento de Equivalência (PE)
Testes focados na validação de tipos de entrada e integridade de dados.

| ID | Entrada (Dados) | Técnica | Resultado Esperado |
| :--- | :--- | :--- | :--- |
| **PE-01** | Esp: "Cardiologia" | Classe Válida | Cadastro realizado com sucesso. |
| **PE-02** | Esp: "Cardiologia" (repetida) | Classe Inválida | Bloquear duplicidade; erro de "Já cadastrado". |
| **PE-03** | Esp: "!@#$%" | Classe Inválida | Bloquear caracteres especiais; erro de validação. |

## 3. Estados e Transições
Representação do ciclo de vida do cadastro de especialidades.

| Estado Atual | Ação (Transição) | Próximo Estado |
| :--- | :--- | :--- |
| **Vazio** | Preencher campos e salvar | Especialidade Cadastrada |
| **Cadastrada** | Editar dados | Especialidade Atualizada |
| **Cadastrada** | Excluir | Vazio (Listagem limpa) |

## 4. Notas sobre Defeitos Identificados
Conforme análise, os seguintes pontos foram mapeados para correção:
- [ ] **Duplicidade:** O sistema não está validando se a especialidade já existe.
- [ ] **Validação de Input:** O sistema aceita qualquer texto (inclusive símbolos) nos campos.
- [ ] **Pré-cadastro:** Ausência de especialidades padrão (ex: Clínica Geral, Pediatria).
