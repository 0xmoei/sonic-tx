# Sonic Auto-Transfer

## 1- Prerequisites:
### Install Node.js
```console
# Check version
node --version

# Delete old files
sudo apt-get remove nodejs -y

sudo apt-get purge nodejs

sudo apt-get autoremove

sudo rm /etc/apt/keyrings/nodesource.gpg
sudo rm /etc/apt/sources.list.d/nodesource.list

# Install Nodejs 18
NODE_MAJOR=18
sudo apt-get update
sudo apt-get install -y ca-certificates curl gnupg
sudo mkdir -p /etc/apt/keyrings

curl -fsSL https://deb.nodesource.com/gpgkey/nodesource-repo.gpg.key | sudo gpg --dearmor -o /etc/apt/keyrings/nodesource.gpg

echo "deb [signed-by=/etc/apt/keyrings/nodesource.gpg] https://deb.nodesource.com/node_${NODE_MAJOR}.x nodistro main" | sudo tee /etc/apt/sources.list.d/nodesource.list

sudo apt-get update
sudo apt-get install -y nodejs
sudo apt-get install npm

# Check Nodejs Version
node --version
```

### Install Solana web3.js
```console
npm install --save @solana/web3.js
```

## 2- Clone Repo:
```console
git clone https://github.com/0xmoei/sonic-tx/
```

## 3- Edit .env:
* You have to set-up a second wallet address to send token to & your main wallet private key in .env file
```console
cd sonic-tx
nano .env

# Copy and Paste this text in the editor
PRIVATE_KEY = your Wallet Private key
RECIPIENT_ADDRESS = your recipient address
```
>  Replace `your Wallet Private key` & `your recipient address`
>
> To save: Ctrl+X+Y Enter
> 
![image](https://github.com/0xmoei/sonic-tx/assets/90371338/6d02cfb8-f7bb-4399-9999-56232071e8ab)


### 4- Run:
```console
# Install
npm install

# Run
node auto-Transfer.js
```

Close it after 100 txns, and come back tomorrow :D
