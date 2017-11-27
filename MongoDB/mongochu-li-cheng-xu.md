#mongo處理程序

### 1.連接

```bash
參數說明：
port -->mongod通訊埠
username -->使用者名稱
password -->資料庫密碼
authenticationDatabase -->要連接的資料庫
```

### 2.export可將檔案輸出成JSON與CSV檔案

```bash
$mongoexport --db test --collection good --out /home/titan/Desktop/good.json
```

### 3.import可將JSON與CSV檔案內容匯入到MongoDB實例中

```bash
$mongoimport --db test --collection good --file /home/titan/Desktop/good.json
```

### 4.mongofiles提供MongoDB分散式檔案儲存系統\(將檔案存入database的fs.files集合內）

```bash
將檔案存入MongoDB
$mongofiles -db test -local /home/titan/Pictures/aaaa.pdf put aaaa.pdf

將檔案由MongoDB取回
$mongofiles -db test -local /home/titan/Pictures/atest.pdf get aaaa.pdf
```

執行結果

上傳檔案

![](/assets/Screenshot from 2017-11-26 19-53-16.png)

mongo JavaScript Shell

![](/assets/Screenshot from 2017-11-26 19-54-05.png)
