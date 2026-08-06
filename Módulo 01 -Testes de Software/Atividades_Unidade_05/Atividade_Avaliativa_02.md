
# Atividade Avaliativa 2

---

# Plano de Testes Resumido: Release de Correção de Login e Ajuste de Saldo

---

## 🎯 1. Escopo de Testes

### 🟢 O que SERÁ testado:
* **Módulo de Login:** Validação de credenciais, correção do travamento/bug anterior e fluxo de autenticação com acesso ao sistema.
* **Componente de Saldo (Tela Inicial):** Renderização do valor na página inicial, formatação dos dados e funcionalidade do ícone de ocultar/exibir saldo.

### 🔴 O que NÃO será testado:
* Módulos periféricos do sistema (Transferências Pix, Pagamento de Boletos, Cartões, Extrato detalhado, Empréstimos) para evitar desperdício de tempo e focar estritamente na entrega da release.

---

## 🧪 2. Tipos de Teste Aplicados

1. **Testes de Smoke:** Execução imediata no primeiro minuto do deploy para conferir se as funções vitais (autenticar e carregar a página inicial com o saldo) estão ativas e estáveis.
2. **Testes de Sanidade:** Validação focada nas correções específicas efetuadas pelos desenvolvedores.

---

## 🚦 3. Critérios de Entrada e Saída

### Critérios de Entrada:
* Deploy implantado com sucesso no ambiente de testes.
* Dados de teste (usuários e saldos válidos) previamente prontos.
* Ausência de bloqueios de infraestrutura no ambiente QA.

### Critérios de Saída (Done):
* 100% dos testes de Smoke aprovados.
* 0 (zero) bugs críticos ou impeditivos abertos nos módulos de Login e Saldo.
* Revalidação e fechamento dos *bugs* no mesmo dia do reporte.

---

## 🖥️ 4. Ambiente de Testes

* **Ambiente:** QA / Homologação (ambiente espelho da produção).
* **Ação Imediata:** Assim que o código for liberado pela equipe de desenvolvimento, a execução do Smoke Test é disparada instantaneamente para validar a estabilidade do build.

---

## 👥 5. Recursos e Responsabilidades

* **Analista de QA / Testador:** Execução rápida dos testes (Smoke e Sanidade), abertura detalhada de defeitos críticos e reteste prioritário no mesmo dia.
* **Desenvolvedores:** Atendimento prioritário e correção imediata de *bugs* reportados durante a janela de testes.
* **Product Owner / Líder Técnico:** Aprovação do reporte do plano e aceite final da release.

---

## ⏱️ 6. Cronograma Básico (Ciclo de 1 Dia)

| Etapa | Ação | Duração Estimada |
| :--- | :--- | :--- |
| **Etapa 1** | Liberação do Build no Ambiente de QA | Hora H |
| **Etapa 2** | Execução Imediata dos Testes de Smoke | + 30 minutos |
| **Etapa 3** | Execução dos Testes de Sanidade (Login e Saldo) | + 1 hora |
| **Etapa 4** | Janela de Correção de Bugs Impeditivos (Devs) | + 2 horas |
| **Etapa 5** | Reteste de Validação e Aceite Final | + 30 minutos |

---

## ⚠️ 7. Riscos e Contingências

| Risco Identificado | Impacto | Plano de Contingência |
| :--- | :--- | :--- |
| **Falha Crítica no Smoke Test (App não loga ou fecha automaticamente)** | Alto | Rejeição imediata do build. O código retorna aos desenvolvedores sem perda de tempo em testes detalhados. |
| **Demora na correção de bugs encontrados** | Alto | Foco exclusivo da equipe de Devs nos impedimentos de Login e Saldo, pausando a criação de novas funcionalidades. |
| **Indisponibilidade do Ambiente de Testes** | Médio | Execução prévia da validação em ambiente local ou pré-configurado. |
