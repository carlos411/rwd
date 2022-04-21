# 4.3 佈局 Layout

## 格線系統(v5)

[https://getbootstrap.com/docs/5.1/layout/grid/](https://getbootstrap.com/docs/5.1/layout/grid/)

![圖一：Bootstrap V5 的格線系統](../.gitbook/assets/bootstrap5\_grid\_layout.png)

記得以下這幾個版面的分界點：

* 576px
* 768px
* 992px
* 1200px
* 1400px



## 瞭解樣式 container 和 container-fluid

### container

div 元素加上 container 樣式：

```markup
<div class="container">
</div>
```

這時的 `div.container`，寬度就會如圖一的 `Container` 來做變化(`max-width` 屬性)。

例：`螢幕寬度 >= 1200px` 時，`div.container` 的最大寬度(`max-width`)就是 `1140px`；`螢幕寬度 >= 1400px` 時，`div.container` 的最大寬度(`max-width`)就是 `1320px`。



### container-fluid

div 元素加上 container-fluid 樣式：

```markup
<div class="container-fluid">
</div>
```

這時的 `div.container-fluid`，寬度就是 100%。



## 範例 1：指定 sm 範圍以上三欄均分

{% embed url="https://codepen.io/carlos411/pen/XvmmPJ" %}
sm 範圍以上三欄均分
{% endembed %}

請試著改成 md 範圍、lg 範圍、xl 範圍、xxl 範圍，並觀察。

## 範例 2：欄的順序

在「欄」的地方，加上 `order-*`，指定順序，這是 flexbox 裡的 order 屬性。

也可以設定 `order-{breakpoint}-*`，指定順序。

例：

{% embed url="https://codepen.io/carlos411/pen/LYVpQZZ" %}



練習：設定螢幕寬度在**小於等於 575.98px** 時，出現的順序由上至下為「**第三欄、第二欄、第一欄**」：

{% embed url="https://codepen.io/carlos411/pen/xxpBWOK" %}



## 範例 3：不論任何範圍，各欄寬度自動均分

{% embed url="https://codepen.io/carlos411/pen/wVKJMR" %}
各欄寬度自動均分及使用 w-100 來斷行
{% endembed %}

也試著將 `container` 改成 `container-fluid` 並觀察。

## 範例 4：不論任何範圍，設定某欄佔幾欄

{% embed url="https://codepen.io/carlos411/pen/GVpMwo" %}
設定某欄佔幾欄
{% endembed %}

試著改變所佔的欄數，例如將 `col-5` 改成 `col-8`。(改成佔8欄)

## 範例 5：指定特定範圍，由內容決定欄寬

透過 `col-{breakpoint}-auto` 可以將該欄設定成：寬度由內容決定。

{% embed url="https://codepen.io/carlos411/pen/MNaEdX" %}
內容決定欄寬
{% endembed %}

## 範例 6：分界點練習 - 所有範圍

{% embed url="https://codepen.io/carlos411/pen/PMZqPr" %}
分界點練習，所有圍範
{% endembed %}



## 範例 7：分界點練習 - sm 範圍以上

{% embed url="https://codepen.io/carlos411/pen/QeybgK" %}
分界點練習，sm 範圍以上
{% endembed %}



## 範例 8：分界點練習 - 同時設定所有範圍及 md 範圍以上

{% embed url="https://codepen.io/carlos411/pen/EqPjoR" %}
分界點練習，多個範圍一起使用&#x20;
{% endembed %}



## 範例 9：垂直方向對齊方式 1

在「列」中，加上以下樣式：

* align-items-start
* align-items-center
* align-items-end

{% embed url="https://codepen.io/carlos411/pen/mNPrVw" %}
垂直方向對齊方式1
{% endembed %}



## 範例 10：垂直方向對齊方式 2

在「欄」中，加上以下樣式：

* align-self-start
* align-self-center
* align-self-end

{% embed url="https://codepen.io/carlos411/pen/rXeMwN" %}
垂直方向對齊方式2
{% endembed %}



## 範例 11：水平方向對齊方式

在「列」中放入以下樣式：

* justify-content-start
* justify-content-center
* justify-content-end
* justify-content-around
* justify-content-between
* justify-content-evenly

{% embed url="https://codepen.io/carlos411/pen/NQNRYe" %}

瞭解水平對齊方式。



## 範例 12：欄的位移

語法：offset-{breakpoint}-{number}

{% embed url="https://codepen.io/carlos411/pen/VoaKRy" %}



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

{% hint style="info" %}
如果是 v4，包住 div.row 的父層 div，設定 `padding-left: 15px`、`padding-right: 15px` 即可。
{% endhint %}



## Grid 練習

暫時性的假圖：

[https://via.placeholder.com/300x200](https://via.placeholder.com/300x200)



請使用格線系統，完成以下佈局：

![](../.gitbook/assets/grid\_prac.png)

可直接開啟這個 CodePen， fork 一份，就可開始寫：[https://codepen.io/carlos411/pen/vYpPRwe](https://codepen.io/carlos411/pen/vYpPRwe?editors=1100)





完成示意，參考作法：

{% embed url="https://codepen.io/carlos411/pen/gOOwzKp" %}

