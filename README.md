geth
=========
Installation of geth and run ethereum node as a service.

Currently it only supports systemd service. Will add more in the future.

Role Variables
--------------
```yaml
---
geth_name: geth

geth_dir: /usr/local
geth_version: geth-linux-amd64-1.7.3-4bb3c89d
geth_url: https://gethstore.blob.core.windows.net/builds

geth_datadir: /root/.ethereum
geth_cache: 1024 # 1gb
geth_testnet: false
geth_rinkeby: false
geth_port: 30303
geth_rpc: false
geth_maxpeer: 25

# geth rpc values if it is true
geth_rpcaddr: 0.0.0.0
geth_rpcport: 8545
geth_rpcapi: "db,eth,net,web3"
geth_rpccorsdomain: "*"

```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: geth }
