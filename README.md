## Visão Geral


Este projeto é de um Token, que é um contrato inteligente (smart contract) implementado em Solidity, seguindo o padrão ERC-20. O contrato define uma interface chamada IERC20, que estabelece os métodos e eventos necessários para operações básicas em tokens, como transferências, aprovações e consultas de saldo.



A implementação principal do contrato é denominada ZMToken, e ela herda da interface IERC20. O token é identificado pelo nome "ZM Token", com o símbolo "ZM" e é divisível em até 18 casas decimais.



O fornecimento total inicial do token é fixado em 10 ether. Ao ser implantado, todo esse fornecimento é alocado na conta do proprietário do contrato, que é a conta que realizou a implantação.



O contrato oferece funcionalidades essenciais, incluindo a transferência de tokens entre contas, a aprovação de gastos por terceiros e a verificação de autorizações para transferências.



É importante notar que o código inclui mecanismos de segurança, como verificações de limites de tokens durante transferências e aprovações, para garantir o correto funcionamento e evitar potenciais exploits.



Este projeto é uma base sólida para a criação e gestão de tokens ERC-20 na blockchain Ethereum, proporcionando interoperabilidade e conformidade com os padrões estabelecidos.

## Informações do Contrato Inteligente

- **Licença:** GPL-3.0
- **Versão do Solidity:** ^0.8.0

## Detalhes do Token

- **Nome:** ZM Token
- **Símbolo:** ZM
- **Decimais:** 18
- **Fornecimento Total:** 10 ether

## Funções

### totalSupply

```solidity
function totalSupply() public view returns (uint256);
```

Retorna o fornecimento total de ZM Tokens.

### balanceOf

```solidity
function balanceOf(address account) public view returns (uint256);
```

Retorna o saldo de ZM Tokens detidos pelo endereço especificado (\`account\`).

### transfer

```solidity
function transfer(address recipient, uint256 amount) public returns (bool);
```

Transfere \`amount\` ZM Tokens da conta do remetente para o endereço de destino (\`recipient\`). Retorna verdadeiro se a transferência for bem-sucedida.

### approve

```solidity
function approve(address spender, uint256 amount) public returns (bool);
```

Permite que o \`spender\` gaste \`amount\` ZM Tokens em nome do remetente. Retorna verdadeiro se a aprovação for bem-sucedida.

### allowance

```solidity
function allowance(address owner, address spender) public view returns (uint256);
```

Retorna a quantidade de ZM Tokens que o \`spender\` está autorizado a gastar em nome do \`owner\`.

### transferFrom

```solidity
function transferFrom(address sender, address recipient, uint256 amount) public returns (bool);
```

Transfere \`amount\` ZM Tokens do \`owner\` para o \`buyer\` se o remetente estiver autorizado a fazê-lo. Retorna verdadeiro se a transferência for bem-sucedida.

## Eventos

- `Transfer`

```solidity
event Transfer(address indexed from, address indexed to, uint256 value);
```

Emitido quando ZM Tokens são transferidos de um endereço para outro.

- `Approval`

```solidity
event Approval(address indexed owner, address indexed spender, uint256 value);
```

Emitido quando um endereço é autorizado a gastar ZM Tokens em nome de outro endereço.

## Implantação

O contrato inteligente está atualmente implantado com um fornecimento total inicial de 10 ether. O proprietário do contrato é a conta que o implanta, e o fornecimento total é alocado no saldo do proprietário.
