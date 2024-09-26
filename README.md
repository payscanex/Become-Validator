# Run a PayScan Validator
## Setting up a node
1. Git clone https://github.com/PYZOfficial/Become-Validator

2. Create an Account

```
chmod +x openethereum
./openethereum account new --config ./node.toml
```
Returned address like that 0x00aa39d30f0d20ff03a22ccfc30b7efbfca597c2

Copy result address to node.toml
Ex:
```
...
[account]
unlock = ["0x00aa39d30f0d20ff03a22ccfc30b7efbfca597c2"]
password = ["password"]

[mining]
force_sealing = true
engine_signer = "0x00aa39d30f0d20ff03a22ccfc30b7efbfca597c2"
reseal_on_txs = "none"
...
```
3. Run the authority nodes
```
./openethereum --config ./node.toml

```
4. Stake

    Stake

    To stake PYZ coin, all you should do is sending your PYZ coin to the PYZ Consensus contract address over the PYZ network from the validator address.
    The PYZ Consensus contract address: 0x17295c5446E147D8BD7e95dd0f5b5d7877f0672b
    The easiest way to do so, is to import your private key or key-store file to your favourite wallet (for example Metamask), switch network to PYZ and send the PYZ coin to the Consensus contract address.

    You can find your key-store (containing your private key) and the password for the created account in:
    /node/keys/PYZ/UTC--xxxx
    /node.pwd

5. Wait for 1 cycle (approximately 48 hours).

    Wait until the next cycle gets started.
