Atividade Avaliativa 01

1. Contexto do Módulo
Ator: Especialidades
Estado Inicial: Estar logado no sistema
O que realmente importa: Cadastrar especialidades
Resultado observável: Exibir lista das especialidades cadastradas

2. Cenários (Gherkin)
Cenário Principal: Cadastro de Especialidade
Background: Acessar a página de especialidades Given: Nenhuma especialidade cadastrada

Cenário: cadastrar nova especialidade

Given: página de cadastro acessada
When: cadastro feito
Then: nome da especialidade e descrição são exibidas
And: cadastro realizado com sucesso
