# 5.2 佈局 Layout

## 網格系統(v5)

[https://getbootstrap.com/docs/5.3/layout/grid/#grid-options](https://getbootstrap.com/docs/5.3/layout/grid/#grid-options)

<figure><img src="../.gitbook/assets/bootstrap_grid_hint.png" alt=""><figcaption></figcaption></figure>

記得以下這幾個版面的分界點：

* **`xs`**：螢幕寬度大於等於 0px。
* **`sm`**：螢幕寬度大於等於 576px。
* **`md`**：螢幕寬度大於等於 768px。
* **`lg`**：螢幕寬度大於等於 992px。
* **`xl`**：螢幕寬度大於等於 1200px。
* **`xxl`**：螢幕寬度大於等於 1400px。



## container 與 container-fluid

如下示意圖：

<figure><img src="../.gitbook/assets/bootstrap_container.png" alt=""><figcaption></figcaption></figure>



## 列、欄與 container

* 將 **`列`** 寫在 container 中。
* 將 **`欄`** 寫在 列中。
* 每一列共有視覺上看不到的 12 欄可做劃分。



## 欄自動排版



### 範例 1：不論任何範圍，各欄寬度自動均分

{% embed url="https://codepen.io/carlos411/pen/wVKJMR" %}



### 範例 2：不論任何範圍，設定某欄佔幾欄

{% embed url="https://codepen.io/carlos411/pen/GVpMwo" %}



## 指定螢幕在特定範圍，設定各欄所佔的欄數



### 範例 1：指定 sm 範圍以上三欄均分

{% embed url="https://codepen.io/carlos411/pen/XvmmPJ" %}



### 範例 2：指定 md 範圍以上，均分或設定所佔的欄數

{% embed url="https://codepen.io/carlos411/pen/QeybgK" %}



### 範例 3：多個斷點一起使用

{% embed url="https://codepen.io/carlos411/pen/EqPjoR" %}



## 其它

### 範例 1：欄的位移

語法：**`offset-{breakpoint}-{number}`**

在某個 {breakpoint} 範圍以上，位移 {number} 欄。例：

{% embed url="https://codepen.io/carlos411/pen/VoaKRy" %}



### 範例 2：欄的順序

語法：**`order-{breakpoint}-{number}`**

在某個 {breakpoint} 範圍以下，{number} 數值較小的先出現。例：

{% embed url="https://codepen.io/carlos411/pen/LYVpQZZ" %}





## 範例 13：巢狀式

在 column 裡面的部份，也可以再放 row 來切 12 欄。

{% embed url="https://codepen.io/carlos411/pen/xxGVMjK" %}



## 範例 14：將 row 用在其它 div

關於左右 margin 負邊界(未指定寬度的情況下，左右的 margin 為負值時，會創造出額外空間)：

{% embed url="https://codepen.io/carlos411/pen/zYYBoxV" %}

將 Bootstrap 的 row(有負邊界) 用在其它 div(需要加上左右 padding)：

{% embed url="https://codepen.io/carlos411/pen/YzzPydQ" %}

(註：[var() 函式預設值的寫法](https://codepen.io/carlos411/pen/oNZzgZp))



結論：

* `.row` 可以運用在任何地方，不一定要放在 `.container` 或 `.container-fluid` 裡面。
* 如果是 v5 的版本，包住 div.row 的父層 div，設定 `padding-left: .75rem`、`padding-right: .75rem` 即可。

