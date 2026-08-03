# Atividade Avaliativa: Tipos de Teste (Smoke, Sanidade e Regressão)

---

## 🟢 1. Testes de Smoke (Fumaça)

> **Objetivo:** Verificar se as funcionalidades mais críticas e vitais do aplicativo estão de pé. Se algum desses falhar, o build é rejeitado imediatamente.

### CT-SM-01: Inicialização do App
* **Cenário:** Abrir o aplicativo bancário a partir da tela inicial do celular.
* **Resultado Esperado:** O app carrega sem fechar sozinho (*crash*) e exibe a tela inicial de autenticação.
* **Justificativa:** Se o aplicativo nem abre, não há como realizar nenhum outro teste.

### CT-SM-02: Carregamento da Tela de Login
* **Cenário:** Visualizar os campos de CPF, Senha e botão "Entrar".
* **Resultado Esperado:** Todos os elementos da tela de login estão visíveis e interativos.
* **Justificativa:** Garante que a porta de entrada da aplicação está acessível ao usuário.

### CT-SM-03: Autenticação com Sucesso
* **Cenário:** Digitar CPF e senha válidos e clicar em "Entrar".
* **Resultado Esperado:** O sistema autentica e navega para o Dashboard (Home) da conta.
* **Justificativa:** O login é o fluxo principal; se a autenticação falhar, todo o sistema fica inacessível.

### CT-SM-04: Carregamento do Dashboard Principal
* **Cenário:** Acessar o painel principal após o login.
* **Resultado Esperado:** O painel carrega com o menu principal, atalhos e a área de saldo visível.
* **Justificativa:** Confirma que o servidor está respondendo e entregando a interface pós-login.

### CT-SM-05: Encerramento de Sessão (Logout)
* **Cenário:** Clicar no botão "Sair".
* **Resultado Esperado:** A sessão é encerrada e o usuário retorna à tela inicial de login.
* **Justificativa:** Garante que a sessão pode ser encerrada com segurança, fechando o ciclo básico de uso.

---

## 🟡 2. Testes de Sanidade

> **Objetivo:** Foco estrito nas alterações e correções recém-feitas (Correção no Login e Ajuste no Saldo). Avalia se as modificações específicas funcionam como esperado sem aprofundar na aplicação inteira.

### CT-SA-01: Validação do Fechamento Inesperado no Login (Bug Fix)
* **Cenário:** Inserir credenciais válidas e efetuar o login.
* **Resultado Esperado:** A autenticação é concluída sem travar o app no momento da validação das credenciais.
* **Justificativa:** Testa diretamente o ponto corrigido no código de login para confirmar que a falha técnica foi sanada.

### CT-SA-02: Exibição do Saldo com Ajuste de Layout/Formatação
* **Cenário:** Carregar o saldo na tela inicial pós-login.
* **Resultado Esperado:** O valor do saldo aparece formatado corretamente (ex: `R$ 1.250,50`) sem sobrepor outros elementos gráficos.
* **Justificativa:** Valida a alteração visual/funcional feita especificamente no componente de saldo.

### CT-SA-03: Ocultar e Revelar Saldo (Ícone do Olho)
* **Cenário:** Clicar no ícone de ocultar/exibir saldo no painel inicial.
* **Resultado Esperado:** O saldo alterna corretamente entre o valor real e o modo mascarado (`R$ ****`).
* **Justificativa:** Garante que o comportamento interativo da área do saldo ajustada continua operando com precisão.

### CT-SA-04: Login com Biometria Facial / Digital
* **Cenário:** Tentar logar utilizando a leitura biométrica cadastrada.
* **Resultado Esperado:** O sistema reconhece a biometria e efetua o login sem erros.
* **Justificativa:** Como o login passou por manutenção, é crucial testar a rota alternativa de autenticação para validar o pacote de login.

### CT-SA-05: Atualização Manual do Saldo (Pull-to-Refresh)
* **Cenário:** Deslizar a tela principal para baixo para recarregar as informações financeiras.
* **Resultado Esperado:** A requisição é enviada ao servidor e o saldo é atualizado na tela.
* **Justificativa:** Testa a comunicação da área ajustada do saldo com a API de contas em tempo real.

---

## 🔴 3. Testes de Regressão

> **Objetivo:** Testar as funcionalidades antigas que NÃO foram alteradas para garantir que a nova versão do código não quebrou nada que já funcionava.

### CT-RE-01: Realização de Transferência via Pix
* **Cenário:** Inserir uma chave Pix, digitar um valor e confirmar com a senha transacional.
* **Resultado Esperado:** A transferência é concluída e o comprovante é gerado.
* **Justificativa:** Garante que mexer no login e na tela de saldo não afetou o motor de transações financeiras.

### CT-RE-02: Pagamento de Boleto com Código de Barras
* **Cenário:** Ler ou digitar a linha digitável de um boleto e efetivar o pagamento.
* **Resultado Esperado:** O sistema valida o boleto, deduz o valor e confirma o pagamento.
* **Justificativa:** Certifica que as regras de negócio de pagamentos continuam íntegras pós-deploy.

### CT-RE-03: Extrato Financeiro e Histórico de Transações
* **Cenário:** Navegar até a aba de Extrato e filtrar lançamentos dos últimos 30 dias.
* **Resultado Esperado:** A lista de entradas e saídas carrega corretamente com datas e descrições.
* **Justificativa:** Verifica se a busca de histórico no banco de dados não foi impactada pelas mudanças na home.

### CT-RE-04: Validação de Bloqueio por Tentativas Incorretas no Login
* **Cenário:** Errar a senha 3 vezes consecutivas.
* **Resultado Esperado:** O sistema exibe o aviso de bloqueio temporário e nega novos acessos.
* **Justificativa:** Assegura que as regras de segurança e proteção do sistema de login antigo continuam ativas após a correção do bug.

### CT-RE-05: Contratação/Consulta de Empréstimo ou Cartões
* **Cenário:** Acessar o menu de "Cartões" ou "Empréstimos" e visualizar os limites disponíveis.
* **Resultado Esperado:** As informações de crédito do cliente são exibidas sem erros de carregamento.
* **Justificativa:** Garante que módulos periféricos da conta continuam funcionando perfeitamente sem efeitos colaterais.
