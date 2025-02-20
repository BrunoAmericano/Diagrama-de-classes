# 💳 Diagrama de Sequência - Emissão de Extrato em Caixa Eletrônico 🏧

Este projeto descreve o **Diagrama de Sequência** para o processo de **emissão de extrato bancário** através de um **caixa eletrônico**. O diagrama ilustra como o cliente interage com o caixa eletrônico, desde a inserção do número do cartão até a entrega do extrato impresso.

---

## 🚶‍♂️ Visão Geral do Processo

A emissão de extrato no caixa eletrônico envolve uma série de etapas, onde o **cliente** fornece seu número de cartão, valida sua senha, e solicita um extrato bancário para um determinado intervalo de datas. O sistema, através de uma série de interações entre a **interface**, o **controlador**, e as classes **Conta Comum** e **Movimento**, gera o extrato e o entrega ao cliente.

---

## 🧩 Etapas do Processo

O diagrama de sequência descreve as seguintes interações entre os objetos:

1. **Cliente fornece número do cartão à interface:** O cliente insere seu número de cartão no caixa eletrônico.
2. **A interface passa o número ao controlador:** O controlador consulta a validade da conta associada ao número de cartão.
3. **Validação de Conta:** O controlador verifica se a conta existe, consultando o objeto **Conta Comum**.
4. **Solicitação de senha:** Se a conta for válida, o controlador solicita a senha ao cliente.
5. **Validação de senha:** O controlador valida a senha fornecida pelo cliente através da **Conta Comum**.
6. **Seleção do extrato:** O cliente escolhe a opção de extrato e informa o intervalo de datas desejado.
7. **Geração do extrato:** O controlador solicita à **Conta Comum** que gere o extrato para o período solicitado.
8. **Análise dos movimentos:** A classe **Conta Comum** consulta os movimentos da **Movimento** para gerar o extrato correto.
9. **Entrega do extrato:** O extrato é impresso pela interface e entregue ao cliente.

---

## 🔄 Diagrama de Sequência

Abaixo está o **Diagrama de Sequência** representando as interações descritas:

> **Nota:** O diagrama de sequência mostra a comunicação entre o **Cliente**, a **Interface**, o **Controlador**, a **Conta Comum** e a **Movimento**.

![Diagrama de Sequência - Emissão de Extrato](https://github.com/BrunoAmericano/Diagramas/blob/main/diagrama-sequencia-extrato/Untitled%20diagram-2025-02-20-200135.png?raw=true)

---

## ⚙️ Como Funciona o Diagrama de Sequência?

1. **Cliente → Interface:** O cliente insere o número do cartão.
2. **Interface → Controlador:** A interface passa o número do cartão para o controlador.
3. **Controlador → Conta Comum:** O controlador consulta a conta associada ao número de cartão.
4. **Conta Comum → Controlador:** A **Conta Comum** retorna a validação da conta.
5. **Controlador → Interface:** O controlador solicita à interface que peça a senha ao cliente.
6. **Cliente → Interface:** O cliente digita sua senha.
7. **Interface → Controlador:** A interface envia a senha para o controlador.
8. **Controlador → Conta Comum:** O controlador valida a senha com a **Conta Comum**.
9. **Conta Comum → Controlador:** A **Conta Comum** retorna a validade da senha.
10. **Cliente → Interface:** O cliente escolhe a opção de extrato e informa o período desejado.
11. **Interface → Controlador:** A interface envia o período escolhido ao controlador.
12. **Controlador → Conta Comum:** O controlador solicita à **Conta Comum** que gere o extrato para o período escolhido.
13. **Conta Comum → Movimento:** A **Conta Comum** chama o método `analisarMovimento` para filtrar os movimentos no intervalo.
14. **Movimento → Conta Comum:** A **Movimento** retorna os dados dos movimentos relevantes.
15. **Controlador → Interface:** O controlador instrui a interface a imprimir e entregar o extrato ao cliente.
16. **Interface → Cliente:** O extrato é impresso e entregue ao cliente.

---

## 🛠️ Ferramentas Utilizadas

- **Lucidchart** ou **Draw.io** para criar o diagrama de sequência visual.
- **Microsoft Visio** para diagramas profissionais e detalhados.

---

## 📚 Benefícios do Diagrama de Sequência

O **Diagrama de Sequência** é uma ferramenta valiosa para entender a interação entre os diversos componentes de um sistema. Ele ajuda a visualizar:

- A comunicação entre a interface, controlador e as classes envolvidas.
- O fluxo de informações entre o cliente, caixa eletrônico e os objetos do sistema.
- A ordem dos eventos, facilitando a compreensão do processo.

---

## 🔄 Fluxo de Interações

A interação entre os componentes no **Diagrama de Sequência** ocorre de forma linear, onde cada mensagem é disparada para realizar uma ação, como validar a conta, validar a senha ou gerar o extrato. O diagrama ajuda a garantir que o fluxo de dados seja realizado corretamente.
