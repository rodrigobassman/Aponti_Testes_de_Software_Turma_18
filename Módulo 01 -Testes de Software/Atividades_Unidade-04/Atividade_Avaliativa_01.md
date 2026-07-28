Atividade Avaliativa:

A partir de comportamentos esperados em uma tela de login, crie pelo menos 10 casos de testes completos, aplicando os conceitos e estruturas vistos em aula.
Além do caminho feliz, pense em cenários alternativos que um bom tester faria (fora da caixinha)
Lembre-se: Linguagem clara e objetiva, steps bem separados, resultado esperado observável e sem termos genéricos.

| ID | TÍTULO | PRÉCONDIÇÕES | RESULTADO ESPERADO |
|---|---|---|---|
| **CT01** | No campo do e-mail, aceitar letras e números | O usuário está na tela de login. | O sistema aceita e exibe corretamente letras e números no campo de e-mail. |
| **CT02** | No campo senha, aceitar apenas números | O usuário está na tela de login. | O sistema restringe a entrada e aceita apenas caracteres numéricos no campo de senha. |
| **CT03** | Aceitar CPF inválido | O usuário está na tela de login e o sistema utiliza CPF. | O sistema identifica a inconsistência, não prossegue com o login e exibe mensagem de erro de CPF inválido. |
| **CT04** | Aceitar CPF com número excedente | O usuário está na tela de login. | O sistema impede a digitação de dígitos extras além do limite de 11 números do CPF. |
| **CT05** | Não reconhecer usuário cadastrado | O usuário está na tela de login com dados inexistentes na base. | O sistema recusa o acesso e exibe mensagem de usuário não encontrado ou inválido. |
| **CT06** | Usuário fazer modificações no cadastro | O usuário está autenticado e na tela de perfil. | O sistema permite alterar e salvar os dados cadastrais permitidos com sucesso. |
| **CT07** | Não aceitar mudança de e-mail | O usuário está logado nas configurações de perfil. | O sistema bloqueia a alteração direta do e-mail principal por razões de segurança. |
| **CT08** | Dificuldade para conseguir recuperar usuário ou senha | O usuário está na tela de login e acessa o fluxo de recuperação. | O sistema processa o pedido ou registra a falha de envio/instabilidade conforme o comportamento do fluxo. |
| **CT09** | Bloqueio por excesso de erros | O usuário está na tela de login. | O sistema bloqueia temporariamente o acesso após várias tentativas consecutivas de senha errada. |
| **CT10** | Sucesso no acesso | O usuário possui cadastro ativo e correto. | O sistema autentica as credenciais e redireciona o usuário para a página principal (dashboard). |
