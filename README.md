# Install modules
```
python3 -m pip install --user pipx
python3 -m pipx ensurepath
pipx install eth-brownie
sudo apt install python3.10-venv
sudo npm install -g ganache-cli
```

# Compile

To compile the smart contract, run:
```
brownie compile
```

# Deploy
## Local Network
To deploy on a local network, run:
```bash
brownie run scripts/deploy.py --network development
```

## Testnet
To deploy on a testnet, get your keys for that testnet and the project id from infura.io.

For example Sepolia testnet:
```
$export PUBLIC_KEY="your_public_key"
$export PRIVATE_KEY="your_private_key"
$export WEB3_INFURA_PROJECT_ID="your_infura_project_id"
$brownie networks add Ethereum sepolia host="https://sepolia.infura.io/v3/your_infura_project_id" chainid=11155111
```
```
$brownie run scripts/deploy.py --network Sepolia
```
