# Dria-node-data

![Image](https://github.com/SKaaalper/Dria-node-data/blob/main/image1.jfif)


## **Dria is a decentralized network that allows millions of AI agents to collaborate on generating synthetic data to improve AI models.**


- ***Official Guide + Windows Version***: [https://dria.co/join](https://dria.co/join)


## 1.**Install Dependecies**:
- **Install docker**
```
sudo apt update -y && sudo apt upgrade -y
for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do sudo apt-get remove $pkg; done

sudo apt-get update
sudo apt-get install ca-certificates curl gnupg
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg

echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt update -y && sudo apt upgrade -y

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

sudo chmod +x /usr/local/bin/docker-compose
```

- **Docker version**
```
docker --version
```

- **Install Ollama**
```
curl -fsSL https://ollama.com/install.sh | sh
```

## 2.**Install Dria**:
```
cd $HOME && curl -L -o dkn-compute-node.zip https://github.com/firstbatchxyz/dkn-compute-launcher/releases/latest/download/dkn-compute-launcher-linux-amd64.zip
```
- **Unzip the file**
```
unzip dkn-compute-node.zip
```
- **Head to directory**
```
cd dkn-compute-node
```

## 3.**Run Dria Node**:
```
./dkn-compute-launcher
```

- Enter your DKN wallet Secret key `Your metamask Private Key without 0x` Use Burner Wallet / Airdrop Wallet
- Pick a Model
 - I use only one model,`gemini-1.5-flash` by selecting `10`
 - `Gemini` is a google API with upto `1500` free requests daily, No cost, doesn't need VPS resources.
 - Get your Google API [here](https://ai.google.dev/gemini-api/docs/api-key) Click `Get a Gemini API key in Google AI Studio` > Click `Create API Key` > Save it and paste it into your VPS model

 ***running multiple models may reduce the performance of your node and prevent it from responding to tasks***

 ![Image](https://github.com/SKaaalper/Dria-node-data/blob/main/image2.png)

- **Skip `Jina` & `Serper API key` by pressing `Enter`**
- **Now your node will start Downloading Models files and Testing them each model must pass its test and it only depends on your system specification**


Error: **If a port conflict occurs, edit the file using this command**:
```
nano $HOME/dkn-compute-node/.env
```
or
```
nano .env
```
- **Change port**
```
DKN_P2P_LISTEN_ADDR="/ip4/0.0.0.0/tcp/2001
```
- Or you can modify it to avoid conflicts with the old ones you are running.

## 4.**Re-run Dria Node**:
- Now that you have ensured your `models` passed the test and your node is running, you should restart your node within a screen session. Press `Ctrl+C` to stop the node and exit.
  
```
screen -S dria
```
```
./dkn-compute-launcher
```

![Image](https://github.com/SKaaalper/Dria-node-data/blob/main/image3.png)

- You can minimze the screen with `CTRL+A`, then click `D`
- To open your screen again `screen -r dria`

## 5.**Earn Node-Keeper Role**
- Join Dria Official `Discord` [here](https://discord.gg/dria)
- Fill up the Form [here](https://docs.google.com/forms/d/e/1FAIpQLSeK090ejc4dg5x1ztb_yAOxGz5o1V8JUqDa-o3AwV1Lq7NpMA/viewform)


## 6.**Check your step (Points)**
- [https://steps.leaderboard.dria.co/](https://steps.leaderboard.dria.co/)
- Paste your DRIA node address





