# Learn Go Ethereum Client

## Initialize a chain
``geth init genesis.json --datadir ./eth_chain/mychain``

## Run a miner node
``sudo geth --rpc --rpcaddr 127.0.0.1 --rpcport 8546``

The chain will be located at ``~/Library/Ethereum/geth/chaindata``. To put it in a different folder use this instead:

``sudo geth --rpc --rpcaddr 127.0.0.1 --rpcport 8546 --datadir=./eth_chain/mychain``

To specify the exact APIs:

``sudo geth --rpc --rpcaddr 127.0.0.1 --rpcport 8546 --rpcapi "eth,net,web3,debug,admin,personal,miner"``

## Connect to the miner node via Javascript console
``geth attach http://127.0.0.1:8546``

Create an account in the Javascript console:

``personal.newAccount()``

Set the account as the Etherbase (i.e., coinbase):

``miner.setEtherbase(eth.accounts[0])``

## Start mining
This can be done using either the Javascript console or the geth command in terminal:

Using Javascript console:

``miner.start()``

Using geth:

``sudo geth --rpc --rpcaddr 127.0.0.1 --rpcport 8546 --miner --rpcapi "eth,net,web3,debug,admin,personal,miner"``

## Delete a chain
Delete the folder ``~/Library/Ethereum/geth/chaindata``

