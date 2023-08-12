# 6 練習

## 1 介面 hamburger icon

檔名建議：`btn_hamburger.html`

例如以下 apple 行動版官網，影片示意：

{% file src=".gitbook/assets/hamburger_icon_sample.mov" %}

提供 html：

```html
<button type="button" id="btn_hamburger"></button>
```

切換 class 的 JS 程式：

```javascript
let btn_hamburger_el = document.getElementById("btn_hamburger");
btn_hamburger_el.addEventListener("click", function(){
  this.classList.toggle("-on")
});
```



參考作法：

{% embed url="https://codepen.io/carlos411/pen/KKrjxYJ" %}



## 2 導覽列縮合

檔名建議：`nav_switch.html`

提供 html：

```markup
<button type="button" class="btn_switch">導覽列縮合按鈕</button>

<nav class="main_nav">
  <ul class="nav_list">
    <li><a href="#">首頁</a></li>
    <li><a href="#">關於我們</a></li>
    <li><a href="#">分類頁</a></li>
  </ul>
</nav>
```



結果示意：

{% embed url="https://youtu.be/8Q7obn9a9hU" %}



以下提供 JavaScript 的展開縮合做法：

{% embed url="https://codepen.io/carlos411/pen/VwrMMjO" %}





## 3 使用 Flexbox 做版位佈局

提供 HTML 如下：

```markup
<div class="all_container">
  <div>
    左側<br>
    另一行
  </div>
  <div>
    中間
  </div>
  <div>
    右側
  </div>
</div>
```

請直接參考下方 CodePen 的畫面結果，實作看看。



參考作法：

{% embed url="https://codepen.io/carlos411/pen/MWWJQvQ" %}



## 4 內容圖片佔滿版

提供 HTML 如下：

```markup
<div class="img_block">
  <img src="https://picsum.photos/id/867/2000/300">
</div>
```

* 當螢幕寬度小於等於 `767.98px` 以下時，`圖片`要在 `div.img_block` 區塊水平方向、垂直方向皆置中；且 `div.img_block` 需佔滿螢幕，且寬高比需是 `2:1`。
* 請參考下方 CodePen 的畫面結果，實作看看。





參考作法：

{% embed url="https://codepen.io/carlos411/pen/JjjELmR" %}





## 5 有 10 個項目的排版

提供 html 如下：

```markup
<div class="list_container">
  <ul class="ul_list">
    <li class="item">
      <div class="item_block">
        <h1>標題1</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
    <li class="item">
      <div class="item_block">
        <h1>標題2</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
    <li class="item">
      <div class="item_block">
        <h1>標題3</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
    <li class="item">
      <div class="item_block">
        <h1>標題4</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
    <li class="item">
      <div class="item_block">
        <h1>標題5</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
    <li class="item">
      <div class="item_block">
        <h1>標題6</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
    <li class="item">
      <div class="item_block">
        <h1>標題7</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
    <li class="item">
      <div class="item_block">
        <h1>標題8</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
    <li class="item">
      <div class="item_block">
        <h1>標題9</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
    <li class="item">
      <div class="item_block">
        <h1>標題10</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
  </ul>
</div>
```

請直接參考下方 CodePen 的畫面結果，實作看看。

參考作法：

{% embed url="https://codepen.io/carlos411/pen/QWWdrbX" %}



## 6 Youtube iframe 影片 RWD

提供以下 iframe 影片，它的寬高比為 `560:315`，也就是 `16:9`。

```markup
<iframe height="315" width="560" class="test" src="https://www.youtube.com/embed/-RAdHJ-aquE" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

執行完的結果示意：

{% embed url="https://youtu.be/uEzbFE37CI8" %}

參考作法：

{% embed url="https://codepen.io/carlos411/pen/PoGdRmB" %}

