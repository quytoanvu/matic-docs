Installing and running Bor node.

### What is Bor?

BOR is the EVM compatible Matic Side chain which currently is built on top of `geth` using `bor` consensus mechanism.

### Installing Bor

```js

$ mkdir -p $GOPATH/src/github.com/maticnetwork
$ cd $GOPATH/src/github.com/maticnetwork
$ git clone https://github.com/maticnetwork/bor
$ cd bor && git checkout master
$ make bor

```

Now you have `bor` installed on your local system and you can run it using `build/bin/bor`

### Adding peers

Bor also supports a feature called static nodes if you have certain peers you always want to connect to. Static nodes are re-connected on disconnects. You can configure permanent static nodes by putting something like the following example into `<datadir>/bor/static-nodes.json:`

```js
[
  "enode://f4642fa65af50cfdea8fa7414a5def7bb7991478b768e296f5e4a54e8b995de102e0ceae2e826f293c481b5325f89be6d207b003382e18a8ecba66fbaf6416c0@33.4.2.1:30303",
  "enode://ENODEID@ip:port"
];
```

For more info on how to connect to peers see [this](https://geth.ethereum.org/docs/interface/peer-to-peer).