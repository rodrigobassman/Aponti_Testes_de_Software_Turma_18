Testes Não Funcionais
Atividade Avaliativa

Dado um sistema proposto, os alunos deverão elaborar um checklist de testes não funcionais, cobrindo obrigatoriamente:
•	Performance
•	Segurança
•	Usabilidade
•	Compatibilidade

Cada item do checklist deve indicar o que será verificado e qual o risco associado.

a)	Performance:
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

