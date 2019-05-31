# DREP 
The DREP Chain is a high-performance public chain fully developed by the DREP team. It is compatible with Smart Contracts in the EVM and WASM format with a dual layer structure constituting of a root chain and sub-chains.


# Features

1. Provides a decentralized ID system and data privacy protection
2. Integrates the underlying chain with both smart contracts and novel smart reputation pipes.
3. Provides the DREP reputation protocols and reputation templates.
4. Has high performance and high compatibilities.

# Installation

## Binaries (Windows/Linux/macOS)

### linux

1. Download the executable from [here](https://github.com/drep-project/test_network), and place it under the directory: `/usr/local/bin`
 
2. Place the configuration file `config.json` under the directory: `/usr/local/bin`

3. Start the node using command: `./drep console`


### win10

1. Download the executable from [here](https://github.com/drep-project/test_network)

2. Place the configuration file `config.json` under the directory: ` C:\Users\$Username$\AppData\Local\Drep` 

3. Open the command-line interface (`cmd.exe`), navigate into the directory at which the executable is placed.

4. Start the node using command: `drep.exe console`


# Usage

1 查询地址对应的币总数目

 curl -H "Content-Type: application/json" -X post --data '{"jsonrpc":"2.0","method":"chain_getBalance","params":["0xb527326623a499f7ea550f1be98a9a6e3b56ee29"],"id":1}' http://127.0.0.1:15645
0xb527326623a499f7ea550f1be98a9a6e3b56ee29 替换本地的账户

2 查询本地账户
 curl -H "Content-Type: application/json" -X post --data '{"jsonrpc":"2.0","method":"account_listAddress","params":[],"id":1}' http://127.0.0.1:15645
 
3 转账交易
 
curl -H "Content-Type: application/json" -X post --data '{"jsonrpc":"2.0","method":"account_transfer","params":["0x7923a30bbfbcb998a6534d56b313e68c8e0c594a","0xb527326623a499f7ea550f1be98a9a6e3b56ee29","0x111","0x110","0x30000",""],"id":1}' http://127.0.0.1:15645
 
0x7923a30bbfbcb998a6534d56b313e68c8e0c594a 替换成转出地址
0xb527326623a499f7ea550f1be98a9a6e3b56ee29 替换成转入地址
0x111 16进制表示的转账金额
0x110 16进制表示的gasprice
0x30000 16进制表示的此交易给的最大的gas