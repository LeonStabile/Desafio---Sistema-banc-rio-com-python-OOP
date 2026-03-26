# Desafio DIO – Sistema Bancário em Python

Este projeto é um sistema bancário simples desenvolvido como desafio da DIO, que permite criar clientes, criar contas, realizar depósitos, saques e consultar extratos.

## Código Original

O código original implementava as seguintes funcionalidades:

- Criação de clientes (`PessoaFisica`) e associação de contas.  
- Criação de contas (`ContaCorrente`) com limite padrão e histórico de transações.  
- Operações de depósito, saque e extrato.  
- Menu interativo para acessar as funcionalidades.  

No entanto, o código original apresentava:

- Limite de conta fixo (`500`) ao criar uma nova conta.  
- Duplicação de código nas funções de saque e depósito.  
- O cliente sempre tinha apenas a primeira conta selecionada, sem opção de escolher entre múltiplas contas.

## Alterações Realizadas

O código foi refatorado para melhorar a usabilidade e remover duplicações:

1. **Limite personalizado na criação de conta**  
   - Agora, ao criar uma conta, o sistema solicita ao usuário o limite desejado.

2. **Remoção de código duplicado**  
   - Funções `sacar` e `depositar` foram unificadas em `realizar_transacao_padrao(clientes, tipo)` para tratar transações de forma genérica.

3. **Correção de timestamp do histórico**  
   - Corrigido o formato da data/hora no histórico de transações.

4. **Melhorias gerais**  
   - Mensagens e formatação mais claras.  
   - Código mais limpo e organizado, facilitando manutenção e futuras funcionalidades.

## Observações

- Atualmente, ao realizar transações, o sistema seleciona a primeira conta do cliente.  
- Futuras melhorias podem incluir a escolha de qual conta usar caso o cliente tenha mais de uma.  
- Código pronto para testes interativos via terminal.
