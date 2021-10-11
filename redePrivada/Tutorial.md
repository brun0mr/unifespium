# Tutorial Para instalar uma rede ethereum privada no windows
## Passo 1
Instalar o Geth
https://geth.ethereum.org/downloads/

## Passo 2
Abrir o Powershell

## Passo 3
Digitar o comando ``` puppeth ``` para criar o bloco genesis 

## Passo 4 
Dentro do puppeth vamos:
1. Colocar o nome da sua rede
2. Escolher opção 2
3. Escolher opção 1
4. Escolher opção 1
5. Apertar enter
6. Digitar no
7. Apertar enter
8. Escolher opção 2
9. Escolher opção 2
10. Apertar enter

## Passo 5
Após isso será criado o seu bloco genesis na pasta que estiver rodando o puppeth
criando o arquivo *nome-da-sua-rede*.json

## Passo 6
Agora vamos entrar na pasta que está o bloco genesis e vamos dar o comando:

``` 
geth --datadir “.” init “.\*nome-da-sua-rede*.json”
```

## Passo 7 
Agora na mesma janela do promp de comando, digite:

```
geth --datadir “.” --networkid 15 --rpc --rpcport "8545" --rpccorsdomain "*" --nodiscover --rpcapi="admin,eth,txpool,net,web3,personal,miner" --allow-insecure-unlock
```

## Passo 8
Agora sem fechar a primeira janela, em outra janela digite:

```
geth attach http://127.0.0.1:8545
```

- Caso quiser criar contas para sua rede, é possível utilizando o comando ``` geth --datadir . account new ``` antes do passo 7

- Caso quiser uma lista das contas na rede utilizar o comando ``` geth --datadir . account list ```

- Comandos para o terminal do passo 8
```
eth.accounts

eth.coinbase

eth.getBalance(eth.coinbase)

eth.getBalance(eth.accounts[1])

web3.fromWei(eth.getBalance(eth.coinbase), "ether")

miner.start()

miner.start(1)

miner.stop()

net.version

personal.unlockAccount(eth.accounts[1])

eth.sendTransaction({from: eth.coinbase, to: eth.accounts[1], value: web3.toWei(10,"ether")})
```
