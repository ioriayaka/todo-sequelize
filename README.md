# todo-sequelize 實作練習
利用Express.js和sequelize實作Todo-list
## 功能介紹
1.  使用者可以註冊帳號
2.  使用者可以輸入帳號密碼登入
3.  使用者可以透過 Facebook 登入
4.  使用者必須登入後才能使用專屬Todo-list之相關功能
5.  使用者可以在首頁瀏覽所有待辦事項
6.  使用者可以新增待辦事項
7.  使用者可以勾選已完成的待辦事項
8.  使用者可以修改待辦事項
9.  使用者可以刪除待辦事項
---
## 環境建置
* Visual Studio Code
* bcryptjs 2.4.3,
* body-parser 1.19.0
* connect-flash 0.1.1
* dotenv 10.0.0
* express 4.17.1
* express-handlebars 5.3.3
* express-session 1.17.2
* method-override 3.0.0
* mysql2 2.3.0
* passport 0.4.1
* passport-facebook 3.0.0
* passport-local 1.0.0
* sequelize 6.6.5
* sequelize-cli 6.2.0

---

## 安裝流程
1. 開啟終端機，並cd 要放專案的位置並執行:

```
git clone https://github.com/ioriayaka/todo-sequelize.git
```

2. 進入專案資料夾

```
cd todo-sequelize.git
```

3. 安裝 npm 套件

```
npm install
```

4. 安裝 nodemon 套件 (若未安裝)

```
npm install -g nodemon
```
5. 環境變數設定
* 將根目錄.env.example檔案中列為SKIP的部分替換為相關ID與金鑰內容,再把.env.example檔案名稱修改為.env 
6. 建立資料庫
* 開啟 MySQL workbench，再連線至本地資料庫，輸入以下建立資料庫 

```
drop database if exists todo_sequelize;
create database todo_sequelize;
use todo_sequelize;
```
7. 建立資料庫欄位
```
npx sequelize db:migrate
```

8. 建立種子資料
```
npx sequelize db:seed:all
```


9. 啟動伺服器，執行 app.js 檔案

```
npm run dev
```

10. 當終端機出現以下字樣，表示啟動完成

```
App is running on http://localhost:3000
```
## 預設使用者 SEED_USER
*   name: root
*   email: root@example.com
*   password: 12345678
