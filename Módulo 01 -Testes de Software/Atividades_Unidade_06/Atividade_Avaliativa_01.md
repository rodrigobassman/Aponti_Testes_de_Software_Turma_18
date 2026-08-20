Atividade Avaliativa 01

1. Contexto do Módulo
Ator: Especialidades
Estado Inicial: Estar logado no sistema
O que realmente importa: Cadastrar especialidades
Resultado observável: Exibir lista das especialidades cadastradas

2. Cenário Principal
Feature: Cadastro de Nova Especialidade como administrador do sistema
  Quero preencher o formulário de nova especialidade
  Para cadastrar uma área de atuação médica ou profissional

 Cenário: Visualizar os campos do formulário de nova especialidade
    Given que o usuário está no formulário de 'Nova Especialidade'
    When visualiza a tela e observa os campos disponíveis
    Then o sistema exibe o campo 'Nome da especialidade'
    And exibe o campo 'Descrição'
    But não exibe o campo de identificação interna do sistema

   3. Cenário Alternativo

   Cenário: Tentar salvar a nova especialidade com campo obrigatório em branco
    Given que o usuário está no formulário de 'Nova Especialidade'
    When tenta salvar o registro sem preencher o 'Nome da especialidade'
    Then o sistema impede a conclusão do cadastro
    But exibe uma mensagem de alerta destacando o campo obrigatório em vermelho
