## Foundry

**Foundry is a blazing fast, portable and modular toolkit for Ethereum application development written in Rust.**

Foundry consists of:

-   **Forge**: Ethereum testing framework (like Truffle, Hardhat and DappTools).
-   **Cast**: Swiss army knife for interacting with EVM smart contracts, sending transactions and getting chain data.
-   **Anvil**: Local Ethereum node, akin to Ganache, Hardhat Network.
-   **Chisel**: Fast, utilitarian, and verbose solidity REPL.

## Documentation

https://book.getfoundry.sh/

## Usage

### Build

```shell
$ forge build
```

### Test

```shell
$ forge test
```

### Format

```shell
$ forge fmt
```

### Gas Snapshots

```shell
$ forge snapshot
```

### Anvil

```shell
$ anvil
```

### Deploy

```shell
$ forge script script/Counter.s.sol:CounterScript --rpc-url <your_rpc_url> --private-key <your_private_key>
```

### Cast

```shell
$ cast <subcommand>
```

### Help

```shell
$ forge --help
$ anvil --help
$ cast --help
```

## conceitos

i_ for immutable variables
s_ for private variables

se eu nao especificar a ree ao realizar um teste ele eh testado no anvil

Tipos de testes:
-> Unit: Teste unitarios - Testa uma parte especifica do codigo
-> Integration: Teste de integração - Testa como o codigo funciona com as demais partes
-> Forked: Teste de codigo em uma ambiente simulado 
-> Staging: Testa o codigo em uma ambiente real mas que ainda não é de produção

--

docs.chain.link/data-feeds
## comandos!!!

- armazenar carteira em documento local com dotenv: 

forge script <PATH-SCRIPT-DEPLOY> --rpc-url <RPC-URL> --broadcast --private-key $PRIVATE_KEY

- armazenar carteira em documento local sem dotenv: 

cast wallet import defaultKey --interactive 

- deployar contrato com carteira armazenada usando script de deploy: 

forge script <PATH-SCRIPT-DEPLOY> --rpc-url <RPC-URL> --account <ACCOUNT> --broadcast 

- enviar coisas para blockchain:

cast send <CONTRACT_ADDRESS> "<METHOD_SIGNATURE>" <PARAMS> --rpc-url <RPC-URL> --private-key $PRIVATE_KEY

- ler o estado da rede:

cast call <CONTRACT_ADDRESS> "<METHOD_SIGNATURE>" <PARAMS> 

- converter se hexadecimal to decimal:

cast --to-base <VALUE> dec

L2 -> lower cost






