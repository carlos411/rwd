# 7.1 手機連本機端網站

## 方式一：使用 ngrok

在本機端開發的時候，我們常常會使用 `http://localhost` 這樣的網址來開發，但問題在實做 RWD 的時候，有時會希望在手機上能實際瀏覽，那就會需要透過 Ngrok 來幫我們達成。

簡而言之，ngrok 會替我們的 **本機端網址**，產生另一個 **暫時性的公開網址**，那我們就可以在手機上的瀏覽器輸入該網址來連線。

{% hint style="info" %}
進行以下步驟之前，需先確認自己本機端有網站正在執行。例如：**`http://127.0.0.1:3000`**
{% endhint %}



### 第一步：註冊 ngrok 並登入

進到[官網](https://ngrok.com/)，執行註冊並登入，如下示意：

![](../.gitbook/assets/ngrok\_new.png)

****

**登入**後，可看到如下後台：

![](../.gitbook/assets/ngrok\_setup.png)





### 第二步：下載 ngrok 指令檔

至 [ngrok 下載網址](https://ngrok.com/download)，下載**解壓縮**，會取得一個檔名為 **`ngrok`** 的檔案，可任意存放在你想存的位置。下載的按鈕如下圖示意：

Mac：

![](../.gitbook/assets/ngrok\_mac\_download.png)

Windows：

![](../.gitbook/assets/ngrok\_window\_download.png)



### 第三步：設定 Authtoken

進到後台，找到下圖的指令，進行複製：

![](../.gitbook/assets/ngrok\_auth.png)

Mac 欲執行的指令(`$` 不需要打，它是表示輸入指令的意思)：

```
$ ./ngrok config add-authtoken 這裡是自己的代碼
```

Windows 欲執行的指令(`$` 不需要打，它是表示輸入指令的意思)：

```
$ ngrok config add-authtoken 這裡是自己的代碼
```





Mac 執行指令示範(使用 Terminal，進到 ngrok 檔案的所在資料夾，然後執行指令)：

{% embed url="https://youtu.be/rS0P442fSls" %}



Windows 執行指令步驟(使用命令提示字元，進到 ngrok 檔案的所在資料夾，然後執行指令)：

1. 將下載的 ngrok，直接點兩下，就會自動用「命令提示字元」開啟，直接就會進到資料夾。
2. 然後直接執行複製的指令即可。



{% hint style="info" %}
此步驟在同一台電腦，只要執行一次即可。
{% endhint %}



### 第四步：執行 ngrok 指令

#### 使用 ngrok - Mac

執行步驟：

1. 將 ngrok 拖曳到 Terminal(終端機)，取得 ngrok 檔案所在的資料夾。
2. 然後執行以下指令(請看以下影片示範，然後 port 3000 如果有不同，需換成自己的，`$`不用輸入)：

```
$ ./ngrok http 3000
```



影片示範：

{% embed url="https://youtu.be/lozGCovPbWg" %}

####

#### 使用 ngrok - Windows

執行步驟：

1. 將下載的 ngrok，直接點兩下，就會自動用「命令提示字元」開啟。
2. 執行以下指令即可。(port 3000 如果有不同，需換成自己的，`$` 不用輸入)：

```
$ ngrok http 3000
```



### 第五步：獲得一個暫時性的公開網址

這時就可以看到：

![使用 ngrok 產生的暫時網址](../.gitbook/assets/ngrok\_demo\_result.png)

如上圖所示，ngrok 幫我們產生了網址，那我們就可以實際用真實的裝置來測試 RWD 的實際狀況，或任何網頁上的操作。



如果要**終斷該暫時性的公開網址**，可直接在終端機(或命令提示字元)，輸入 **`Ctrl + c`** 即可。





## 方式二：相同區網

直接找到自己電腦的 IP。

### Mac

![](../.gitbook/assets/mac\_find\_ip\_method.png)

註：如果 Mac 想透過像以下的 Windows 那樣輸入指令的話，就在終端機中，輸入 **`ifconfig`** 尋找。(不是 ~~**`ipconfig`**~~。)





### Windows

開啟「命令提示字元」：

![](../.gitbook/assets/window\_find\_ip\_method.png)

