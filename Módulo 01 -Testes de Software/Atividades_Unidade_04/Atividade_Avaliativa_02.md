# Atividade Avaliativa: Testes de Sistema e de Aceitação

---

## Etapa 1: Escopo das Funcionalidades e Cenários

### Funcionalidade 01 – Login
* **Fluxo Principal**
  1. **Login Simples:** O usuário acessa a página do sistema bancário, digita CPF e senha corretamente e clica em "Entrar". O sistema valida os dados e autoriza o acesso.
  2. **Login com Reconhecimento Facial:** O usuário faz o login por biometria, o sistema lê a face válida e autoriza o acesso.
* **Variação de Fluxo**
  1. **Senha Incorreta:** O usuário digita uma senha incorreta e clica em "Entrar". O sistema rejeita e exibe: "CPF ou senha inválidos".
  2. **Conta Bloqueada por Várias Tentativas:** O usuário digita a senha incorreta por três vezes consecutivas. O sistema bloqueia o acesso por segurança e exibe a mensagem: "Conta temporariamente bloqueada".

---

### Funcionalidade 02 – Acessar a Conta
* **Fluxo Principal**
  1. **Acesso Simples:** O sistema verifica que a sessão do usuário é válida após o login. O sistema redireciona o usuário para a tela principal da sua conta.
  2. **Acesso com Validação de Segurança:** O usuário realiza o login por um novo dispositivo. O sistema solicita a inserção de um código de verificação. O usuário digita o código correto, o sistema autoriza a nova sessão e redireciona para a tela principal.
* **Variação de Fluxo**
  1. **Sessão Expirada por Inatividade:** O sistema bloqueia o acesso e redireciona para a tela principal com a mensagem: "Sessão expirada. Faça login novamente".
  2. **Acesso Simultâneo:** O usuário faz login em outro Smartphone enquanto mantém a sessão atual aberta. O sistema, ao invés de mostrar o painel, exibe uma mensagem: "Deseja sair da sessão atual?".

---

### Funcionalidade 03 – Visualizar Saldo Atual
* **Fluxo Principal**
  1. **Exibição Automática do Saldo:** O sistema faz a requisição do valor atual no banco de dados ao carregar a página principal.
  2. **Revelar Saldo Oculto:** O sistema abre o painel com saldo oculto por privacidade. O usuário clica no ícone de "olho" e o sistema exibe o valor do saldo.
* **Variação de Fluxo**
  1. **Falha na Exibição do Saldo:** O sistema carrega a página principal, mas apresenta a mensagem: "Erro ao carregar o saldo" ao invés do saldo atual.
  2. **Conta Inoperante:** O sistema tenta buscar o saldo de uma conta que está em manutenção. O sistema exibe um aviso: "Consulta de saldo indisponível no momento.".

---

## Etapa 2: Tabela de Testes de Sistema

