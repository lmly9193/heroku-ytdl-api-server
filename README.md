# youtube-dl-api-server

基於 [youtube-dl](http://rg3.github.io/youtube-dl/) , [youtube-dl-api-server ](https://github.com/jaimeMF/youtube-dl-api-server), [youtube-dl-api-server-heroku](https://github.com/GeeekyBoy/youtube-dl-api-server-heroku) 的 RESTful API 伺服器，本儲存庫用途為將 youtube-dl-api-server 直接部屬到 Heroku。

## 部屬到 Heroku

### 一鍵部屬

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

### 手動部屬

0. 確保你已安裝且設置好 [Heroku toolbelt](https://toolbelt.heroku.com).

1. 克隆這個儲存庫

   ```bash
   git clone https://github.com/lmly9193/heroku-ytdl-api-server
   ```

2. 建立一個 Heroku 應用

   ```bash
   cd heroku-ytdl-api-server
   heroku create <your-app-name>
   ```

3. 推送及部屬

   ```bash
   git push -u heroku master
   ```

4. 查看執行日誌或狀態

   ```bash
   heroku logs
   
   heroku ps
   ```

5. 你的 API 伺服器版本可以在此查看`https://<your-app-name>.herokuapp.com/api/version`.

## Updating Python packages

0. Setup virtualenvwrapper and activate it. Install [pip-tools (>= 1.2)](https://github.com/nvie/pip-tools/): `pip install -U pip-tools`.

1. Update to the latest packages: `pip-compile --upgrade`.

2. Clear the environment and reload packages: `pip-sync`.

3. Commit changes: `git commit -m "Updated packages." requirements.txt`.

4. Push to deploy changes: `git push`.
