# Atividade Avaliativa 1

## 🎯 1. Objetivo da Estratégia

Com base no cenário apresentado, crie uma estratégia de testes contendo os itens abaixo:
* Objetivo da estratégia
* O que é mais importante garantir com os testes?
* Quais aspectos do sistema merecem maior atenção?
* Tipos de Teste Prioritários
* Quais tipos de teste serão executados?
* Quais terão menor prioridade?
* Justifique às escolhas com base em risco e contexto

---

## 🛡️ 2. O que é Mais Importante Garantir?

* **Acessibilidade e Autenticação (Login Ativo):** Garantir que todos os usuários consigam autenticar no aplicativo sem sofrer com travamentos ou recusa indevida de credenciais válidas.
* **Integridade dos Dados Financeiros (Saldo):** Garantir que o valor exibido na tela inicial esteja correto, formatado adequadamente e que o mecanismo de mascarar/revelar o saldo (ícone do olho) funcione perfeitamente.
* **Ausência de Regressão Crítica:** Assegurar que a correção aplicada no login não impeça a navegação para a tela inicial.

---

## 🔍 3. Aspectos do Sistema que Merecem Maior Atenção

1. **Tratamento de Exceções e Resiliência no Login:** O comportamento da aplicação ao receber respostas do servidor de autenticação (evitando fechamentos inesperados).
2. **Interface e Layout na Tela Inicial (UI):** A renderização correta do componente de saldo para evitar sobreposição de texto ou quebra de layout em diferentes tamanhos de tela de smartphones.
3. **Comunicação com APIs de Sessão e Saldo:** A velocidade e a segurança do consumo de dados que retornam do *backend* após o login bem-sucedido.

---

## 🧪 4. Tipos de Teste Prioritários

### 🟢 Tipos de Teste Executados (Alta Prioridade):
* **Testes de Smoke:** Executados imediatamente no início da entrega para validar funcionalidades vitais.
* **Testes de Sanidade:** Focados na verificação da correção do *bug* no login e no comportamento do componente de saldo ajustado.
* **Testes de Usabilidade e Interface (UI):** Validação visual da exibição do saldo, formatação monetária e usabilidade de botões na tela inicial.

### 🔴 Tipos de Teste de Menor Prioridade / Fora de Foco:
* **Testes Regressivos Completos (End-to-End):** Validação detalhada de fluxos como PIX, pagamentos, contratação de empréstimos e solicitação de cartões.
* **Testes de Carga/Estresse:** Simulações de pico massivo de acessos simultâneos na infraestrutura# Estratégia de Testes: Release de Correção de Login e Ajuste de Saldo

---

## 🎯 1. Objetivo da Estratégia

Com base no cenário apresentado, crie uma estratégia de testes contendo os itens abaixo:
* Objetivo da estratégia
* O que é mais importante garantir com os testes?
* Quais aspectos do sistema merecem maior atenção?
* Tipos de Teste Prioritários
* Quais tipos de teste serão executados?
* Quais terão menor prioridade?
* Justifique às escolhas com base em risco e contexto

---

## 🛡️ 2. O que é Mais Importante Garantir?

* **Acessibilidade e Autenticação (Login Ativo):** Garantir que 100% dos usuários consigam autenticar no aplicativo sem sofrer com *crashes*, travamentos ou recusa indevida de credenciais válidas.
* **Integridade dos Dados Financeiros (Saldo):** Garantir que o valor exibido na tela inicial esteja correto, formatado adequadamente e que o mecanismo de mascarar/revelar o saldo (ícone do olho) funcione perfeitamente.
* **Ausência de Regressão Crítica:** Assegurar que a correção aplicada no login não tenha quebrado o fluxo de entrada do sistema nem impedido a navegação para a tela principal (*Home*).

---

## 🔍 3. Aspectos do Sistema que Merecem Maior Atenção

1. **Tratamento de Exceções e Resiliência no Login:** O comportamento da aplicação ao receber respostas do servidor de autenticação (evitando fechamentos inesperados).
2. **Interface e Layout na Tela Inicial (UI):** A renderização correta do componente de saldo para evitar sobreposição de texto ou quebra de layout em diferentes tamanhos de tela de smartphones.
3. **Comunicação com APIs de Sessão e Saldo:** A velocidade e a segurança do consumo de dados que retornam do *backend* após o login bem-sucedido.

---

## 🧪 4. Tipos de Teste Prioritários

### 🟢 Tipos de Teste Executados (Alta Prioridade):
* **Testes de Smoke (Fumaça):** Executados imediatamente no início da entrega para validar os fluxos vitais (*App abre? Login funciona? Saldo aparece?*).
* **Testes de Sanidade:** Focados estritamente na verificação da correção do *bug* no login e no comportamento do componente de saldo ajustado.
* **Testes de Usabilidade e Interface (UI):** Validação visual da exibição do saldo, formatação monetária e usabilidade de botões na tela inicial.

### 🔴 Tipos de Teste de Menor Prioridade / Fora de Foco:
* **Testes Regressivos Completos (End-to-End):** Validação detalhada de fluxos como PIX, pagamentos, contratação de empréstimos e solicitação de cartões.
# Estratégia de Testes: Release de Correção de Login e Ajuste de Saldo

---

## 🎯 1. Objetivo da Estratégia