| ID | Título | Pré-condições | Passos | Resultado Esperado |
| :--- | :--- | :--- | :--- | :--- |
| **CT-FP-01** | Login Simples | 1. O sistema bancário está acessível.<br>2. O usuário possui CPF e senha válidos. | 1. Acessar a página do sistema bancário.<br>2. Digitar o CPF e a senha corretamente.<br>3. Clicar em "Entrar". | O sistema valida os dados com sucesso e autoriza o acesso do usuário. |
| **CT-VA-01** | Login com Senha Incorreta | 1. O sistema bancário está na tela de login. | 1. Digitar o CPF e uma senha incorreta.<br>2. Clicar no botão "Entrar". | O sistema rejeita o acesso e exibe a mensagem: "CPF ou senha inválidos". |
| **CT-FP-02** | Login com Reconhecimento Facial | 1. O aplicativo bancário está instalado.<br>2. O usuário possui biometria facial cadastrada. | 1. Selecionar a opção de login por biometria/reconhecimento facial.<br>2. Posicionar o rosto para a leitura do sistema. | O sistema lê a face válida e autoriza o acesso do usuário. |
| **CT-VA-02** | Bloqueio de Conta por Várias Tentativas | 1. O usuário possui conta ativa no sistema bancário. | 1. Digitar uma senha incorreta e clicar em "Entrar".<br>2. Repetir o processo mais duas vezes consecutivas (3 falhas no total). | O sistema bloqueia o acesso por segurança e exibe a mensagem: "Conta temporariamente bloqueada". |
| **CT-FP-03** | Acesso Simples à Conta | 1. O usuário realizou o login no sistema. | 1. Concluir a etapa de autenticação de login. | O sistema verifica que a sessão é válida e redireciona o usuário para a tela principal da sua conta. |
| **CT-VA-03** | Sessão Expirada por Inatividade | 1. O usuário está autenticado na sua conta. | 1. Permanecer sem realizar nenhuma interação no sistema por tempo superior ao limite. | O sistema bloqueia o acesso e redireciona para a tela principal com a mensagem: "Sessão expirada. Faça login novamente". |
| **CT-FP-04** | Acesso com Validação de Segurança | 1. O usuário está realizando o acesso a partir de um novo dispositivo. | 1. Realizar o login na conta em um novo dispositivo.<br>2. Receber a solicitação do código de verificação.<br>3. Digitar o código de verificação correto. | O sistema valida o código, autoriza a nova sessão e redireciona para a tela principal da conta. |
| **CT-VA-04** | Acesso Simultâneo | 1. O usuário possui uma sessão ativa aberta no Smartphone A. | 1. Efetuar login na mesma conta a partir de um Smartphone B. | O sistema intercepta o acesso no novo dispositivo e exibe a mensagem: "Deseja sair da sessão atual?". |
| **CT-FP-05** | Exibição Automática do Saldo | 1. O usuário possui acesso à tela principal da conta. | 1. Acessar a página principal da conta após o login. | O sistema faz a requisição do valor atual no banco de dados e exibe o saldo na página principal. |
| **CT-VA-05** | Falha na Exibição do Saldo | 1. O usuário realizou login com sucesso, mas o serviço de saldo está indisponível. | 1. Acessar a página principal da conta. | O sistema carrega a página principal, porém exibe a mensagem: "Erro ao carregar o saldo" no local do valor. |
| **CT-FP-06** | Revelar Saldo Oculto | 1. O usuário está no painel principal com o saldo oculto por privacidade. | 1. Localizar o campo de saldo no painel principal.<br>2. Clicar no ícone de "olho". | O sistema altera a exibição e apresenta o valor do saldo na tela. |
| **CT-VA-06** | Consulta de Saldo em Conta Inoperante | 1. A conta do usuário está em processo de manutenção no servidor. | 1. O sistema tenta buscar o saldo da conta durante o carregamento da página. | O sistema exibe o aviso: "Consulta de saldo indisponível no momento". |

---

## Etapa 3: Tabela de Testes de Aceitação

