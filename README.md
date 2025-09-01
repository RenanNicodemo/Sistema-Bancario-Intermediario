### Projeto de Sistema Bancário v2.0
Este projeto é uma simulação de um sistema bancário com operações básicas e intermediárias, refatorado para utilizar funções, tornando o código mais modular, organizado e eficiente.

📜 Descrição
O sistema evoluiu para uma estrutura mais robusta, onde cada operação principal — depositar, sacar, extrato, criar usuário e criar conta corrente — foi encapsulada em sua própria função. Essa abordagem melhora a legibilidade, facilita a manutenção e permite um melhor reaproveitamento do código. O sistema agora distingue entre "usuário" (a pessoa) e "conta" (a conta bancária), permitindo que um mesmo usuário possa, futuramente, ter múltiplas contas.

✨ Funcionalidades
O sistema agora é dividido em funções que gerenciam usuários, contas e operações financeiras.

👤 Gestão de Usuários e Contas
Criar Usuário:

Função dedicada a cadastrar um novo cliente no sistema.

Solicita dados pessoais como nome, data de nascimento e CPF.

Valida para que não seja possível cadastrar um CPF já existente.

Criar Conta Corrente:

Função para vincular uma nova conta corrente a um usuário já existente.

A conta é composta por uma agência (número fixo, ex: "0001") e um número de conta sequencial.

Um usuário pode ter mais de uma conta.

🏧 Operações Bancárias
As operações agora são funções que recebem os dados da conta como parâmetros.

#### [ 1 ] - Depositar:

Recebe o saldo, o valor do depósito e o extrato como argumentos.

Permite apenas a entrada de valores positivos.

Retorna o novo saldo e o extrato atualizado.

Mensagem de sucesso:

✅ Depósito de R$ 250,00 realizado com sucesso!
#### [ 2 ] - Sacar:

Recebe o saldo, o valor do saque, o extrato, o limite por saque, o número de saques realizados e o limite diário de saques como argumentos.

Mantém as regras de negócio:

Limite de 3 saques diários.

Valor máximo de R$ 500,00 por operação.

O saldo em conta deve ser suficiente.

Retorna o novo saldo e o extrato atualizado.

#### [ 3 ] - Extrato:

Recebe o saldo e o extrato como argumentos.

Exibe todas as transações (depósitos e saques) registradas.

Mostra o saldo atual da conta no final.

#### [ 0 ] - Sair:

Encerra a aplicação com uma mensagem de agradecimento.

🚀 Como Executar
Clone este repositório.

Execute o arquivo principal do projeto em um terminal (python banco_v2.py, por exemplo).

O menu principal será exibido.

Primeiro, crie um usuário e, em seguida, uma conta corrente para poder realizar as operações.

Siga as instruções na tela para cada operação.

🛠️ Arquitetura e Tecnologias
Este projeto foi concebido para ser implementado em qualquer linguagem de programação que suporte programação funcional e modular, como:

#### Python: Ideal pela sua simplicidade e clareza na definição de funções.
