# 5.1 作業一

## 依螢幕寬度區隔，設定某區塊的 Media Query

請 fork 以下程式，然後將 `div.my_div1` 區塊水平置中，並將該區塊按照以下 media query 規則設定：

* 瀏覽器寬度 < 576px 時，`div.my_div1` 的寬度設定成 100%。
* 576px <= 瀏覽器寬度 < 768px 時，`div.my_div1` 的寬度設定成 540px。
* 768px <= 瀏覽器寬度 < 992px 時，`div.my_div1` 的寬度設定成 720px。
* 992px <= 瀏覽器寬度 < 1200px 時，`div.my_div1` 的寬度設定成 960px。
* 1200px <= 瀏覽器寬度 < 1400px 時，`div.my_div1` 的寬度設定成 1140px。
* 瀏覽器寬度>= 1400px 時，`div.my_div1` 的寬度設定成 1320px。
* 留意圖片不得超出 `div.my_div1` 的區塊。而且當 `div.my_div1` 的寬度大於圖片寬度時，圖片應維持原圖尺吋。

{% hint style="info" %}
註：`瀏覽器寬度 < 768`，在 media query 中請寫 `max-width: 767.98px`，也就是減 0.02。
{% endhint %}

{% embed url="https://codepen.io/carlos411/pen/ZgEWrN" %}
依螢幕寬度區隔，設定某區塊的 Media Query
{% endembed %}





結果示意：

{% embed url="https://youtu.be/C3tEOdpZfTM" %}



參考作法：