| ID | Título | Pré-condições | Passos | Resultado Esperado (Valor & Negócio) |
| :--- | :--- | :--- | :--- | :--- |
| **CT-TA-FP-01** | Aceitação de Login Simples | 1. O usuário possui conta ativa e credenciais válidas. | 1. Acessar a página de login.<br>2. Informar CPF e senha corretos.<br>3. Clicar em "Entrar". | **Valor ao Usuário:** Acesso rápido e seguro à sua conta bancária sem atritos ou barreiras desnecessárias. |
| **CT-TA-VA-01** | Proteção contra Credenciais Inválidas | 1. O usuário está na página de login. | 1. Informar CPF e senha incorreta.<br>2. Clicar em "Entrar". | **Expectativa do Negócio:** Impedir acessos não autorizados e proteger a conta contra invasões, informando o erro sem expor dados sensíveis. |
| **CT-TA-FP-02** | Aceitação de Agilidade por Biometria | 1. O usuário cadastrou sua face no app do banco. | 1. Selecionar o login por reconhecimento facial.<br>2. Posicionar o rosto para validação. | **Valor ao Usuário:** Praticidade e conveniência de acessar o banco em segundos sem precisar digitar senhas em locais públicos. |
| **CT-TA-VA-02** | Proteção de Conta contra Força Bruta | 1. A conta do usuário está ativa no sistema. | 1. Errar a senha por 3 vezes consecutivas. | **Expectativa do Negócio:** Mitigar ataques automatizados de força bruta, bloqueando a conta temporariamente e garantindo o patrimônio do cliente. |
| **CT-TA-FP-03** | Continuidade e Fluidez da Sessão | 1. O usuário acabou de se autenticar com sucesso. | 1. Aguardar o direcionamento após a validação da sessão. | **Valor ao Usuário:** Experiência contínua e sem interrupções, permitindo iniciar suas operações financeiras imediatamente. |
| **CT-TA-VA-03** | Encerramento de Sessão Inativa para Segurança | 1. O usuário está com o app aberto na tela da conta. | 1. Deixar o sistema inativo sem nenhuma interação por tempo prolongado. | **Expectativa do Negócio:** Proteger os dados e o saldo do cliente caso ele esqueça o celular desbloqueado em local público. |
| **CT-TA-FP-04** | Validação de Segurança em Novo Dispositivo | 1. O usuário está tentando acessar por um aparelho não cadastrado. | 1. Fazer login no novo dispositivo.<br>2. Digitar o código de verificação enviado ao seu canal seguro. | **Valor ao Usuário & Negócio:** Equilíbrio entre usabilidade e alta segurança (2FA), garantindo que apenas o verdadeiro titular autorize novos aparelhos. |
| **CT-TA-VA-04** | Prevenção de Acessos Duplos / Simultâneos | 1. O usuário já possui uma sessão ativa no Smartphone A. | 1. Iniciar uma nova sessão na mesma conta pelo Smartphone B. | **Expectativa do Negócio:** Evitar conflitos de transações, fraudes de uso concorrente e alertar o usuário caso sua conta esteja sendo acessada em outro local. |
| **CT-TA-FP-05** | Transparência e Clareza na Informação Financeira | 1. O usuário está logado e no painel principal. | 1. Carregar a tela inicial da conta. | **Valor ao Usuário:** Acesso imediato à sua informação financeira para tomada de decisão e controle do seu orçamento. |
| **CT-TA-VA-05** | Transparência em Caso de Indisponibilidade Técnica | 1. O serviço de consulta de saldo está fora do ar. | 1. Carregar a página principal. | **Valor ao Usuário:** Comunicação clara de falha temporária, evitando que o cliente pense que seu dinheiro sumiu ou que a conta foi zerada. |
| **CT-TA-FP-06** | Privacidade Financeira (Modo Discreto) | 1. O saldo inicia oculto por padrão na tela. | 1. Clicar no ícone de "olho" quando desejar visualizar o valor. | **Valor ao Usuário:** Privacidade para consultar o aplicativo em locais públicos ou perto de terceiros sem expor sua vida financeira. |
| **CT-TA-VA-06** | Gestão de Expectativa em Contas em Manutenção | 1. A conta do cliente passa por manutenção programada. | 1. Tentar visualizar o saldo na tela principal. | **Expectativa do Negócio:** Manter o cliente informado sobre o status da conta, reduzindo chamados desnecessários no suporte/SAC durante manutenções. |

---

## Etapa 4: Classificação e Justificativa dos Testes

