# OA2

## 🦈 Requirements
- NodeJS
- Server Mariadb/MySQL
- Datacenter/Residentiel Proxy
- Optionnel:
  - PM2

## 🚀 Installation
- Use script
  - On Linux: `./install.sh`
  - On Windows: `./install.bat`
- Create a User with all privileges in your database and put the credentials in `Database/index.ts`.
- Compilate folder
  - On Linux: `./compilate.sh`
  - On Windows: `./compilate.bat`
- Run `npm start` in `API` folder
  - Using PM2: `pm2 start dist --name "API"`
- Use `runClient.sh` in `Client` folder to run the client
  - Example: `./runClient.sh IdOfBot Token`
  - You can also use `runClient.bat IdOfBot Token` on Windows
    - Using node directly: `node dist/Client/Client.js Token`
- Configure your proxy in `ips-data_center.json`
  - Example: 
```json
[
    "IP:PORT:USER:PASSWORD",
    "IP:PORT:USER:PASSWORD",
    ...
]
```

## 📝 Bot Configuration
- Edit file `Client/config.ts` to set `REDIRECTION_URI`
  - Example: `http://localhost:3000/callback`
  - Example: `http://IP:3000/callback`
  - Example: `http://DOMAIN:3000/callback`
  - Example: `http://DOMAIN/callback`
- Got in discord developer portal and create a new application
- Check All Privilege Intents
  - ![](https://s3files.m1000.fr/screenshot/2023/04/chrome_NbJEKtGOsy.png)
- Go in `OAuth2` -> `General` and fill the `Redirects` field with the link of your API
  - Exemple: `http://localhost:3000/callback`
  - Exemple: `http://IP:3000/callback`
  - Exemple: `http://DOMAIN:3000/callback`
  - Exemple: `http://DOMAIN/callback`

## 🔒 Get Invite Link
- Go in `OAuth2` -> `URL Generator` and check the `bot` scope and the `Administrator` permission
  - ![](https://s3files.m1000.fr/screenshot/2023/04/chrome_ACkzihgTq2.png)

## 📅 Routine
<!-- Requirement Proxy list -->
**⚠️ For the routine you need a proxy list !**
- Start the routine with `node dist/Routine` in `Routine` folder
  - Using PM2: `pm2 start dist/Routine/Routine.js --name "Routine"`