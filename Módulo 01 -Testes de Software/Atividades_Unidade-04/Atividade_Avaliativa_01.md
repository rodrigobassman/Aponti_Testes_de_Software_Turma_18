# Atividade Avaliativa - Casos de Teste

| ID | Título | Pré-condições | Passos | Resultado Esperado |
| :--- | :--- | :--- | :--- | :--- |
| **CT01** | No campo do e-mail, aceitar letras e números | O usuário está na tela de login. | 1. Clicar no campo de e-mail<br>2. Digitar letras e números | O sistema aceita e exibe corretamente letras e números no campo de e-mail. |
| **CT02** | No campo senha, aceitar apenas números | O usuário está na tela de login. | 1. Clicar no campo de senha<br>2. Tentar inserir caracteres que não sejam números | O sistema restringe a entrada e aceita apenas caracteres numéricos no campo de senha. |
| **CT03** | Aceitar CPF inválido | O usuário está na tela de login e o sistema utiliza CPF. | 1. Inserir um CPF inválido no campo correspondente<br>2. Tentar prosseguir com o login | O sistema identifica a inconsistência, não prossegue com o login e exibe mensagem de erro de CPF inválido. |
| **CT04** | Aceitar CPF com número excedente | O usuário está na tela de login. | 1. Tentar digitar um número de CPF com mais de 11 dígitos | O sistema impede a digitação de dígitos extras além do limite de 11 números do CPF. |
| **CT05** | Não reconhecer usuário cadastrado | O usuário está na tela de login com dados inexistentes na base. | 1. Inserir dados de usuário inexistentes<br>2. Tentar realizar o login | O sistema recusa o acesso e exibe mensagem de usuário não encontrado ou inválido. |
| **CT06** | Usuário fazer modificações no cadastro | O usuário está autenticado e na tela de perfil. | 1. Realizar alterações nos dados permitidos<br>2. Salvar as alterações | O sistema permite alterar e salvar os dados cadastrais permitidos com sucesso. |
| **CT07** | Não aceitar mudança de e-mail | O usuário está logado nas configurações de perfil. | 1. Tentar alterar o endereço de e-mail principal diretamente | O sistema bloqueia a alteração direta do e-mail principal por razões de segurança. |
| **CT08** | Dificuldade para conseguir recuperar usuário ou senha | O usuário está na tela de login e acessa o fluxo de recuperação. | 1. Clicar na opção de recuperar usuário/senha<br>2. Tentar seguir o fluxo de recuperação | O sistema processa o pedido ou registra a falha de envio/instabilidade conforme o comportamento do fluxo. |
| **CT09** | Bloqueio por excesso de erros | O usuário está na tela de login. | 1. Inserir senhas incorretas consecutivas até atingir o limite de tentativas | O sistema bloqueia temporariamente o acesso após várias tentativas consecutivas de senha errada. |
| **CT10** | Sucesso no acesso | O usuário possui cadastro ativo e correto. | 1. Inserir e-mail e senha válidos e corretos<br>2. Confirmar o login | O sistema autentica as credenciais e redireciona o usuário para a página principal (dashboard). |