| Funcionalidade | Classificação | Justificativa |
| :--- | :--- | :--- |
| **01. Login Simples**<br>*(Fluxo Principal)* | **Teste de Aceitação** | **Objetivo:** Garantir que o usuário consiga acessar a conta sem atritos.<br>**Ponto de Vista:** Usuário / Negócio.<br>**Tipo de Validação:** Valida a entrega de valor no fluxo principal de entrada no banco. |
| **01. Senha Incorreta**<br>*(Variação de Fluxo)* | **Teste de Sistema** | **Objetivo:** Validar o tratamento técnico de entradas inválidas.<br>**Ponto de Vista:** Técnico (QA / Desenvolvimento).<br>**Tipo de Validação:** Valida se o sistema bloqueia os dados e retorna a mensagem de erro esperada. |
| **01. Reconhecimento Facial**<br>*(Fluxo Principal)* | **Teste de Aceitação** | **Objetivo:** Oferecer um método rápido, prático e moderno de acesso.<br>**Ponto de Vista:** Usuário.<br>**Tipo de Validação:** Valida a conveniência e a usabilidade de logar sem digitar senhas. |
| **01. Conta Bloqueada por Tentativas**<br>*(Variação de Fluxo)* | **Teste de Sistema** | **Objetivo:** Validar a regra de contagem interna e o mecanismo de segurança.<br>**Ponto de Vista:** Técnico.<br>**Tipo de Validação:** Valida se o contador atinge 3 falhas e altera o status da conta no sistema. |
| **02. Acesso Simples à Conta**<br>*(Fluxo Principal)* | **Teste de Aceitação** | **Objetivo:** Garantir a navegação fluida após a autenticação.<br>**Ponto de Vista:** Usuário.<br>**Tipo de Validação:** Valida a expectativa do cliente de ser levado direto ao painel da sua conta. |
| **02. Sessão Expirada por Inatividade**<br>*(Variação de Fluxo)* | **Teste de Sistema** | **Objetivo:** Validar o temporizador (*timeout*) e o encerramento automático da sessão.<br>**Ponto de Vista:** Técnico.<br>**Tipo de Validação:** Valida se a aplicação encerra a conexão após o tempo limite sem interação. |
| **02. Validação em Novo Dispositivo**<br>*(Fluxo Principal)* | **Teste de Aceitação** | **Objetivo:** Autorizar a entrada em novos aparelhos com segurança.<br>**Ponto de Vista:** Usuário / Negócio.<br>**Tipo de Validação:** Valida a experiência do titular ao cadastrar e validar um novo dispositivo. |
| **02. Acesso Simultâneo**<br>*(Variação de Fluxo)* | **Teste de Sistema** | **Objetivo:** Validar o controle de concorrência de múltiplas conexões.<br>**Ponto de Vista:** Técnico.<br>**Tipo de Validação:** Valida a capacidade do software de detectar duas sessões ativas e exibir a tela de confirmação. |
| **03. Exibição Automática do Saldo**<br>*(Fluxo Principal)* | **Teste de Aceitação** | **Objetivo:** Entregar a informação financeira de forma clara e imediata.<br>**Ponto de Vista:** Usuário.<br>**Tipo de Validação:** Valida a satisfação da necessidade básica do cliente ao abrir o aplicativo. |
| **03. Falha na Exibição do Saldo**<br>*(Variação de Fluxo)* | **Teste de Sistema** | **Objetivo:** Validar o tratamento de exceção em caso de queda de servidor/API.<br>**Ponto de Vista:** Técnico.<br>**Tipo de Validação:** Valida se o sistema trata a falha de requisição em vez de quebrar a tela do aplicativo. |
| **03. Revelar Saldo Oculto**<br>*(Fluxo Principal)* | **Teste de Aceitação** | **Objetivo:** Proporcionar privacidade ao cliente em ambientes públicos.<br>**Ponto de Vista:** Usuário.<br>**Tipo de Validação:** Valida o recurso de proteção visual do saldo atendendo à escolha do usuário. |
| **03. Conta Inoperante**<br>*(Variação de Fluxo)* | **Teste de Sistema** | **Objetivo:** Validar a checagem de status do banco de dados durante manutenções.<br>**Ponto de Vista:** Técnico.<br>**Tipo de Validação:** Valida se a flag de manutenção é identificada e dispara o aviso de indisponibilidade. |

---

## Etapa 5: Discussão e Conclusão

*Concluída em sala de aula (Raciocínio correto de Caio).*
