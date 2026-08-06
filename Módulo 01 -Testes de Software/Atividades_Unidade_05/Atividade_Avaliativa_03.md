# Atividade Avaliativa 3: Estratégia de Execução de Testes (Manual vs. Automatizado)

---

## 🎯 Objetivo
Analisar diferentes cenários de teste propostos até esta etapa e decidir qual abordagem de execução é mais adequada, considerando custo, repetição, estabilidade e objetivo do teste. Classificar cada cenário como Manual ou Automatizado e justificar brevemente a decisão.


---

## 📋 Classificação e Justificativa dos Cenários

### 1. Testes de Smoke
* **Classificação:** 🤖 **AUTOMATIZADO**
* **Justificativa:** Os testes de Smoke cobrem funcionalidades críticas e vitais da aplicação (abrir o app, logar com sucesso e verificar se o saldo carregou). Por serem executados a cada novo *deploy* e exigirem validação imediata, a automação garante execução instantânea e reduz erro humano.

### 2. Testes de Sanidade (Validação da Correção de Bug e Ajustes de Layout)
* **Classificação:** ✋ **MANUAL**
* **Justificativa:** A sanidade foca em verificar se após da alteração de uma funcionalidade importante, continua funcionando corretamente. Como é um ajuste pontual, não há necessidade de automatizar, pois fica  mais fácil de perceber comportamentos anômalos, evitando perder tempo codando automação.

### 3. Testes Exploratórios e de Usabilidade
* **Classificação:** ✋ **MANUAL**
* **Justificativa:** Testes exploratórios são guiados pela intuição técnica , criatividade e experiência. Não seguem padrões de testes tradicionais e são executados com base em hipóteses, riscos e principalmente comportamentos do sistema. A automação possui limitações graves para avaliar a  usabilidade, clareza de mensagens ou sensação de fluidez da interface.

### 4. Testes de Regressão (Módulos Periféricos - Pix, Boletos, Extrato)
* **Classificação:** 🤖 **AUTOMATIZADO**
* **Justificativa:** O  teste de regressão verifica se após uma modificação de funcionalidade, o que não foi alterado continua funcionando corretamente. Por serem altamente estáveis e repetitivas, a execução do teste regressivo automatizado permite um custo operacional baixíssimo sem consumir o tempo do analista de QA.

### 5. Testes de Performance (Carga e Estresse)
* **Classificação:** 🤖 **AUTOMATIZADO**
* **Justificativa:** É humanamente inviável simular manualmente acessos simultâneos ao serviço de login e saldo. A automação é indispensável para gerar volume e mensurar requisições e métricas como tempo de resposta, vazão e taxa de erro.

---

## 📊 Quadro Resumo da Abordagem

| Cenário de Teste | Abordagem | Fator Determinante para a Decisão |
| :--- | :--- | :--- |
| **Smoke (Login e Saldo)** | 🤖 Automatizado | Velocidade de resposta no deploy e alta repetição. |
| **Sanidade** | ✋ Manual | Verificação visual imediata e instabilidade pós-correção. |
| **Exploratório e Usabilidade** | ✋ Manual | Dependência do julgamento, experiência e intuição humana. |
| **Regressão Geral do App** | 🤖 Automatizado | Funcionalidades estáveis e alto volume de repetição. |
| **Performance (Carga e Estresse)** | 🤖 Automatizado | Impossibilidade física de simulação manual de carga. |
