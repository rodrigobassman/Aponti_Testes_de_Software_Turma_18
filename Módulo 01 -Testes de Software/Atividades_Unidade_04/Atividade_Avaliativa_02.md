Atividade Avaliativa Testes de Sistema e de Aceitação

Etapa 1:

Funcionalidade 01 – Login • Fluxo Principal

Login Simples: o usuário acessou a página do sistema bancário, digita CPF e senha corretamente e clicou em “Entrar”. O sistema valida os dados e autoriza o acesso.

Login com Reconhecimento Facial: o usuário faz o login por biometria, o sistema lê o rosto válido e autoriza o acesso.

• Variação de Fluxo

Senha Incorreta: O usuário digita uma senha incorreta e clicou em “Entrar”, O sistema rejeita e exibe: “CPF ou senha inválidos”.

Conta bloqueada por várias tentativas: o usuário digita a senha incorreta por três vezes consecutivas, o sistema bloqueia o acesso por segurança e exibe a mensagem: “Conta temporariamente bloqueada”.

Funcionalidade 02 – Acessar a Conta • Fluxo Principal:

Acesso simples: o sistema verifica se a sessão do usuário é válida após o login. O sistema redireciona o usuário para a tela principal de sua conta.

Acesso com validação de segurança: o dispositivo do usuário realiza o login por um novo. O sistema solicita a inserção de um código de verificação. O usuário digita o código correto, o sistema autoriza a nova sessão e redireciona para a tela principal.

• Variação de Fluxo:

Sessão Expirada por Inatividade: o sistema bloqueia o acesso e redireciona para a tela principal com a mensagem “Sessão expirada. Faça login novamente”.
Acesso Simultâneo: o usuário faz login em outro Smartphone, enquanto mantém a sessão atual aberta. O sistema ao invés de mostrar o painel, exibe uma mensagem: “Deseja sair da sessão atual?”.
Funcionalidade 03 – Visualizar Saldo Atual • Fluxo Principal

Exibição automática de saldo: o sistema faz a requisição do valor atual no banco de dados ao acessar a página principal.

Revelar Saldo Oculto: o sistema abre o painel com saldo oculto por privacidade. O usuário clicou no ícone de “olho” e o sistema exibe o valor do saldo.

• Variação de Fluxo

Falha na exibição do Saldo: o sistema carrega a página principal, mas apresenta a mensagem: “erro ao carregar o saldo” ao invés do saldo atual.

Conta inoperante: O sistema tenta buscar o saldo de uma conta que está em manutenção. O sistema exibe um aviso: “Consulta de saldo indisponível no momento.”
