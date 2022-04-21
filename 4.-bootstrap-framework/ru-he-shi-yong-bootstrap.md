# 4.2 如何使用 Bootstrap

## 方式一：下載 Bootstrap

進到 [下載頁面](https://getbootstrap.com/docs/5.1/getting-started/download/)，如下圖，點選 Download，如下圖：

![](../.gitbook/assets/download\_bootstrap\_v5\_1.png)

下載之後，找到以下兩個檔案，網頁載入：

* css/bootstrap.min.css
* js/bootstrap.bundle.min.js



所以網頁當中，若要使用 Bootstrap，就需要載入的原始碼如下：

```markup
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
    
    <!-- Bootstrap 的 CSS -->
    <link rel="stylesheet" href="./vendors/bootstrap/css/bootstrap.min.css">
  </head>
  <body>
  
    <!-- 其它 html -->

        
    <!-- body 結束標籤之前，載入Bootstrap 的 JS -->
    <script src="./vendors/bootstrap/js/bootstrap.bundle.min.js"></script>
  </body>
</html>
```

[下載已安裝好的 Bootstrap V5 的資料夾](https://alldata.sgp1.digitaloceanspaces.com/sample/bootstrap\_installed\_v5\_1.zip) (已更新至 5.1.x)



## 方式二：直接使用 CDN

將官方提供的 CDN 路徑載入，結果如下原始碼：

```markup
<!DOCTYPE html>
<html>
  <head>

    <!-- Bootstrap 的 CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet">
  </head>
  <body>
  
    <!-- 其它 html -->
    
        
    <!-- body 結束標籤之前，載入Bootstrap 的 JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js"></script>
  </body>
</html>
```



## 方式三：在 CodePen 中使用

將上述的「方式二」提供的兩個 CDN 連結，放入到下圖：

步驟 Settings → CSS → JS → Save & Close，如下圖：

![載入 Bootstrap V5 的 CSS](../.gitbook/assets/codepen\_download\_b5\_css.png)

![載入 Bootstrap V5 的 JS](../.gitbook/assets/codepen\_download\_b5\_js.png)

