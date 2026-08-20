Atividade Avaliativa 02:

1. Cenário Principal
Feature: Gerenciamento de Especialidades
  Como administrador do sistema
  Quero visualizar e gerenciar as especialidades cadastradas
  Para manter o sistema atualizado

  Scenario: Visualizar a lista de especialidades cadastradas
    Given: que o usuário acessa a tela de 'Especialidades'
    When: visualiza a lista de registros e observa as opções exibidas
    Then: o sistema exibe as especialidades pré-cadastradas no banco de dados
    And: disponibiliza o campo 'Descrição' para edição
    But: restringe a alteração do 'Nome da especialidade' para garantir a integridade dos dados

  2. Cenário Alternativo
     Scenario: Tentar editar uma especialidade protegida do sistema
    Given: que o usuário acessa a tela de 'Especialidades'
    When: seleciona uma especialidade padrão do sistema para edição
    Then: o sistema permite a visualização dos dados
    But: impede a alteração ou exclusão do registro por ser uma especialidade protegida
