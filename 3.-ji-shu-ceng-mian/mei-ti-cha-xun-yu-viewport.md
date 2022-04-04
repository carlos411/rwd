# 3.3 實際裝置瀏覽

## 下載範例原始碼或任何本機端頁面

請[下載這份已經做好的「固定式版型」轉成「響應式版型」的頁面](https://alldata.sgp1.digitaloceanspaces.com/sample/rwd\_fixed\_layout\_to\_rwd.zip)。在 767px 以下時，會變成行動版。(或者用自己的專題網站也可以。)



用編輯器開啟 `rwd_fixed_layout_to_rwd` 這個專案資料夾，並開啟 index.html 原始碼：有以下兩個重點

一、在 css 資料夾中有一個 index\_mobile.css 檔案，將這個檔案於 index.html 頁面中載入：

```markup
<link rel="stylesheet" href="./css/index_mobile.css">
```

二、viewport(有註解起來)

```markup
<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
```

接下來請確認可以使用 `http://127.0.0.1` 或 `http://localhost` 等本機端方式來瀏覽頁面。



## 實際用手機瀏覽本機端網站

請瀏覽「**7.1 手機連本機端網站**」。



