# Atividade Avaliativa: Testes Exploratórios e Usabilidade

---

## 🔍 1. Cinco pontos para explorar livremente no sistema (Teste Exploratório)

O teste exploratório busca simular comportamentos reais e imprevisíveis do usuário para identificar falhas não cobertas por scripts formais.

* **Interrupção de Fluxos Críticos:** Iniciar uma transferência via Pix ou pagamento de boleto e, na tela de validação da senha, alternar de aplicativo, fechar a tela ou ativar o modo avião para verificar a segurança do cancelamento.
* **Comportamento do Botão "Voltar" Nativo:** Pressionar o botão físico ou virtual de "Voltar" do smartphone repetidamente durante a transição de carregamento da transação, garantindo que o pagamento não seja duplicado.
* **Entrada de Dados Extremos ou Inválidos (Monkey Testing):** Inserir valores negativos, quantias acima do limite permitido ou colar caracteres especiais/emojis no campo de descrição do Pix para testar a validação do formulário e a integridade da interface.
* **Navegação Acelerada e Caótica:** Alternar rapidamente entre menus (Extrato, Cartões, Configurações) antes que as informações terminem de carregar, avaliando o gerenciamento de requisições e a estabilidade do app.
* **Recuperação de Sessão Expirada:** Manter o aplicativo aberto em segundo plano por um longo período (ex: 15 minutos) e tentar realizar uma ação sensível para validar se a sessão é encerrada com segurança.

---

## 🛑 2. Cinco possíveis problemas de usabilidade que poderiam existir

Os problemas de usabilidade geram atrito e dificultam a fluidez da experiência do usuário no aplicativo.

* **Falta de Feedback Visual (Status do Sistema):** Ausência de indicadores de carregamento (*loading*) ao clicar em botões de confirmação, deixando o usuário incerto sobre o processamento da ação.
* **Mensagens de Erro Técnicas ou Confusas:** Exibição de códigos do servidor (como `Error 500: NullPointerException`) em vez de avisos claros e acionáveis, como *"Não foi possível conectar ao servidor. Tente novamente em instantes"*.
* **Alvos de Toque Pequenos (Touch Targets):** Ícones interativos (como o "olho" para ocultar/exibir saldo) ou links situados muito próximos de outros elementos, favorecendo cliques acidentais.
* **Excesso de Passos para Tarefas Simples:** Exigência de múltiplas confirmações e telas intermediárias para fluxos rotineiros, como a função Pix Copia e Cola.
* **Baixo Contraste e Tipografia Inadequada:** Uso de textos em tons claros sobre fundos claros na exibição de dados do extrato, prejudicando a legibilidade sob luz natural ou para usuários com limitações visuais.

---

## 🧠 3. Por que esses problemas impactam o usuário?

O impacto na experiência do usuário reflete-se na **confiança, na eficiência e na percepção de segurança** em relação à aplicação:

1. **Ansiedade e Risco Financeiro:** A falta de *feedback* imediato faz com que o usuário repita ações (como clicar várias vezes no botão de pagamento), o que pode acarretar duplicidade de cobranças e sobrecarga operacional.
2. **Erosão da Confiança no Sistema:** Erros técnicos visíveis e falhas de layout transmitem a sensação de um sistema vulnerável e amador, desestimulando a utilização do aplicativo bancário.
3. **Aumento do Volume de Atendimento (SAC):** A complexidade nos fluxos e mensagens pouco claras forçam o usuário a recorrer ao suporte técnico para resolver dúvidas simples, aumentando o custo operacional.
4. **Fadiga Cognitiva e Abandono:** A sobrecarga de passos e a má navegabilidade em momentos de urgência geram frustração, levando o cliente a abandonar o aplicativo em favor de alternativas mais intuitivas.
