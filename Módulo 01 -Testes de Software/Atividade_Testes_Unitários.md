Atividade Avaliativa de Testes Funcionais

Dado um sistema fictício, os alunos deverão analisar suas funcionalidades e indicar:
a)	Quais testes seriam unitários?
•	Cálculo automático do valor total do pedido: Validar se a função de cálculo multiplica corretamente a quantidade * preço de cada item e retorna a soma correta.
•	Validação da regra "O pedido deve conter pelo menos um item": Validar se o método responsável por processar o carrinho/pedido lança um erro/exceção ou retorna false caso a lista de itens esteja vazia (quantidade = 0).
•	Validação da regra "Após a confirmação, o pedido não pode ser alterado": Testar a lógica da classe/objeto Pedido para garantir que, quando o atributo status for igual a "Confirmado", qualquer método de alteração seja bloqueado.
•	Validação de formato dos dados no Cadastro de Usuários: Validar se a entrada de dados aceita formatos diferentes das especificações.
	Justificativa: O foco dos Testes Unitários é validar a lógica interna de métodos e funções isoladas. E no caso do Sistema Fictício, é necessário testar apenas algoritmos e estruturas de dados na memória. Não dependendo da rede, da interface do usuário nem do banco de dados para rodar, sendo executados de forma instantânea e isolada.

b)	Quais testes seriam de integração?
• Consulta de catálogo de produtos no Banco de Dados: Validar se a função do sistema consegue se conectar ao Banco de Dados de Produtos, enviar a busca e retornar a lista correta de itens com preços e estoques atualizados.
• Autenticação de Usuários via serviço/API externa: Validar se a chamada enviada pelo sistema para o Serviço de Autenticação consegue trafegar os dados de login (e-mail/senha), receber a validação e obter o token de acesso de volta com sucesso.
• Envio e criação do pedido no Serviço de Pedidos: Validar se, ao finalizar a compra, as informações do carrinho (itens, valores e cliente) são enviadas no formato correto para o Serviço de Pedidos e salvas na base de dados sem erros de comunicação.
• Persistência do novo cadastro de usuário: Validar se as informações preenchidas no Cadastro de Usuários são gravadas com sucesso na tabela de usuários do banco de dados e podem ser consultadas em seguida.
	Justificativa: No Teste de Integração, uma funcionalidade (ou pedaço do sistema) depende da resposta de outra para conseguir completar o trabalho.

c) Quais testes seriam de sistema?
• Jornada Completa de Compra (Do Login ao Pagamento): Validar se o usuário consegue realizar todo o fluxo: fazer login na aplicação, buscar um produto no catálogo, adicionar ao carrinho, preencher o endereço, selecionar a forma de pagamento e receber a tela de "Compra Realizada com Sucesso".
• Fluxo de Tentativa de Compra com Carrinho Vazio: Validar a experiência do usuário de ponta a ponta ao tentar navegar até a tela de checkout sem itens adicionados, garantindo que o sistema exiba a mensagem amigável na tela e bloqueie a finalização.
• Jornada de Primeiro Acesso (Cadastro ao Primeiro Pedido): Validar o fluxo completo de um novo cliente: criar a conta no formulário da tela, ser redirecionado para a página inicial já autenticado, navegar pelos produtos e concluir o primeiro pedido.
• Fluxo de Recuperação de Senha no Navegador: Validar se o usuário consegue clicar em "Esqueci minha senha", receber o e-mail de redefinição, alterar a senha na tela e fazer o login com a nova credencial.
	Justificativa: Ele testa se o conjunto completo funciona junto no ambiente final: tela Web + código + banco de dados + servidores + internet.

d) Quais testes seriam de aceitação?
•	validação dos Critérios de Aceite das Regras de Negócio do Carrinho: O dono do negócio testando se o sistema aplica corretamente as regras comerciais;
•	Homologação do Fluxo Completo de Vendas: Um grupo de usuários reais ou a equipe de negócios executando simulações de compras reais no ambiente de homologação para dar o "ok" antes do sistema ir para o ar.
•	Validação de Conformidade e LGPD no Cadastro: Testar e aprovar se o formulário de cadastro de usuários solicita e armazena o consentimento do uso de dados do cliente exatamente de acordo com os requisitos jurídicos e de compliance da empresa.
•	Teste de Acessibilidade e Usabilidade Comercial: O cliente/contratante validando se as telas do SGP atendem aos padrões estipulados de usabilidade (se é fácil para o cliente final usar) e acessibilidade exigidos no projeto.
	Justificativa: No Teste de Aceitação, validamos se o sistema atende às regras do negócio e entrega o valor que foi combinado no contrato/requisitos.

