Atividade Avaliativa 03:
Comparar o mesmo comportamento do sistema usando duas abordagens diferentes.
Criar um cenário BDD e um cenário Tradicional
Responder:

Qual o formato mais fácil de escrever?
O teste de sistema é mais fácil de pensar e documentar.

Qual comunica melhor o comportamento?
O teste BDD comunica melhor o comportamento do sistema com
visão ampla.

Qual seria mais fácil de manter?
O BDD é melhor de compreender e manter, pois permite uma visão melhor para correção de Bugs.

Cenário BDD:
Given: que o usuário está no formulário de 'Nova Especialidade'
When: preenche o campo 'Nome da especialidade' com um nome já existente e clica em 'Salvar'
And: aguarda o envio do formulário
Then: o sistema exibe uma mensagem informando que a especialidade já está cadastrada
And: bloqueia a criação do registro duplicado

Teste de Sistema
ID: CT-FP-01
Título: Cadastro de especialidades
Pré-condições: O usuário estar logado como Administrador.
Passos:
1.Acessar a página especialidades
2. Preencher o nome da especialidade e a descrição
Resultado Esperado
3. Clicar em "Salvar Cadastro".
Resultado Esperado: O sistema valida os dados com sucesso e cadastra a nova especialidade.

Id: CT-VA-01
Título: Formulário de cadastro ambíguo
Pré-condições: O usuário estar logado como Administrador.
Passos:
1. preencher o campo "Nome" com o nome do médico e o campo "Descrição" com a especialidade.
2. Clicar em "Salvar Cadastro".

