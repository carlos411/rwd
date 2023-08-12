# 6 練習

## 1 介面 hamburger icon

例如以下 apple 行動版官網，影片示意：

{% file src=".gitbook/assets/hamburger_icon_sample.mov" %}

提供 html：

```html
<button type="button" class="hamburger_icon">
  <span class="-hr -top"></span>
  <span class="-hr -middle"></span>
  <span class="-hr -bottom"></span>
</button>
```



切換 class (使用 jQuery)：

```javascript
// 按鈕狀態的切換
$("button.hamburger_icon").on("click", function(){
  $(this).toggleClass("-on");
});
```

切換 class (使用 JavaScript)：

```javascript
// 按鈕狀態的切換
var hamburger_icon = document.getElementsByClassName("hamburger_icon")[0];
hamburger_icon.addEventListener("click", function(){
  hamburger_icon.classList.toggle("-on");
});
```

結果示意：

{% embed url="https://youtu.be/6rJP4TZF4SU" %}



參考作法：

{% embed url="https://codepen.io/carlos411/pen/rNBErJy" %}





## 2 套用 hamburger icon 的外掛

[套件官網](https://jonsuh.com/hamburgers/)。

[官方所提供的 css 在這](https://raw.githubusercontent.com/jonsuh/hamburgers/master/dist/hamburgers.css)。

自行挑選一個效果，學會套用。只需要看官網裡的 Usage 1 \~ 4 點即可。



切換 class：

```javascript
// JavaScript 版本
var btn_hamburger = document.getElementsByClassName("hamburger")[0];
btn_hamburger.addEventListener("click", function(){
  this.classList.toggle("is-active");
});

/*
// jQuery 版本
$("button.hamburger").on("click", function(){
  $(this).toggleClass("is-active");
});
*/
```



參考作法：

{% embed url="https://codepen.io/carlos411/pen/xvVLyR" %}





## 3 導覽列縮合

指定檔名：`nav_switch.html`

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

提供 jQuery 的展開縮合的做法(較簡單)：

```javascript
// 點擊按鈕，選單縮放
$("button.btn_switch").on("click", function(){
  $("nav.main_nav").slideToggle();
});
```



結果示意：

{% embed url="https://youtu.be/8Q7obn9a9hU" %}



參考作法(使用 jQuery 做展開縮合)：

{% embed url="https://codepen.io/carlos411/pen/XvGKQz" %}

以下提供 JavaScript 的展開縮合做法：

{% embed url="https://codepen.io/carlos411/pen/VwrMMjO" %}



## 4 導覽列開啟，不推開底下內容

直接使用這個 CodePen，也可建立新的網頁檔來寫：

{% embed url="https://codepen.io/carlos411/pen/gOoVjJa?editors=1010" %}

撰寫 CSS，完成以下參考作法的結果。





參考作法：

{% embed url="https://codepen.io/carlos411/pen/NWXQBeb" %}



## 5 使用 Flexbox 做版位佈局

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



## 6 內容圖片佔滿版

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





## 7 有 10 個項目的排版

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



## 8 Youtube iframe 影片 RWD

提供以下 iframe 影片，它的寬高比為 `560:315`，也就是 `16:9`。

```markup
<iframe height="315" width="560" class="test" src="https://www.youtube.com/embed/-RAdHJ-aquE" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

執行完的結果示意：

{% embed url="https://youtu.be/uEzbFE37CI8" %}

參考作法：

{% embed url="https://codepen.io/carlos411/pen/PoGdRmB" %}

