# Documentação de Testes: Módulo de Especialidades

## 1. Contexto do Módulo
* **Ator:** Especialidades
* **Estado Inicial:** Estar logado no sistema
* **O que realmente importa:** Cadastrar especialidades
* **Resultado observável:** Exibir lista das especialidades cadastradas

---

## 2. Cenários (Gherkin)

### Cenário Principal: Cadastro de Especialidade
**Background:** Acessar a página de especialidades
**Given:** Nenhuma especialidade cadastrada

**Cenário:** cadastrar nova especialidade
* **Given:** página de cadastro acessada
* **When:** cadastro feito
* **Then:** nome da especialidade e descrição são exibidas
* **And:** cadastro realizado com sucesso

### Cenário Alternativo: Cadastro Duplicado (Bug Report)
**Background:** Acessar a página de especialidades
**Given:** Permite cadastro duplo

**Cenário:** cadastrar nova especialidade (duplicata)
* **Given:** página de cadastro acessada
* **When:** cadastro repetido
* **Then:** o sistema aceitou sem nenhuma ressalva
* **And:** As duas especialidades em duplicidade são exibidas

---

## 3. Registro de Bugs Percebidos
* **Feedback:** Não exibe mensagem de cadastro realizado com sucesso.
* **Validação:** Permite o cadastro de qualquer texto nos campos.
* **Integridade:** Permite cadastro duplo (falha na chave única).
* **Usabilidade:** Ambiguidade entre Nome e Descrição (Sugestão: Renomear para "Nome da especialidade").
* **Funcionalidade:** Não possui campo para o nome do médico responsável.
* **Configuração:** Não possui especialidades pré-cadastradas.

---

## 4. Teste Exploratório

* **ID:** TEF-ESP-01
* **TÍTULO:** Validar bloqueio de cadastro duplo na funcionalidade de Especialidades
* **PRÉ-CONDIÇÕES:**
    1. Estar logado no sistema da clínica psicológica.
    2. Ter acesso à tela de cadastro de especialidades (campos Nome e Descrição).

* **PASSOS DO TESTE:**
    1. Acessar a tela de cadastro de especialidades.
    2. Preencher o campo **Nome** com `Psicologia Clínica` e o campo **Descrição** com `Atendimento focado em adultos`.
    3. Clicar no botão para salvar o registro.
    4. Preencher novamente o campo **Nome** com `Psicologia Clínica` e o campo **Descrição** com `Atendimento focado em adultos`.
    5. Clicar novamente no botão para salvar o registro.

* **VALIDAÇÃO DO COMPORTAMENTO:**
    1. Verificar se o sistema impede o segundo salvamento e exibe uma mensagem de alerta informando que a especialidade já está cadastrada.
    2. Conferir na listagem de especialidades se o sistema permitiu a criação de dois registros idênticos (comportamento de erro encontrado).

---

## 5. Reflexão sobre a Abordagem

| Pergunta | Resposta |
| :--- | :--- |
| **Qual o formato mais fácil de escrever?** | Teste Unitário (mais técnico e direto). |
| **Qual comunica melhor o comportamento?** | Teste exploratório (pois o unitário se limita à funcionalidade esperada, enquanto o exploratório cobre o comportamento real do usuário). |
| **Qual seria mais fácil de manter?** | O exploratório, pois é mais abrangente e depende da intuição do QA, indo além dos limites pré-estabelecidos pelo código. |
