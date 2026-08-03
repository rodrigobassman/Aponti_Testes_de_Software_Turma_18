markdown_content = """# Atividade Avaliativa: Análise de Relatório de Teste de Performance

Este documento apresenta a análise técnica detalhada aplicada aos cenários do sistema bancário (Ajustes de Login e Exibição de Saldo na Tela Inicial).

---

## 🟢 Cenário 1: Teste de Carga (Simulação do Volume Esperado)

> **Contexto:** Avaliação da performance do sistema durante o fluxo operacional diário sob carga normal e de pico prevista em contrato/SLA.

### 1. O sistema pode ser considerado aprovado?
**Parcialmente aprovado (com ressalvas).** 
Embora a funcionalidade de exibição do saldo tenha respondido dentro dos limites aceitáveis de SLA, o módulo de login demonstrou instabilidade operacional sob volume simultâneo de acessos, apresentando elevação no tempo de resposta e pequenas intermitências. Para aprovação definitiva em ambiente de produção, as falhas encontradas no login precisam ser sanadas.

### 2. Quais métricas indicam problemas de performance?
* **Tempo de Resposta ($p95$ / $p99$):** Elevação expressiva nos percentis mais altos durante requisições de autenticação.
* **Taxa de Erro (*Error Rate*):** Ocorrência de respostas `HTTP 500` (Internal Server Error) e `HTTP 504` (Gateway Timeout) superiores ao limite tolerado de 0,5% na rota de Login.
* **Vazão (*Throughput / RPS*):** Estagnação do número de requisições por segundo processadas durante a subida de usuários no Login.

### 3. Quais possíveis gargalos podem existir?
* **Consultas no Banco de Dados:** Processamento lento na verificação de hash de senha e leitura de dados cadastrais do cliente (falta de índices ou *pool* de conexões sobrecarregado).
* **Bloqueio de Threads / Concorrência:** Concorrência excessiva no serviço de autenticação sem balanceamento adequado.
* **Integrações de Terceiros:** Latência em chamadas síncronas a serviços externos de verificação/segurança.

### 4. Esse cenário se aproxima mais de Carga, Stress ou Capacidade?
**Cenário de Carga (*Load Testing*).**
O objetivo principal deste cenário é simular o volume esperado de usuários simultâneos no uso cotidiano e em horários de pico normais (ex: início da manhã ou dias de pagamento) para garantir que a aplicação atende aos requisitos de SLA sem degradação visual ou funcional.

### 5. O que você recomendaria ao time técnico?
* **Otimização de Banco de Dados:** Revisar e indexar as consultas de autenticação e ajustar as configurações do *connection pool*.
* **Estratégia de Cache:** Implementar cache distribuído (ex: Redis) para dados de sessão e consulta de saldo, reduzindo requisições diretas ao banco primário.
* **Ajuste de Timeouts e Retries:** Otimizar as chamadas de API do módulo de login para responder rapidamente antes do limite do *gateway*.

---

## 🔴 Cenário 2: Teste de Estresse (Limite de RUPTURA / PICO EXTREMO)

> **Contexto:** Submissão do sistema a uma carga muito superior à capacidade projetada para identificar o ponto de quebra (*breaking point*) e avaliar a recuperação graciosa.

### 1. O sistema pode ser considerado aprovado?
**Reprovado.**
Sob volume extremo de acessos simultâneos, o sistema apresentou degradação severa, falha geral no módulo de autenticação e inconsistência no tempo de renderização do componente de saldo. O sistema não demonstrou capacidade de recuperação automática (*self-healing*) adequada após a redução da carga.

### 2. Quais métricas indicam problemas de performance?
* **Consumo de Recursos de Hardware:** CPU e Memória RAM dos servidores de aplicação atingindo **100% de utilização**.
* **Taxa de Erro (*Error Rate*):** Pico acentuado de erros `HTTP 502/503/504` afetando mais de 15% das requisições totais.
* **Tempo Médio de Resposta (ART):** Degradado de centenas de milissegundos para vários segundos por requisição.
* **E/S de Disco e Rede:** *Bottleneck* no processamento de leitura/escrita e esgotamento da largura de banda.

### 3. Quais possíveis gargalos podem existir?
* **Ausência de Auto-Scaling:** Infraestrutura rígida sem escalabilidade horizontal automática para absorver picos repentinos.
* **Vazamento de Memória (*Memory Leak*):** Falha no gerenciamento de memória do serviço de saldo durante requisições acumuladas em fila.
* **Esgotamento de Sockets/Portas:** Esgotamento das conexões de rede disponíveis nos servidores web/proxy.

### 4. Esse cenário se aproxima mais de Carga, Stress ou Capacidade?
**Cenário de Estresse (*Stress Testing*).**
O foco deste teste é levar a infraestrutura ao seu ponto extremo de ruptura para observar o comportamento do sistema sob degradação e verificar se ele falha de forma segura (sem expor dados sensíveis) e se recupera sem necessidade de reinicialização manual.

### 5. O que você recomendaria ao time técnico?
* **Auto-Scaling e Elasticidade:** Configurar políticas de autoscaling baseadas em consumo de CPU/Requisições na nuvem.
* **Mecanismos de Defesa (*Circuit Breaker* e *Rate Limiting*):** Implementar *Rate Limiting* no login para mitigar ataques/excessos e padrão *Circuit Breaker* para isolar falhas.
* **Filas Assíncronas:** Migrar tarefas não essenciais de backend para processamento assíncrono via mensageria.
* **Monitoramento e Alertas:** Configurar alertas de alta prioridade (Prometheus/Grafana/Datadog) para detecção rápida de esgotamento de recursos.
"""

filename = "analise_performance_cenarios.md"
with open(filename, "w", encoding="utf-8") as f:
    f.write(markdown_content)

print(f"File generated successfully: {filename}")
