Atividade Avaliativa 02:

Teste de Sistema
ID: CT-FP-01 
Título: Cadastro de especialidades 
Pré-condições: O usuário estar logado como Administrador. 
Passos: 1.Acessar a página especialidades 
2. Preencher o nome da especialidade e a descrição Resultado Esperado 
3. Clicar em "Salvar Cadastro". 
Resultado Esperado: O sistema valida os dados com sucesso e cadastra a nova especialidade.

Id: CT-VA-01 Título: Formulário de cadastro ambíguo 
Pré-condições: O usuário estar logado como Administrador. 
Passos:
1.preencher o campo "Nome" com o nome do médico e o campo "Descrição" com a especialidade.
2.Clicar em "Salvar Cadastro".
Resultado esperado: O usuário pode cadastrar o nome da especialidade
no campo "Nome" e o Médico especialista no campo "Descrição" ou
o médico no campo "Nome" e a especialidade no campo "Descrição".

ID: CT-FP-02
Título: Consultar Especialidades pré-cadastradas
Pré-condições:  O usuário estar logado como Administrador.
Passos:
1. Acessar a página de especialidades
2. Consultar as especialidades cadastradas
Resultado esperado: exibir as especialidades existentes

ID: CT-VA-02
Título: Especialidades inexistentes
Pré-condições: O usuário estar logado como Administrador.
Passos:
1.Acessar a página de Especialidades
2.consultar especialidades cadastradas
Resultado esperado: O sistema permite o cadastro, mesmo sem uma especialidade pré-cadastrada.

ID: CT-FP-03
Título: Mensagem de validação de cadastro
Pré-condições:O usuário estar logado como Administrador.
Passos:
1.O usuário preenche todos os campos corretamente
2. O sistema valida os dados
3.Clicar em "Salvar Cadastro".
Resultado esperado: exibir mensagem "Cadastro feito com sucesso!"

ID: CT-VA-03
Título: Ausência de confirmação de cadastro.
Pré-condições: O usuário estar logado como Administrador.
Passos:
1.O usuário preenche todos os campos corretamente
2. O sistema valida os dados
3.Clicar em "Salvar Cadastro".
Resultado esperado: a nova especialidade fica disponível, mas o sistema não exibe mensagem de sucesso.

ID: CT-FP-04
Título: Pré-cadastro de médico especialista
Pré-condições: O usuário estar logado como Administrador.
Passos:
1.O usuário acessa a página de especialidades
2.O usuário preenche os campos do formulário
3. O usuário clica em "salvar cadastro".
Resultado esperado: Ao acessar o campo nome, o sistema aciona o 
sistema de autopreenchimento e carrega as especialidades existentes.

ID: CT-VA-04
Título: Não existe cadastro do médico especialista
Pré-condições:O usuário estar logado como Administrador.
Passos:
1.O usuário inicia o cadastro da nova especialidade e o sistema não
sugere um médico associado a especialidade
2. O usuário clica em "salvar cadastro".
Resultado esperado: Como não existe o cadastro do médico especialista, o sistema aceita o cadastro normalmente, ocasionando
transtornos em marcações de consultas.

ID: CT-FP-05
Título: Validação de duplicidade no cadastro da especialidade
Pré-condições: O usuário clica em "salvar cadastro".
Passos:
1.O usuário acessa a página de especialidades
2.O usuário cadastra uma nova especialidade
3.O usuário clica em "salvar cadastro".
Resultado esperado: O sistema valida se existe duplicidade no cadastro.

ID: CT-VA-05
Título: Validação de duplicidade no cadastro da especialidade
Pré-condições: O usuário clica em "salvar cadastro".
Passos:
1.O usuário acessa a página de especialidades
2.O usuário cadastra uma nova especialidade
3.O usuário clica em "salvar cadastro".
Resultado esperado: a validação falha e o sistema permite o cadastro duplicado.
