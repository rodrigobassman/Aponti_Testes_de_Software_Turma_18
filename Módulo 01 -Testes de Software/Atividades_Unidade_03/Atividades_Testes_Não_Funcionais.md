Testes Não Funcionais
Atividade Avaliativa

Dado um sistema proposto, os alunos deverão elaborar um checklist de testes não funcionais, cobrindo obrigatoriamente:
•	Performance
•	Segurança
•	Usabilidade
•	Compatibilidade

Cada item do checklist deve indicar o que será verificado e qual o risco associado.

a)	Performance:
Tempo de Resposta na Consulta de Especialidades e Profissionais
	O que será verificado:
•	O tempo que o sistema leva para carregar os dados quando o paciente aplica filtros de busca.
•	Se a resposta da busca é entregue em menos de 2 segundos.

	Risco Associado:
•	Lentidão e Desistência do Agendamento: Pacientes abandonarem a plataforma por demora do carregamento dos dados, ocasionando perdas de consultas.

Comportamento sob Carga em Horários de Pico
	O que será verificado:
•	A capacidade de o servidor manter a estabilidade quando muitos usuários simultâneos acessam a plataforma.
	Risco Associado:
•	Queda do Sistema: o sistema ficar indisponível ou retornar erros.

Concorrência e Conflito de Horários Simultâneos
	O que será verificado: 
•	Como a API e a transação de banco de dados se comportam quando dois usuários clicam para agendar a mesma vaga ao mesmo tempo.

	Risco Associado:
•	Inconsistência de Dados: O banco de dados aceitar o agendamento duplo, violando as regras do sistema.

Desempenho Quanto ao Envio Massivo de Notificações
	O que será verificado:
•	Se o processamento e o disparo das mensagens de confirmação ocorrem sem travamentos no momento em que o usuário clica em “Confirmar”.

	Risco Associado:
•	Travamento da Tela de Confirmação: O usuário ficar com a tela congelada, levando-o a clicar várias vezes, gerando requisições duplicadas

b)	Segurança:
Autenticação de Usuários e Controle de Acesso 
	O que Será Verificado:
•	Se o fluxo de cadastro/autenticação impede que um usuário comum acesse a área administrativa de gestão de horários.
•	Se tentativas de agendamento por usuários não logados são bloqueadas e redirecionadas para a tela de login.

	Risco Associado:
•	Invasão da Área Administrativa: Usuários comuns com o poder de alterar dados.

Proteção de Dados Pessoais e Sensíveis
	O que Será Verificado: 
•	Criptografia via protocolo HTTPS/TLS.
•	Se dados sensíveis estão armazenados de forma segura.

	Risco Associado:
•	Exposição de dados e penalidades legais: vazamentos de informações do paciente ou falhas de armazenamento, resultando em multas pesadas.

Gestão de Sessão e Desconexão Automática:
	O que Será Verificado:
•	Se a sessão do usuário é expirada automaticamente após um período definido de inatividade.
•	Se botão de “voltar” do navegador reabra uma área logada. 

	Risco Associado:  agendamento ou cancelamento de consultas via terceiros no nome do usuário em casos de dispositivos compartilhados.

Privacidade nas Notificações de Confirmação
	O que será verificado:
•	Se as notificações enviadas exibem apenas o mínimo necessário para a confirmação., omitindo dados sensíveis.

	Risco Associado:
•	Quebra de sigilo do paciente: pessoas com acesso à tela de notificação ou e-mail do usuário podem visualizar informações médicas confidenciais.

c)	Usabilidade:



d)	Compatibilidade:


