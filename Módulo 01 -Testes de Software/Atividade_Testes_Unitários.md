# Atividade Avaliativa de Testes Funcionais

---

## a) Quais testes seriam unitários?

* **Cálculo automático do valor total do pedido:** Validar se a função de cálculo multiplica corretamente a quantidade pelo preço de cada item (`quantidade * preço`) e retorna a soma correta.
* **Validação da regra "O pedido deve conter pelo menos um item":** Validar se o método responsável por processar o carrinho/pedido lança uma exceção ou retorna `false` caso a lista de itens esteja vazia (`quantidade = 0`).
* **Validação da regra "Após a confirmação, o pedido não pode ser alterado":** Testar a lógica da classe/objeto Pedido para garantir que, quando o atributo `status` for igual a `"Confirmado"`, qualquer método de alteração seja bloqueado.
* **Validação de formato dos dados no Cadastro de Usuários:** Validar se a entrada de dados rejeita formatos que não atendem às especificações técnicas.

> **Justificativa:** O foco dos **Testes Unitários** é validar a lógica interna de métodos e funções isoladas. No contexto do sistema, testa-se apenas algoritmos e estruturas de dados em memória. Não dependem de rede, interface de usuário ou banco de dados para rodar, sendo executados de forma instantânea e completamente isolada.

---

## b) Quais testes seriam de integração?

* **Consulta de catálogo de produtos no Banco de Dados:** Validar se a função do sistema consegue se conectar ao Banco de Dados de Produtos, enviar a busca e retornar a lista correta de itens com preços e estoques atualizados.
* **Autenticação de Usuários via serviço/API externa:** Validar se a chamada enviada pelo sistema para o Serviço de Autenticação consegue trafegar os dados de login (e-mail/senha), receber a validação e obter o *token* de acesso de volta com sucesso.
* **Envio e criação do pedido no Serviço de Pedidos:** Validar se, ao finalizar a compra, as informações do carrinho (itens, valores e cliente) são enviadas no formato correto para o Serviço de Pedidos e salvas na base de dados sem erros de comunicação.
* **Persistência do novo cadastro de usuário:** Validar se as informações preenchidas no Cadastro de Usuários são gravadas com sucesso na tabela de usuários do banco de dados e podem ser consultadas em seguida.

> **Justificativa:** No **Teste de Integração**, foca-se no "passe de bola" e na comunicação entre diferentes componentes. Testa-se como uma funcionalidade (ou pedaço do sistema) depende da resposta de outra para conseguir completar a transação com sucesso.

---

## c) Quais testes seriam de sistema?

* **Jornada Completa de Compra (Do Login ao Pagamento):** Validar se o usuário consegue realizar todo o fluxo: fazer login na aplicação, buscar um produto no catálogo, adicionar ao carrinho, preencher o endereço, selecionar a forma de pagamento e visualizar a tela de *"Compra Realizada com Sucesso"*.
* **Fluxo de Tentativa de Compra com Carrinho Vazio:** Validar a experiência do usuário de ponta a ponta ao tentar navegar até a tela de *checkout* sem itens adicionados, garantindo que o sistema exiba uma mensagem amigável na interface e bloqueie a finalização.
* **Jornada de Primeiro Acesso (Cadastro ao Primeiro Pedido):** Validar o fluxo completo de um novo cliente: criar a conta no formulário da tela, ser redirecionado para a página inicial já autenticado, navegar pelos produtos e concluir o primeiro pedido.
* **Fluxo de Recuperação de Senha no Navegador:** Validar se o usuário consegue clicar em *"Esqueci minha senha"*, receber o e-mail de redefinição, alterar a senha na tela e fazer o login com a nova credencial.

> **Justificativa:** Os **Testes de Sistema** (End-to-End / E2E) testam o software do ponto de vista do usuário final. Eles validam se o conjunto completo funciona de forma integrada no ambiente final: Interface Web + Código + Banco de Dados + Servidores + Redes.

---

## d) Quais testes seriam de aceitação?

* **Validação dos Critérios de Aceite das Regras de Negócio do Carrinho:** O dono do negócio (*Product Owner*) testando se o sistema aplica corretamente as regras comerciais (como frete grátis e cupons de desconto conforme regulamento).
* **Homologação do Fluxo Completo de Vendas (UAT / Beta Test):** Um grupo de usuários reais ou a equipe de negócios executando simulações de compras no ambiente de homologação para dar o aval ("carimbo final") antes de publicar o sistema em produção.
* **Validação de Conformidade e LGPD no Cadastro:** Testar e aprovar se o formulário de cadastro solicita e armazena o consentimento do uso de dados do cliente exatamente de acordo com os requisitos jurídicos e de *compliance* da empresa.
* **Teste de Acessibilidade e Usabilidade Comercial:** O cliente/contratante validando se as telas do SGP atendem aos padrões de usabilidade e acessibilidade estipulados no projeto.

> **Justificativa:** Nos **Testes de Aceitação**, valida-se se o sistema atende estritamente às regras de negócio e entrega o valor combinado nos requisitos do contrato. É a etapa em que os *stakeholders* confirmam que o produto atende às suas expectativas estratégicas.

