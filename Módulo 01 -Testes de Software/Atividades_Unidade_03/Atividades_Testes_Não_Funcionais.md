# Testes Não Funcionais — Atividade Avaliativa

Dado um sistema proposto, os alunos deverão elaborar um checklist de testes não funcionais, cobrindo obrigatoriamente:
* Performance
* Segurança
* Usabilidade
* Compatibilidade

Cada item do checklist deve indicar o que será verificado e qual o risco associado.

---

## a) Performance

### Tempo de Resposta na Consulta de Especialidades e Profissionais
| Verificação | Risco Associado |
| :--- | :--- |
| **O que será verificado:**<br>• O tempo que o sistema leva para carregar os dados quando o paciente aplica filtros de busca.<br>• Se a resposta da busca é entregue em menos de 2 segundos. | **Lentidão e Desistência do Agendamento:**<br>Pacientes abandonarem a plataforma por demora do carregamento dos dados, ocasionando perdas de consultas. |

### Comportamento sob Carga em Horários de Pico
| Verificação | Risco Associado |
| :--- | :--- |
| **O que será verificado:**<br>• A capacidade de o servidor manter a estabilidade quando muitos usuários simultâneos acessam a plataforma. | **Queda do Sistema:**<br>o sistema ficar indisponível ou retornar erros. |

### Concorrência e Conflito de Horários Simultâneos
| Verificação | Risco Associado |
| :--- | :--- |
| **O que será verificado:**<br>• Como a API e a transação de banco de dados se comportam quando dois usuários clicam para agendar a mesma vaga ao mesmo tempo. | **Inconsistência de Dados:**<br>O banco de dados aceitar o agendamento duplo, violando as regras do sistema. |

### Desempenho Quanto ao Envio Massivo de Notificações
| Verificação | Risco Associado |
| :--- | :--- |
| **O que será verificado:**<br>• Se o processamento e o disparo das mensagens de confirmação ocorrem sem travamentos no momento em que o usuário clica em “Confirmar”. | **Travamento da Tela de Confirmação:**<br>O usuário ficar com a tela congelada, levando-o a clicar várias vezes, gerando requisições duplicadas. |

---

## b) Segurança

### Autenticação de Usuários e Controle de Acesso
| Verificação | Risco Associado |
| :--- | :--- |
| **O que será verificado:**<br>• Se o fluxo de cadastro/autenticação impede que um usuário comum acesse a área administrativa de gestão de horários.<br>• Se tentativas de agendamento por usuários não logados são bloqueadas e redirecionadas para a tela de login. | **Invasão da Área Administrativa:**<br>Usuários comuns com o poder de alterar dados. |

### Proteção de Dados Pessoais e Sensíveis
| Verificação | Risco Associado |
| :--- | :--- |
| **O que será verificado:**<br>• Criptografia via protocolo HTTPS/TLS.<br>• Se dados sensíveis estão armazenados de forma segura. | **Exposição de dados e penalidades legais:**<br>vazamentos de informações do paciente ou falhas de armazenamento, resultando em multas pesadas. |

### Gestão de Sessão e Desconexão Automática
| Verificação | Risco Associado |
| :--- | :--- |
| **O que será verificado:**<br>• Se a sessão do usuário é expirada automaticamente após um período definido de inatividade.<br>• Se botão de “voltar” do navegador reabra uma área logada. | **Uso Indevido por Terceiros:**<br>agendamento ou cancelamento de consultas via terceiros no nome do usuário em casos de dispositivos compartilhados. |

### Privacidade nas Notificações de Confirmação
| Verificação | Risco Associado |
| :--- | :--- |
| **O que será verificado:**<br>• Se as notificações enviadas exibem apenas o mínimo necessário para a confirmação, omitindo dados sensíveis. | **Quebra de sigilo do paciente:**<br>pessoas com acesso à tela de notificação ou e-mail do usuário podem visualizar informações médicas confidenciais. |

---

## c) Usabilidade

### Clareza e Transparência na Regra de Cancelamento
| Verificação | Risco Associado |
| :--- | :--- |
| **O que será verificado:**<br>• Se o sistema exibe corretamente o prazo limite para cancelamento tanto na tela de detalhes da consulta, quanto no momento do agendamento.<br>• Se ao tentar cancelar uma consulta a menos de 24 horas do horário, o sistema exibe uma mensagem sobre não ser possível cancelar pelo sistema ao invés de travar ou dar um erro. | **Frustração do Paciente e Sobrecarga do Suporte:**<br>Reclamações por o usuário não entender por que não consegue cancelar. |

### Facilidade no Fluxo Principal de Agendamento e Consulta
| Verificação | Risco Associado |
| :--- | :--- |
| **O que será verificado:**<br>• Quantidade de etapas/cliques necessários até a confirmação do agendamento.<br>• Se os filtros de especialidade e profissional oferecem retorno rápido e exibição organizada. | **Abandono do Agendamento:**<br>Dificuldade do uso gerar desistências no agendamento. |

### Feedback Visual e Prevenção de Erros
| Verificação | Risco Associado |
| :--- | :--- |
| **O que será verificado:**<br>• Se a plataforma fornece avisos visuais imediatos e sem erros após uma ação.<br>• Se botões de confirmação ficam desabilitados após o primeiro clique para evitar envios por ansiedade. | **Ações duplicadas por incerteza:**<br>Cliques repetidos no botão confirmar por não saber se a ação funcionou. |

### Eficiência na Área Administrativa de Gestão de Horários
| Verificação | Risco Associado |
| :--- | :--- |
| **O que será verificado:**<br>• Se a interface administrativa permite visualizar, cadastrar, bloquear e liberar horários de maneira rápida. | **Erros Operacionais da Equipe:**<br>Cadastros errados ou indisponíveis. |

---

## d) Compatibilidade

### Suporte a Diferentes Sistemas Operacionais
| Verificação | Risco Associado |
| :--- | :--- |
| **O que será verificado:**<br>• Se o comportamento do sistema permanece estável ao alternar entre diferentes sistemas operacionais. | **Incompatibilidade de Scripts:**<br>Recursos essenciais do fluxo de agendamento em um sistema operacional específico. |

### Compatibilidade de Entrada e Seleção de Dados em Dispositivos Touch
| Verificação | Risco Associado |
| :--- | :--- |
| **O que será verificado:**<br>• Se os campos de entrada de dados ativam os teclados virtuais. | **Erros de Digitação e Lentidão no Cadastro:**<br>Dificuldade extrema para preencher dados cadastrais, ocasionando abandono ou dados incorretos. |