Com base no cenário apresentado, crie uma estratégia de testes contendo os itens abaixo:
* Objetivo da estratégia
* O que é mais importante garantir com os testes?
* Quais aspectos do sistema merecem maior atenção?
* Tipos de Teste Prioritários
* Quais tipos de teste serão executados?
* Quais terão menor prioridade?
* Justifique às escolhas com base em risco e contexto

---

## 🛡️ 2. O que é Mais Importante Garantir?

* **Acessibilidade e Autenticação (Login Ativo):** Garantir que 100% dos usuários consigam autenticar no aplicativo sem sofrer com *crashes*, travamentos ou recusa indevida de credenciais válidas.
* **Integridade dos Dados Financeiros (Saldo):** Garantir que o valor exibido na tela inicial esteja correto, formatado adequadamente e que o mecanismo de mascarar/revelar o saldo (ícone do olho) funcione perfeitamente.
* **Ausência de Regressão Crítica:** Assegurar que a correção aplicada no login não tenha quebrado o fluxo de entrada do sistema nem impedido a navegação para a tela principal (*Home*).

---

## 🔍 3. Aspectos do Sistema que Merecem Maior Atenção

1. **Tratamento de Exceções e Resiliência no Login:** O comportamento da aplicação ao receber respostas do servidor de autenticação (evitando fechamentos inesperados).
2. **Interface e Layout na Tela Inicial (UI):** A renderização correta do componente de saldo para evitar sobreposição de texto ou quebra de layout em diferentes tamanhos de tela de smartphones.
3. **Comunicação com APIs de Sessão e Saldo:** A velocidade e a segurança do consumo de dados que retornam do *backend* após o login bem-sucedido.

---

## 🧪 4. Tipos de Teste Prioritários

### 🟢 Tipos de Teste Executados (Alta Prioridade):
* **Testes de Smoke (Fumaça):** Executados imediatamente no início da entrega para validar os fluxos vitais (*App abre? Login funciona? Saldo aparece?*).
* **Testes de Sanidade:** Focados estritamente na verificação da correção do *bug* no login e no comportamento do componente de saldo ajustado.
* **Testes de Usabilidade e Interface (UI):** Validação visual da exibição do saldo, formatação monetária e usabilidade de botões na tela inicial.

### 🔴 Tipos de Teste de Menor Prioridade / Fora de Foco:
* **Testes Regressivos Completos:** Validação detalhada de fluxos como PIX, pagamentos, contratação de empréstimos e solicitação de cartões.
* **Testes de Carga/Estresse:** Simulações de pico massivo de acessos simultâneos na infraestrutura.

---

## ⚖️ 5. Justificativa das Escolhas (Risco vs. Contexto)

* **Contexto de Tempo Limitado:** Como o prazo de entrega é curto e a alteração é pontual, direcionar o esforço de testes exclusivamente para o Login e a Exibição do Saldo evita o desperdício de recursos e permite um ciclo rápido de *feedback* para a equipe de desenvolvimento.
* **Matriz de Risco do Negócio:** O **Login** é a porta de entrada da aplicação — se ele falhar, o sistema fica 100% indisponível para o cliente (Risco Crítico). O **Saldo** é a primeira informação financeira consumida pelo usuário ao abrir a conta (Risco Alto de Percepção de Qualidade e Confiança). 
* **Funcionalidades não prioritárias Justificadas:** Módulos periféricos (como emissão de comprovantes ou contratação de serviços) foram colocados em menor prioridade porque **não sofreram alterações de código nesta versão**. Testá-los profundamente geraria custo de tempo desnecessário e risco de descumprimento do prazo da release.

---

## ⚖️ 5. Justificativa das Escolhas (Risco vs. Contexto)

* **Contexto de Tempo Limitado:** Como o prazo de entrega é curto e a alteração é pontual, direcionar o esforço de testes exclusivamente para o Login e a Exibição do Saldo evita o desperdício de recursos e permite um ciclo rápido de *feedback* para a equipe de desenvolvimento.
* **Matriz de Risco do Negócio:** O **Login** é a porta de entrada da aplicação — se ele falhar, o sistema fica 100% indisponível para o cliente (Risco Crítico). O **Saldo** é a primeira informação financeira consumida pelo usuário ao abrir a conta (Risco Alto de Percepção de Qualidade e Confiança). 
* **Funcionalidades não prioritárias Justificadas:** Módulos periféricos (como emissão de comprovantes ou contratação de serviços) foram colocados em menor prioridade porque **não sofreram alterações de código nesta versão**. Testá-los profundamente geraria custo de tempo desnecessário e risco de descumprimento do prazo da release.

---

## ⚖️ 5. Justificativa das Escolhas (Risco vs. Contexto)

* **Contexto de Tempo Limitado:** Como o prazo de entrega é curto e a alteração é pontual, direcionar o esforço de testes exclusivamente para o Login e a Exibição do Saldo evita o desperdício de recursos e permite um ciclo rápido de *feedback* para a equipe de desenvolvimento.
* **Matriz de Risco do Negócio:** O **Login** é a porta de entrada da aplicação — se ele falhar, o sistema fica 100% indisponível para o cliente (Risco Crítico). O **Saldo** é a primeira informação financeira consumida pelo usuário ao abrir a conta (Risco Alto de Percepção de Qualidade e Confiança). 
* **Funcionalidades não prioritárias Justificadas:** Módulos periféricos (como emissão de comprovantes ou contratação de serviços) foram colocados em menor prioridade porque **não sofreram alterações de código nesta versão**. Testá-los profundamente geraria custo de tempo desnecessário e risco de descumprimento do prazo da release.
