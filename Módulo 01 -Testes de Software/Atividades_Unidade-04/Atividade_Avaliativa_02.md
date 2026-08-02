Atividade Avaliativa
Testes de Sistema e de Aceitação

Etapa 1:

Funcionalidade 01 – Login
	Fluxo Principal: o usuário acessa a página do sistema bancário, digita CPF e senha corretamente e clica em “Entrar”. O sistema valida os dados de entrada com sucesso e permite o acesso.
	Variação de Fluxo:  o usuário digita a senha incorreta, o sistema identifica a divergência, nega o acesso e exibe a mensagem: “CPF ou senha inválidos”. Por desespero/ansiedade, o usuário digita a senha incorreta mais duas vezes consecutivas. O sistema bloqueia o acesso.

Funcionalidade 02 – Acessar a Conta
	Fluxo Principal: O sistema verifica que a sessão do usuário é válida após o login. O sistema redireciona o usuário para a tela principal da sua conta.
	Variação de Fluxo: o usuário tenta acessar a tela principal da conta, mas a sessão expirou por inatividade. O sistema bloqueia o acesso e redireciona para a tela principal com a mensagem “Sessão expirada. Faça login novamente”.

Funcionalidade 03 – Visualizar Saldo Atual
	Fluxo Principal: o sistema faz a requisição do valor atual no banco de dados ao carregar a página principal.
	Variação de Fluxo:  o sistema carrega a página principal, mas apresenta a mensagem: “erro ao carregar o saldo” ao invés do saldo atual.

