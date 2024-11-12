screene giris yapalim
```console
screen -r dria
```
Çalışan servis varsa ctrl+c ile durduralım

  DKN_WALLET_SECRET_KEY i bir yere not edin
```console
  nano ~/dkn-compute-node/.env
  ```
  ```console
rm -rf dkn-compute-node
  ```
  güncelleme
   
    ```console
sudo apt update && sudo apt upgrade -y

  ```
 
  ```console
curl -fsSL https://ollama.com/install.sh | sh

 ```

  Dria kurulumu
```console
curl -L -o dkn-compute-node.zip https://github.com/firstbatchxyz/dkn-compute-launcher/releases/latest/download/dkn-compute-launcher-linux-amd64.zip
unzip dkn-compute-node.zip
cd dkn-compute-node
```
Buradan bir Gemini_api_key alalim https://ai.google.dev/gemini-api/docs/api-key?hl=tr

.env içerisine  DKN_WALLET_SECRET_KEY i ve GEMINI_API_KEY i ekliyoruz.
   ```console
nano .env
  ```
ctrl+x y enter ile çıkalım

  Dria yı çalıştırıyoruz
   ```console
ollama pull hellord/mxbai-embed-large-v1:f16

./dkn-compute-launcher -m=gemini-1.5-flash,llama3.1:latest
  ```
Gemini api key isterse tekrar girelim.Digerlerini enter ile gecelim.
