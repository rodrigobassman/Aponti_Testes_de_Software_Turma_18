# Atividade Avaliativa: Aplicação de Heurísticas de Testes de Software

**Funcionalidade Analisada:** Cadastro de Especialidades  
**Objetivo:** Identificar falhas, mapear riscos de software e propor áreas prioritárias de atenção com base em heurísticas reconhecidas da área de Qualidade de Software (QA).

---

## 1. Abordagens e Heurísticas Escolhidas

Para a realização deste teste exploratório e estruturado, foram selecionadas duas abordagens complementares:

1. **10 Heurísticas de Usabilidade de Nielsen**
   * **Foco:** Avaliar a interface do usuário, clareza das informações e feedback em tempo real das ações executadas.
2. **Testing Tours (Feature Tour & Garbage Tour)**
   * **Foco:** Explorar os limites do formulário, a consistência das regras de negócio e a validação de entrada de dados no banco de dados.

---

## 2. Diagnóstico da Funcionalidade: Cadastro de Especialidades

### 🚩 Falhas Identificadas

* **Ambuidade no Formulário:** No formulário de cadastro, o rótulo (label) do campo *"Nome"* não especifica se refere-se ao nome da especialidade ou do médico.
  * *Violação Nielsen:* Prevenção de erros / Correspondência com o mundo real.
* **Falta de Feedback Operacional:** Ao finalizar o cadastro, o sistema não exibe nenhuma mensagem de confirmação de sucesso ou erro.
  * *Violação Nielsen:* Visibilidade do status do sistema.
* **Permissão de Dados Duplicados:** O sistema permite o cadastramento de uma mesma especialidade repetidas vezes.
  * *Falha via Garbage Tour:* Ausência de validação de dados únicos e consistência.
* **Ausência de Estrutura Inicial:** Não existe pré-cadastro de especialidades nem mapeamento/associação prévia entre médicos e especialidades.

---

### ⚠️ Riscos Identificados

| Risco | Impacto no Sistema / Usuário |
| :--- | :--- |
| **Erro de Preenchimento** | O usuário pode inserir o nome do médico no campo da especialidade (e vice-versa) por falta de clareza no formulário. |
| **Inconsistência de Dados** | Cadastro de informações com erros de digitação e sem padronização nos nomes das especialidades/médicos. |
| **Incerteza Operacional** | Dúvida se a operação foi concluída com sucesso, podendo levar o usuário a clicar repetidamente no botão de salvar. |
| **Redundância e Lixo no Banco** | Cadastro de especialidades duplicadas e com informações conflitantes, comprometendo relatórios e buscas futuras. |

---

### 🎯 Áreas que Merecem Mais Atenção

* **Validação de Entrada & Regras de Duplicidade:** Implementação de travas para impedir registros idênticos e validação no *front-end* e *back-end*.
* **Arquitetura de Dados & Relacionamentos:** Estruturação de fluxos de pré-cadastro e criação formal dos relacionamentos N:N ou 1:N entre as entidades *Médico* e *Especialidade*.
* **Interface e Experiência do Usuário (UX/UI):** Ajuste dos rótulos (labels), *placeholders* e inclusão de componentes de visualização de status (mensagens *toast* / alertas).

---

## 3. Justificativa das Escolhas

> A combinação das **Heurísticas de Nielsen** com os **Testing Tours** foi escolhida por proporcionar uma cobertura holística da funcionalidade, avaliando tanto a **experiência do usuário (UX)** no *front-end* quanto a **integridade e consistência das regras de negócio** no *back-end*:
>
> 1. **Nielsen (Usabilidade & Interface):** Permitiu identificar falhas graves de comunicação entre o sistema e o usuário, como a ambiguidade nos rótulos (*campo "Nome" sem contexto*) e a falta de resposta do sistema (*ausência de confirmação*). Isso reduz drasticamente a probabilidade de erros humanos durante o uso do software.
> 2. **Testing Tours (Feature Tour & Garbage Tour):** Permitiu testar os limites do formulário e a robustez da persistência de dados. Essa abordagem evidenciou a falta de restrições de duplicidade e a inconsistência no modelo de dados, prevenindo a degradação e o acúmulo de dados incorretos no banco.
