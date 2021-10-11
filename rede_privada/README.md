# Como criar uma rede privada usando a Ethereum

## Prequisitos
  Instalar o geth no link  https://geth.ethereum.org/downloads/ 

## Criando o bloco *genesis*
    Primeiro precisamos iniciar criando o primeiro bloco da nossa cadeia, esse bloco tem o nome de Genesis. Faça isso criando o arquivo genesis.json no local em que você deseja iniciar sua rede e cole o sgeuinte texo nele:
   
  '''
    {
      “config”: {
        “chainID”: 15,
        “homesteadBlock”: 0,
        “eip150Block”: 0,
        “eip155Block”: 0,
        “eip158Block”: 0,
        “byzantiumBlock”: 0,
        “constantinopleBlock”: 0,
        “petersburgBlock”: 0,
        “istanbulBlock”: 1000
  },
        "difficulty": "0x400",
        "mixhash": "0x0000000000000000000000000000000000000000000000000000000000000000",
        "parentHash": "0x0000000000000000000000000000000000000000000000000000000000000000",
        "gasLimit": "0xffffffff",
        "alloc": {
  }
}
 '''
