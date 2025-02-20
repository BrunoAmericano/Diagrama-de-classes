# 📊 Diagrama de Comunicação - Sistema de Venda de Ingressos de Cinema 🎥🍿

Este repositório contém o **Diagrama de Comunicação** do **Sistema de Venda de Ingressos de Cinema**, um modelo detalhado das interações entre os componentes do sistema durante o processo de venda de ingressos. O diagrama de comunicação foi desenvolvido para ilustrar claramente como as mensagens circulam entre os objetos envolvidos na venda de ingressos.

---

## 🚀 O Que é o Diagrama de Comunicação?

O **Diagrama de Comunicação** descreve como os **objetos** do sistema interagem entre si. Ao invés de mostrar a sequência temporal das interações (como no diagrama de sequência), ele se foca no **fluxo de mensagens** entre os objetos, destacando a relação e os detalhes de cada troca de informações.

Neste caso, o diagrama ilustra o processo completo de **venda de ingressos de cinema**, desde a solicitação do funcionário para visualizar as sessões até a emissão do ingresso ao cliente.

---

## 🏞️ Visão Geral do Diagrama

### Fluxo de Interações:

1. **Funcionário inicia a venda:** O processo começa quando o **Funcionário** solicita à **Interface** a visualização das sessões disponíveis de cinema.
2. **Carregamento das Sessões:** A **Interface** repassa essa solicitação para a **Controladora**, que inicia um laço para consultar todas as sessões de cinema ainda não encerradas.
3. **Consulta à Sala e ao Filme:** Para cada sessão, a **Controladora** consulta o **Sistema de Sessões** para obter informações sobre a **Sala** e o **Filme** apresentado.
4. **Exibição das Sessões:** As informações são passadas da **Controladora** para a **Interface**, que exibe as opções de sessões para o **Funcionário** escolher.
5. **Escolha da Sessão:** O **Funcionário** escolhe a sessão desejada e confirma.
6. **Geração de Ingresso:** A **Controladora** então solicita ao **Sistema de Ingressos** a criação do ingresso, e o ingresso é gerado.
7. **Emissão do Ingresso:** O ingresso gerado é exibido na **Interface**, que o entrega ao **Funcionário** para ser dado ao **Cliente**.

---

## 💡 Como Funciona o Diagrama de Comunicação?

Este diagrama mostra a **interação dos objetos** com base nas seguintes entidades principais:

- **Funcionário:** O usuário responsável por escolher a sessão e gerar o ingresso.
- **Cliente:** O destinatário final do ingresso.
- **Interface:** A camada de apresentação, onde o funcionário interage com o sistema.
- **Controladora:** A lógica de negócios que orquestra o processo de venda de ingressos.
- **Sistema de Sessões:** Gerencia todas as informações sobre as sessões de cinema, filmes e salas.
- **Sistema de Ingressos:** Responsável por gerar os ingressos para os clientes.

### **Fluxo de Mensagens**

1. **Solicitação de Sessões:** O **Funcionário** solicita as sessões disponíveis.
2. **Carregamento das Sessões:** A **Controladora** carrega as sessões não encerradas e obtém informações sobre elas.
3. **Exibição de Sessões:** A **Interface** apresenta as sessões ao **Funcionário**.
4. **Escolha e Confirmação:** O **Funcionário** escolhe uma sessão e confirma a compra.
5. **Geração do Ingresso:** A **Controladora** solicita ao **Sistema de Ingressos** a criação do ingresso.
6. **Emissão do Ingresso:** O ingresso é gerado e exibido para o **Funcionário**.

---

## 📷 Diagrama de Comunicação

![Diagrama de Comunicação de Venda de Ingressos de Cinema](https://github.com/BrunoAmericano/Diagramas/blob/main/diagrama-comunicacao-processo-venda-cinema/Untitled%20diagram-2025-02-20-191846.png?raw=true)

> O diagrama acima ilustra o fluxo de mensagens entre os componentes do sistema durante o processo de venda de ingressos.

---

## 📚 Como Interpretar o Diagrama

Cada **seta** no diagrama representa uma **mensagem** ou **ação** de um componente para outro. A direção das setas mostra de quem para quem a mensagem é enviada. As mensagens podem ser de diferentes tipos, como **consulta**, **informação**, **confirmação**, ou **geração de objetos**.

Por exemplo:
- **A Controladora consulta o Sistema de Sessões** para obter informações sobre a sala e o filme.
- **O Funcionário escolhe a sessão e envia para a Controladora**, que então gera um ingresso.

---

## 🛠️ Como o Diagrama se Relaciona ao Sistema

O diagrama de comunicação serve como uma representação clara de como o sistema funciona em termos de **interações entre objetos**. Ele é fundamental para entender:

- Como as informações fluem entre os diferentes componentes do sistema.
- Como o sistema mantém a comunicação entre **interface** e **lógica de controle**.
- A ordem das ações em um nível mais técnico, sem a necessidade de detalhes temporais.

---

## 🔧 Próximos Passos

Este diagrama serve como base para o desenvolvimento e implementação do **Sistema de Venda de Ingressos de Cinema**. As próximas etapas incluem:

- **Implementação do Backend:** Criar a lógica para controle de sessões e geração de ingressos.
- **Desenvolvimento da Interface:** Criar a interface de usuário intuitiva para o **Funcionário** e o **Cliente**.
- **Testes:** Validar o fluxo de mensagens para garantir que o sistema funcione conforme esperado.
