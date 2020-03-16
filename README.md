## Bitcoin-container
[See at docker hub](https://hub.docker.com/repository/docker/siandreev/bitcoind-regtest)

This container is designed to work with blocking bitcoin in regtest mode. An image with a tag **alice-bob-regtest** launches inside itself two connected nodes of the blockchain network of the bitcoin network in regtest mode. Nodes correspond to two fictitious users: Alice and Bob
#### Alice 
- start with 5050 BTC
- config:
``` 
rpcuser=alice
rpcpassword=password
port=19000
rpcport=18443
```
#### Bob 
- start with 50 BTC
- config:
``` 
rpcuser=bob
rpcpassword=password
port=19001
rpcport=18444
```
#### How to run
Type
```
docker run -p 18443:18443 -p 18444:18444 siandreev/bitcoind-regtest:alice-bob-regtest
```
and wait for "The node is ready!" message.
