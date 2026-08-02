Atividade Avaliativa
Testes de Sistema e de Aceitação

Etapa 1:

Funcionalidade 01 – Login
•	Fluxo Principal
1.	Login Simples: o usuário acessa a página do sistema bancário, digita CPF e senha corretamente e clica em “Entrar”. O sistema valida os dados e autoriza o acesso.

2.	Login com Reconhecimento Facial:  o usuário faz o login por biometria, o sistema lê a face válida e autoriza o acesso.

•	Variação de Fluxo
1.	 Senha Incorreta: O usuário digita uma senha incorreta e clica em “Entrar”, O sistema rejeita e exibe: “CPF ou senha inválidos”.

2.	Conta Bloqueada por Várias Tentativas: o usuário digita a senha incorreta por três vezes consecutivas, o sistema bloqueia o acesso por segurança e exibe a mensagem: “Conta temporariamente bloqueada”.

Funcionalidade 02 – Acessar a Conta
•	Fluxo Principal: 
1.	Acesso simples: o sistema verifica que a sessão do usuário é válida após o login. O sistema redireciona o usuário para a tela principal da sua conta.

2.	Acesso com validação de segurança: o usuário realiza o login por um novo dispositivo. O sistema solicita a inserção de um código de verificação. O usuário digita o código correto, o sistema autoriza a nova sessão e redireciona para a tela principal.

•	Variação de Fluxo: 
1.	Sessão Expirada por Inatividade: o sistema bloqueia o acesso e redireciona para a tela principal com a mensagem “Sessão expirada. Faça login novamente”.
2.	Acesso Simultâneo: o usuário faz login em outro Smartphone, enquanto mantém a sessão atual aberta. O sistema ao invés de mostrar o painel, exibe uma mensagem: “Deseja sair da sessão atual? ”.
3.	
Funcionalidade 03 – Visualizar Saldo Atual
•	Fluxo Principal
1.	Exibição automática do saldo: o sistema faz a requisição do valor atual no banco de dados ao carregar a página principal.

2.	Revelar Saldo Oculto: o sistema abre o painel com saldo oculto por privacidade. O usuário clica no ícone de “olho” e o sistema exibe o valor do saldo. 

•	Variação de Fluxo
1.	  Falha na exibição do Saldo: o sistema carrega a página principal, mas apresenta a mensagem: “erro ao carregar o saldo” ao invés do saldo atual.

2.	Conta inoperante: O sistema tenta buscar o saldo de uma conta que está em manutenção. O sistema exibe um aviso: “Consulta de saldo indisponível no momento. ”
