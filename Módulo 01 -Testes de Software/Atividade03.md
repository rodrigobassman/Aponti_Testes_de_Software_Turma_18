# Quadro Comparativo e Reflexão: O Papel do QA

Este documento apresenta uma visão clara e direta sobre a evolução da Garantia de Qualidade (QA) no desenvolvimento de software, comparando o modelo tradicional com o modelo moderno (Ágil/DevOps), além de listar os principais desafios enfrentados pelas equipas no dia a dia.

---

## 1. Quadro Comparativo: Tradicional vs. Moderno

| Critério | No Passado (Tradicional) | Hoje em Dia (Moderno / Ágil) |
| :--- | :--- | :--- |
| **Quando o QA entra?** | Só no final, depois de o sistema já estar totalmente pronto. | Desde o início, ajudando a planejar como o sistema deve funcionar. |
| **Qual é o objetivo?** | Encontrar erros que os programadores já cometeram (Reativo). | Evitar que os erros aconteçam antes mesmo de programar (Proativo). |
| **Como testa?** | Uma pessoa a clicar no ecrã seguindo um roteiro manual passo a passo. | Computadores e scripts a testar sozinhos (Automação) de forma super rápida. |
| **De quem é a responsabilidade?** | Do QA, que era visto como o único que "deixava passar" o bug. | De toda a gente. A equipe inteira (Devs, QAs e POs) cuida da qualidade. |
| **Velocidade do Feedback** | Demorado. Demorava dias ou semanas para saber se o sistema estava a funcionar. | Rápido. Em poucos minutos a equipa sabe se a alteração partiu alguma coisa. |

---

## 2. O que mais atrapalha os projetos reais hoje?

Mudar do modelo antigo para o moderno não é só comprar ferramentas novas, exige uma mudança na forma de pensar de toda a equipe. Na prática, estes são os três maiores desafios atuais:

### 🚨 A Armadilha da Pressa (Velocidade vs. Qualidade)
As empresas precisam de lançar novidades na aplicação ou site todas as semanas (ou até todos os dias). O QA corre contra o tempo para testar tudo rápido. Se o processo não estiver bem ajustado, o QA torna-se o "gargalo" que atrasa a entrega, ou a equipe salta etapas e o cliente final acaba por descobrir o bug.

### 🤖 A Ilusão da "Automação Total"
Muitas equipas tentam automatizar 100% dos testes para poupar tempo. O resultado prático costuma ser a criação de robôs de teste frágeis, que partem por qualquer bobeira (como a mudança de cor de um botão). A equipe acaba por gastar mais tempo a consertar os robôs de teste do que a testar o sistema real.

### 🤷‍♂️ Achar que Qualidade é Obrigação Apenas do QA
O erro mais comum em projetos ditos "ágeis" é o programador terminar o código a correr e "atirá-lo para cima da mesa" do QA para ele se orientar a descobrir os erros. Se a qualidade não começar na hora de escrever o código (com o desenvolvedor a fazer os seus próprios testes básicos), o QA moderno falha e o projeto acumula problemas.

---

## Conclusão

O QA moderno não serve para "caçar bugs" no final do projeto. O papel dele hoje é dar **confiança e velocidade** para que a empresa possa lançar novidades sem medo de que o sistema fique fora do ar.

