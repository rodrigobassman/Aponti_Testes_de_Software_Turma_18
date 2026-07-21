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

