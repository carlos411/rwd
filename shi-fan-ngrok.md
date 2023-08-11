# 8 手機連本機端網站

## 使用相同區網方式

在本機端開發的時候，我們常常會使用 `http://localhost` 這樣的網址來開發，但問題在實做 RWD 的時候，有時會希望在手機上能實際瀏覽，那就讓手機及電腦連到**相同區網**即可，那我們就可以在手機上的瀏覽器輸入網址來連線。

{% hint style="info" %}
進行以下步驟之前，需先確認自己本機端有網站正在執行。例如：**`http://127.0.0.1:5500`**
{% endhint %}









### 第五步：獲得一個暫時性的公開網址

這時就可以看到：

![使用 ngrok 產生的暫時網址](.gitbook/assets/ngrok\_demo\_result.png)

如上圖所示，ngrok 幫我們產生了網址，那我們就可以實際用真實的裝置來測試 RWD 的實際狀況，或任何網頁上的操作。



如果要**終斷該暫時性的公開網址**，可直接在終端機(或命令提示字元)，輸入 **`Ctrl + c`** 即可。





### 錯誤訊息記錄



![](<.gitbook/assets/相片 2022-4-22 12 06 41.jpg>)

![](<.gitbook/assets/相片 2022-4-22 12 56 27.png>)



## 方式二：相同區網

直接找到自己電腦的 IP。

### Mac



<figure><img src=".gitbook/assets/mac_ip.webp" alt=""><figcaption></figcaption></figure>

註：如果 Mac 想透過像以下的 Windows 那樣輸入指令的話，就在終端機中，輸入 **`ifconfig`** 尋找。(不是 ~~**`ipconfig`**~~。)



### Windows

開啟「命令提示字元」：

![](.gitbook/assets/window\_find\_ip\_method.png)

