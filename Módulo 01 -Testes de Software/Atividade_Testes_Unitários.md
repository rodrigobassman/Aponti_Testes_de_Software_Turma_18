Atividade Avaliativa de Testes Funcionais

Dado um sistema fictício, os alunos deverão analisar suas funcionalidades e indicar:
a)	Quais testes seriam unitários?
•	Cálculo automático do valor total do pedido: Validar se a função de cálculo multiplica corretamente a quantidade * preço de cada item e retorna a soma correta.
•	Validação da regra "O pedido deve conter pelo menos um item": Validar se o método responsável por processar o carrinho/pedido lança um erro/exceção ou retorna false caso a lista de itens esteja vazia (quantidade = 0).
•	Validação da regra "Após a confirmação, o pedido não pode ser alterado": Testar a lógica da classe/objeto Pedido para garantir que, quando o atributo status for igual a "Confirmado", qualquer método de alteração seja bloqueado.
•	Validação de formato dos dados no Cadastro de Usuários: Validar se a entrada de dados aceita formatos diferentes das especificações.
	Justificativa: O foco dos Testes Unitários é validar a lógica interna de métodos e funções isoladas. E no caso do Sistema Fictício, é necessário testar apenas algoritmos e estruturas de dados na memória. Não dependendo da rede, da interface do usuário nem do banco de dados para rodar, sendo executados de forma instantânea e isolada.
b)	Quais testes seriam de integração
c)	Quais testes seriam de sistema
